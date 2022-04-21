<template>
  <div class="home">
    <div class="container px-5 flex flex-col justify-around">
      <div class="title">
        <h1 class="title-text text-3xl tracking-widest mb-3">Chit Chat</h1>
        <p class="font-thin">Flirt, chat and meet people around you.</p>
      </div>
      <div class="buttons w-9/12 mx-auto">
        <router-link :to="{ name: 'Signup' }" class="block py-3 tracking-wide rounded-md bg-red-500 text-white">SIGN UP NOW</router-link><br>
        <router-link :to="{ name: 'Login' }" class="block py-3 tracking-wide rounded-md bg-blue-900 text-white">LOGIN</router-link>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@200;300;400&family=Roboto:wght@100;300;400;500&display=swap');

.home{
  min-height: 100vh;
  position: relative;
  isolation: isolate;
  color: #fff;
  text-align: center;
  background-image: url('../assets/imgs/girl-pose.jpg');
  background-position: center;
  background-size: cover;
}
.home::after{
  content: '';
  inset: 0;
  position: absolute;
  background: rgba(0, 0, 0, .8);
  z-index: -1;
}
.container{
  min-height: 100vh;
}

</style>