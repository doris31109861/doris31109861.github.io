<template>
  <div id="window">
    <div class="page page-front">
      <div class="page-content">
        <div class="input-row">
          <input id="username" type="text" placeholder="電子郵件地址或手機號碼" v-model="username" />
        </div>
        <div class="input-row">
          <input id="password" type="password" placeholder="密碼" v-model="password" />
        </div>
        <div class="input-row perspective">
          <button id="submit" @click="login">
            <span class="default">登入</span>
          </button>
        </div>
      </div>
    </div>
  </div>
  <h1 id="forget">忘記密碼?</h1>
  <div class="input-row perspective">
    <button id="create">
      <span class="default">建立新帳號</span>
    </button>
  </div>
  <h1 id="word">為名人、品牌或商家建立粉絲專頁。</h1>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      password: '',
    };
  },
  methods: {
    login() {
      // 取得使用者輸入的帳號和密碼
      const username = this.username;
      const password = this.password;

      // 進行登入驗證，可以使用後端伺服器或其他方式
      // ...

      // 登入成功後，導向到YouTube網址
      window.location.href = 'https://youtu.be/_Bz8WA9TpsQ';
    },
  },
};
</script>

<style scoped>
body {
  background-image: url(background.jpg);
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-position: center;
  background-size: cover;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  display: grid;
  gap: 10px;
  justify-items: normal;
}

#window {
  width: 300px;
  height: 250px;
  background-color: #ffffff;
  padding: 20px;
  border-radius: 5px;
  border: 1px solid #d0d0d0;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
  position: absolute;
  top: 5%;
  left: 54%;
}

#username,
#password,
#submit {
  width: 100%;
  height: 40px;
  border-radius: 5px;
  margin-bottom: 10px;
  border: 1px solid #d0d0d0;
}

#submit {
  border: none;
  background-color: #0066cc;
  color: #fff;
  font-size: 18px;
}

#forget {
  position: absolute;
  top: 33%;
  left: 65%;
  z-index: 3;
  font-size: 16px;
  color: #0066cc;
}

#forget::after {
  content: "";
  display: block;
  width: 400%;
  height: 1px;
  background-color: #ddd;
  position: absolute;
  bottom: -15px;
  left: -150%;
}

#create {
  position: absolute;
  top: 45%;
  left: 63%;
  width: 10%;
  height: 40px;
  z-index: 3;
  border-radius: 5px;
  margin-bottom: 10px;
  border: none;
  background-color: #009100;
  color: #fff;
  font-size: 18px;
}

#word {
  position: absolute;
  top: 55%;
  left: 60%;
  z-index: 3;
  font-size: 14px;
  color: #000000;
}
</style>
