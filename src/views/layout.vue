<template>
  <el-container>
    <el-header />
    <el-container>
      <el-aside width="200px">
        <el-menu>
          <el-menu-item v-for="item in menus" :key="item.id" :index="item.url" :value="item.menuName">
            <span>{{ item.menuName }}</span>
          </el-menu-item>
        </el-menu>
      </el-aside>
      <el-main />
    </el-container>
  </el-container>
</template>

<script>
// import home from '@/views/home'
export default {
  name: 'Layout',
  components: {
    // home
  },
  data: function() {
    return {
      menus: []
    };
  },
  created() {
    const res = { "code": 0, "msg": "成功", "result": [{ "id": 3, "menuCode": "CD002", "menuName": "订单管理", "fatherMenuCode": "0", "url": "/order", "serialNumber": 120, "status": 2, "createUser": "09686", "updateUser": "09686", "isDeleted": 0, "createTime": "2020-07-10T20:03:04.000+0800", "updateTime": "2020-07-21T11:31:58.000+0800", "childMenus": [{ "id": 6, "menuCode": "CD002-1", "menuName": "订单管理详情", "fatherMenuCode": "CD002", "url": "/orderdetail", "serialNumber": 121, "status": 3, "createUser": "09686", "updateUser": "09686", "isDeleted": 0, "createTime": "2020-07-31T20:03:04.000+0800", "updateTime": "2020-07-21T11:32:16.000+0800" }] }, { "id": 5, "menuCode": "CD003", "menuName": "退货单管理", "fatherMenuCode": "0", "url": "/refundOrder", "serialNumber": 150, "status": 2, "createUser": "09686", "updateUser": "09686", "isDeleted": 0, "createTime": "2020-07-06T20:03:04.000+0800", "updateTime": "2020-07-21T11:32:05.000+0800", "childMenus": [{ "id": 7, "menuCode": "CD003-1", "menuName": "退货单管理详情", "fatherMenuCode": "CD003", "url": "/returnorderdetail", "serialNumber": 151, "status": 3, "createUser": "09686", "updateUser": "09686", "isDeleted": 0, "createTime": "2020-07-19T20:03:04.000+0800", "updateTime": "2020-07-21T15:31:44.000+0800" }] }, { "id": 8, "menuCode": "CD004", "menuName": "账单管理", "fatherMenuCode": "0", "url": "/billlist", "serialNumber": 152, "status": 2, "createUser": "09686", "updateUser": "09686", "isDeleted": 0, "createTime": "2020-10-29T10:32:49.000+0800", "updateTime": "2020-10-29T10:35:15.000+0800", "childMenus": [{ "id": 10, "menuCode": "CD004-1", "menuName": "账单详情", "fatherMenuCode": "CD004", "url": "/billdetail", "serialNumber": 154, "status": 3, "createUser": "09686", "updateUser": "09686", "isDeleted": 0, "createTime": "2020-10-29T10:36:28.000+0800", "updateTime": "2020-10-29T10:37:58.000+0800" }] }, { "id": 9, "menuCode": "CD005", "menuName": "发票管理", "fatherMenuCode": "0", "url": "/invoicelist", "serialNumber": 153, "status": 2, "createUser": "09686", "updateUser": "09686", "isDeleted": 0, "createTime": "2020-10-29T10:34:57.000+0800", "updateTime": "2020-10-29T10:36:14.000+0800", "childMenus": [{ "id": 11, "menuCode": "CD005-1", "menuName": "发票详情", "fatherMenuCode": "CD005", "url": "/invoicedetail", "serialNumber": 155, "status": 3, "createUser": "09686", "updateUser": "09686", "isDeleted": 0, "createTime": "2020-10-29T10:38:26.000+0800", "updateTime": "2020-10-29T10:40:12.000+0800" }] }] }
    this.menus = res.result
    console.log(this.menus);
  },
  methods: {

  }
}
</script>

<style lang='scss' scoped>
.el-container{
    height: 100%;
    background-color: purple;
}
.el-header{
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
}

.el-aside{
    background-color: #D3DCE6;
    color: #333;
    text-align: center;
}

.el-main{
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
}
</style>
