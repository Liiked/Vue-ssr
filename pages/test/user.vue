<template>
  <div>
    这是用户页面
    {{name}}
    <button>前往其他页面</button>
  </div>
</template>
<script>
  import axios from 'axios'
  export default {
    asyncData() {
      return axios.get('http://118.24.118.235:2333').then((res)=> {
        return {name: res.data.name}
      })
    },
    data() {
      return {

      };
    },
    methods: {
      to() {
        this.$router.push('/product/index')
      }
    }
  };
</script>
