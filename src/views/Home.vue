<template>

<div>
  <div class="menu">
    <a v-for="(a,i) in menu" :key="a">{{i}}{{a}}</a>
  </div>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
  </div>
  <div>
    <h4 class="red">{{products[0]}}</h4>
    <p>만원</p>
  </div>
  <div>
    <h4>{{products[1]}}</h4>
    <p>천원</p>
  </div>
  <div>
    <h4>{{products[2]}}</h4>
    <p>천원</p>
  </div>
  <input class="abc" v-model="text" type="text" />
  {{text}}
  <button class="btn" @click="[btnClick(),change()]"> 버튼 </button>
  <div class="list">
    {{this.products}}
  </div>
</div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  data(){
    return{
      text: "",
      products :['역삼동원룸', '천혼동원룸', '마포구원룸'],
      menu:['home', 'products', 'about'],
      // style: 'color : blue',
      

    }
  },
  components: {
    
  },
  methods: {
    btnClick(){
      this.products.push(this.text,)
    },
    change(){
      this.text = ""
    }
  }
}
</script>

<style lang="scss">

.menu{
  background-color:rgb(12, 63, 56);
  font-size:20px;
  padding: 15px;
  border-radius: 5px;
  a{
    color:white;
    font-size:25px;
    margin-right:50px;
    font-weight: 700;
    padding:10px;
  }
}

</style>