<template>
  <div></div>
</template>

<script lang="ts">
  export default {
    name: 'App',
    mounted() {
      // array
      let hobbies: any[] = ['Cooking', 'Sports'];
      hobbies = [100];
      // hobbies = 100;

      // tuples
      const address: [string, number] = ['Superstreet', 99];

      // enum
      enum Color {
        Gray,
        Green,
        Blue = 20,
      }
      const myColor: Color = Color.Blue;
      console.log(myColor);

      // any
      let car: any = 'BMW';
      console.log(car);
      car = { brand: 'BMW', series: 3 };
      console.log(car);

      // functions
      const myName = 'Cindy';
      const myAge = 23;
      function returnMyName(): string {
        return myName;
      }
      console.log(returnMyName());

      // void
      function sayHello(): void {
        console.log('Hello!');
      }

      // argument types
      function multiply(value1: number, value2: number): number {
        return value1 * value2;
      }
      console.log(multiply(2, 3));
    },
    methods: {
    },
  };
</script>
