<template>
  <main>
    <div class="main-container-80">
      <div class="cards-container">
        <!-- STAMPO N COMPONENTI COMICCARD -->
        <ComicCard
        v-for="(card,index) in cards"
        :key="index" 
        :thumb="card.thumb"
        :price='card.price'
        :series='card.series'
        :type='card.series'
        />
      </div>
      <button>LOAD MORE</button>
    </div>
  </main>
</template>



<script>

import ComicCard from '@/components/ComicCard'
import cards from '@/assets/data/dc-comics.js'

export default {
  name:'Main',
  components:{
    ComicCard
  },
  data(){
    return{
      cards
    }
  }
}
</script>

<style lang='scss' scoped>
@import '../assets/css/main.scss';
@import '../assets/css/variables.scss';
button{
  padding: 5px 15px;
  border-radius: 0;
  outline: 0;
  border: none;
  margin-bottom: 30px;
  background-color: $lightbluecolor;
  color: white;
  font-weight: 500;
}
</style>