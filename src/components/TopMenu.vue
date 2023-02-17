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
        Navigation Four - Link
      </a>
    </a-menu-item>
  </a-menu>
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
