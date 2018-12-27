<template>
  <div></div>
</template>

<script lang="ts">
  export default {
    name: 'App',
    mounted() {
      const myName: string = 'Max';
      const myAge: number = 23;
      let anything;
      anything = 12;

      // myName = 30;

      function controlMe(isTrue: boolean, somethingElse: boolean) {
        let result: number;
        if (isTrue) {
          result = 12;
        }
        result = 33;
        return result;
      }
    },
  };
</script>
