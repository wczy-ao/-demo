<template>
  <div class="container">
    <button @click="testBus">bus测试</button>
    <p>222</p>
    <tetstt></tetstt>
    <gantt class="left-container" :tasks="tasks"></gantt>
  </div>
</template>
 
<script>
import Gantt from './gantt713.vue';
 import tetstt from './bustets.vue'
export default {
  name: 'app',
  components: {Gantt,tetstt},
  data () {
    return {
      tasks: {
        data: [
          {id: '1', text: 'Task #1', start_date: '2020-01-17', duration: 3, progress: 0.6},
          {id: '2', text: 'Task #2', start_date: '2020-01-20', duration: 3, progress: 0.4, },
          {id: '3', text: 'Task #2', start_date: '2020-01-20', duration: 3, progress: 0.4, },
          {id: '4', text: 'Task #2', start_date: '2020-01-20', duration: 3, progress: 0.4, }
        ],
        links: [
          {source: '3', target: 2, type: 0}
        ]
      },
    }
  },
  methods:{
    testBus(){
      EventBus.$emit('ganttOk',"ok")
    }
  }
}
</script>

<style >
  
  .container {
    height: 500px;
    width: 100%;
  }
  .left-container {
    overflow: hidden;
    position: relative;
    height: 100%;
  }
</style>