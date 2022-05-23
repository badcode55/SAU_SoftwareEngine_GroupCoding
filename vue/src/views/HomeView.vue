<template>
  <div>
    <el-button @click="resetDateFilter">重置选定日期</el-button>
    <el-button @click="clearFilter">重置所有过滤选项</el-button>
    <el-table ref="tableRef" row-key="date"
              :data="tableData"
              style="width: 100%">
      <el-table-column
          prop="date"
          label="创建日期"
          sortable
          width="180"
          column-key="date"
          :filters="[
        { text: '2022-05-20', value: '2022-05-20' },
        { text: '2022-05-21', value: '2022-05-21' },
        { text: '2022-05-22', value: '2022-05-22' },
        { text: '2022-05-23', value: '2022-05-23' },
      ]"
          :filter-method="filterHandler"
      />
      <el-table-column prop="name" label="奖池名" width="180"/>
      <el-table-column prop="address" label="详细信息" :formatter="formatter"/>

      <el-table-column
          prop="tag"
          label="是否启用"
          width="100"
          :filters="[
        { text: '是', value: 'Home' },
        { text: '否', value: 'Office' },
      ]"
          :filter-method="filterTag"
          filter-placement="bottom-end"
      >
        <template #default="scope">
          <el-tag
              :type="scope.row.tag === 'Home' ? '' : 'success'"
              disable-transitions
          >{{ scope.row.tag }}
          </el-tag
          >
        </template>
      </el-table-column>
    </el-table>

  </div>
</template>



<script>
// @ is an alias to /src


export default {
  name: 'HomeView',
  components: {},
  data() {
    return {
      tableDate: [
        {
          date: '2022-05-20',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles',
          tag: 'Home',
        },
        {
          date: '2022-05-21',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles',
          tag: 'Office',
        },
        {
          date: '2022-05-22',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles',
          tag: 'Home',
        },
        {
          date: '2022-05-23',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles',
          tag: 'Office',
        },
      ]
    }
  }

}
</script>
