<<template>
  <div id="app">
    <Layout>
      <Header>
        <MyHeader />
      </Header>
      <Content>
        <router-view/>
      </Content>
    </Layout>
  </div>
</template>
<script>
import MyHeader from "@/components/header/Header.vue";

export default {
  components: {
    MyHeader
  }
}
</script>
<style lang="less">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.ivu-layout-header {
  height: 80px !important;
  background-color: #fff !important;
}
.ivu-layout-content {
  background-color: #fff;
}
</style>
