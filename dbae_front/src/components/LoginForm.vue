<script>
  export default {
    methods: {
      onClick() {
        this.btnText = 'Loading'
        this.isDisabled = true
      },
    },
    data() {
      return {
        btnText: 'Logi',
        isDisabled: false,
      }
    }
  }
</script>


<template>
  <div class="greetings">
    <form class="green">
      <input type="user">
      <input type="password">
      <button @click="onClick()" :disabled="this.isDisabled" >{{ this.btnText  }}</button>
    </form>


    
  </div>
</template>

<style scoped>
form {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
