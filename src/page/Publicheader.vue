<template>
  <div class="header">
    <img class="header-logo" src="../assets/images/login/thclogo@2x.png"/>
    <div class="header-contact">
      <img src="../assets/images/login/home-phone@2x.png"/>
      <span>400-522--6565</span>
    </div>
  </div>
</template>

<script>
export default {
  name: '', //模块名称
  data() {
    return {};
  },
  //父组件传递过来的数据（两种方式声明：1.数组 2.对象）
  props: [],
  //对象方式
  /*props: {
      age: {
        type: Number,
        default: 0,
        required: true,
        validator: function (value) {
          return value >= 0
        }
      }
    }*/
  //要用到哪些子组件（如果组件已是最小粒度，那么可省略该属性）
  components: {},
  //计算属性
  computed: {
    /* fullName() {
         return this.firstName + this.lastName
       } */
  },
  //监听
  watch: {
    /* title(preVal, newVal) {
        console.log(`改变之前的值：${preVal}；改变之后的值：${newVal}`)
      } */
  },
  //函数集，自己封装，便于开发使用
  methods: {
    /* getCurrentDate() {
        return new Date().toLocaleDateString()
      } */
  },
  //生命周期钩子：实例初始化之后，数据观测(data observer) 和 event/watcher 事件配置之前被调用
  beforeCreated() {},
  //生命周期钩子：组件实例完成创建之后调用
  created() {},
  //生命周期钩子：组件实例渲染完成时调用
  mounted() {}
};
</script>

<style scoped lang="less">
.header {
  height: 50px;
  width: @body-width;
  margin: 0 auto;
  padding: 9px 0;
  overflow: hidden;
  position: relative;
  .header-logo {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    width: 84px;
    height: 32px;
    margin:auto;
  }
  .header-contact{
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    margin:auto;
    height: 16px;
    img{
      width: 18px;
      height: 16px;
    }
    span{
      font-size: 15px;
      color: #333333;
      font-weight: 800;
      vertical-align: text-bottom;
    }
  }
}
</style>
