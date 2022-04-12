<template>
  <div id="app">
    <ganttView msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// import gantt637 from './components/gantt637.vue'
import ganttView from './components/ganttView.vue'
import {EventBus} from './components/Bus.js'
import moment from 'moment'
export default {
  name: 'App',
  components: {
    // gantt637
    ganttView
  },
  created () {

    let reg = /[0-9]{4}-([0][1-9]|[1][0-2])-[0-2][0-9]|[3][0-1]/
    console.log(reg.test('2020-09-09'));
    // })
  },
  methods: {
    getdata(e){
      console.log(e.target.value);
    }
  }
  
}
</script>

<style>
</style>
