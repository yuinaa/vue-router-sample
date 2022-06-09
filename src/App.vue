<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <div v-for="test in tests" :key="test.id">
      <router-link :to="`/test/${test.id}`">
      Title id:{{ test.id }}
      </router-link> |
    </div>
  </nav>
  <router-view/>
</template>
<script>
export default {
  data(){
    return {
      tests: [
        {
          id:1
        },
        {
          id:2
        }
      ]
    }
  }
}
</script>