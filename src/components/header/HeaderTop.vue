<template>
  <div class="header-top">
    <picture>
      <source srcset="@/assets/santa.webp" type="image/webp" />
      <img src="@/assets/santa.png" class="santa" v-show="load" />
    </picture>
    <Navigation />
    <h1 class="header-top-title">
      Watataku's<br />
      X'mas special site at 2020
    </h1>
  </div>
</template>

<script>
import Navigation from "../Navigation";

export default {
  components: {
    Navigation,
  },
  data() {
    return {
      load: false,
    };
  },
  mounted() {
    window.onload = () => {
      this.load = true;
    };
  },
};
</script>

<style scoped>
@keyframes animation-santa {
  0% {
    width: 0%;
  }
  100% {
    width: 400px;
  }
}

@keyframes animation-santa-tb {
  0% {
    width: 0%;
  }
  100% {
    width: 35vw;
  }
}

@keyframes animation-santa-sp {
  0% {
    width: 0%;
  }
  100% {
    width: 30vh;
  }
}

/*PC*/
@media screen and (min-width: 1026px) {
  .header-top {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: #152c4e;
    width: 100%;
    height: 65vh;
  }

  .santa {
    position: absolute;
    top: 0;
    left: 0;
    width: 400px;
    animation: animation-santa 3s;
  }

  .header-top .header-top-title {
    z-index: 20;
    margin-right: 5%;
    color: #999;
    letter-spacing: 1px;
    font-size: 3.5em;
    font-weight: bold;
    font-family: "Kaushan Script", cursive;
    font-family: "Bad Script", cursive;
  }
}

/*タブレット*/
@media screen and (min-width: 482px) and (max-width: 1025px) {
  .header-top {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: #152c4e;
    width: 100%;
    height: 75vh;
  }

  .santa {
    position: absolute;
    top: 0;
    left: 0;
    width: 35vw;
    animation: animation-santa-tb 3s;
  }

  .header-top .header-top-title {
    padding-right: 3vh;
    z-index: 10;
    color: #999;
    font-size: calc(3.5vw + 0.5em);
    font-weight: bold;
    font-family: "Kaushan Script", cursive;
    font-family: "Bad Script", cursive;
  }
}
/*スマホ*/
@media screen and (max-width: 481px) {
  .header-top {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    background-color: #152c4e;
    width: 100%;
    height: 65vh;
  }

  .santa {
    position: absolute;
    top: 0;
    left: 0;
    width: 30vh;
    animation: animation-santa-sp 3s;
  }

  .header-top .header-top-title {
    color: #999;
    letter-spacing: 1px;
    font-size: 1.3em;
    font-weight: bold;
    font-family: "Kaushan Script", cursive;
    font-family: "Bad Script", cursive;
  }
}
</style>
