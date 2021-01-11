<template>
  <div class="btn">
    <button :class="'button'" :style="sys_option">
      <slot />
    </button>
  </div>
</template>

<script>
export default {
  name: "HaxButton",
  props: {
    size: {
      type: String,
      default: "",
    },
    color: {
      type: String,
      default: "",
    },
    border: {
      type: String,
      default: "none",
    },
  },
  computed: {
    sys_option: function() {
      return {
        "--size": this.sys_size[this.size || 0],
        "--border-radius": ()=>{
          switch (this.border) {
            case 'auto':
              return '13px'
          
            default:
              break;
          }
          return '13px'
        }
      };
    },
  },
  data() {
    return {
      sys_size: {
        min: "13px",
        mid: "18px",
        big: "22px",
        biger: "25px",
      },
      sys_color: [],
      sys_options: [],
    };
  },
};
</script>

<style scoped>
.btn {
  display: block;
  position: relative;
  box-sizing: border-box;
}
.button {
  font-size: var(--size);
  min-width: fit-content;
  min-height: fit-content;
  background: #df7171;
  border: var(--border);
  border-radius: var(--border-radius);
  outline: none;
}
</style>
