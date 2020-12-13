<template>
  <div id="app">
    <b-button @click="modalShowA = !modalShowA">Open Modal A</b-button>
    <b-button @click="modalShowB = !modalShowB">Open Modal B</b-button>
    <!-- props + emit -->
    <ModalA :propsData="modalShowA" @closeModal="closeModal"/>
    <!-- cutom v-modal -->
    <ModalB v-model="modalShowB"/>
  </div>
</template>

<script>
import ModalA from '@/components/modal-a'
import ModalB from '@/components/modal-b'

export default {
  name: 'App',
  components: {
    ModalA,ModalB
  },
  data() {
    return {
      modalShowA: false,
      modalShowB: false,
    }
  },
  methods: {
    closeModal() {
      this.modalShowA = false
    }
  },
}
</script>
