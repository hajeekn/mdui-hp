<template>
  <div class="mdui-appbar">
    <div class="mdui-toolbar mdui-color-teal-600">
      <a class="mdui-btn mdui-btn-icon mdui-ripple" mdui-drawer="{target: '#left-drawer'}">
        <i class="mdui-icon material-icons">menu</i>
      </a>
      <router-link to="/" class="mdui-typo-title">Hajeekn</router-link>
      <div class="mdui-toolbar-spacer"></div>
      <a @click="reload" class="mdui-btn mdui-btn-icon mdui-ripple">
        <i class="mdui-icon material-icons">refresh</i>
      </a>
    </div>
  </div>
  <div class="mdui-drawer mdui-drawer-close" id="left-drawer">
      <ul class="mdui-list">
        <div class="mdui-btn mdui-list-item" mdui-drawer-close>
          <i class="mdui-icon material-icons">close</i><div class="mdui-list-item-content">收起</div></div>
          <li class="mdui-subheader">首页</li>
          <a href="../">
          <li class="mdui-list-item mdui-ripple" mdui-drawer-close>
          <i class="mdui-list-item-icon mdui-icon material-icons">home</i>
          <div class="mdui-list-item-content">首页</div>
        </li>
      </a>
        <li class="mdui-list-item mdui-ripple">
          <i class="mdui-list-item-icon mdui-icon material-icons">games</i>
          <div class="mdui-list-item-content">游戏</div>
        </li>
        <a href="/about/">
        <li class="mdui-list-item mdui-ripple">
          <i class="mdui-list-item-icon mdui-icon material-icons">people</i>
          <div class="mdui-list-item-content">关于</div>
        </li>
      </a>
      </ul>
    </div>
  <router-view />
</template>

<script>
import mdui from 'mdui'
export default {
  methods: {
    alert (context) {
      mdui.alert(context)
    },
    reload () {
      window.location.reload()
    }
  }
}
</script>

<style lang="stylus">
#app
  font-family Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50
</style>
