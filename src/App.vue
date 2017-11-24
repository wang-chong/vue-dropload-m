<template>
  <div class="dropload-container">
    <p>以下数据是可以更新的哦~~~</p>
    <div>
      <dropload ref="drop" :loadUpFn="reFreshData" :loadDownFn="getMoreData">
        <div v-for="item in datalist" class="list">
          我是随机数{{item}}！！！
        </div>
      </dropload>
    </div>
  </div>
</template>

<script>
function getData() {
  let data = []
  for (let i = 0; i < 5; i++) {
    data.push(parseInt(Math.random() * 1000))
  }
  return data
}

export default {
  data () {
    return {
      datalist: [1,2,3]
    }
  },
  methods: {
    reFreshData () {
      const vm = this
      setTimeout(function () {
        vm.datalist = getData()
        vm.$refs.drop.resetUp()
      }, 2000)
    },
    getMoreData () {
      const vm = this
      setTimeout(function () {
        vm.datalist = vm.datalist.concat(getData())
        vm.$nextTick(vm.$refs.drop.resetDown)
      }, 2000)
    }
  }
}
</script>

<style lang="scss">
$color1: red;
html,body{
  margin: 0;
  padding: 0;
  height: 100%;
  position: relative;
}
p{
  margin: 0;
  padding: 20px
}
.dropload-container {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-bottom: 20px;
  .list{
    border-top: 1px solid $color1;
    padding: 12px;
    &:nth-last-child(1) {
      border-bottom: 1px solid $color1;
    }
  }
}
</style>
