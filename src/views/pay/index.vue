<template>
  <div class="app-init pay-page scroll-box">
    <header-back title="whoops"></header-back>

    <div class="padding-box">
  
      <p>whoops</p>
      <p>服务好像失败了</p>
      <p>请联系管理员重启服务器</p>


    </div>

  </div>
</template>

<script type="text/ecmascript-6">
  import headerBack from '../../components/header-back'

  export default{
    name: 'pay',
    components: {
      headerBack
    }
  }
</script>

<style type="text/sass" lang="sass">
  .pay-page
    background-color: #fff
    .padding-box
      padding: 0.4rem
      color: #333
      .color
        color: orange
      ul
        padding-left: 0.8rem
      li
        list-style: disc
</style>
