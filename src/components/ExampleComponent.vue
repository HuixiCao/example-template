<template>
  <div>111</div>
  <div><fpcButton /></div>
  <div><fpcButton2 /></div>
  <div>
    <absentForm :formData="formData" />
  </div>
</template>

<script lang="ts">
import { defineAsyncComponent, defineComponent, ref } from 'vue';
export default defineComponent({
  name: 'ExampleComponent',
  components: {
    fpcButton: defineAsyncComponent(() => import('ui/components/fpcButton')),
    fpcButton2: defineAsyncComponent(() => import('ui/components/fpcButton2')),
    absentForm: defineAsyncComponent(() => import('ui/components/absentForm')),
  },
  setup(props) {
    const formData = ref({
      AbsentReasonCode: '',
      StartDateTime: '',
      EndDateTime: '',
      Note: '',
    });
    return {
      formData,
    };
  },
});
</script>
