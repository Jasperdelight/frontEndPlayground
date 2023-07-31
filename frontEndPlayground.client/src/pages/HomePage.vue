<template>
<div class="container-fluid">
  <section class="row bg-primary">
    <div class="col-12 text-center">
      Hello World
    </div>
  </section>
  <section class="row">
    <div class="col-4 bg-dark" style="height: 60vh;"> First col</div>
    <div class="col-4 bg-dark d-flex justify-content-around align-items-end " style="height: 20vh;">
      <p>Second col</p>
      <p>Second col 2</p>
       </div>
    <div class="col-4 bg-dark"> Third col</div>
  </section>
  <section class="row">
    <div class="col-12 bg-danger text-center">
      Bot
    </div>
  </section>

</div>

<head>
  <title>Animated Cheeseburger</title>
</head>
<body class="">
  <div class="burger justify-content-center">
  <div class="bun top"></div>
  <div class="cheese animated-cheese"></div>
  <div class="patty animated-patty"></div>
  <div class="bun bottom animated-bun"></div>
</div>
</body>
</template>

<script>
export default {
  setup() {
    return {}
  }
}
</script>

<style scoped lang="scss">
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
  background-color: #f7f7f7;
}

.burger {
  width: 100px;
  height: 100px;
  position: relative;
}

.bun {
  width: 100%;
  height: 30%;
  background-color: #e2c98a;
  border-radius: 10px;
}

.top {
  top: 0;
}

.bottom {
  bottom: -10%;
  position: relative;
}

.cheese {
  width: 80%;
  height: 10%;
  position: absolute;
  top: 25%;
  left: 10%;
  background-color: #ffd166;
  border-radius: 5px;
}

.patty {
  width: 70%;
  height: 20%;
  position: absolute;
  top: 30%;
  left: 15%;
  background-color: #73422b;
  border-radius: 3px;
}

@keyframes bounce {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
}

@keyframes rotate {
  0%, 100% {
    transform: rotate(0);
  }
  50% {
    transform: rotate(-5deg);
  }
}
.animated-cheese {
  animation: bounce 1s infinite;
}

.animated-patty {
  animation: rotate 1s infinite;
}
</style>
