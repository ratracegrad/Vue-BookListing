<template>
  <form action="#" method="post" class="" @submit.prevent="bookSubmit(bookTitle, bookAuthor)">
    <input type="text" name="title" value="" placeholder="Book Title" v-model="bookTitle">
    <input type="text" name="author" value="" placeholder="Book Author" v-model="bookAuthor">
    <button type="submit" name="button">Add Book</button>
  </form>
</template>

<script>
    export default {
        name: "BookForm",
      props: ['books'],
      data() {
          return {
            bookTitle: '',
            bookAuthor: ''
          }
      },
      methods: {
          bookSubmit(bookTitle, bookAuthor) {
            this.$emit('addBook', bookTitle, bookAuthor);
          }
      }
    }
</script>

<style scoped>

</style>
