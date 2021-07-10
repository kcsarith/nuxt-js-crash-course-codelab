<template>
<div>
    <div class="container">
      <Hero/>
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
        />
        <SmallCardDisplay
        v-for="cardInfo in smallCardSections"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
        />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'


import { largeCardSections, smallCardSections } from "../assets/data.js"
export default Vue.extend({
  data(){
    return {largeCardInfo: largeCardSections, smallCardSections}
    }
  }
)
</script>
