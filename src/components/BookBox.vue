<template>
    <div class="bookbox">
        <div v-for="book in books" :key="book.id" >
            <BookItem :book="book"/>
        </div>
    </div>
    


</template>

<script>

    import BookItem from "@/components/BookItem.vue";


    export default{
        name: 'BookBox',
        components: {
            BookItem
        },
        props:{
            books: Array
        }
    }

</script>

<style scoped>

.bookbox{

background-color: bisque;
padding: 1em;
color: gray;
}

</style>