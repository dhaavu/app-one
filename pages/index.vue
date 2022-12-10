<template>


<header class="flex justify-between flex-wrap gap-3 pr-14 pl-14 bg-green-500  drop-shadow ">
  <div class="brand flex justify-center">
    <img class="h-16 m-7" src="logo.png" alt="">
  </div>
  <div   class="lg:hidden flex flex-wrap content-center cursor-pointer">
    <span class="material-symbols-outlined self-center  text-3xl" @click="toggle">
    {{menu}}
   </span>
  </div>
  
  <ul class="menu hidden gap-4 flex-wrap content-center lg:flex " :class="{'active': isActive}">
    <li>Home</li>
    <li>Account</li>
    <li>Contact</li>
    <li>Opportunity</li>
  </ul>

  <div class="settings p-5 hidden justify-center content-center flex-wrap  lg:flex" :class="{'active': isActive }">
   <span class="material-symbols-outlined border-2 rounded-full p-1 border-solid border-black text-3xl self-end ">
    person
   </span>
  </div>
</header>
</template>

<script>
export default {
  name: 'IndexPage', 
  data(){
    return {
      isActive: false, 
      menu: 'menu'
    }
  }, 
  methods: { 
    toggle(){
      this.isActive = !this.isActive; 
      if(this.menu == 'menu')
        this.menu='close'
      else 
        this.menu = 'menu'
    }
  }
}
</script>
<style scoped>


.header{
  min-height: 85px;
}

/* .menu{
  flex-grow: 4;
} */

.menu li{
  font-size: 30px; 
  padding:10px
}

/* .settings{
  flex-grow: 2;
}

.brand{
  flex-grow: 1;
} */

.settings{
  flex-basis: 20%;
}

.brand{
  flex-basis:10%
}
.menu{
  flex-basis:60%
}

.active{
  display: flex;
  flex-basis: 100%;
  margin-top: 30px;
  flex-direction: column;
}
</style>
