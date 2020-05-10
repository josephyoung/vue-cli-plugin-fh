<template>
  <div style="text-align: center;">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld';

export default {
  name: 'Home',
  components: {
    HelloWorld
  },

  methods: {
    handleLogoClick() {
      console.log({ 'html-version': document.documentElement.version });
      function* gen() {
        for (let i = 0; i < 10; i++) yield i;
      }
      const x = gen();
      for (const i of x) {
        console.info(`%c ${i}`, 'color: red;');
      }
      return Promise.resolve('yes i am');
    }
  },

  mounted() {
    const aa = { a: 1, b: 2, c: 3 };
    for (const key in aa) {
      if (aa.hasOwnProperty(key)) {
        const element = aa[key];
        console.log({ element });
      }
    }
  }
};
</script>
