<template>
  <div class="TopMenu">
  <a-menu v-model:selectedKeys="current" mode="horizontal">
    <a-menu-item key="mail">
      <template #icon>
        <mail-outlined />
      </template>
      Navigation One
    </a-menu-item>
    <a-menu-item key="alipay">
      <a href="https://www.facebook.com/ninjanguyenhoanganhhh" target="_blank" rel="noopener noreferrer">
        Tôi là VIỆT ANH ĐỖ
      </a>
    </a-menu-item>
  </a-menu>
    <div style="padding: 20px;">
      <h1> Tuyển tập "Um, nhà anh trồng mít thái"</h1> <div style="display: flex">
      <a style="margin: 20px">hình tôi đỉnh</a>
      <img
          style="width: 400px; height: 400px;"
          src="../img/vietanhdo_1.jpg"
      />
      <br/>
      <a style="margin: 20px" >hình tôi cực đỉnh</a>
      <img
          style="width: 400px; height: 400px;"
          src="../img/vietanhdo_2.jpg"
      />
    </div>
      <div style="display: flex">
        <a style="margin: 20px">Mít đặc</a>
        <img
            style="width: 400px; height: 400px;"
            src="../img/Vad_3.jpg"
        />
        <br/>
        <a style="margin: 20px" >OK, i dont know</a>
        <img
            style="width: 400px; height: 400px;"
            src="../img/Dc.jpg"
        />
      </div>
    </div>
    
   
    
  </div>
</template>
<script>
import { defineComponent, ref } from 'vue';
import { MailOutlined } from '@ant-design/icons-vue';
export default defineComponent({
  components: {
    MailOutlined,
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
