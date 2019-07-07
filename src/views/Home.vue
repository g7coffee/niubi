<template>
  <div style="height:calc(100vh - 80px);">
    <Row type="flex" justify="center" >
      <span class="boss-words">
        {{currentWord}}
      </span>
    </Row>
    <Row type="flex" justify="center" >
      <Button type="success" shape="circle" class="again-words" @click="anotherWords">再熬一碗</Button>
    </Row>
  </div>
</template>
<script>
export default {
  data() {
    return {
      currentWord: '',
      index: 0,
      bossWords: [
        { id: 1, word: '今天的事不用放在今天做，万一明天死了呢，就可以不用做了' },
        { id: 2, word: '重修倒是问题不大' },
        { id: 3, word: '只要事情能办成，胆子大一点' },
        { id: 4, word: '依葫芦画瓢' },
      ]
    }
  },
  mounted() {
    this.currentWord = this.currentWord = this.bossWords[this.index].word
  },
  methods: {
    anotherWords() {
      this.index ++
      if(this.index >= this.bossWords.length) this.index = 0
      this.currentWord = this.bossWords[this.index].word
    }
  }
}
</script>

<style>
.boss-words {
  font-size: 40px;
  font-weight: bold;
  text-align: center;
  margin-top: 16%;
}
.again-words {
  font-size: 26px !important;
  font-weight: bold !important;
  margin-top: 2%;
  width: 200px;
}
</style>