<template>
  <main>
    <h1>Counter</h1>
    <h1>{{ number }}</h1>
    <div class="input">
      <input type="button" value="+" @click="add()">
      <input type="button" value="-" @click="reduce()">
    </div>
  </main>
</template>
<script>
export default{
  data(){
    return{
      number: 0
    }
  },
  methods:{
    add(){
      this.number++;
    },
    reduce(){
      this.number--;
    }
  }
}
</script>

<style lang="scss">
main{
  background-color: #f5f5f5;
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  box-sizing: border-box;
  h1{
    font-size: 100px;
    font-weight: 100;
    margin: 0;
  }
  .input{
    display: flex;
    justify-content: center;
    align-items: center;
    input{
      width: 50px;
      height: 50px;
      font-size: 30px;
      border: none;
      background-color: #fff;
      margin-left: 1rem;
      cursor: pointer;
      box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
      &:hover{
        background-color: #ccc;
      }
    }
  }
}

</style>