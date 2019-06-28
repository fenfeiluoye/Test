<template>
  <div class="hello">
    <!-- <el-input v-model.number="inVal" size="small" style="width:100px" @change="handleChange"></el-input> -->
    <el-input-number v-model="xxx" :controls="false" :debounce="900" @change="handleChangeNumber"></el-input-number>
    <span>{{ money }}</span>
    <el-button @click="show"></el-button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      inVal: '',
      money: '',
      xxx: ''
    }
  },
  mounted() {

  },
  methods:{
    handleChange(){
      // setTimeout(() => {
      //   this.money = this.inVal * 20
      // },500)

console.log(this.inVal)
    //       var re = /^\d+(?=\.{0,1}\d+$|$)/ 
    // if (this.money != "") { 
    //     if (!re.test(this.money)) { 
    //         alert("请输入正确的数字"); 
    //         this.money = ''

    //     } 
    // } 
    },
    handleChangeNumber(){
      //  let _this = this
      //  console.log(this.xxx)
       setTimeout(() => {
this.xxx = Number(this.xxx).toFixed(2)
       },1000)
    },
    show(){
      console.log(this.xxx.toFixed(2),2121)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
span{
  display: inline-block;
  width: 100px;
  height: 30px;
  background: #ccc;
}
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
    -webkit-appearance: none;
    appearance: none; 
    margin: 0; 
}
</style>
