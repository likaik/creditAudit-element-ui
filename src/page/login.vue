<template>
  <div class="login">
      <public-header></public-header> 
      <div class="login-body">
        
      </div>
      <public-footer></public-footer>
  </div>
</template>

<script>
  import PublicHeader from './PublicHeader.vue';
  import PublicFooter from './publicFooter.vue';
  export default {
    name: '', //模块名称
    data() {
      return {

      }
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
    components: {
      PublicHeader,
      PublicFooter
    },
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
    beforeCreated() {

    },
    //生命周期钩子：组件实例完成创建之后调用
    created() {

    },
    //生命周期钩子：组件实例渲染完成时调用
    mounted() {

    }

  }
</script>

<style scoped>
  
</style>
