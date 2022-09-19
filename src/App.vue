<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import { ref } from '@vue/reactivity';
import RestaurantInformation from './components/RestaurantInformation.vue';
import Menu from './components/Menu.vue';

const condition = ref(false)
const listMenu = ref(null)

</script>

<template>
   
<!-- header site -->
<nav class="bg-white border-gray-200 px-2 sm:px-4 py-2.5 rounded dark:bg-gray-900">
  <div class="container flex flex-wrap  items-center mx-auto md:justify-center">
    
    <button @click="condition = !condition"  data-collapse-toggle="navbar-default" type="button" class="inline-flex items-center p-2 ml-3 text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600" aria-controls="navbar-default" aria-expanded="false">
      <span class="sr-only">Open main menu</span>
      <svg class="w-6 h-6" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z" clip-rule="evenodd"></path></svg>
    </button>
    <button class="absolute bg-red-400 p-2 left-6 top-3 rounded md:hidden"><svg class="h-6 w-6 text-white"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round">  <path d="M6 2L3 6v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V6l-3-4z" />  <line x1="3" y1="6" x2="21" y2="6" />  <path d="M16 10a4 4 0 0 1-8 0" /></svg></button>

    <div  :class="condition ? '' : 'hidden'" class="w-full md:inline-block md:w-auto" id="navbar-default">
      <ul  class="flex flex-col p-4 mt-4 bg-gray-50 rounded-lg border border-gray-100 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
        
        <li>
          <a href="#" class="block py-2 pr-4 pl-3 underline text-gray-700 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">صفحه اصلی</a>
        </li>
        <li>
          <a href="#" class="block  py-2 pr-4 pl-3 text-gray-700 rounded hover:bg-gray-100 md:hover:bg-transparent md:mr-4 md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">منو</a>
        </li>
        <li>
          <a href="#" class="block py-2 pr-4 pl-3 text-gray-700 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">تماس با ما</a>
        </li>
        
      </ul>
    </div>

    <div class="hidden md:flex md:absolute md:left-20">
      <div class="bg-yellow-400 rounded hover:bg-yellow-600"><button class="p-2"><svg class="h-6 w-6 text-white"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round">  <path d="M6 2L3 6v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V6l-3-4z" />  <line x1="3" y1="6" x2="21" y2="6" />  <path d="M16 10a4 4 0 0 1-8 0" /></svg></button></div>
      <div class="mr-4 bg-yellow-400 rounded-xl hover:bg-yellow-600"><button class="p-3 text-white">پنل کاربری</button></div>
    </div>
  </div>
</nav>

  <RestaurantInformation  />

  <!-- Menu and food list -->
  <Menu class="mt-24" />

  <div class="mt-12  img-footer"></div>

<!-- Contact us and send a comment -->
  <div class="md:grid grid-cols-2 mt-12 mr-4">

    <div>
      <div class="text-red-400">به رستوران ما خوش آمدید امیدواریم از غذاها و محصولات ما لذت ببرید:)))</div>

      <div class="flex flex-col mt-8">
        <div>
          <ul class="flex">
            <li class="rounded-full bg-pink-200 p-4 hover:p-6"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 01-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 00-1.091-.852H4.5A2.25 2.25 0 002.25 4.5v2.25z" />
                </svg>
            </li>
            <li class="mr-4 mt-4">09121234567</li>
          </ul>
        </div>

        <div class="mt-8">
          <ul class="flex">
            <li class="rounded-full bg-pink-200 p-4 hover:p-6">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                         <path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
                         <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
               </svg>
            </li>
            <li class="mr-4 mt-4">تهران - بزرگراه نواب </li>
          </ul>
        </div>
        
        <div class="mt-8">
          <ul class="flex">
            <li class="rounded-full bg-pink-200 p-4 hover:p-6">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75" />
              </svg>
            </li>
            <li class="mr-4 mt-4">muhamad.reza.naderi@gmail.com</li>
          </ul>
        </div>

      </div>
    </div>

    <div class="mt-8">
      
<form style="width:95%">
  <div class="mb-6">
    <input type="email" id="email" class="bg-white-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="نام و نام خانوادگی" required="">
    
  </div>
  <div class="mb-6">
    <input type="password" id="password" class="bg-white-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="شماره تماس" required="">
  </div>
  <div class="flex items-start mb-6">
    <textarea id="message" rows="4" class="block p-2.5 w-full text-sm text-gray-900 bg-white-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="پیام شما برای ما"></textarea>
  </div>
  <div class="w-28"><button type="submit" class="text-white bg-yellow-400 hover:bg-yellow-600 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm w-full sm:w-auto px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">ارسال</button></div>
</form>

    </div>

    <div></div>

  </div>

<!-- footer -->
  <div class="footer bg-red-500 h-8 rounded-md text-center mt-8 text-white">
    طراحی شده توسط MohammadReza Naderi
  </div>
</template>

<style >

*{
  font-family: "Byekan";
}

@font-face {
  font-family: "Byekan";
  src: url("./assets/Byekan.ttf");
}

@media screen and (max-width:572px){
  /* #navbar-default{
    display: block;
  } */
}

.img-footer{
    height: 10rem;
    border-bottom-left-radius: 150px;
    border-bottom-right-radius: 150px;
    background: orange;
    background-image: url('https://resizer.otstatic.com/v2/photos/wide-huge/2/43613556.jpg');
    background-repeat: round;
}

</style>
