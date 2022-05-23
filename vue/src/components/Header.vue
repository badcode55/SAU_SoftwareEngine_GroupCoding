<template>
  <div style="height: 50px; line-height: 50px; border-bottom: 1px solid #ccc;display: flex">
    <div style="width: 200px;padding-left: 30px;font-weight: bold; color: cornflowerblue">抽奖系统后台管理</div>
    <div style="flex: 1"></div>
    <div style="width: 120px">
      <el-dropdown>
        <el-button type="primary" style="margin-top: 10px">
          🐂🐏
          <el-icon class="el-icon--right">
            <arrow-down/>
          </el-icon>
        </el-button>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item>充值</el-dropdown-item>
            <el-dropdown-item>中奖记录</el-dropdown-item>
            <el-dropdown-item>个人信息</el-dropdown-item>
            <el-dropdown-item>退出</el-dropdown-item>
          </el-dropdown-menu>
        </template>
      </el-dropdown>


    </div>
  </div>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style scoped>

</style>