<template>
  <div>
    <h1>Welcome to {{title}}!</h1>
    <input type="text" v-model="input1" />
    <button type="button" @click="getData">Get</button>
    <button type="button" @click="setData">Set</button>

    <select class="form-control" v-model="region" @change="changeRegion">
      <option :key="i" :value="data.text" v-for="(data,i) in options">{{data.text}}</option>
    </select>

    <table class="table table-bordered" v-show="tableShow">
      <tr :key="i" v-for="(data,i) in options">
        <td>{{data.value}}</td>
        <td>{{data.text}}</td>
      </tr>
    </table>
    <a href="/about"> /about gogo </a>

  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "하이하이 뷰뷰뷰",
      title2: "Seoul",
      input1: "abcd",
      options: [
        { value: "S", text: "Seoul" },
        { value: "J", text: "Jeju" },
        { value: "B", text: "Busan" },
      ],
      region: "Seoul",
      tableShow: true,
    };
  },
  watch: {
    input1() {
      console.log(this.input1);
    },
    title() {},
  },
  methods: {
    getData() {
      alert(this.input1);
    },
    setData() {
      this.input1 = "12345";
    },
    changeRegion() {
      console.log(this.region);
    },
  },
  beforeCreate() {
    console.log("beforeCreate");
  },
  created() {
    console.log("created");
  },
  beforeMount() {
    console.log("beforeMount");
  },
  mounted() {
    console.log("mounted");
  },
  beforeUpdate() {
    console.log("beforeUpdate");
  },
  updated() {
    console.log("updated");
  },
  beforeDestroy() {
    console.log("beforeDestroy");
  },
  destroyed() {
    console.log("beforeDestroy");
  },
};
</script>