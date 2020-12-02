<template>
  <div>
    <h1>{{ title }}</h1>
    <div>내용 : {{ contents }}</div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "About Page 테스트 중",
      contents: "변수 테스트 중",
    };
  },
};
</script>