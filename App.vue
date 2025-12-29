<template>
  

    <div class="menu">
      <a v-for="작명 in 메뉴들" :key="작명">{{작명}}</a>
    
    </div>

    <div class="black-bg" v-if="모달창열렸니1 == true">
      <div class="white-bg">
          <h4>역삼동 원룸</h4>
          <p>역삼동 웜룸에 관한것입니다.</p>
          <button  @click="모달창열렸니1=false">버튼</button>
      </div>

      

    </div>
    <div class="black-bg" v-if="모달창열렸니2 == true">
      <div class="white-bg">
          <h4>천호동 원룸</h4>
          <p>천호동 웜룸에 관한것입니다.</p>
          <button  @click="모달창열렸니2=false">버튼</button>
      </div>

    </div>
    <div class="black-bg" v-if="모달창열렸니3 == true">
      <div class="white-bg">
          <h4>마포구 원룸</h4>
          <p>마포구 웜룸에 관한것입니다.</p>
          <button  @click="모달창열렸니3=false">버튼</button>
      </div>

    </div>

    



    <div>
      <img src="./assets/img1.jpg" class="room-img">
       <h4 @click="모달창열렸니1=true">{{ products[0] }} </h4>
       
      <p>50 만원</p>
      <button v-on:click="increase1">허위매물 신고버튼</button><span>신고수 : {{신고수}}</span>
    </div>

    <div>

      
    </div>

    <div>
      <img src="./assets/img2.jpg" class="room-img">
      <h4 @click="모달창열렸니2=true">{{ products[1] }} </h4>
      <p>50 만원</p>
      <button v-on:click="increase2">허위매물 신고버튼</button><span>신고수 : {{신고수1}}</span>
      
    </div>

    <div>
      <img src="./assets/img3.jpg" class="room-img">
      <h4 @click="모달창열렸니3=true">{{ products[2] }}</h4>
      <p>50 만원</p>
       <button v-on:click="increase3">허위매물 신고버튼</button><span>신고수 : {{신고수2}}</span>
      
    </div>
</template>


<script>

export default {

  name: 'App',
  data(){

    return{
        모달창열렸니1: false,
        모달창열렸니2: false,
        모달창열렸니3: false,
        스타일: 'color : blue',
        메뉴들: ['Home','Shop','About'],
        products : ['역삼동원룸','천호동원룸','마포구원룸'],
        신고수: 0,
        신고수1: 0,
        신고수2: 0,
       
       
    }

  },
  methods: {
    increase1(){
      this.신고수+=1;

    },
    increase2(){
      this.신고수1+=1;

    },
     increase3(){
      this.신고수2+=1;

    },
   

  },
 
 
  components: {
    
  }
}
</script>

<style>

body{

  margin: 0

}

div {

  box-sizing:border-box;
}

.black-bg{
  width: 100%; height: 100%;
  background: rgba(red, green, blue, alpha);
  position: fixed; padding: 20px;
}

.white-bg{
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;


}




#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;


}

.menu {
  background:darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a{
  color: white;
  padding: 10px;

}

.room-img{
  width: 100%;
  margin-top: 40px;

}



</style>
