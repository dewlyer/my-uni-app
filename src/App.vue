<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  mpType: 'app',
  globalData: {
    appSubText: 'text'
  },
  onLaunch() {
    console.log('App Launch')
  },
  onShow() {
    console.log('App Show')
  },
  onHide() {
    console.log('App Hide')
  }
});
</script>

<style lang="scss">
@import "~uview-ui/index.scss";
</style>
