<template>
<div class="hero is-fullheight">
    <div class="hero-body">
        <h1 class="title has-text-centered">
            <glitch :text="'I am ' +  words[currentWord]" background="#252525"></glitch>
        </h1>
    </div>
</div>
</template>

<script>
import Glitch from 'vue-glitch'

export default {
    components: {
        Glitch
    },
    data () {
        return {
            words: [
                'Cloud',
                'a Web Developer',
                'a Programmer',
                'a Progamer'
            ],
            currentWord: 0
        }
    },
    methods: {
        changeWord () {
            this.currentWord < this.words.length - 1 ? this.currentWord++ : this.currentWord = 0
        }
    },
    created () {
        setInterval(() => this.changeWord(), 1500)
    }
}
</script>

<style scoped lang="scss">
.hero{
    background-color: #252525;
}

h1.title{
    font-size: 6em;
}
</style>
