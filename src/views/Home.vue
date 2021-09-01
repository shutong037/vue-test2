<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <p>开始进行学习 {{num}}</p>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      num: '456'
    }
  },
  mounted () {
    this.init()
  },
  methods: {
    init () {
      console.log('123')
    }
  }
}
</script>
