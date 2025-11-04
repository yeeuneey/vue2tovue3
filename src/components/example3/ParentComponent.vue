<template>
  <div>
    <ChildComponent
        :message="parentMessage"
        @custom-event="handleEvent"
    />
  </div>
</template>

<script>
import { defineComponent, ref } from 'vue'
import ChildComponent from './ChildComponent.vue'

export default defineComponent({
  name: 'E05ParentComponent',
  components: {
    ChildComponent
  },
  setup() {
    const parentMessage = ref('Hello from parent')

    const handleEvent = (payload) => {
      console.log(payload)
    }

    return {
      parentMessage,
      handleEvent
    }
  }
})
</script>
