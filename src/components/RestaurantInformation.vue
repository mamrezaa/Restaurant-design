<script setup>
import { ref } from 'vue'


</script>

<template>

<!-- Restaurant Information -->

<div class="w-full img-header">
  <h1 class="text-white text-xl pt-20  font-bold text-center">هر زمان غذای  سالم سفارش دهید</h1>
</div>

 <div class="text-center relative bottom-5 md:hidden"><button class="bg-yellow-400 w-36 h-10 text-white rounded-full text-center p-2">حالا سفارش دهید</button></div>

<div class="w-full flex flex-col">

  <div class="order-describe">
    <div class="flex justify-around mt-1">
      <div class="w-24 hover:p-1"><img class="rounded-xl" src="https://snapp.market/blog/wp-content/uploads/2022/02/Type-of-Eating-vegetables-02.jpg" alt=""></div>
      <div class="w-24 hover:p-1"><img class="rounded-xl" src="https://cdn.familytasty.com/wp-content/uploads/2022/01/%D9%81%D9%88%D8%A7%D8%A6%D8%AF-%D8%A7%D9%84%D9%81%D9%84%D9%81%D9%84-%D8%A7%D9%84%D8%A7%D8%AE%D8%B6%D8%B1.jpg" alt=""></div>
    </div>
    <div class="text-center mt-6"><h1 class="font-bold">چطور سفارش بدم؟</h1><p class="font-thin">مراحل زیر را به ترتیب برو جلو</p></div>
  </div>

  <div class="flex justify-center buy-step mt-12 md:justify-around md:mt-28">

    <div class="flex flex-col">
      <div class="bg-pink-300 rounded-full w-24 h-24"><svg class="h-16 w-16 mt-4 text-gray-500 pr-4 hover:pr-1"  width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">  <path stroke="none" d="M0 0h24v24H0z"/>  <g transform="rotate(27 12 12)">  <rect x="7" y="4" width="10" height="16" rx="1" />  <line x1="11" y1="5" x2="13" y2="5" />  <line x1="12" y1="17" x2="12" y2="17.01" />  </g>  <path d="M6 4l-2 1v2.5l-2 1v2.5" />  <path d="M22 13v2.5l-2 1v2.5l-2 1" /></svg></div>
      <div class="text-center">1</div>
      <div>انتخاب غدا</div>
    </div>
    
    <div class="text-red-700">- - - - -</div>

    <div class="flex flex-col">
      <div class="bg-pink-300 rounded-full w-24 h-24"><svg class="h-16 w-16 mt-4 mr-2 text-gray-500 pr-4 hover:pr-1"  width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">  <path stroke="none" d="M0 0h24v24H0z"/>  <path d="M14 3v4a1 1 0 0 0 1 1h4" />  <path d="M17 21h-10a2 2 0 0 1 -2 -2v-14a2 2 0 0 1 2 -2h7l5 5v11a2 2 0 0 1 -2 2z" />  <line x1="9" y1="7" x2="10" y2="7" />  <line x1="9" y1="13" x2="15" y2="13" />  <line x1="13" y1="17" x2="15" y2="17" /></svg></div>
      <div class="text-center">2</div>
      <div>فاکتور خرید</div>
    </div>

   <div class="text-red-700">- - - - - </div>

    <div class="flex flex-col">
      <div class="bg-pink-300 rounded-full w-24 h-24"><svg class="h-16 w-16 mt-4 mr-2 text-gray-500 pr-4 hover:pr-1"  fill="none" viewBox="0 0 24 24" stroke="currentColor">
  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"/></svg></div>
      <div class="text-center">3</div>
      <div>پرداخت هزینه</div>
    </div>

  </div>

</div>


</template>

<style scoped>
@media screen and (max-width:572px) {
  .order-describe{
        height: 200px;
        border-bottom-left-radius: 80%;
        border-bottom-right-radius: 80%;
        border-bottom: dotted;
}
}

@media  screen and (min-width:572px) {
  .buy-step{
    height: 200px;
    border-bottom-left-radius: 80%;
    border-bottom-right-radius: 80%;
    border-bottom: dotted;
  }
}

.img-header{
        height: 300px;
        border-bottom-left-radius: 80%;
        border-bottom-right-radius: 80%;
        background: orange;
        background-image: url('https://files.virgool.io/upload/users/217651/posts/rwnr3pnfrwso/mfpn1pmwk7mu.jpeg');
        
    }

</style>
