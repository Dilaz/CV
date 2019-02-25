<template>
    <div class="enjoyment">
        <span>Enjoyment: </span>
        <span class="screen-reader-only">{{enjoyment}} out of 5</span>
        <div class="rating" aria-hidden="true">
            <span v-for="i in enjoyment">
                <Icon name="heart"></Icon>
            </span>
        </div>
    </div>
</template>

<script>
    import {Component, Vue} from 'vue-property-decorator';
    import Icon from './Icon.vue';

    @Component({
        props: {
            enjoyment: Number,
        },
        components: { Icon },
    })

    export default class Enjoyment extends Vue {
    }
</script>

<style scoped lang="scss">
    svg {
        fill: red;
    }

    .enjoyment {
        display: flex;
    }

    .rating {
        display: flex;
        margin-left: 5px;
        align-items: center;
    }
</style>
