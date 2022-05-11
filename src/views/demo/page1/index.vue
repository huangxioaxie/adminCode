//在Echarts.vue文件中
<template>

  <d2-container>
    <template slot="header">Page 1 header</template>
    Hello World
    <div id="main" style="width: 600px;height: 400px;"></div>
    <div id="main1" style="width: 600px;height: 400px;"></div>
  </d2-container>
  

</template>
 
<script>
  import * as echarts from 'echarts';
  export default {
    name: "echarts",
    data() {
      return {}
    },
    mounted() {
      this.echartsInit()
    },
    methods:{
      echartsInit() {
　　　　　//使用时只需要把setOption里的对象换成echarts中的options或者自己的参数即可
        echarts.init(document.getElementById('main')).setOption({
          xAxis: {
            type: 'category',
            data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']
          },
          yAxis: {
            type: 'value'
          },
          series: [{
            data: [120, 200, 150, 80, 70, 110, 130],
            type: 'bar',
            showBackground: true,
            backgroundStyle: {
              color: 'rgba(220, 220, 220, 0.8)'
            }
          }]
        })

        echarts.init(document.getElementById('main1')).setOption({
          xAxis: {
            type: 'category',
            data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']
          },
          yAxis: {
            type: 'value'
          },
          series: [{
            data: [120, 200, 150, 80, 70, 110, 130],
            type: 'bar',
            showBackground: true,
            backgroundStyle: {
              color: 'rgba(220, 220, 220, 0.8)'
            }
          }]
        })
      }
    }
  }
</script>
