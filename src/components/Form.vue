<template>
  <div class="bg-white w-1/2 m-4 rounded-lg shadow p-4 mx-auto text-black">
    <label class="block">
      <span class="text-gray-700">Title</span>
      <input 
        class="form-input mt-1 block w-full" placeholder="My New Note"
        v-model="title"
      >
  </label>
   <label class="block mt-4">
      <span class="text-gray-700">Cotent</span>
      <textarea 
        class="form-textarea mt-1 block w-full" placeholder="Content of Note"
        v-model="content"
      ></textarea>
  </label>
  <div class="buttons w-full flex justify-center">
    <button class="bg-gray-500 hover:bg-gray-700 text-white font-bold py-2 px-4 rounded mt-4 mr-4 flex-grow"
      @click="$router.push('/')"
    >
      Cancel
    </button>
     <button 
      class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded mt-4 flex-grow"
      @click="add"
     >
      Add
    </button>
  </div>
  </div>
</template>

<script>
  export default {
    name:'Form',
    data() {
      return {
        title: '',
        content:''
      }
    },
    methods: {
      add() {
        this.$store.dispatch('addNote', {
          id:'?', 
          title: this.title,
          content: this.content
        }),
        this.$router.push('/')
      }
    },
  }
</script>

<style lang="scss" scoped>

</style>