<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <p>开始进行学习 {{num}}</p>
  </div>
</template>

<script>
import { formatDate } from '@/utils/common.js'

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
      const time = formatDate(new Date())
      console.log(time)
    }
  }
}
</script>
