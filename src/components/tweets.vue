<template>
<div>
    <div class="gridtweet"></div>
    <h3 v-html="tweet.author"></h3>
    <div class="list-underline"></div>
    <h3 v-html="tweet.content"></h3>
    <p class="tweet.date"><strong>{{tweet.date}}</strong></p>
</div>

   
</template>

<script>
    export default {
       name: "user-tweet",
       props:{
          tweet: {
            type: Object,
            required: true,
         },
       },
    };
</script>

<style scoped>
.gridtweet{
    border-radius: 15px;
    box-shadow: 3px 3px 6px lightsteelblue;
     padding: 15px;
     transition: all 0.05s ease-in-out;
}
.tweet-date {
    margin: 2vh 0;
}
.gridtweet:active{
   box-shadow: 0px 0px 1px lightslategray;
   transition: all 0.05s ease-in-out; 
}
</style>