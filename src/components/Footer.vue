<template>
  <footer>
    <div class="sns">
      <ShareFacebook color="black" class="footer-link-facebook"/>
      <div class="module--spacing--very--small"></div>
      <ShareTwitter color="black" class="footer-link-twitter" />
    </div>
    <small>&copy;2020 Watataku.</small>
  </footer>
</template>

<script>
import ShareTwitter from "../components/ShareTwitter";

import ShareFacebook from "../components/ShareFacebook";
export default {
  components: {
    ShareTwitter,
    ShareFacebook
  }
}
</script>

<style scoped>

.module--spacing--very--small {
  height: 5px;
}

footer {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  padding-top: 1vh;
  padding-bottom: 1vh;
  height: 30vh;
  background-color: #ddd;
}

.sns {
  position: absolute;
  bottom: 3vh;
  right: 3vh;
}

small {
  font-size: 1em;
  letter-spacing: 2px;
}
</style>
