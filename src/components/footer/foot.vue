<template>
  <div class="footer">
      <router-link :to="v.link" exact tag="div" v-for="(v, i) in list" key="i" class="footer-item" active-class="footer-active-item">
          {{v.page}}
      </router-link>
  </div>
</template>

<script>
export default {
    data() {
        return {
            list: [
                {page: '首页', link: '/'},
                {page: '购物', link: '/shop'},
                {page: '我的', link: '/my'}
            ]
        }
    }
}
</script>

<style lang="sass?indentedSyntax" scoped>
    @import "../../style/base.sass"
    .footer
        position: fixed
        left: 0
        bottom: 0
        width: 100%
        display: flex
        border-top: 1px solid rgba(0,0,0,.1)
    .footer-item
        flex: 1
        text-align: center
        line-height: 3.2rem
        font-size: 1.4rem
    .footer-active-item
        color: red
</style>
