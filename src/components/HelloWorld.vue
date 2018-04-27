<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
      <Link v-for="item in linkdata" :key="item.title" v-bind="item"/>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <Link v-for="item in Ecosystem" :key="item.title" v-bind="item"/>
    </ul>
  </div>
</template>
<script>
import Link from '@/components/Link'
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      linkdata: [{
          outUrl: 'https://forum.vuejs.org',
          outTitle: 'Forum'
        }, {
          outUrl: 'https://chat.vuejs.org',
          outTitle: 'Community Chat'
        }, {
          outUrl: 'https://twitter.com/vuejs',
          outTitle: 'Twitter'
        }, {
          outUrl: 'http://vuejs-templates.github.io/webpack/',
          outTitle: 'Docs for This Template'
        }, {
          outUrl: 'https://vuejs.org',
          outTitle: 'Core Docs'
        }
      ],
      Ecosystem: [{
            outUrl: 'http://router.vuejs.org/',
            outTitle: 'vue-router'
        }, {
            outUrl: 'http://vuex.vuejs.org/',
            outTitle: 'vuex'
        }, {
            outUrl: 'http://vue-loader.vuejs.org/',
            outTitle: 'vue-loader'
        }, {
            outUrl: 'https://github.com/vuejs/awesome-vue',
            outTitle: 'awesome-vue'
        }
      ]
    }
  },
  components: {
    Link
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
</style>
