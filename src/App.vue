<template>
  <div id="app">
      <first></first>
      <second></second>
  </div>
</template>

<script>
// import FullPage from 'vue-fullpage.js/src/FullPage.vue'
// import fullPageMixin from 'vue-fullpage.js/src/fullPageMixin.js'
import first from '@/components/first'
import second from '@/components/second'

export default{
    name: 'App',
    // mixins: [fullPageMixin],
    data () {
        return {
            asd: null
        }
    },
    components: {
        // FullPage,
        first,
        second
    },
    methods: {
        log () {
            ['a', 'b'].forEach(item => {
                console.log(item)
            })
        }
    },
    created () {
        this.log()
    }
}
</script>

<style lang="scss">
@import '~bulma/sass/utilities/_all';

@import '~bulma';
@import '~buefy/src/scss/buefy';
</style>
