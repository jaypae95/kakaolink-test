<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>
    <br>
    <img v-on:click="kakaoShare" src="//developers.kakao.com/assets/img/about/logos/kakaolink/kakaolink_btn_small.png">
  </div>
</template>
<script src="https://developers.kakao.com/sdk/js/kakao.js"></script>
<script>Kakao.init('82734c9efef1596fe344120a0103749e')</script>
<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    kakaoShare() {
      console.log('hi')
      Kakao.Link.sendDefault({
        objectType: 'feed',
        content: {
          title: '테스트중입니다',
          imageUrl: 'https://w.namu.la/s/d2fe77ef48637db195e9cc4ac7dacc6ff088a60c8df7d1bcc25b8c26d1650e191bd30f48c148613849be8eb083dabfaeb1d6332605d9109ad0782eff225c1f94a6ee29492a0fc20a7da3dcd8ccb695c520f7ab42c0cc83cbf123ba011fcfef5b08951d560cc65da3b004774ee38f7328',
          link: {
            mobileWebUrl: 'https://naver.com',
            webUrl: 'https://naver.com'
          }
        }
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
