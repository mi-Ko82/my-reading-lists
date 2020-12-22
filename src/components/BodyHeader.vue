<template lang="pug">
header
  h1 My Reading Lists
</template>

<style lang="scss" scoped>
  @import '../assets/css/_var.scss';
  @import '../assets/css/_mixin.scss';

  header {
    height: 60px;
    text-align: center;
    background: linear-gradient(to right, #72beff 0%,#8029f7 100%,#7db9e8 100%);
    box-shadow: 0 4px 10px rgba($black, .16);

    @include pc {
      height: 80px;
    }

    h1 {
      display: flex;
      justify-content: center;
      align-items: center;
      color: $white;
      line-height: 60px;
      letter-spacing: .06em;
      font-size: 2.8rem;

      @include pc {
        line-height: 80px;
        font-size: 4.2rem;
      }

      &::before ,
      &::after {
        content: "";
        display: block;
        width: 12px;
        height: 18px;
        border-left: 3px solid $white;
        border-right: 3px solid $white;

        @include pc {
          width: 22px;
          height: 26px;
        }
      }

      &::before {
        transform: skew(45deg);
        margin-right: 16px;

        @include pc {
          margin-right: 36px;
        }
      }

      &::after {
        transform: skew(-45deg);
        margin-left: 16px;

        @include pc {
          margin-left: 36px;
        }
      }
    }
  }
</style>