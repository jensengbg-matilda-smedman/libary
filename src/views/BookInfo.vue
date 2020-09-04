<template>
  <div class="about">
    <router-link to="/"> Back to library </router-link>
    <p>Informaton about chosen book:</p>
    <article>
      <h3>{{ infoBook.title }}</h3>
      <p>{{ infoBook.plot }}</p>
      <p> - {{ infoBook.year }}</p>
    </article>
  </div>
</template>

<script>
export default {
 name: 'BookInfo',
 props: {
     books: Array
 },
 computed: {
    infoBook(){ 
        return this.books.filter( b => b.id == this.$route.params.id )[0]
    }
 }
}
</script>