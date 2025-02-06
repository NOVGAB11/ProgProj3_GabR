<script setup>
import {ref} from 'vue';

const fortuneMessage = ref('')
const audio = ref(null);

const showFortune = () => {
  const randomIndex = Math.floor(Math.random() * fortunes.lenght);
  fortuneMessage.value = fortunes[randomIndex];

  if(audio.value && audio.value.paused) {
    audio.value.play();
  }
};


const fortunes = [
    "Someone will surprise you with a gift this month. ๑(◕‿◕)๑",
    "Patience is a virtue and you are virtuous. (づ ◕‿◕ )づ",
    "All that hard work will pay off soon, trust the process. ♡(ŐωŐ人)",
    "You will soon be taking a trip, an adventure awaits! ▼(´ᴥ`)▼",
    "Give yourself time today to recharge and do some soul searching. ♡(ŐωŐ人)",
    "You are beautiful, you are smart, you are amazing, YOU ARE WORTHY! ( ͡° ᴥ ͡° ʋ)",
    "Happiness is just around the corner. (=◉ᆽ◉=)",
    "You are Kenough!(づ ◕‿◕ )づ",
    "You are HIM, you've always been HIM!(=◉ᆽ◉=)",
    "Your future is so bright you need sunglasses!๑(◕‿◕)๑",
    "You've got this!"
];


</script>

<template>
  <main class="app"> 
   
    <audio id="Audio" ref="audio">
      <source src="src\assets\perfect-beauty-191271.mp3" type="audio/mp3"/>
    </audio>

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


