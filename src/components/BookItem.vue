<template>

    <div>
        <h1> {{book.company_name}}</h1>
        <h2> {{book.company_startyear}}</h2>
        <section id="rank"><h4> Rank: {{book.company_rank}}</h4></section>
        <h2> CEO : {{book.company_ceo}}</h2>
        
    </div>

</template>

<script>




export default{
    name: 'BookItem',
    props:{
        book: Array
    }
}


</script>

<style scoped>

h2{
    text-align: center;
}

h1{
    text-align: center;
}
#rank{
  background-image: linear-gradient(to bottom right, #fde2e4, #cccef0, #e2ece9, #cedfe2);
  color: black;
    padding: 1em;
    text-align: center;

}
#body{
  background-color: #e6ff00;
}
div{
    background-color: #ffb89e;
    color: black;
    padding: 1em;
}

.red{
background-color: orangered !important;

}
.green{
    color: white;
}


</style>
