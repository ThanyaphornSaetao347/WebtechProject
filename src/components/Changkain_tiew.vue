<template>
  <div class="col" v-for="(n) in travellist" :key="n">
    <div class="name">
      <h3>{{ n.name }}</h3>
    </div>
    <div class="tipark">
      <RouterLink to="/changkain_tipak">ที่พัก</RouterLink> /
      <RouterLink to="/changkain_tiew">สถานที่เที่ยว</RouterLink>
    </div>
  </div>
      <h3>สถานที่เที่ยวใกล้ๆ</h3>
  <div class="col" v-for="(near, index) in neartravel" :key="index">
      <div class="name">
        <div class="name">
        <img :src="near.img"  style="width: 80%;" alt="รูปภาพ 1">
        <br><br>
        <h4>{{ near.name }}</h4>
      </div>
      <div class="titravel">
        <p>{{ near.text_box }}</p>
        <p>สถานที่ : {{ near.Location }}</p>
        <p>เบอร์ติดต่อ : {{ near.phone }}</p>
        <p>เวลา : {{ near.time }}</p>
        <p>ราคา : {{ near.Price }}</p>
        <p>พิกัด : <a :href="near.place">{{ near.place }}</a></p>
      </div>
    </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const travellist=ref([
{name: 'ขุนช่างเคี่ยน', img:"https://www.reviewchiangmai.com/wp-content/uploads/2022/06/khun-chang-kian-1536x1024.jpg", quantity: 0 ,
text_box:'เดินทางโดยสวัสดิภาพ'
}])

const neartravel =ref([
{ name: 'View Suai Coffee' , 
  img: "https://img.restaurantguru.com/r6e2-Beautiful-Coffee-facade.jpg",
  text_box:'' ,
  Location:'53 ถนน ช้างเผือก Tambon Don Kaeo, Mueang Chiang Mai District, Chiang Mai 50300' ,
  place:'  https://maps.app.goo.gl/NdsWuW8hNQRTJMUE6 ',
  phone:' 081 026 7984',
  time:'-',
  Price:'-'
},
{ name: 'Chong Wa Coffee Shop' , 
  img: "https://img.wongnai.com/p/1920x0/2020/12/12/44a622e01b80440daa1f3031a8fb3a22.jpg",
  text_box:'' ,
  Location:'ตำบล ดอนแก้ว อำเภอเมืองเชียงใหม่ เชียงใหม่(หมู่บ้านม้ง ขุนช่างเคี่ยน ตรงใจกลาง เจอป้ายวางตรงต้นไม้ใหญ่ เดินลงมาตามทางจะเจอร้าน)' ,
  place:'https://maps.app.goo.gl/PFbjbaTgSo9dzv22A',
  phone:'081 180 4722',
  time:'8.00-20.00 น.',
  Price:'-'
},
{ name: 'Fernpresso at Khun Chang Khian' , 
  img: "https://10619-2.s.cdn12.com/rests/original/105_510203442.jpg",
  text_box:'' ,
  Location:'ตำบลสุเทพ อำเภอเมืองเชียงใหม่ จังหวัดเชียงใหม่' ,
  place:'https://maps.app.goo.gl/wj5GzQuKoWup4uvk6',
  phone:' 062-302-5224',
  Price:' กาแฟคั่ว เริ่มที่ 80 บาท',
  time:'07.30-17.30 น. (หยุดทุกวันอังคาร-วันพุธ เฉพาะวันพฤหัสบดีเปิด 08:30-17:30)'
},
{ name: 'กาแฟขุนช่างเคี่ยน formula hmong coffee' , 
  img: "https://cms.dmpcdn.com/travel/2020/11/27/c00efc40-3095-11eb-a4cd-6dfb9f8577eb_original.jpg",
  text_box:'' ,
  Location:'บ้านขุนช่างเคี่ยน ตำบลช้างเผือก อำเภอเมือง จังหวัดเชียงใหม่' ,
  place:' https://maps.app.goo.gl/LKNBzbFC3A1yvaHY8',
  phone:'083 322 9732',
  Price:'กาแฟคั่วเริ่มต้นที่ 340 บาท',
  time:'06.00-18.00 น.'
},
  
])

</script>

<style>

.card-img-top{
height: 100%;
padding: 25px;

}
.box_all{
justify-content: center;
align-items: center;
margin-left: 30%;
text-align: center
}

</style>