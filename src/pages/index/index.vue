<template>
  <view>
    <view>
      <view class="u-flex user-box u-p-l-30 u-p-r-20 u-p-t-30 u-p-b-30">
        <view class="u-m-r-10">
          <u-avatar :src="pic" size="140"/>
        </view>
        <view class="u-flex-1">
          <view class="u-font-36 u-p-b-20">uView ui</view>
          <view class="u-font-24 u-tips-color">微信号 123456789</view>
        </view>
        <view class="u-m-l-10 u-p-10">
          <u-icon color="#969799" name="scan" size="48"/>
        </view>
      </view>
      <view class="u-m-b-30">
        <u-cell-group>
          <u-cell-item icon="rmb-circle" title="支付"/>
        </u-cell-group>
      </view>
      <view class="u-m-b-30">
        <u-cell-group>
          <u-cell-item icon="star" title="收藏"/>
          <u-cell-item icon="photo" title="相册"/>
          <u-cell-item icon="coupon" title="卡券"/>
          <u-cell-item icon="heart" title="关注"/>
        </u-cell-group>
      </view>
      <view class="u-m-b-30">
        <u-cell-group>
          <u-cell-item icon="setting" title="设置"/>
        </u-cell-group>
      </view>
    </view>
    <u-tabbar v-model="current" :list="list" :mid-button="true"/>
  </view>
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
      current: 0
    }
  },
  onLoad() {

  },
  methods: {}
})
</script>

<style lang="scss" scoped>
page {
  background-color: #ededed;
}

.camera {
  width: 54px;
  height: 44px;

  &:active {
    background-color: #ededed;
  }
}

.user-box {
  background-color: #fff;
}

</style>
