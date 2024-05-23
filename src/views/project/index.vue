<template>
    <div>
        <el-container>
            <el-header>我的项目</el-header>
            <el-main>
                <div>
                    <el-input v-model="input3" style="max-width: 300px" placeholder="请输入项目名称"
                        class="input-with-select">
                        <template #append>
                            <el-button icon="el-icon-search" />
                        </template>
                    </el-input>
                </div>
                <div style="margin-top: 20px;" >
                    <el-space wrap  :size = "20">
                        <el-card   class="box-card" style="width: 280px;height: 200px">
                            <template #header>
                                <!-- <div class="card-header">
                                    <span>项目一</span>
                                    <el-button class="button" size="small" style="margin-left: 45px;">编辑</el-button>
                                    <el-button class="button" size="small">删除</el-button>
                                </div> -->
                            </template>
                            <div>
                                <el-button circle class="button" size="large" style="width: 100px!important; height: 100px !important; margin-left: 70px; margin-top: 20px;">
                                    新增<i class="el-icon-plus el-icon--right"></i>
                                </el-button>
                            </div>
                        </el-card>
                        <el-card v-for="i in 3" :key="i" class="box-card" style="width: 280px;height: 200px">
                            <template #header>
                                <div class="card-header">
                                    <span>项目一</span>
                                    <el-button class="button" size="small" style="margin-left: 78px;">编辑</el-button>
                                    <el-button class="button" size="small">删除</el-button>
                                </div>
                            </template>
                            <div >
                               <span style="font-size: 15px;">创建时间：yyyy:mm:dd:hh:mm:ss</span>
                            </div>
                        </el-card>
                    </el-space>
                </div>
            </el-main>
        </el-container>
    </div>
</template>
<script>

export default {
    name: 'project',

    data() {
        return {

        }
    },
    mounted() {

    },
    methods: {

    }
}

</script>

<style></style>