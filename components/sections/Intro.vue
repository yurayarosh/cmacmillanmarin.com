<!--
    components/sections/Intro.vue
-->

<template>
    <div class="c-intro">
        <p class="emoji">👻</p>
        <p>Hi, I’m Christian, a 28 y/o islander based in Barcelona. Nowadays busy working as Creative Developer at <a href="">B-Reel</a>, running <a href="">Burundanga Studio</a> and judging the best of digital industry at <a href="">FWA</a>.</p>
    </div>
</template>

<script>

    export default {
        name: "Intro"
    }

</script>

<style lang="scss" scoped>

    .c-intro {
        padding-top: 25%;
        width: 50%;
        p {
            font-size: 2em;
        }
        a {
            color: $white;
            font-weight: 700;
        }
        span {
            mix-blend-mode: difference;
        }
    }

</style>

