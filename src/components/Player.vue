<template>
  <div class="player">
    <div class="player__top">
      <div class="music">
        <div class="music__container">
          <div class="music__info">
            <div class="music__cover">
              <img src="../assets/images/elphnt-logo.png" alt="Album Cover">
            </div>
            <div class="music__detail">
              <h1 class="music__album">Ambitions</h1>
              <p class="music__singer">ELPHNT</p>
              <div class="music__repertoire">
                <FontAwesomeIcon :icon="iconHeadphones" />
                <h2>Sunn Forest</h2>
              </div>
            </div>
          </div>
          <div class="music__function">
            <div class="music__function-top">
              <button class="music__playlist">
                <FontAwesomeIcon :icon="iconList" />
              </button>
            </div>
            <div class="music__function-bottom">
              <button class="music__mode-btn">
                <FontAwesomeIcon :icon="iconSyncAlt" />
              </button>
              <i class="music__mode-line"></i>
              <button class="music__mode-btn">
                <FontAwesomeIcon :icon="iconRandom" />
              </button>
              <button class="music__mode-btn">
                <FontAwesomeIcon :icon="iconRetweet" />
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="player__middle"></div>
    <div class="player__bottom"></div>
  </div>
</template>

<script>
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { faHeadphones, faList, faSyncAlt, faRandom, faRetweet } from "@fortawesome/free-solid-svg-icons";

export default {
  name: "Player",
  props: {
    msg: String
  },
  data() {
    return {
      iconHeadphones: faHeadphones,
      iconList: faList,
      iconSyncAlt: faSyncAlt,
      iconRandom: faRandom,
      iconRetweet: faRetweet
    }
  },
  components: {
    FontAwesomeIcon
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.player {
  display: flex;
  flex-direction: column;
  height: 100vh;

  &__top {
    flex: 2;
  }

  &__middle {
    flex: 1;
    background: transparent linear-gradient(180deg, #AFC5FF 0%, #FACEFF 100%) 0% 0% no-repeat padding-box;
  }

  &__bottom {
    flex: 1;
  }
}

.music {
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  height: 100%;
  padding-bottom: 3%;

  &__container {
    display: flex;
    padding: 0 12% 0 11%;
  }

  &__info {
    flex: 1;
    display: flex;
    min-width: 0;
  }

  &__cover {
    box-sizing: border-box;
    width: 140px;
    height: 140px;
    border: 1px solid #979797;
    border-radius: 2px;
    background-color: #fff;

    > img {
      width: 100%;
      height: auto;
      min-width: 100%;
      min-height: 100%;
    }
  }

  &__detail {
    flex: 1;
    display: flex;
    min-width: 0;
    flex-direction: column;
    justify-content: center;
    padding: 0 40px;
  }

  &__album {
    font-size: 28px;
    line-height: 40px;
    letter-spacing: 0;
    text-align: left;
    padding-bottom: 6px;
    color: #A7A7A7;
  }

  &__singer {
    font-size: 16px;
    line-height: 22px;
    letter-spacing: 0;
    text-align: left;
    padding-bottom: 20px;
    color: #A7A7A7;
  }

  &__repertoire {
    font-size: 24px;
    display: flex;
    align-items: center;
    color: #B6C6FF;

    > h2 {
      flex: 1;
      min-width: 0;
      line-height: 33px;
      letter-spacing: 0;
      text-align: left;
      text-overflow: ellipsis;
      white-space: nowrap;
      overflow: hidden;
      padding-left: 21px;
    }
  }

  &__function {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 264px;

    &-top {
      display: flex;
      flex-direction: row-reverse;
    }

    &-bottom {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  }

  &__playlist {
    font-size: 40px;
    line-height: 0;
    display: block;
    color: #6A65AC;
    background-color: transparent;

    &:hover {
      color: #E9E9E9;
    }
  }

  &__mode-btn {
    font-size: 40px;
    line-height: 0;
    display: block;
    color: #B6C6FF;
    background-color: transparent;

    &:hover {
      color: #FFF;
    }
  }

  &__mode-line {
    display: block;
    width: 1px;
    height: 45px;
    background-color: #B6C6FF;
  }
}
</style>
