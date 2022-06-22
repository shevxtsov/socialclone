<template>
  <div class="preloader">
    <div class="preloader__inner"></div>
  </div>
</template>

<script>
export default {
  name: 'McvLoading'
}
</script>

<style scoped>
  .preloader{
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    overflow: hidden;
    background-color: #fff;
    background: rgba(255, 255, 255, 0.2);
    -webkit-backdrop-filter: blur(10px);
    backdrop-filter: blur(10px);
    z-index: 9999;
  }

  .preloader__inner{
    width: 70px;
    margin: 0 auto;
    margin-top: 20px;
    margin-bottom: 20px;
    opacity: 1;
    transition: opacity 1000ms;
    height: 70px;
    pointer-events: none;
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
    border-radius: 150px;
    border: 3px solid #5cb85c;
    transform: translate(-0%, -0%);
  }

  .preloader__inner::after{
    content: '';
    position: absolute;
    left: -4px;
    top: -4px;
    right: -4px;
    bottom: -4px;
    border-radius: 70px;
    border: 3px solid transparent;
    border-right-color: #fff;
    border-bottom-color: #fff;
    animation: spinner 1s linear infinite;
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden
  }

  @-webkit-keyframes spinner {
    from {
      -webkit-transform: rotate(0deg);
      transform: rotate(0deg);
    }
    to {
      -webkit-transform: rotate(360deg);
      transform: rotate(360deg);
    }
  }
  @keyframes spinner {
    from {
      -webkit-transform: rotate(0deg);
      transform: rotate(0deg);
    }
    to {
      -webkit-transform: rotate(360deg);
      transform: rotate(360deg);
    }
  }
</style>
