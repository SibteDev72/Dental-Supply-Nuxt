<template>
  <div
    id="categories"
    class="w-full h-fit flex flex-col gap-16 items-center py-[4rem] px-6 md:px-8 lg:px-[4rem]"
  >
    <SlidersSlider :data="{ name: 'Product Categories', variant: 'category' }">
      <CardsCategory
        class="keen-slider__slide"
        v-for="(item, index) in categories"
        :key="index"
        :data="item"
      />
    </SlidersSlider>
    <SlidersSlider :data="{ name: 'Brands', variant: 'brand' }">
      <CardsBrand
        class="keen-slider__slide"
        v-for="(item, index) in brands"
        :key="index"
        :data="item"
      />
    </SlidersSlider>
  </div>
</template>

<script setup lang="ts">
import { categories, brands } from "~/constant/data";
import "keen-slider/keen-slider.min.css";
</script>
