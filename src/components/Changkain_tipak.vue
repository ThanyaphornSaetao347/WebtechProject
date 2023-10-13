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
  <h3>ที่พัก</h3>
    <div class="col" v-for="(stay, index) in stayy" :key="index">
      <div class="name">
        <div class="name">
        <img :src="stay.img" style="width: 80%;" alt="รูปภาพ 1">
        <br>
        <br>
        <img :src="stay.img2" style="width: 80%;" alt="รูปภาพ 2">
        <br><br>
        <h4>{{ stay.name }}</h4>
      </div>
      <div class="tipark">
        <p>{{ stay.text_box }}</p>
        <p>สถานที่ : {{ stay.Location }}</p>
        <p>เบอร์ติดต่อ : {{ stay.phone }}</p>
        <p>Facebook : <a :href="stay.link">{{ stay.Facebook }}</a></p>
        <p>พิกัด : <a :href="stay.place">{{ stay.place }}</a></p>
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

const stayy=ref([
{name:'บ้านพักอุทยานแห่งชาติ ดอยสุเทพ-ปุย (At Doi Suthep Pui National Park)' , 
  img: "https://resource.nationtv.tv/uploads/images/contents/w1024/2021/11/h0BsJUkwojp64TrQS7vz.webp",
  img2:"https://media-cdn.tripadvisor.com/media/photo-s/13/80/71/b4/4.jpg",
  text_box:''  ,
  Location:'ถนนศรีวิชัย ตำบลสุเทพ อำเภอเมือง จังหวัดเชียงใหม่ 50200 ',
  phone:'0 5321 0244 (ที่ทำการฯ) 0 5329 5041 (บ้านพักนักท่องเที่ยวสวนสน) ',
  Price:'คนไทย เด็ก 10 บาท ผู้ใหญ่ 20 บาท, ชาวต่างชาติ เด็ก 50 บาท ผู้ใหญ่ 100 บาท',
  link: 'https://nps.dnp.go.th/home.php?id=120&name=%25E0%25B8%25AD%25E0%25B8%258A.%25E0%25B8%2594%25E0%25B8%25AD%25E0%25B8%25A2%25%25B8%25AA%25E0%25B8%25B8%25E0%25B9%2580%25E0%25B8%2597%25E0%25B8%259E%25E0%25B8%259B%25E0%25B8%25B8%25E0%25B8%25A2',
  Facebook:'บ้านพักอุทยานแห่งชาติ ดอยสุเทพ-ปุย (At Doi Suthep Pui National Park) ',
  place:'https://maps.app.goo.gl/4BQroLfNmC7QEHZY6'
},
{ name: 'จุดกางเต็นท์' , 
  img: "https://2.bp.blogspot.com/-T01yde1WjoI/UtITZ-2eDsI/AAAAAAAAC9Q/yd2zQy-t2LA/s1600/khun_chang_keeng_014.jpg",
  img2: "https://tatcontactcenter.com/wp-content/uploads/2023/01/326284552_6198963473448004_8624843654563489621_n-1024x683.jpg",
  text_box:'สำหรับการตั้งแค้มป์กางเต็นท์ ภายในสถานีไม่มีลานกางเต็นท์ไว้รองรับนักท่องเที่ยว หากนักท่องเที่ยวมีความประสงค์จะกางเต็นท์ จะต้องมากางในพื้นที่ของศูนย์บริการนักท่องเที่ยว อุทยานแห่งชาติดอยสุเทพ-ปุย ซึ่งอยู่ห่างจากสถานีประมาณ 4 กิโลเมตร' ,
  Location:'ถนนแม่บัวมุง ตำบล ดอนแก้ว อำเภอแม่ริม เชียงใหม่ 50300',
  place:'https://maps.app.goo.gl/T7eWXFtsA3h5etbW8' ,
  Price:'ค่าบริการ เต็นท์ขนาด 3 คน ราคา 225 บาท ไม่รวมเครื่องนอน โดยค่าบริการเฉพาะเครื่องนอน ได้แก่ ถุงนอน 30 บาท/คน/คืน ที่รองนอน 20 บาท/คน/คืน และหมอน 10 บาท/คน/คืน  ค่าบริการในการใช้พื้นที่ กรณีไม่ใช้เต็นท์ของอุทยาน ต้องชำระค่าใช้พื้นที่ตามขนาดเต็นท์ ในราคา 30 บาท/คน/คืน เช่น เอาเต็นขนาด 4 คนนอนมากางเอง ต้องชำระค่าเช่าใช้พื้นที่ 4x30 = 120 บาท/คืน แม้ว่าจะนอนไม่เต็มเต็นท์ก็ตาม สามารถจองเต็นท์ล่วงหน้าก่อนวันเข้าพัก 60 วัน',
  phone:'053-210244, 086-4205242',
  link:'-',
  Facebook:'-',
},
{ name: 'โฮมเสตย์บ้านม้งขุนช่างเคี่ยน' , 
  img: "https://img.wongnai.com/p/1920x0/2018/11/16/5b66986d35af4932ae11b24a6b8ca0e2.jpg",
  img2: "https://f.ptcdn.info/550/040/000/o3cp131s1kAIe9KagJ4-o.jpg",
  text_box:'ได้มาสัมผัสบรรยากาศธรรมชาติอย่างแท้จริง เรียบง่าย และสมถะ โดยโฮมสเตย์จะตั้งอยู่ที่หมู่บ้านม้งขุนช่างเคี่ยน (ห่างจากสถานีวิจัยและศูนย์ฝึกอบรมเกษตรที่สูงขุนช่างเคี่ยนไม่เกิน 1 กิโลเมตร) และแน่นอนเลยว่า พลาดไม่ได้กับการชมความงามของดอกนางพญาเสือโคร่งที่สวยงาม และออกดอกให้ชมเพียงปีละครั้งเท่านั้น' ,
  Location:'ทางหลวงพิเศษหมายเลข 7 - 9 กรุงเทพมหานคร 10240' ,
  place:' https://maps.app.goo.gl/M6juwZUtA837xeXg6' ,
  phone:'083 322 9732',
  Price:'500 บาท',
  link:'https://www.facebook.com/profile.php?id=100063487270996',
  Facebook:'โฮมสเตย์ บ้านม้งขุนช่างเคี่ยน'
},
{ name: 'วีรันดา เชียงใหม่ เดอะ ไฮ รีสอร์ท (Veranda Chiang Mai The High Resort)' , 
  img: "https://itravel.in.th/wp-content/uploads/2020/07/%E0%B8%A7%E0%B8%B5%E0%B8%A3%E0%B8%B1%E0%B8%99%E0%B8%94%E0%B8%B2-%E0%B9%84%E0%B8%AE-%E0%B8%A3%E0%B8%B5%E0%B8%AA%E0%B8%AD%E0%B8%A3%E0%B9%8C%E0%B8%97-%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%9E%E0%B8%B1%E0%B8%81%E0%B9%80%E0%B8%8A%E0%B8%B5%E0%B8%A2%E0%B8%87%E0%B9%83%E0%B8%AB%E0%B8%A1%E0%B9%88%E0%B8%A1%E0%B8%B5%E0%B8%AA%E0%B8%A3%E0%B8%B0%E0%B8%A7%E0%B9%88%E0%B8%B2%E0%B8%A2%E0%B8%99%E0%B9%89%E0%B8%B3%E0%B8%AA%E0%B9%88%E0%B8%A7%E0%B8%99%E0%B8%95%E0%B8%B1%E0%B8%A7-itravel.jpg",
  img2: "https://prod-true-visions-media.s3.ap-southeast-1.amazonaws.com/c08d5068a10ffa88c72e534ea77f7c_IMG_8085%20copy.jpg",
  text_box:'วีรันดา ไฮ รีสอร์ท เชียงใหม่ คือสถานที่หรูหราที่ตั้งอยู่ในพื้นที่เงียบสงบและสวยงามของเชียงใหม่ รีสอร์ทนี้มีการออกแบบสมัยใหม่ที่มีเสน่ห์อันเป็นเอกลักษณ์ของไทย และมีสวนสวยที่งามเต็มไปด้วยความอุดมสมบูรณ์และมุมมองที่น่าทึ่งของภูมิภาครอบๆ ให้บริการห้องพักซึ่งตั้งอยู่บนพื้นที่ลาดของหุบเขา ท่านจะได้เพลิดเพลินกับทิวทัศน์ธรรมชาติอันน่าตื่นตาตื่นใจ ไม่ว่าจะเป็นลำธารบนภูเขา หรือนาและไร่ชาขั้นบันได ดื่มด่ำกับมรดกทางวัฒนธรรมของภาคเหนือในประเทศไทย และชื่นชมการตกแต่งในสไตล์ร่วมสมัยไปพร้อม ๆ กัน' ,
  Location:'192 หมู่ 2 บ้านโป่ง หางดง, บ้านปง, อำเภอหางดง, เชียงใหม่' ,
  place:'https://maps.app.goo.gl/HcHghmstvmHYGRN49 ',
  phone:'053 365 007',
  Price:'Deluxe 3,900 บาท/คืน Pool Suite 7,900 บาท/คืน Pool Villa 11,900 บาท/คืน',
  link:'  https://www.facebook.com/verandachiangmaithehighresort/?locale=th_TH',
  Facebook:'Veranda High Resort Chiang Mai – Mgallery'
},
{ name: 'From Farm to Sip' , 
  img: "https://10619-2.s.cdn12.com/rests/original/102_528617076.jpg",
  img2: "https://10619-2.s.cdn12.com/rests/original/102_528617074.jpg",
  text_box:'' ,
  Location:'7 หมู่4 บ้านขุนช่างเคี่ยน ตำบลช้างเผือก อำเภอเมืองเชียงใหม่, Chiang Mai, Thailand, Chiang Mai' ,
  place:'https://maps.app.goo.gl/TARjQhxma5Mgz7KV9',
  phone:'084 612 8047',
  Price:'กาแฟคั่วเริ่มต้นที่ 380 บาท',
  link:'https://www.facebook.com/KhunChangKienCoffee',
  Facebook:'กาแฟขุนช่างเคี่ยน - KCK Beans',
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