<template>
 <h1>{{ title }}</h1>
 <p>Welcome...</p> 
 <div v-if="showModal">
  <Modal :header="header" :text="text" theme="sale" @close="toggleModal"/>
 </div>
 <button @click.alt="toggleModal">open modal</button>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components:{Modal},
  data(){
    return{
      title:'My first vue App :)',
      header:'sign up for the giveaway',
      text:'grab your ninja swag for half price',
      showModal: false
    }
  },
  methods:{
    toggleModal(){
      this.showModal=!this.showModal
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
</style>
