<template>
  <div class="bg-white w-1/5 mx-4 mb-4 rounded-lg shadow p-4 text-black">
    <h1 class="text-2xl text-blue-900">{{note.title}}</h1>
    <p class="text-sm">{{ note.content }}</p>
    <div class="flex justify-end text-xs">
      <button class="text-green-500 pr-2">Edit</button>
      <button class="text-red-500">Delete</button>
    </div>
  </div>
</template>

<script>
  export default {
    name:'Card',
    props: {
      note: {
        type: Object,
        default: () => ({
          id:0,
          title: '',
          content:''
        })
      },
    },
  }
</script>

<style lang="scss" scoped>

</style>