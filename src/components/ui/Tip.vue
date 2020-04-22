<template>
  <span class="tip">
    <warning-icon />
    <div class="text">
      <p>{{ textForTip }}</p>

    </div>

  </span>
</template>

<script>
import WarningIcon from '@/components/icons/WarningIcon.vue'

export default {
  components: {
    WarningIcon,
  },
  props: {
    textForTip : {
      required : true,
      default: 'tip'
    }
  },
}
</script>

<style lang="scss" scoped>
$mainColor: #4C5056;
.tip {
  position: relative;
  &:hover .text {
    display: block;
  }
  .text {
    min-width: 200px;
    display: none;
    background-color: $mainColor;
    border-radius: 5px;
    color: #fff;
    position: absolute;
    top: 22px;
    left: 50%;
    transform: translate(-50%);
    &:after {
      content: "";
      position: absolute;
      width: 0;
      height: 0;
      border-left: 5px solid transparent;
      border-right: 5px solid transparent;
      border-bottom: 5px solid $mainColor;
      transform: rotate(-180deg);
      top: -5px;
      left: 50%;
      transform: translate(-50%);
    }
    p {
      margin-top: 0;
      margin-bottom: 0;
      padding: 8px;
    }

  }
}
</style>
