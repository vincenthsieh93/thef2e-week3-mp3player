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
                <i></i>
                <h2>Sunn Forest</h2>
              </div>
            </div>
          </div>
          <div class="music__function"></div>
        </div>
      </div>
    </div>
    <div class="player__middle"></div>
    <div class="player__bottom"></div>
  </div>
</template>

<script>
export default {
  name: "Player",
  props: {
    msg: String
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
    display: flex;
    align-items: center;

    > i {
      display: block;
      width: 22px;
      height: 24px;
      background-color: #B6C6FF;
    }

    > h2 {
      flex: 1;
      min-width: 0;
      font-size: 24px;
      line-height: 33px;
      letter-spacing: 0;
      text-align: left;
      text-overflow: ellipsis;
      white-space: nowrap;
      overflow: hidden;
      padding-left: 21px;
      color: #B6C6FF;
    }
  }

  &__function {
    width: 264px;
  }
}
</style>
