<template>
<div>
    <el-input id="accountNumber"  size="large" placeholder="请输入账号" v-model="accountNumber" clearable></el-input>
     <el-input id="pwd" placeholder="请输入密码" v-model="pwd" size="large" show-password></el-input>
     <el-button id="lognBtn" type="primary" @click="login">登录</el-button>
</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Index from '@/components/Index.vue'; // @ is an alias to /src

@Component({
  name:'login',
  components: {
    Index,
  },
})
export default class extends Vue {
  private accountNumber ='';
  private pwd ='';

  private login(){
    console.log("登录...",this.accountNumber,this.pwd );
    this.$router.push('/home')
  }
}
</script>

<style >
  #lognBtn {
    margin-top: 10px;
  }
  #accountNumber {
    width: 400px;
    margin-top: 10px;
  }
  #pwd {
    width: 400px;
    margin-top: 10px;
  }
</style>