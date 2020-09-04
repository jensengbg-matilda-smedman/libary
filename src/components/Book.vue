<template>
    <article @click="goTo()" 
    v-bind:style="{background: book.color}">
        <p> {{ book.title }} </p>
    </article>
</template>

<script>
export default {
    name: 'Book',
    props: {
        book: Object
    },
    methods: {
        goTo(){
            this.$router.push(`/bookInfo/` + this.book.id)
        }
    }
}
</script>

<style>

</style>