<script setup>
import Footer from '../components/footer.vue'
</script>

<template>
    <div class="container mt-3">
        <div class="row">
            <div class="col-4 mx-auto">
                <div class="card p-3 rounded-0 text-black">
                    <div class="header">
                        <img src="/public/img/Instagram.png" class="imgFb" style="width: 70%" />
                        <p class="text-center" style="font-size: 16px; padding: 20px">
                            Sign up to see photos and videos from your friends.
                        </p>
                        <a href="#" style="text-decoration: none">
                            <div class="fbw">
                                <img src="/public/img/fb.png" alt="" style="width: 10%" />
                                <h6 style="color: white; margin-top: 5px">Log in with Facebook</h6>
                            </div>
                        </a>
                    </div>
                    <div class="container mt-0">
                        <div class="line"></div>
                        <span class="text">OR</span>
                        <div class="line"></div>
                    </div>
                    <div class="input">
                        <input class="form-control rounded-0" type="text" placeholder="Mobile Number or Email"
                            aria-label="readonly input example" style="background-color: #fafafa; font-size: smaller" />
                    </div>
                    <div class="input">
                        <input class="form-control rounded-0" type="text" placeholder="Full name"
                            aria-label="readonly input example" style="background-color: #fafafa; font-size: smaller" />
                    </div>
                    <div class="input">
                        <input class="form-control rounded-0" type="text" placeholder="Username"
                            aria-label="readonly input example" style="background-color: #fafafa; font-size: smaller" />
                    </div>
                    <div class="input">
                        <input class="form-control rounded-0" type="text" placeholder="Password"
                            aria-label="readonly input example" style="background-color: #fafafa; font-size: smaller" />
                    </div>
                    <div class="container">
                        <h6 class="text-center mt-4" style="
                            color: #737373;
                            font-size: 12px;
                            padding-left: 30px;
                            padding-right: 30px;
                        ">
                            People who use our service may have uploaded your contact information to Instagram. Learn
                            More
                        </h6>
                    </div>
                    <div class="container">
                        <h6 class="text-center mt-1" style="
                            color: #737373;
                            font-size: 12px;
                            padding-left: 30px;
                            padding-right: 30px;
                        ">
                            By signing up, you agree to our Terms , Privacy Policy and Cookies Policy . </h6>
                    </div>
                    <div class="container">
                        <button class="signup">
                            <h6 style="margin-top: 5px;">Sign Up</h6>
                        </button>
                    </div>
                </div>
                <div class="card mt-3 rounded-0 text-black">
                    <div class="sign">
                        <p style="margin-top: 15px; margin-right: 10px">Have an account?</p>
                        <router-link to="/" class="button-signup"> Log in </router-link>
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
    <Footer/>
</template>

<style>
.imgFb {
    width: 100%;
    height: 100%;
    margin-left: 50px;
}

.button-signup {
    text-decoration: none;
}

.header {
    padding: 20px;
}

.fbw {
    background-color: #1877f2;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    border-radius: 6px;
    padding: 5px;
}

.signup {
    background-color: #4CB5F9;
    border-radius: 6px;
    padding: 3px;
    color: #FFFFFF;
    border: none;
    margin-top: 10px;
    margin-bottom: 30px;
    width: 80%;
}

.input {
    margin: 5px;
}
</style>
