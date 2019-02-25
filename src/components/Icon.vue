<template>
    <svg>
        <use :xlink:href="'/img/icons/iconpack.svg#icon-' + name"></use>
    </svg>
</template>

<script>
    import {Component, Vue} from 'vue-property-decorator';

    @Component({
        props: {
            name: String,
        },
    })

    export default class Icon extends Vue {
    }
</script>

<style scoped lang="scss">
    svg {
        $size: 12px;
        height: $size;
        width: $size;
        display: inline-block;
        margin-right: 3px;
    }
</style>
