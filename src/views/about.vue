<template>
    <!-- echarts图形默认宽高为0 -->
  <div ref = "mychart" id="demo"></div>
  <!-- dom元素 id 为要设置的名称 -->
   <div>test

   </div>
</template>

<script>
import * as echarts from "echarts"
export default {
    mounted(){
      let myEcharts = echarts.init(this.$refs.mychart)
      myEcharts.setOption({
        title:{//设置echart标题
            text:"helloword"
        },
        xAxis:{
            data:["EZ","VN","NOC","MF"]
        },

        yAxis:{

        },
        series:{//设置当前数据所能映射出的图形
            name:"图形1",
            type:"bar",
            data[2400,4800,3200,6400]
        }
      })
    }
}
</script>

<style>
    #demo{
        width: 500px;
        height: 500px;
        border: lpx solid red;
    }
</style>