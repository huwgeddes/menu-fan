<template>
  <div>
    <button @click="show = !show">Click Here</button>
      <div class="menu-container" style="font-family: sans-serif; width: 60px; height: 60px; top: 200px; left: 30px; transition: none 0s ease 0s;">
        <div class="menu-list" style="top: -70px; left: 300px; width: 200px; height: 200px;">

          <transition name="spin-one">
            <div class="wing wing-1" v-if="show">
              <svg class="wing-svg" height="100%" width="100%" style="touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);">
                <path style="pointer-events: auto; touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);" fill="#ea2a29" d="M53,85 L193,48 A200,200 0 0, 1 193,151 L53,115  A55,55 1 0, 0 53,85 z"></path>
              </svg>
            </div>
          </transition>

            <transition name="spin-two">
              <div class="wing wing-2" v-if="show">
                <svg class="wing-svg" height="100%" width="100%" style="touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);">
                  <path style="pointer-events: auto; touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);" fill="#f16729" d="M53,85 L193,48 A200,200 0 0, 1 193,151 L53,115  A55,55 1 0, 0 53,85 z"></path>
                </svg>
              </div>
            </transition>

            <transition name="spin-three">
              <div class="wing wing-3" v-if="show">
                <svg class="wing-svg" height="100%" width="100%" style="touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);">
                  <path style="pointer-events: auto; touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);" fill="#4d7190" d="M53,85 L193,48 A200,200 0 0, 1 193,151 L53,115  A55,55 1 0, 0 53,85 z"></path>
                </svg>
              </div>
            </transition>

            <transition name="spin-four">
              <div class="wing wing-4" v-if="show">
                <svg class="wing-svg" height="100%" width="100%" style="touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);">
                  <path style="pointer-events: auto; touch-action: none; user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);" fill="#ffcf14" d="M53,85 L193,48 A200,200 0 0, 1 193,151 L53,115  A55,55 1 0, 0 53,85 z"></path>
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
  }

  .wing-1 {
    transform: rotate(0deg) scale(1);
  }
  .wing-1:hover {
    transition: all 0.5s ease;
    transform: rotate(0deg) scale(1.2);
  }

  .wing-2 {
    transform: rotate(90deg) scale(1);
  }
  .wing-2:hover {
    transition: all 0.5s ease;
    transform: rotate(90deg) scale(1.2);
  }

  .wing-3 {
    transform: rotate(180deg) scale(1);
  }
  .wing-3:hover {
    transition: all 0.5s ease;
    transform: rotate(180deg) scale(1.2);
  }

  .wing-4 {
    transform: rotate(270deg) scale(1);
  }
  .wing-4:hover {
    transition: all 0.5s ease;
    transform: rotate(270deg) scale(1.2);
  }



  .spin-one-enter-active, .spin-two-enter-active, .spin-three-enter-active, .spin-four-enter-active {
    transition: all 0.5s ease
  }
  .spin-one-enter, .spin-two-enter, .spin-three-enter, .spin-four-enter {
    transform: rotate(0) scale(1);
  }
  .spin-one-enter-to {
    transform: rotate(0deg) scale(1);
  }
  .spin-two-enter-to {
    transform: rotate(90deg) scale(1);
  }
  .spin-three-enter-to {
    transform: rotate(180deg) scale(1);
  }
  .spin-four-enter-to {
    transform: rotate(270deg) scale(1);
  }

</style>
