<template>
  <div class="TopMenu">
  <a-menu v-model:selectedKeys="current" mode="horizontal">
    <a-menu-item key="mail">
      <template #icon>
        <mail-outlined />
      </template>
      Navigation One
    </a-menu-item>
    <a-sub-menu key="sub1">
      <template #icon>
        <setting-outlined />
      </template>
      <template #title>Navigation Three - Submenu</template>
      <a-menu-item-group title="Item 1">
        <a-menu-item key="setting:1">Option 1</a-menu-item>
        <a-menu-item key="setting:2">Option 2</a-menu-item>
      </a-menu-item-group>
      <a-menu-item-group title="Item 2">
        <a-menu-item key="setting:3">Option 3</a-menu-item>
        <a-menu-item key="setting:4">Option 4</a-menu-item>
      </a-menu-item-group>
    </a-sub-menu>
    <a-menu-item key="alipay">
      <a href="https://antdv.com" target="_blank" rel="noopener noreferrer">
        Tôi là VIỆT ANH ĐỖ
      </a>
    </a-menu-item>
  </a-menu>
    <div>
      <img
        style="width: 400px; height: 400px;"
        src="https://scontent.fsgn2-5.fna.fbcdn.net/v/t1.6435-9/39861845_2668043143420215_6705299111404371968_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=8bfeb9&_nc_ohc=glExUawv0RMAX_B5hNl&_nc_ht=scontent.fsgn2-5.fna&oh=00_AfDF43ABNj-lSvmKJtv3Enn_S56HG0m79n1RTkd-9oYp3A&oe=6504081E" />
    </div>
  </div>
</template>
<script>
import { defineComponent, ref } from 'vue';
import { MailOutlined, SettingOutlined } from '@ant-design/icons-vue';
export default defineComponent({
  components: {
    MailOutlined,
    SettingOutlined,
  },
  setup() {
    const current = ref(['mail']);
    return {
      current,
    };
  },
});
</script>

<style>
.TopMenu{
  position: relative;
  top: 20px;
  left: 35%;
  width: 700px;
}
</style>
