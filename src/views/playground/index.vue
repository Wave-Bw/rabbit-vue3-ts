<script lang="ts" setup>
import { ref } from 'vue'
// 订单状态
const orderStatus = [
  { name: 'all', label: '全部订单' },
  { name: 'unpay', label: '待付款' },
  { name: 'deliver', label: '待发货' },
  { name: 'receive', label: '待收货' },
  { name: 'comment', label: '待评价' },
  { name: 'complete', label: '已完成' },
  { name: 'cancel', label: '已取消' },
]

const activeName = ref('all')
const fn = (tab: any, index: any) => {
  console.log(tab, index)
}
</script>

<template>
  <XtxTabs v-model="activeName" @tab-click="fn">
    <XtxTabsPane label="用户管理" name="first">用户管理</XtxTabsPane>
    <XtxTabsPane
      v-for="item in orderStatus"
      :key="item.name"
      :label="item.label"
      :name="item.name"
      >{{ item.name }} 的内容</XtxTabsPane
    >
  </XtxTabs>
</template>

<style scoped lang="less"></style>
