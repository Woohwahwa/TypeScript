<template>
  <div></div>
</template>

<script lang="ts">
  export default {
    name: 'App',
    mounted() {
      function sayHello(): void {
        console.log('Hello!');
      }

      function multiply(value1: number, value2: number): number {
        return value1 * value2;
      }
      console.log(multiply(16, 23));

      // function types
      let myMultiply: (a: number, b: number) => number;
      // myMultiply = sayHello;
      // myMultiply();
      myMultiply = multiply;
      console.log(myMultiply(5, 26));

      // objects
      let userData: { name: string, age: number };
      userData = { name: 'Hello', age: 22 };

      const complex: { data: number[], output: (all: boolean) => number[] } = {
        data: [100, 3.99, 10],

        output(all: boolean): number[] {
          return this.data;
        },
      };

      // type alias
      interface Complex {
        data: number[];
        output: (all: boolean) => number[];
      }

      const complex2: Complex = {
        data: [100, 3.99, 10],

        output(all: boolean): number[] {
          return this.data;
        },
      };

      // union types
      let myRealRealAge: number | string = 23;
      myRealRealAge = '23';
      // myRealRealAge = true;

      // check types
      const finalValue = 30;
      if (typeof finalValue === 'number') {
        console.log('Final value is a number');
      }

      // never
      function neverReturns(): never {
        throw new Error('An error!');
      }

      // Nullable Types
      let canBeNull: number | null = 12;
      canBeNull = null;
      let canAlsoBeNull;
      canAlsoBeNull = null;
      let canThisBeAny: number | null = null;
      canThisBeAny = 12;
    },
  };
</script>
