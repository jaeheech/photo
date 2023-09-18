<!-- <template>
  <div class="img">
    <img src="../assets/home2.jpg" alt="" />

    <h1 class="overlay-text">안녕하세요 최재희 입니다.</h1>
  </div>
</template>
<script></script>
<style>
body html {
  width: 100%;
}
img {
  width: 100%;
  height: 100%;
}
.overlay-text {
  position: absolute;
  top: 50%;
  left: 60%;
  transform: translate(-230%, -700%);
  color: white;
  font-size: 24px;
  font-weight: bold;
  padding: 10px 20px;
  border-radius: 5px;
  display: inline;
  vertical-align: middle;
  border-right: 0.05em solid black;
}
ul {
  margin-top: 120px;
}

nav li {
  margin-top: 95px;
}
</style> -->

<template>
  <div class="img">
    <img src="../assets/home2.jpg" alt="" />
    <h1 class="overlay-text">{{ textToType }}</h1>
  </div>
</template>
<script>
export default {
  mounted() {
    const overlayText = document.querySelector('.overlay-text')
    const textToType = '안녕하세요 최재희 입니다.'
    let currentIndex = 0

    function typeText() {
      if (currentIndex < textToType.length) {
        overlayText.textContent += textToType.charAt(currentIndex)
        currentIndex++
        setTimeout(typeText, 100) // 타이핑 속도 조절
      }
    }

    typeText()
  }
}
</script>
<style>
/* 이하 스타일은 동일합니다 */
body html {
  width: 100%;
}
img {
  width: 100%;
  height: 100%;
}
.overlay-text {
  position: absolute;
  left: 60%; /* 원하는 가로 위치 */
  top: 50%; /* 원하는 세로 위치 */
  transform: translate(-230%, -700%);
  color: white;
  font-size: 24px;
  font-weight: bold;
  padding: 10px 20px;
  border-radius: 5px;
  display: inline;
  vertical-align: middle;
  border-right: 0.05em solid black;
  white-space: nowrap; /* 텍스트가 한 줄로 유지되도록 설정 */
  overflow: hidden; /* 텍스트 넘침 숨김 */
}

ul {
  margin-top: 120px;
}

nav li {
  margin-top: 95px;
}
</style>
