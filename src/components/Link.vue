<template>
    <li>
        <a
            v-bind:href=url
            target="_blank"
        >
            {{title}}
        </a>
    </li>
</template>
<script>
export default {
    name: 'Link',
    props: {
        outUrl: String,
        outTitle: String
    },
    data () {
        return {
            url: 'https://www.baidu.com',
            title: 'baidu'
        }
    },
    // watch: {
    //     outUrl () {
    //         this.url = this.outUrl
    //     }
    // },
    created () {
        if (typeof this.outUrl === 'string') {
            this.url = this.outUrl
            this.title = this.outTitle
        }
    }
}
</script>
<style scoped>
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
