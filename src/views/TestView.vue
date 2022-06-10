<template>
    <div class="test">
        <p>TEST{{ $route.params.id }}</p>
    </div>
</template>

<script>
export default {
  mounted(){
    console.log(this.$route)
  }
}
</script>