<template>
    <div class="col" v-for="(n) in travellist" :key="n">
    <div class="name">
      <h3>{{ n.name }}</h3>
    </div>
    <div class="tipark">
      <RouterLink to="/noname_tipak">ที่พัก</RouterLink> /
      <RouterLink to="/noname_tiew">สถานที่เที่ยว</RouterLink>
    </div>
  </div>
   <h3>สถานที่เที่ยวใกล้ๆ</h3>
  <div class="col" v-for="(near, index) in neartravel" :key="index">
      <div class="name">
        <div class="name">
        <img :src="near.img" style="width: 80%;" alt="รูปภาพ 1">
        <br><br>
        <h4>{{ near.name }}</h4>
      </div>
      <div class="titravel">
        <p>{{ near.text_box }}</p>
        <p>สถานที่ : {{ near.Location }}</p>
        <p>เบอร์ติดต่อ : {{ near.phone }}</p>
        <p>Facebook : <a :href="near.link">{{ near.Facebook }}</a></p>
        <p>พิกัด : <a :href="near.place">{{ near.place }}</a></p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import { RouterLink } from 'vue-router';

const travellist=ref([
{name: 'ดอยไม่มีชื่อ', img:"https://www.reviewchiangmai.com/wp-content/uploads/2022/06/doi-noname-1536x1027.jpg", quantity: 0 ,
text_box:'เดินทางโดยสวัสดิภาพ'
}])

const neartravel=ref([
{ name: 'กระท่อมกลางนา' , 
  img: "https://cms.dmpcdn.com/travel/2020/09/09/420edb30-f265-11ea-8d35-2f4d8511ef61_original.JPG",
  text_box:'เรียกได้ว่าเป็น ที่เที่ยวลับในเชียงใหม่ เลยก็ว่าได้ เพราะตั้งอยู่กลางทุ่งนาสีเขียวที่สงบเงียบ เป็นส่วนตัว เป็นการหลีกหนีความวุ่นวายจากเมืองที่แสนคึกคัก ไปสัมผัสกับธรรมชาติ และสูดอากาศดีๆ นอกเมืองเชียงใหม่' ,
  Location:'ตำบลแม่แดด อำเภอกัลยาณิวัฒนา จังหวัดเชียงใหม่' ,
  place:' https://goo.gl/maps/pbwm2YNNP6WYg93SA',
  phone:'08-3433-1478',
  link:'https://www.facebook.com/KratomKlangNa',
  Facebook:'กระท่อมกลางนา / Kratom Klang Na'
},
])
</script>