<template>
  <ons-input :modifier="normalizedModifier">
    <slot></slot>
  </ons-input>
</template>

<script>
  /* This file was generated automatically by 'generate-components' task in bindings/vue/gulpfile.babel.js */
  import 'onsenui/esm/elements/ons-input';
  import { deriveEvents, modelInput, modifier } from '../mixins';

  const name = 'v-ons-input';

  export default {
    name,
    mixins: [deriveEvents(name), modelInput, modifier]
  };
</script>