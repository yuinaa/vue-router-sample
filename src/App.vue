<template>
  <nav>
    <ul>
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/about">About</router-link></li>
      <li v-for="test in tests" :key="test.id">
        <router-link :to="`/test/${test.id}`">
        Title id:{{ test.id }}
        </router-link>
      </li>
    </ul>
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

<style>
nav ul{
margin: 0 ;
padding: 0 ;
}
nav li{
list-style: none;
display: inline-block;
padding: 0 1em;
}
nav li:not(:last-child){
border-right:1px solid #888;
}
/* ul {
  list-style-type: none;
  display: flex;
  padding: 0;
}
li {
  padding-right: 2em;
} */
</style>