<template>
  <ons-select v-bind="$attrs" :modifier="normalizedModifier">
    <select v-model="selectedValue">
      <slot></slot>
    </select>
  </ons-select>
</template>

<script>
  import 'onsenui/esm/elements/ons-select';
  import { modifier } from '../mixins';

  export default {
    name: 'v-ons-select',
    mixins: [modifier],
    model: {
      prop: 'modelProp',
      event: 'modelEvent'
    },
    props: {
      modelProp: [Number, String],
      modelEvent: {
        type: String,
        default: 'input'
      }
    },
    emits: ['modelEvent'],
    computed: {
      selectedValue: {
        get() {
          return this.modelProp;
        },
        set(val) {
          this.$emit('modelEvent', val);
        }
      }
    }
  };
</script>
