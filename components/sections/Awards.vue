<!--
    components/sections/Awards.vue
-->

<template>
    <div class="s-awards">
        <div class="flexGrid _horizontal">
            <div class="flexGrid__cell press">
                <h2 v-text="$t(data.pressTitle)" />
                <list :items="data.press" />
            </div>
            <div class="flexGrid__cell awards">
                <div>
                    <h2 v-text="$t(data.title)" />
                    <list :items="data.awards" class="awards-list" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>

    const data = {
        title: "s-awards:title",
        awards: [
            { name: "s-awards:fwa", quantity: "s-awards:fwa:q" },
            { name: "s-awards:awwwards", quantity: "s-awards:awwwards:q" },
            { name: "s-awards:css", quantity: "s-awards:css:q" },
            { name: "s-awards:marathon", quantity: "s-awards:marathon:q" },
            { name: "s-awards:half", quantity: "s-awards:half:q" }
        ],
        pressTitle: "s-articles:title",
        press: [
            { name: "s-articles:wired", url: "https://www.wired.co.uk/article/lvmh-brands-group-digital-technology" },
            { name: "s-articles:thefwa", url: "https://thefwa.com/fwa-jury/christian-macmillan" },
            { name: "s-articles:robRepport", url: "https://robbreport.com/style/watch-collector/hublots-new-experiential-digital-platform-is-a-radical-way-to-buy-a-watch-2799213/" },
            { name: "s-articles:wwd", url: "https://wwd.com/accessories-news/watches/hublot-digital-boutique-program-1202694234/" },
            { name: "s-articles:realClear", url: "http://www.realclearlife.com/fashion/hublot-digital-boutique/#1" },
            { name: "s-articles:watchprosite", url: "https://www.watchprosite.com/hublot/the-opening-of-hublot-s-first-digital-boutique-in-new-york-/871.1213266.9914741/" },
            { name: "s-articles:creative-blog", url: "https://www.creativebloq.com/portfolios/examples-712368" },
            { name: "s-articles:awwwards", url: "https://www.awwwards.com/case-study-xavier-cusso-portfolio.html" },
            { name: "s-articles:comarts", url: "https://www.commarts.com/webpicks/xavier-cuss" }
        ]
    }

    import { mapState } from "vuex";

    import List from "~/components/List";

    export default {
        name: "Awards",
        props: {
            data: {
                type: Object,
                default: () => data
            }
        },
        computed: {
            ...mapState({
                mobile: state => state.breakpoints.mobile
            })
        },
        components: {
            List
        }
    }

</script>

<style lang="scss" scoped>

    .s-awards {
        .press {
            width: 50%;
            box-sizing: content-box;
            padding-right: 50%;
            @include respond-to("desktop") {
                width: 25%;
                padding-left: 25%;
                padding-right: 0%;
                padding-bottom: 40px;
            }
        }
        .awards {
            width: 50%;
            padding-top: 25px;
            padding-left: 50%;
            box-sizing: content-box;
            @include respond-to("desktop") {
                padding-top: 0px;
                width: 25%;
                padding-left: 25%;
                transform: translateY(100px);
            }
        }
    }

</style>


