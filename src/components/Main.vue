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
</style>