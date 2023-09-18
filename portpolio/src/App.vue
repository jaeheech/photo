<template>
  <div id="app">
    <div class="container">
      <div class="sidebar">
        <nav>
          <ul>
            <li><router-link to="/">Home</router-link></li>
            <li><router-link to="/nodejs">Node.js</router-link></li>
            <li><router-link to="/vuejs">Vue.js</router-link></li>
            <li><router-link to="/tensorflow">Tensorflow</router-link></li>
          </ul>
        </nav>
        <!-- 전화번호와 이메일을 사이드바 하단에 추가 -->
        <div class="contact">
          <p>Phone: 010-7566-4551</p>
          <p>Email: wodud8242@gmail.com</p>
        </div>
      </div>
      <div class="content"></div>
    </div>
    <!-- 이미지가 나머지 75%를 차지하도록 설정 -->
    <!-- <div class="image-container">
      <img src="./assets/home2.jpg" alt="" />
    </div> -->
    <router-view />
  </div>
</template>
<style>
body {
  margin: 0;
  padding: 0;
}
#app {
  display: flex;
  flex-grow: 1;
  font-family: Arial, sans-serif;
}

nav {
  font-size: 2.5rem;
}

.container {
  display: flex;
  align-items: flex-start;
  margin: 0;
}

.sidebar {
  width: 25%;
  height: 100vh;
  min-width: 250px;
  background-color: black;
  color: whitesmoke;
  display: flex;
  flex-direction: column;
}
nav ul {
  list-style-type: none;
  padding: 0;
}

nav li {
  margin: 10px 0;
}

nav a {
  text-decoration: none;
  color: white;
  font-size: 1.5rem;
}

nav a:hover {
  color: #007bff;
}

.content {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 75%;
}
.contact {
  margin-top: 200px;
  color: wheat;
}
</style>
