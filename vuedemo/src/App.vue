<template>
  <div style="border:1px solid red;display: flex">
  <div id="app" style="border:1px solid red;display: block">
    <el-row class="tac" style="display: block;width: 205px">
      <el-col :span="24">
        <el-menu
          default-active="1-2"
          class="el-menu-vertical-demo"
          @open="handleOpen"
          @close="handleClose"
          background-color="#545c64"
          text-color="#fff"
          active-text-color="#ffd04b">
          <el-submenu index="1">
            <template slot="title">
              <i class="el-icon-menu"></i>
              <span>菜单扫描</span>
            </template>
            <el-menu-item index="1-2">扫描1</el-menu-item>
            <el-menu-item index="1-3">扫描2</el-menu-item>
          </el-submenu>
          <el-submenu index="2">
            <template slot="title">
              <i class="el-icon-menu"></i>
              <span>环境管理</span>
            </template>
            <el-menu-item index="2-2">环境1</el-menu-item>
            <el-menu-item index="2-3">环境2</el-menu-item>
          </el-submenu>
        </el-menu>
      </el-col>
    </el-row>
  </div>


    <router-view></router-view>
  </div>
</template>

<script>
  export default {
    methods: {
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>
