<template>
  <main>
    <section>
      <h2>Library:</h2>
    </section>
      <div class="home">
        <Book v-for="book in books" :key="book.id" :book="book"/>
      </div>
  </main>
</template>

<script>
import Book from '@/components/Book.vue'

export default {
  name: 'Books',
    props: {
    books: Array
  },
  components: {
    Book
  }
}
</script>
