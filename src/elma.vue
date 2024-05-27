<script> // JavaScript kodları buraya yazılır.
export default{ //Varsayılanı dışa aktar demektir.
data(){
    // Değişkenler buraya yazılır.
    return{
    elma:1,
    armut:2,
    inpText: "Mehmet",
    isimler:["Ali","Mehmet","Cafer","Ahmet"],
    }

},
methods:{
   // fonksiyonlar buraya yazılır.
   // Burada değişken oluşturmak için değişkenin başına "this." gelir.
},
computed:{
  // fonksiyonlar buraya yazılabilir. Fakat şu üç özelliği var:
  // 1. Parametre almaz
  // 2. Parantez almaz
  // 3. methods'a göre daha kullanışlıdır
  // Burada değişken oluşturmak için değişkenin başına "this." gelir.
},
};
</script>
<template><!-- HTML kodları buraya yazılır -->

<!-- v-if: Eğer şart sağlanıyorsa içindeki değer sayfada gözükür. -->
 <div v-if="elma=1">Merhaba</div>

 <!--v-else-if: Eğer "v-if" deki şart sağlanmazsa bunun içerdiği şarta bakılır, eğer şart sağlanıyorsa sayfada gözükür. -->
 <div v-else-if="elma=2">Hoşgeldin</div>

 <!-- v-else: Eğer hiçbir şart sağlanmazsa bu çalışır. -->
 <div v-else>Neden Geldin?</div>

<!-- v-show: "v-if" ile aynı işe yarar ama "v-if" daha güvenlidir. -->
 <div v-show="armut=2">Görüşürüz</div>

 <!-- @click: "vue" da "onclick" yerine kullanılır. Farklı kullanım şekilleri de vardır. -->
 <button @click="kek()">Tıklama</button>

 <!-- v-for: Aşağıdaki kek, isimler listesindeki her elemanın karşılığı olur ve hepsini yazdırır. -->
 <div v-for="kek in isimler">{{ kek }}</div>

 <!-- v-model: Bir yazıyı aynı anda hem input, hem de başka yerde yazdırır. -->
 <input type="text" v-model="inpText" placeholder="isminizi yazınız" required/>
 <div>{{ inpText }}</div>

 <!-- Aşağıdaki "value, input" kısmı "v-model" ile aynı görevi yapar. -->
<input type="text" :value="elma" @input="(e)=>elma=e.target.value" />

<!-- Aşağıdaki kod, rasgele üç sayı oluşturur. -->
(Math.floor(Math.random()*3))

</template>
<style> /* CSS kodları buraya yazılır. */

</style>