<template>
  <div class="container">
    <div v-if="isActive === true" v-on:click="ao()" class="hoge">{{ msg }}</div>
    <div v-if="isActive === false" v-on:click="ao()" class="piyo">カキクケコ</div>
  </div>
</template>

<style>
.hoge {
  width: 100%;
  height: 1000px;

  background-color: #feffefe;
}

.piyo {
  width: 500px;
  height: 500px;
  background-color: rgb(255, 0, 0);
}
</style>

<script>
export default {
  data() {
    return {
      msg: "Portfolio",
      isActive: true
    };
  },
  methods: {
    ao() {
      if (this.isActive === true) {
        this.isActive = false;
      } else {
        this.isActive = true;
      }
    }
  }
};
</script>
