<template>
  <Row type="flex" justify="center" style="height:80px;">
    <Col :span="8" >
      <div class="head-title">
        老板的经典语录
      </div>
    </Col>
    <Col :span="8"></Col>
    <Col :span="8">
      <Button type="success" shape="circle" class="head-button" style="width:140px;"
        @click="toIssues('https://github.com/g7coffee/niubi/issues')">
        添加一碗
      </Button>
    </Col>
  </Row>
</template>

<script>
export default {
  methods: {
    toIssues(to) {
      window.location.href = to
    }
  }
}
</script>

<style lang="less">
.head-title {
  margin-top: 20px;
  height: 80px;
  line-height: 80px;
  font-size: 36px;
  font-weight: bold;
  color: #1AAF5D;
}
.head-button {
  margin-top: 30px;
  font-size: 24px !important;
}
</style>
