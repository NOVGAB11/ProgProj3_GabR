<script setup>

</script>

<template>
  <main class="app"> 
   
    <section class="greeting">
      <h1 class="main-title">Hi! I am the Medium between you and the Cosmos!</h1>
      <h2>Click on the button for a message from the Cosmos...</h2>
    </section>

    <section class="UserSection">

      <button @click="showFortune" id="UserButton" type="button">Talk to me</button>
      <p v-if="fortuneMessage" id ="UsersFortune">{{ fortuneMessage}}</p>
      
    </section>



  






  </main>
</template>


