<script setup>
import { reactive } from "@vue/reactivity";

// list foods
let foods = reactive([{id:0,imgPath:'https://bia2safa.net/goto/file/image/2590975',name:'زرشک پلو با مرغ',price:Intl.NumberFormat().format(90000)},
{id:1,imgPath:'https://noktechi.ir/wp-content/uploads/2022/04/kabab-koubide-arzan.jpg',name:'کوبیده با برنج',price:Intl.NumberFormat().format(120000)},
{id:2,imgPath:'https://images.kojaro.com/2020/11/0a3c00fb-8b92-42cb-b789-21f96616e25b.jpg',name:'جوجه با برنج',price:Intl.NumberFormat().format(90000)},
{id:3,imgPath:'https://salamdonya.com/assets/images/37/37896ucz5.jpg',name:' قورمه سبزی',price:Intl.NumberFormat().format(80000)},
{id:4,imgPath:'https://parsiday.com/wp-content/uploads/2019/02/fish-rice-vegetables.jpg',name:' سبزی پلو با ماهی',price:Intl.NumberFormat().format(100000)},
{id:5,imgPath:'https://blog.okcs.com/wp-content/uploads/2022/06/f333.jpg',name:' خورشت قیمه',price:60000},
{id:6,imgPath:"https://cdn.sarashpazpapion.com/files/recipes/pictures/org/2020/09/01/mc21gn6a5rrb3jisc5uqfu3lh4jivnp030wpaEUpnS3ozOxC.webp",name:'دیزی',price:Intl.NumberFormat().format(90000)}
])
</script>

<template>
  
  <div class="text-center mt-8">
      <h1 class="text-2xl font-bold">منوهای فروشگاه</h1>
      <p style="font-size:0.8rem">غذاهایی که میخوای رو انتخاب کن</p>
  </div>

  <div class="mt-8">
      <hr style="border-top: 1px solid black;">
      <div class="flex justify-around mt-4 mb-4 md:justify-center">
          <div><a class="underline">غذا</a></div>
          <div><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                 <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5L8.25 12l7.5-7.5" />
                </svg>
            </div>

          <div class="md:mr-8"><a>نوشابه</a></div>
          
          <div><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                   <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5L8.25 12l7.5-7.5" />
               </svg>
          </div>

          <div class="md:mr-8"><a>ساندویچ</a></div>
      </div>
      <hr style="border-top: 1px solid black;">
  </div>

  <div class="mr-6 md:grid grid-cols-3" >

<!-- list foods -->
<div  v-for="(food , index) in foods" :key="index" class="mr-4 mt-8 pr-12 max-w-sm bg-white rounded-lg shadow-md dark:bg-gray-800 dark:border-gray-700">
    <a href="#" >
        <img class="p-8 rounded-t-lg w-full" :src="food.imgPath" alt="product image">
    </a>
    <div class="px-5 pb-5">
        <div class="flex items-center mt-2.5 mb-5">
            <svg aria-hidden="true" class="w-5 h-5 text-yellow-300" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>First star</title><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
            <svg aria-hidden="true" class="w-5 h-5 text-yellow-300" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Second star</title><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
            <svg aria-hidden="true" class="w-5 h-5 text-yellow-300" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Third star</title><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
            <svg aria-hidden="true" class="w-5 h-5 text-yellow-300" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Fourth star</title><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
            <svg aria-hidden="true" class="w-5 h-5 text-yellow-300" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Fifth star</title><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path></svg>
            <span class="bg-blue-100 text-blue-800 text-xs font-semibold mr-2 px-2.5 py-0.5 rounded dark:bg-blue-200 dark:text-blue-800 ml-3">5.0</span>
        </div>
        <a href="#">
            <h5 class="text-xl font-semibold tracking-tight text-gray-900 dark:text-white">{{food.name}}</h5>
        </a>
        
        <div class="mt-2"><span class="text-sm font-bold text-gray-900 dark:text-white">قیمت: {{food.price}} هزار تومان</span></div>

        <div class="flex justify-between items-center">
            <div class="text-sm text-red-400" style="font-size:0.8rem">همراه با سبزی  و پیاز</div>
            
            <div class="flex">
                <div class="bg-red-600 rounded-full"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                         <path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
                     </svg>
                </div>
                <div class="w-6 mr-3"><p>0</p></div>
                <div class="bg-gray-400 rounded-full"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 12h-15" />
                     </svg>
                </div>
            </div>
        </div>

    </div>
</div>


  </div>

  <div class="flex justify-start mr-4 mt-4">
      <div><button class="bg-yellow-500 p-2 rounded-xl text-white hover:bg-yellow-700">ارسال فاکتور و اتمام خرید</button></div>
  </div>
</template>


<style scoped>

</style>
