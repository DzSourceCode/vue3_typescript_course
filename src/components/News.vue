<template>
  <div>
    News组件--{{title}}
    <br>
    count={{count}}
    <br>
    <button @click="setCount">改变Count</button>
    <br>
    <button @click="setTitle(123)">改变title</button>
  </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue';

interface News{
  title:string,
  description:string,
  count:number|string|boolean,
  content?:string
}
// let newsData:News={
//   title:"新闻联波",
//   description:"新闻描述",
//   count:12
// }
let newsData={
  title:"新闻联波",
  description:"新闻描述",
  count:12
} as News

export default defineComponent({
  data() {
    return newsData
  },
  methods: {
    setCount():void{
      this.count = 123
    },
    setTitle(title:string):void{
      this.title = title
    }
  },
})
</script>

<style lang="scss">

</style>