<template>
  <h1>{{ title }}</h1>
  <div v-if="showModal">
    <Modal theme="" @close="toggleModal">
      <h1>Giveaway!</h1>
      <p>Free Stuff!</p>
      <template v-slot:links>
        <a href="#">sign up5</a>
        <a href="#">more info</a>
      </template>
    </Modal>
  </div>

  <div v-if="showModalTwo">
    <Modal @close="toggleModalTwo">
      <h1>test</h1>
    </Modal>
  </div>

  <br/>
  <button @click="toggleModal">open modal</button>
  <button @click="toggleModalTwo">open other modal</button>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: {
    Modal
},
  data() {
    return {
      title: 'Vue App :)',
      showModal: false,
      showModalTwo: false
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    },
    toggleModalTwo() {
      this.showModalTwo = !this.showModalTwo
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
