//在Echarts.vue文件中
<template>
  <d2-container>
    <template slot="header">Page 1 header</template>
    Hello World
    <div id="main" style="width: 600px;height: 400px;"></div>
  </d2-container>
  

</template>
 
<script>
export default {
  name: 'page1',
  methods: {
    myEcharts(){
      var myChart = this.$echarts.init(document.getElementById('main'));
      var myChart = echarts.init(document.querySelector("#main"));
      //配置图表
      var option = {
        title: {
          text: 'echarts入门示例',
        },
        tooltip: {},
        legend: {
          data: ['销量']
        },
        xAxis: {
          data: ['衬衫','羊毛衫','雪纺衫','裤子','高跟鞋','袜子']
        },
        yAxis: {},
        series: [{
          name: '销量',
          type: 'bar',
          data: [5,20,36,10,10,20]
        }]
      };
      myChart.setOption(option);
    }
  },
  mounted(){
    this.myEcharts();
  }
}


     

</script>
 
<style>
 
</style>