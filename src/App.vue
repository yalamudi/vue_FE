<template>
  <div class="container">
    <HeaderTop bookName="Top Companies in IT Sector" authorName="and their CEOs" />

    <BookBox :books="books" />

</div>
</template>

<script>

import HeaderTop from './components/HeaderTop.vue'
import BookBox from './components/BookBox.vue'

export default {
  name: 'App',
  components: {    
    HeaderTop,
    BookBox
  },

  data(){
    return {
      books: []
    }

  },

  methods: {

    // promises

    async fetchBooks(){
      const resposeData = await fetch('https://sowmya-web-backend.herokuapp.com/api')
      const res = await resposeData.json()
      console.log( res )
      return res.data;
    }


  },
  async created(){
    this.books = await this.fetchBooks()
  }
}

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;
}

</style>
