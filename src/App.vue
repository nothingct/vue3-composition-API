<template>
  <h1 @click="increase">
    {{ count }} / {{ doubleCount }}
  </h1>
  <h1>
    {{ message }} / {{ reversedMessage }}
  </h1>
</template>

<script>
export default {
  data(){
    return{
      message: 'Here Comes The Life',
      count : 0
    }
  },
  computed:{
    doubleCount(){
      return this.count*2
    },
    reversedMessage(){
      return this.message.split('').reverse().join('')
    }
  },
  methods:{
    increase(){
      history.count+=1
    }
  }
}
</script>