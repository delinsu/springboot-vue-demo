<template>
  <div style="width: 100%; padding: 10px">
    <div style="display: flex">
      <div style="width: 300px; margin: 10px 0">
        <el-row>
          <el-button type="primary">新增</el-button>
          <el-button type="primary">导入</el-button>
          <el-button type="primary">导出</el-button>
        </el-row>
      </div>
      <div style="flex: 1"></div>
      <div style="width: 300px; margin: 10px 0">
        <el-input v-model="search" placeholder="Please input" style="width: 70%"/>
        <el-button type="primary" style="margin-left: 8px">搜索</el-button>
      </div>
    </div>
    <div style="display: flex">
      <el-table :data="tableData" border stripe>
        <el-table-column prop="date" label="Date" sortable width="180" />
        <el-table-column prop="name" label="Name" width="180" />
        <el-table-column prop="address" label="Address" width="180" />
        <el-table-column label="Operations" width="180">
          <template #default>
            <el-button type="primary" size="small" @click="handleEdit">编辑</el-button>
            <el-popconfirm title="确定删除?">
              <template #reference>
                <el-button type="danger" size="small">删除</el-button>
              </template>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>

  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {

  },
  data() {
    return {
      search: "",
      tableData: [
        {
          date: '2016-05-03',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles',
        },
        {
          date: '2016-05-02',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles',
        },
        {
          date: '2016-05-04',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles',
        },
        {
          date: '2016-05-01',
          name: 'Tom',
          address: 'No. 189, Grove St, Los Angeles',
        },
      ]
    }
  },
  methods: {
    handleEdit() {

    }
  }
}
</script>
