<template>
  <div>
    User组件--{{title}}
    <br>
    username--{{username}}
    <br>
    <button @click="setUsername('旺旺')"></button>
  </div>
</template>

<script lang="ts">
import {defineComponent, reactive, toRefs} from 'vue';

interface User{
  username:string,
  age:number,
  setUsername(username:string):void,
  getUsername():string
}

export default defineComponent({
  setup() {
    let user:User=reactive({
      username: "张三",
      age: 20,
      setUsername() {
        this.username = "李四"
      },
      getUsername() {
        return this.username
      }
    })
    return{
      ...toRefs(user)
    }
  }
})
</script>

<style lang="scss">

</style>