<template>
    <div>
        <el-container>
            <el-main>
                <el-tabs :tab-position="tabPosition" style="height: 100%;">
                    <el-tab-pane label="原始数据集">
                        <el-container>
                            <el-main>
                                <div>
                                    <el-row>
                                        <el-col :span="6">
                                            <el-input size="large" v-model="input3" style="width: 300px"
                                                placeholder="请输入项目名称" class="input-with-select">
                                                <template #append>
                                                    <el-button icon="el-icon-search" />
                                                </template>
                                            </el-input>
                                        </el-col>
                                        <el-col :span="6" :offset="1">
                                            <el-select size="large" v-model="value" clearable placeholder="请选择" style="width: 300px;">
                                                <el-option v-for="item in options" :key="item.value" :label="item.label"
                                                    :value="item.value">
                                                </el-option>
                                            </el-select>
                                        </el-col>
                                        <el-col :span="4" >
                                            <el-button type="primary" size="large">新增</el-button>
                                        </el-col>

                                    </el-row>
                                    <!-- 表格 -->
                                    <el-table :data="tableData" border style="width: 100%; margin-top: 20px;">
                                        <el-table-column prop="date" label="数据集名称" width="180" />
                                        <el-table-column prop="name" label="原数据类型" width="180" />
                                        <el-table-column prop="name" label="感兴趣区格式" width="180" />
                                        <el-table-column prop="date" label="创建时间" width="180" />
                                        <el-table-column prop="name" label="EDA状态" width="180" />
                                        <el-table-column prop="address" label="地址" />
                                        <el-table-column fixed="right" label="操作" width="160">
                                            <template #default>
                                                <el-button link type="primary" size="small" @click="handleClick">
                                                    Detail
                                                </el-button>
                                                <el-button link type="primary" size="small">Edit</el-button>
                                            </template>
                                        </el-table-column>
                                    </el-table>
                                    <el-pagination style="margin-top: 20px; float: right;" background
                                        layout="prev, pager, next" :total="1000" />
                                </div>
                            </el-main>
                        </el-container>
                    </el-tab-pane>
                    <el-tab-pane label="特征数据集">特征数据集</el-tab-pane>
                    <el-tab-pane label="临床数据集">临床数据集</el-tab-pane>
                    <el-tab-pane label="推理数据集">推理数据集</el-tab-pane>
                </el-tabs>
            </el-main>
        </el-container>
    </div>
</template>
<script>
export default {
    name: 'dataset',
    data() {
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
            tableData: [{
                date: '2016-05-02',
                name: '王小虎',
                address: '上海市普陀区金沙江路 1518 弄'
            }, {
                date: '2016-05-04',
                name: '王小虎',
                address: '上海市普陀区金沙江路 1517 弄'
            }, {
                date: '2016-05-01',
                name: '王小虎',
                address: '上海市普陀区金沙江路 1519 弄'
            }, {
                date: '2016-05-03',
                name: '王小虎',
                address: '上海市普陀区金沙江路 1516 弄'
            },
            {
                date: '2016-05-03',
                name: '王小虎',
                address: '上海市普陀区金沙江路 1516 弄'
            },
            {
                date: '2016-05-03',
                name: '王小虎',
                address: '上海市普陀区金沙江路 1516 弄'
            },
            {
                date: '2016-05-03',
                name: '王小虎',
                address: '上海市普陀区金沙江路 1516 弄'
            },
            {
                date: '2016-05-03',
                name: '王小虎',
                address: '上海市普陀区金沙江路 1516 弄'
            }
            ]
        }
    },
    mounted() {

    },
    methods: {

    }
}

</script>

<style scoped></style>