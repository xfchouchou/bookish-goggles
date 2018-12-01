<template>
  <div class="login-page">
    <form class="login">
      <div class="title">欢迎登录</div>
      <input type="text" class="user" v-model="account" placeholder="用户名" />
      <input type="password" class="pwd" v-model="password" placeholder="密码" />
      <div class="remember">
        <input type="checkbox" />
        <span>记住密码</span>
      </div>
      <input type="submit" value="登录" @click.prevent="login" class="login-btn"/>
    </form>
    <div class="register_button">
      <input type="submit" value="创建账户" @click.prevent="register" class="register-btn"/>
      <div>© News | 使用条款 | 隐私政策</div>
    </div>
  </div>
</template>

<script>
    // @ is an alias to /src
    /* eslint-disable */
    export default {
        name: '',
        components: {},
        data: function () {
            return {
            }
        },
        methods: {
            login(){
                this.$router.push('/Home');
            }
        },
        created() {
        },
        mounted() {
        }
    }
</script>

<style lang="scss" scoped>
  @import '../../styles/themes.scss';
  .login-page {
    background: url("~@/assets/backgroundpic.png") center top no-repeat fixed;
    height: 100%;
    width: 100%;
    background-size:cover;
  }
  .login{
    width: 360px;
    height: 330px;
    background: rgba(255,255,255,0.9);
    position: absolute;
    left: 50%;
    margin-left: -180px;
    top: 50%;
    margin-top: -190px;
    box-shadow: 0 2px 4px 0 rgba(0,0,0,0.13);
    padding: 0 30px;
    box-sizing: border-box;
    .title{
      margin-top: 26px;
      color: #585858;
      font-size: 20px;
      font-weight: bold;
    }
    .user, .pwd{
      background: rgba(32,53,128,0.01);
      border: 1px solid #DCE0E6;
      border-radius: 3px;
      width: 300px;
      height: 50px;
      box-sizing: border-box;
      font-size: 14px;
      padding-left: 14px;
    }
    .user{
      margin: 26px 0 24px 0;
    }
    .remember{
      margin: 14px 0;
      font-size: 12px;
      display: flex;
      align-items: center;
      input{
        margin-right: 14px;
      }
    }
    .login-btn{
      color: #FFFFFF;
      width: 300px;
      height: 50px;
      line-height: 40px;
      text-align: center;
      font-size: 18px;
      font-weight: bold;
      cursor: pointer;
      margin: 0 auto;
      background-color: $themes-BgColor;
      border: none;
    }
  }
  .register-btn {
    margin-top: 20px;
    width: 300px;
    height: 50px;
    line-height: 40px;
    text-align: center;
    font-size: 18px;
    font-weight: bold;
    cursor: pointer;
    background-color: #fff;
    border: none;
    color: #1f4f82;
  }

  .register_button {
    width: 360px;
    height: 120px;
    background: rgba(255,255,255,0.9);
    position: absolute;
    margin-left: -180px;
    top: 70%;
    left: 50%;
    box-sizing: border-box;
    div{
      color: #324b5c;
      margin-top: 20px;
      font-size: 12px;
    }
  }
</style>
