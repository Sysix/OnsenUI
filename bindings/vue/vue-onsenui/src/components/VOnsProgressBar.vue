<template>
  <ons-progress-bar :modifier="normalizedModifier">
    <slot></slot>
  </ons-progress-bar>
</template>

<script>
  /* This file was generated automatically by 'generate-components' task in bindings/vue/gulpfile.babel.js */
  import 'onsenui/esm/elements/ons-progress-bar';
  import { deriveEvents, modifier } from '../mixins';

  const name = 'v-ons-progress-bar';

  export default {
    name,
    mixins: [deriveEvents(name), modifier]
  };
</script>