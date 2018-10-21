<template>
  <div>
    <button @click="show = !show">Click Here</button>
      <div class="menu-container" style="font-family: sans-serif;width: 0px;height: 0px;top: 0px;left: 0px;">
        <div class="menu-list" style="top: 200px;left: 300px;width: 100px;height: 100px;">

          <transition name="spin">
            <div class="wing wing-1" v-if="show">
              <svg class="wing-svg" height="100%" width="100%" style="touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);">
                <path style="pointer-events: auto; touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);" fill="#ea2a29" d="M38,11 L70,-21 A100,100 0 0, 1 70,120 L38,89  A55,55 1 0, 0 38,11 z"></path>
                <text class="wing-text" dominant-baseline="central" x="50%" y="50%" text-anchor="middle" transform="rotate(90, 60, 60)" >
                  Add Info
                </text>
              </svg>
            </div>
          </transition>

            <transition name="spin">
              <div class="wing wing-2" v-if="show" @click="show = !show">
                <svg class="wing-svg" height="100%" width="100%" style="touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);">
                  <path style="pointer-events: auto; touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);" fill="#f16729" d="M38,11 L70,-21 A100,100 0 0, 1 70,120 L38,89  A55,55 1 0, 0 38,11 z"></path>
                  <text class="wing-text" dominant-baseline="central" x="50%" y="50%" text-anchor="middle" transform="rotate(270, 60, 40)" >
                    Cancel
                  </text>
                </svg>
              </div>
            </transition>

            <transition name="spin">
              <div class="wing wing-3" v-if="show">
                <svg class="wing-svg" height="100%" width="100%" style="touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);">
                  <path style="pointer-events: auto; touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);" fill="#4d7190" d="M38,11 L70,-21 A100,100 0 0, 1 70,120 L38,89  A55,55 1 0, 0 38,11 z"></path>
                  <text class="wing-text" dominant-baseline="central" x="50%" y="50%" text-anchor="middle" transform="rotate(90, 60, 60)" >
                    Go to user
                  </text>
                </svg>
              </div>
            </transition>

            <transition name="spin">
              <div class="wing wing-4" v-if="show">
                <svg class="wing-svg" height="100%" width="100%" style="touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);">
                  <path style="pointer-events: auto; touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);" fill="#ffcf14" d="M38,11 L70,-21 A100,100 0 0, 1 70,120 L38,89  A55,55 1 0, 0 38,11 z"></path>
                  <text class="wing-text" dominant-baseline="central" x="50%" y="50%" text-anchor="middle" transform="rotate(90, 60, 60)" >
                    Go to user
                  </text>
                </svg>
              </div>
            </transition>

        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      show: false
    }
  },
  computed: {
    wingOne () {
      return this.show ? 'transform: rotate(30deg) scale(1);' : ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .menu-container {
    position: fixed;
    z-index: 99999;
  }
  .menu-list {
    position: absolute;
    pointer-events: none;
  }
  .wing {
    width: 100%;
    height: 100%;
    position: absolute;
    transform-origin: 0 50%;
    cursor: pointer;
  }
  .wing-text {
    font-size: 16px;
    fill: #fff
  }
  .wing path:hover {
    fill: #000
  }
  .wing-svg {
    overflow: visible;
  }

  .wing-1 {
    transform: rotate(0deg) scale(1);
  }
  .wing-2 {
    transform: rotate(90deg) scale(1);
  }
  .wing-3 {
    transform: rotate(180deg) scale(1);
  }
  .wing-4 {
    transform: rotate(270deg) scale(1);
  }

  .spin-enter-active {
    transition: all 0.5s ease
  }
  .spin-enter {
    transform: rotate(0) scale(0);
  }


</style>
