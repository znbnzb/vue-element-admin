<template>
    <div class="app-container">
        <el-row :gutter="20">
            <el-col :span="16">
                <div class="grid-content bg-purple">
                    <!-- 卡片 -->
                    <el-row>
                        <el-col
                            :span="8"
                            v-for="(o, index) in 2"
                            :key="o"
                            :offset="index > 0 ? 2 : 0"
                        >
                            <el-card :body-style="{ padding: '0px' }">
                                <img
                                    src="../../assets/401_images/401.gif"
                                    class="image"
                                >
                                <div style="padding: 14px;">
                                    <span>好吃的汉堡</span>
                                    <div class="bottom clearfix">
                                        <time class="time">{{ currentDate }}</time>
                                        <el-button
                                            type="text"
                                            class="button"
                                        >操作按钮</el-button>
                                    </div>
                                </div>
                            </el-card>
                        </el-col>
                    </el-row>
                </div>
            </el-col>
            <el-col :span="8">
                <div class="grid-content bg-purple">
                    567567
                </div>
            </el-col>
        </el-row>
    </div>
</template>
<script>
import BoxCard from '../dashboard/admin/components/BoxCard'

export default {
  name: 'BoxCard',
  data() {
    return {
      currentDate: new Date(),
      img: []
    }
  },
  components: {
    'tab-box': BoxCard
  },
  methods: {}
}
</script>

<style scoped>
.time {
    font-size: 13px;
    color: #999;
}

.bottom {
    margin-top: 13px;
    line-height: 12px;
}

.button {
    padding: 0;
    float: right;
}

.image {
    width: 50%;
    display: block;
}

.clearfix:before,
.clearfix:after {
    display: table;
    content: "";
}

.clearfix:after {
    clear: both;
}
</style>