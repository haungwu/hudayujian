<template>
  <div>
      <i-card  v-for="item in top" :key="item" i-class="split" :extra="item.name" :thumb="item.iamge">
    <view slot="content">{{item.remark}}</view>
    <view slot="footer">{{item.address}}</view>
</i-card>

    </div>
</template>

<script>


export default {
  data () {
    return {
     list:[]
      
    }
  },

   onLoad(option){

  this.recommand = require('@/data/' + option.type + '.json')
  console.log(this.list)
   },
  methods: {
  
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>

</style>
