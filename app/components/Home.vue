<template>
  <Page>
    <ActionBar>
      <Label text="Home"/>
    </ActionBar>

    <GridLayout>
      <list class="grocery-list"
        :dataList="groceryList"
        />
    </GridLayout>
  </Page>
</template>

<script lang="ts">
  import Vue from "nativescript-vue";

  import List from './list.vue';

  export default Vue.extend({
    components: {
      List,
    },
    data() {
      return {
        groceryList: [
          {
            type: 'fruit',
            name: 'bannana',
          },
          {
            type: 'fruit',
            name: 'apple',
          },
          {
            type: 'veggies',
            name: 'Cucumber',
          },
          {
            type: 'fruit',
            name: 'strawberries',
          },
          {
            type: 'veggies',
            name: 'Spinash',
          },
        ]
      };
    },
  });
</script>

<style scoped lang="scss">
  @import '@nativescript/theme/scss/variables/blue';

  // Custom styles
  .fas {
    @include colorize($color: accent);
  }

  .info {
    font-size: 20;
    horizontal-align: center;
    vertical-align: center;
  }
</style>
