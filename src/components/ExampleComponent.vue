<template>
  <div>111</div>
  <div><fpcButton /></div>
  <div><fpcButton2 /></div>
</template>

<script lang="ts">
import { defineAsyncComponent, defineComponent } from 'vue';
export default defineComponent({
  name: 'ExampleComponent',
  components: {
    fpcButton: defineAsyncComponent(() => import('ui/components/fpcButton')),
    fpcButton2: defineAsyncComponent(() => import('ui/components/fpcButton2')),
  },
  setup(props) {
    return {};
  },
});
</script>
