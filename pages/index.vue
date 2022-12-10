<template>
<header class=" flex flex-wrap content-center justify-between pl-12 pr-12 bg-green-500 h-16 drop-shadow">
  <div class="logo self-center">
    <img src="logo.png" alt="" class="w-9"/>
  </div>
  
  <div class="lg:hidden">
    <span class="material-symbols-outlined self-center">
    menu
  </span>
</div>
<div class="flex justify-between ">
  <ul class="hidden gap-10 self-center basis-full lg:basis-auto color-white lg:flex">
    <li class="self-center">
      Home 
    </li>
    <li class="self-center">
      Accounts 
    </li>
    <li class="self-center">
      Contacts 
    </li>
  </ul>
</div>

 
 


  




</header>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
