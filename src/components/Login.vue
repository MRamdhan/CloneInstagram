<template>
  <div>
    <div class="container mt-3">
      <div class="row">
        <div class="col-5" style="margin-left: 10%">
          <img src="/public/img/igLogin.png" alt="" />
        </div>
        <div class="col-4 mt-4">
          <div class="card rounded-0 text-black">
            <div style="padding-left: 50px; padding-top: 50px; padding-right: 50px">
              <img src="/public/img/Instagram.png" alt="" style="width: 80%; margin-left: 30px" />
            </div>
            <div class="input">
              <input class="form-control rounded-0" type="text" placeholder="Phone nummber,username, or email"
                aria-label="readonly input example" style="background-color: #fafafa; font-size: smaller" v-model="username" />
            </div>
            <div class="input">
              <input class="form-control rounded-0" type="password" placeholder="Password"
                aria-label="readonly input example" style="background-color: #fafafa; font-size: smaller" v-model="password"/>
            </div>
            <div class="input mt-3">
              <button @click="login" style="
                  background-color: #4cb5f9;
                  width: 100%;
                  border: none;
                  padding: 5px;
                  border-radius: 9px;
                  color: #ffffff;
                  font-size: medium;
                  font: bold;
                ">
                Login
              </button>
              <div class="container mt-4">
                <div class="line"></div>
                <span class="text">OR</span>
                <div class="line"></div>
              </div>
            </div>
            <div class="mt-3">
              <div class="fb">
                <img src="/public/img/facebook.png" alt="" width="15px;" class="img" />
                <a href="#" class="txt">Log in with Facebook </a>
              </div>
              <div class="mt-4 mb-4">
                <p class="forget-password text-center" style="font-size: 13px">Forget password?</p>
              </div>
            </div>
          </div>
          <div class="card mt-3 rounded-0 text-black">
                    <div class="sign">
                        <p style="margin-top: 15px; margin-right: 10px">Don't have an account?</p>
                        <router-link to="/signup" class="button-signup"> Sign up </router-link>
                    </div>
                </div>
          <p class="mt-3 text-center">Get the app.</p>
          <div class="another">
            <img src="/public/img/plystore.png" alt="" style="width: 150px" />
            <img src="/public/img/microsoft.png" alt="" style="width: 110px" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data(){
    return {
      username : '',
      password : '',
    }
  },
  methods : {
    async login() {
      try {
        const response = await axios.post('http://127.0.0.1:8000/api/v1/auth/login', {
          username : this.username,
          password : this.password
        });
        if(response && response.status === 200){
          const token  = response.data.token;
          localStorage.setItem('token', token);
          alert('Login Success');
          this.$router.push('/home');   
        }
      } catch(err){
        alert('Email or password incorrect');
        console.log(err);
      }
    }
  }
}
</script>


<style>
.another {
  display: flex;
  justify-content: center;
  align-items: center;
}

.signup {
  text-decoration: none;
}

.sign {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-left: 20px;
}

.input {
  margin-top: 20px;
  padding-left: 30px;
  padding-right: 30px;
}

.txt {
  text-decoration: none;
  font: bold;
  color: #3851a0;
  margin-left: 10px;
}

.fb,
.img {
  margin-top: 20px;
  margin: 2px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  width: fit-content;
}

.line {
  width: 100px;
  height: 0.6px;
  background-color: rgb(179, 177, 177);
}

.text {
  margin: 0 10px;
}

input {
  padding: 1px;
  font-size: small;
  background-color: #fafafa;
}
</style>