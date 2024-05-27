<script>
export default {
  data() {
    return {
      isim: "Mehmet",
      yas: 26,
      sayi1: null,
      sayi2: null,
    };
  },
  methods: {
    mesajGoster() {
      const uretilenSayi= (Math.floor(Math.random()*3))+1
      const uretilenSayi2 = (Math.floor(Math.random()*3))+1
      this.sayi1 = uretilenSayi;
      this.sayi2 = uretilenSayi2;

      if(this.sayi1==1 & this.sayi2==2 || this.sayi1==2 & this.sayi2==3 || this.sayi1==3 & this.sayi2==1 ){
        document.getElementById("kazanan").innerHTML="Kazanan 1.Oyuncu";
        document.getElementById("kazanan").style.color="tomato";
      }
 
       else if(this.sayi1 == this.sayi2){
        document.getElementById("kazanan").innerHTML="BERABERE";
        document.getElementById("kazanan").style.color="gray";
      }

      else{
        document.getElementById("kazanan").innerHTML="Kazanan 2.Oyuncu";
        document.getElementById("kazanan").style.color="tomato";
      }

    },
  },
};
</script>
<template>
 
  <div class="div-1">
    <div class="div-2">
      <div class="div-3">
        <div v-if="sayi1>0" class="oyuncu"><p id="win-1" class="Oyuncu-1">1. Oyuncu</p></div>
        <div v-if="sayi1 == 1"><img class="obje" src="./assets/images/tas.webp"/></div>
        <div v-else-if="sayi1 == 2"><img class="obje" src="./assets/images/makas.jpg"/></div>
        <div v-else-if="sayi1== 3"><img class="obje" src="./assets/images/kagit.webp"/></div>
        <div v-else></div>
      </div>
      <div class="div-3">
        <div v-if="sayi2>0" class="oyuncu"><p id="win-2" class="Oyuncu-1">2. Oyuncu</p></div>
        <div  v-if="sayi2 == 1"><img class="obje" src="./assets/images/tas.webp"/></div>
        <div v-else-if="sayi2 == 2"><img class="obje" src="./assets/images/makas.jpg"/></div>
        <div v-else-if="sayi2 == 3"><img class="obje" src="./assets/images/kagit.webp"/></div>
        <div></div>
      </div>
    </div>
  </div>
  <div>
    <button id="button" @click="mesajGoster()">tıkla</button>
  </div>
    
  <div id="kazanan">

  </div>
  
</template>
<style>
.obje{
  height:120px;
  width:150px;
}
.div-1 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 500px;
  margin-bottom:60px;
}
.div-2 {
  margin-bottom: 10px;
  display:flex;
  flex-direction: row;
}
.div-3{
  margin-left:430px;
  font-size:35px;
}
#button{
  margin-left:-410px;
  width: 750px;
  font-family: monospace;
  font-size: 35px;
  margin-top: 170px;
  height:54px;
  border-radius: 7cqb;
  background-color: lightslategrey;
  color: aliceblue;
}
.Oyuncu-1{
  margin-top:-63px;
  color:tomato;
}
.oyuncu{
  width:155px;
}
#kazanan{
  color: #7c7373;
  width: 70px;
  height: 205px;
  margin-top: 23px;
  margin-left: 369px;
  font-size: 39px;
  font-family: auto;
  font-weight: lighter;
}
</style>




