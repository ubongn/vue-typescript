<template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName('Blingz')">change name</button>
    <button @click="changeAge(30)">change age</button>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  name: "App",
  components: {},
  data() {
    return {
      name: "Ubdev",
      age: 25 as number | string,
    };
  },
  methods: {
    changeName(name: string) {
      this.name = name;
    },
    changeAge(age: number) {
      this.age = age;
    },
  },
})
export default class App extends Vue {
  // [x: string]: any;
  //   name: any;
  //   changeName(): void {
  //     throw new Error("Method not implemented.");
  //   }
}
</script>

<style></style>
