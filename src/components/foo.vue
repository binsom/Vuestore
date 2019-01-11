<template>
  <div>
    <div @click="goLogin()">gg{{msg}}</div>

    <router-link to="/fooChild1">Go to FooChild1</router-link>
    <router-link to="/fooChild2">Go to FooChild2</router-link>
    <router-view/>
  </div>
</template>

<script>
  export default {
    name: 'foo',
    data () {
      return {
        msg: 'foo'
      }
    },
    methods: {
      goLogin () {
        this.$store.commit('login',{
          username: '22',
          password: '33'
        });
      }
    }
  }
</script>
