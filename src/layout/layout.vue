<template>
    <a-layout  style="height:100%" id="components-layout-demo-custom-trigger">
      <a-layout-sider
        :trigger="null"
      >
        <div class="logo" />
        <a-menu theme="dark" mode="inline" :defaultSelectedKeys="['1']">
          <a-menu-item key="1"><a-icon type="user" />option1</a-menu-item>
          <a-sub-menu key="sub2">
            <span slot="title"><a-icon type="laptop" />subnav 2</span>
            <a-menu-item key="5">option5</a-menu-item>
            <a-menu-item key="6">option6</a-menu-item>
            <a-menu-item key="7">option7</a-menu-item>
            <a-menu-item key="8">option8</a-menu-item>
          </a-sub-menu>
          <a-menu-item key="10"><a-icon type="user" />option1</a-menu-item>
        </a-menu>
      </a-layout-sider>
      <a-layout >
        <a-layout-header style="background: #fff; padding: 0">
            <a-row style="float:right">
                <a-col style="margin-right:12px;">User1 <a-avatar style="backgroundColor:#87d068" icon="user" /></a-col>
            </a-row>
        </a-layout-header>
        <a-layout-content :style="{ margin: '24px 16px', padding: '24px', background: '#fff'}">
          <slot />
        </a-layout-content>
      </a-layout>
    </a-layout>
</template>
<script>
import {Menu, Layout, Avatar} from 'ant-design-vue'
export default {
    name: "layout",
  components: {
    AMenu: Menu,
    ASubMenu: Menu.SubMenu,
    AMenuItem: Menu.Item,
    ALayout: Layout,
    ALayoutSider: Layout.Sider,
    ALayoutHeader: Layout.Header,
    ALayoutContent: Layout.Content,
    AAvatar: Avatar
  },
}
</script>
<style>
#components-layout-demo-custom-trigger .trigger {
  font-size: 18px;
  line-height: 64px;
  padding: 0 24px;
  cursor: pointer;
  transition: color .3s;
}

#components-layout-demo-custom-trigger .trigger:hover {
  color: #1890ff;
}

#components-layout-demo-custom-trigger .logo {
  height: 45px;
  background: url("../assets/logo.png") no-repeat;
  background-size: 100% 100%;
  margin: 8px;
}
</style>
