<template>
  <div class="footer">
   <p>北京奥创科技开发有限公司丨Copyright Reserved 2011-2018丨京ICP备13002974号-3丨京公网安备 11010802020586丨ICP经营许可证编号：京B2-20170280</p>
   <div class="footer-img">
    <img @mouseover="imgIn($event,index)" @mouseout="imgOut($event,index)" :src="item.a" v-for="(item,index) in imgUrl"  :type="1" :key="index">
   </div>
  </div> 
</template>

<script>
export default {
  name: '', //模块名称
  data() {
    return {
      type:1,
      imgUrl:[
        {a:'../../static/images/login/fooder-1.png',b:'../../static/images/login/fooder-1h.png'},
        {a:'../../static/images/login/fooder-2.png',b:'../../static/images/login/fooder-2h.png'},
        {a:'../../static/images/login/fooder-3.png',b:'../../static/images/login/fooder-3h.png'},
        {a:'../../static/images/login/fooder-4.png',b:'../../static/images/login/fooder-4h.png'},
        {a:'../../static/images/login/fooder-5.png',b:'../../static/images/login/fooder-5h.png'}
      ]
    };
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
      imgIn(el,index){
        el.path[0].src = this.imgUrl[index].b;
      },
      imgOut(el,index){
         el.path[0].src = this.imgUrl[index].a;
      }
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
.footer{
  width: @body-width;
  margin: 0 auto 50px;
  text-align: center;
  p{
    text-align: center;
    margin: 11px 0;
  }
  .footer-img{
    img{
      margin: 0 10px;
    }
  }
}
</style>
