<template>
    <div id="wrapper">
        <el-row :gutter="20">
            <el-col :span="6">
                <div class="grid-content bg-purple">
                    <el-select v-model="value" placeholder="请选择">
                        <el-option
                                v-for="item in options"
                                :key="item.value"
                                :label="item.label"
                                :value="item.value">
                        </el-option>
                    </el-select>
                </div>
            </el-col>
            <el-col :span="6">
                <div class="grid-content bg-purple">
                    <chart :chartData="chartData"></chart>
                </div>
            </el-col>
            <el-col :span="6">
                <div class="grid-content bg-purple">
                    <el-select v-model="value" placeholder="请选择">
                        <el-option
                                v-for="item in options"
                                :key="item.value"
                                :label="item.label"
                                :value="item.value">
                        </el-option>
                    </el-select>
                </div>
            </el-col>
            <el-col :span="6">
                <div class="grid-content bg-purple"></div>
            </el-col>
        </el-row>
    </div>
</template>

<script>
  import Chart from './LandingPage/Chart.vue'

  export default {
    name: 'Landing',
    data () {
      return {
        options: [{
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
        }],
        value: '',
        chartData: [
          0.9700, 0.9700, 0.9700, 0.9698, 0.9700, 0.9699, 0.9699, 0.9700, 0.9702, 0.9699
        ]
      }
    },
    components: {Chart}
  }
</script>

<style>

</style>
