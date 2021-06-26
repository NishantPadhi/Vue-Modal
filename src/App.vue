<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>
  <div v-if="showModal">
    <Modal theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href="#">contact me</a>
        <a href="#">more info</a>
      </template>
      <h1>Nishant Padhi...</h1>
      <p>Full-developer at Factset</p>
    </Modal>
  </div>  
  <button @click.alt="toggleModal">open modal (alt click)</button>
</template>

<script>
import Modal from './components/Modal'
export default {
  name: 'App',
  components: { Modal },
  data() {
    return {
      title: 'My First Vue App!',
      showModal: false,
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
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