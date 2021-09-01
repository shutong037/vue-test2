<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <p class="tip" @click="linkPage()">开始进行学习 {{step}}</p>
    <div class="poetry">
      <h3>{{poetry.title}}</h3>
      <h6>{{poetry.author}}</h6>
      <p v-for="item in poetry.content"  :key="item">{{item}}</p>
    </div>
  </div>
</template>

<script>
import { formatDate} from '@/utils/common.js'

export default {
  name: 'Home',
  data () {
    return {
      step: '踩坑步骤！',
      poetry: {
        title: '水调歌头',
        author: '作者：苏轼',
        content: ['丙辰中秋，欢饮达旦，大醉，作此篇，兼怀子由。', '明月几时有，把酒问青天。', '不知天上宫阙，今夕是何年。',
          '我欲乘风归去，又恐琼楼玉宇，高处不胜寒。', '起舞弄清影，何似在人间。', '转朱阁，低绮户，照无眠。', '不应有恨，何事长向别时圆？',
          '人有悲欢离合，月有阴晴圆缺，此事古难全。', '但愿人长久，千里共婵娟。']
      }
    }
  },
  mounted () {
    this.init()
  },
  methods: {
    init () {
      const time = formatDate(new Date())
      console.log(time)
    },
    linkPage () {
      this.$router.push({ path: '/about' })
    }
  }
}
</script>
<style scoped lang="scss">
  *{
    margin: 0;
    padding: 0;
  }
  .tip{
    font-size: 16px;
    color: #333333;
    font-weight: bold;
    cursor: pointer;
  }
  .poetry{
    margin-top: 40px;
    color: #333333;
    h3{
      height: 30px;
      line-height: 30px;
    }
    h6{
      height: 24px;
      line-height: 24px;
    }
    p{
      height: 32px;
      line-height: 32px;
    }
  }
</style>
