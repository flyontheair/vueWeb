<template>
  <select v-model="selectValue">
    <option v-for="item in options" :label="item.label" :value="item.value"></option>
  </select>
</template>

<script>
  export default{
    name:"",//一般不用
    data(){
    return {
      options: [],
      selectValue:''//选择结果
    }

  },
  props:[],//向子级传递的信息
    methods:{
    getSelectList(){
      //获取列表逻辑
      this.options=[{//测试数据
        value: '选项1',
        label: '黄金糕'
      }, {
        value: '选项2',
        label: '双皮奶'
      }, {
        value: '选项3',
        label: '蚵仔煎'
      }, {
        value: '选项4',
        label: '龙须面'
      }, {
        value: '选项5',
        label: '北京烤鸭'
      }]
    }

  },
  mounted(){//
    this.getSelectList();
  },
  computed:{//计算属性，跟angular的watch差不多，vue也有watch，推荐使用这个计算属性

  },
  components:{//声明组件

  }
  }
</script>

