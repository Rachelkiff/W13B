<template>
<div id="body-container">
    
  <div id="toggler-button" @click="isGrid = !isGrid">
 <p v-if="isGrid">List View</p>
 <p v-else>Grid View</p>
 </div>
    
 <div id="tweets" :class="{grid: isGrid, list: !isGrid}">
 <user-tweet
     :class="{gridTweet: isGrid, listtweet: !isGrid}" v-for="tweet in tweets" v-bind:key="tweet" :tweet="tweet"></user-tweet>
 </div>
</div>

   
</template>

<script>
import UserTweet from "./tweets"

export default {
 name: "page-body",
 components: { UserTweet,
 },
 
 data  () {
   return {
     isGrid: true,
     tweets: [
 {  
    content:
     "Your current situation is not your final destination.",
    author: "LifeTweets",
    date: "01-21-2019", 
},
{
    content: "Be brave enough to be bad at something new.",
    author: "LifeTweets",
    date: "01-30-2019", 
},
{
    content: "If they say it’s impossible; it’s impossible for them, not you.",
    username: "LifeTweets",
    date: "02-17-2019", 
},
{
    content: "You deserve a wild love from a gentle soul.",
    username: "LifeTweets",
    date: "03-03-2019", 
},
{
    content: "Let it go. Something beautiful wants to grow in its place.",
    username: "LifeTweets",
    date: "04-14-2019", 
},
{
    content: "Keep watering yourself until you feel like you again",
    username: "LifeTweets",
    date: "06-02-2019", 
},
{
    content: "Pay attention to the things you are naturally drawn to. They are good for your soul.",
    username: "LifeTweets",
    date: "08-11-2019", 
},
{
    content:  "Don’t waste your energy on revenge. Your inner peace is more important.",
    username: "LifeTweets",
    date: "03-15-2020", 
},
{
    content: "May the next few months be a period of beautiful transformation for you.",
    username: "LifeTweets",
    date: "07-21-2020", 
},
{
    content: "Wherever you're at in your life, you're not alone.",
    username: "LifeTweets",
    date: "09-21-2020", 
},
],

   }
 },

 
};

</script>


<style scoped>
* {
   padding: 0;
   margin: 0;

}
.grid {
  width: 80%;
  margin-left: 5%;
  display: grid;
  grid-template-columns: (auto-fit, minmax(200px, 1fr));
  column-gap: 5%;
  row-gap: 5vh;
}
.list {
 display: grid;
 align-items: center;
 justify-items: center;
 row-gap: 30px;
}
#body-container {
 min-height: 80vh;
}
#toggler-button {
    transition:all 0.05s ease-in-out;
    margin: 15px;
    border-radius: 15px;
    padding: 30px;
    background: lightpink;
    color: lightsalmon;
    width: 75px;
    box-shadow: 3px 3px 6px lightsteelblue ;
}
#toggler-button:hover{
    cursor: pointer;
}
#toggler-button:active {
    transition: all 0.05s ease-in-out;
    cursor: pointer;
    box-shadow: 0px 0px 0px lightsteelblue ;
}
</style>
