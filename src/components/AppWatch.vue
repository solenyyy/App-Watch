<script>
export default {
  name: 'AppWatch',
  props: {
    timeZone: {
      type: String,
      default: 'en-US',
      required: false
    },
    color: {
      type: String,
      default: 'white',
      required: false
    }
  },
  data() {
    return {
      date: '--:--:--'
    }
  },
  mounted() {
    setInterval(() => this.setTime(), 1000)
  },
  methods: {
    setTime() {
      this.date = new Date().toLocaleTimeString(this.timeZone)
    }
  }
}
</script>

<template>
  <div class>
    <img class="correa" src="../assets/CORREA-TOP.jpeg" alt />
    <div class="container-watch">
      <div class="container-hour">
        <div class="date" :class="color">{{ date }}</div>
      </div>
      <div class="words">LED WATCH</div>
      <div class="rueda">
        <hr />
        <hr />
        <hr />
        <hr />
        <hr />
      </div>
      <div class="btn"></div>
    </div>
    <img class="correa" src="../assets/CORREA.jpeg" alt />
  </div>
</template>

<style scoped>
.correa {
  width: 117px;
  margin-left: 12%;
  margin-bottom: -5%;
}

.correa-bottom {
  width: 117px;
  margin-left: 12%;
  margin-top: -5%;
}

hr {
  margin: 2.5px;
  margin-left: -1px;
  border: 1px solid #888686da;
  width: 10px;
}

h1 {
  color: rgb(248, 112, 134);
}
.container-watch {
  width: 155px;
  height: 175px;
  background-color: #dfdbdb;
  filter: brightness(1.1);
  border-radius: 25px;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: inset 0px 0px 6px 3px grey;
}
.container-hour {
  width: 140px;
  height: 160px;
  background-color: black;
  filter: brightness(1.6);
  border-radius: 25px;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: inset 0px 0px 4px 1px rgb(175, 170, 170);
}
.date.pink {
  color: rgb(240, 45, 142);
}

.date.blue {
  color: rgb(1, 143, 143);
}
.date.white {
  color: white;
}
.date {
  color: #e6111f;
  font-size: 32px;
  font-family: "Abril Fatface";
  text-shadow: 0 0 2px rgb(150, 17, 17);
  text-align: center;
}
.words {
  font-family: Arial, Helvetica, sans-serif;
  color: white;
  font-size: 10px;
  position: absolute;
  bottom: 20px;
}

.rueda {
  background-color: #adaaaa;
  filter: brightness(1.1);
  width: 11px;
  height: 25px;
  border-radius: 5px;
  position: absolute;
  right: -7%;
  bottom: 60%;
  border: 1px solid #807d7d;
  box-shadow: inset 0px 0px 4px 1px rgb(131, 128, 128);
}

.btn {
  background-color: #adaaaa;
  filter: brightness(1.2);
  width: 2px;
  height: 25px;
  border-radius: 8px;
  position: absolute;
  right: -2%;
  bottom: 30%;
  border: 1px solid #646363;
  box-shadow: inset 0px 0px 4px 1px rgb(131, 128, 128);
}
</style>
