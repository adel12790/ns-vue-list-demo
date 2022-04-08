<template>
    <GridLayout class="list-wrapper">
        <ListView class="list"
            :items="dataList"
            :itemTemplateSelector="selector"
        >
            <v-template name="fruit">
                <Label :text="`Sweat ${item.name}`" />
            </v-template>
            <v-template name="veggies">
                <Label :text="item.name" />
            </v-template>
            <v-template name="default">
                <Label text="not on the list" />
            </v-template>
        </ListView>
    </GridLayout>
</template>

<script>
import Vue from 'nativescript-vue';

export default Vue.extend({
    name: 'list',
    props: {
        dataList: {
            type: Array,
            default: () => ([]),
        },
    },
    methods: {
        selector(item) {
            return item.type;
        },
    },
});
</script>

<style>

</style>