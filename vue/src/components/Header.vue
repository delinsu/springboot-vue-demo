<template>
  <div style="height: 60px; line-height: 60px; border-bottom: 1px solid #ccc; display: flex">
    <div style="width: 300px; padding-left: 30px; font-weight: bold; color: dodgerblue">后台管理</div>
    <div style="flex: 1"></div>
    <div style="width: 100px">
      <el-dropdown>
        张三
        <span class="el-dropdown-link">
          <el-icon class="el-icon--right">
            <arrow-down />
          </el-icon>
        </span>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item>个人信息</el-dropdown-item>
            <el-dropdown-item>退出系统</el-dropdown-item>
          </el-dropdown-menu>
        </template>
      </el-dropdown>
    </div>
  </div>
</template>

<script>
  import { ArrowDown } from '@element-plus/icons-vue'

  export default {
    components: {
      ArrowDown
    }
  }
</script>

<style scoped>

</style>