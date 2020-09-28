<template>
  <div>
    <div>
      <div class="u-flex user-box u-p-l-30 u-p-r-20 u-p-t-30 u-p-b-30">
        <div class="u-m-r-10">
          <u-avatar :src="pic" size="140"/>
        </div>
        <div class="u-flex-1">
          <div class="u-font-36 u-p-b-20">uView ui</div>
          <div class="u-font-24 u-tips-color">微信号 123456789</div>
        </div>
        <div class="u-m-l-10 u-p-10">
          <u-icon color="#969799" name="scan" size="48"/>
        </div>
      </div>
      <div class="u-m-b-30 u-m-t-30">
        <u-cell-group>
          <u-cell-item icon="rmb-circle" title="支付"/>
        </u-cell-group>
      </div>
      <div class="u-m-b-30">
        <u-cell-group>
          <u-cell-item icon="star" title="收藏"/>
          <u-cell-item icon="photo" title="相册"/>
          <u-cell-item icon="coupon" title="卡券"/>
          <u-cell-item icon="heart" title="关注"/>
        </u-cell-group>
      </div>
      <div class="u-m-b-30">
        <u-cell-group>
          <u-cell-item icon="setting" title="设置"/>
        </u-cell-group>
      </div>
    </div>
    <u-tabbar v-model="current"
              :list="list"
              :bg-color="bgColor"
              :active-color="activeColor"
              :inactive-color="inactiveColor"
              :mid-button="false"/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      pic: 'https://uviewui.com/common/logo.png',
      show: true,
      list: [
        {
          iconPath: "home",
          selectedIconPath: "home-fill",
          text: '首页',
          count: 2,
          isDot: true,
          customIcon: false,
        },
        {
          iconPath: "photo",
          selectedIconPath: "photo-fill",
          text: '放映厅',
          customIcon: false,
        },
        {
          iconPath: "https://cdn.uviewui.com/uview/common/min_button.png",
          selectedIconPath: "https://cdn.uviewui.com/uview/common/min_button_select.png",
          text: '发布',
          midButton: true,
          customIcon: false,
        },
        {
          iconPath: "play-right",
          selectedIconPath: "play-right-fill",
          text: '直播',
          customIcon: false,
        },
        {
          iconPath: "account",
          selectedIconPath: "account-fill",
          text: '我的',
          count: 23,
          isDot: false,
          customIcon: false,
        }
      ],
      bgColor: '#3e3e3e',
      activeColor: '#ffffff',
      inactiveColor: '#cccccc'
    }
  },
  onLoad() {
    // uni.showToast({
    //   title: '标题',
    //   duration: 2000
    // });
    // uni.showLoading({
    //   title: '加载中'
    // });
    // uni.showModal({
    //   title: '提示',
    //   content: '这是一个模态弹窗',
    //   success: function (res) {
    //     if (res.confirm) {
    //       console.log('用户点击确定');
    //     } else if (res.cancel) {
    //       console.log('用户点击取消');
    //     }
    //   }
    // });
    uni.showActionSheet({
      itemList: ['A', 'B', 'C'],
      success: function (res) {
        console.log('选中了第' + (res.tapIndex + 1) + '个按钮');
      },
      fail: function (res) {
        console.log(res.errMsg);
      }
    });
  },
  methods: {}
})
</script>

<style lang="scss">
page {
  background-color: #f7f7f7;
}
</style>
<style lang="scss" scoped>
.user-box {
  background-color: #fff;
}
</style>
