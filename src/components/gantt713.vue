<template>
  <div ref="gantt"></div>
</template>
 
<script>
// import { gantt } from '../assets/gantt_trial';
import { gantt } from 'dhtmlx-gantt';
import '../assets/locale/locale_cn'  // 本地化
console.log('aaa')
export default {
  name: 'gantt',
  props: {
    tasks: {
      type: Object,
      default () {
        return {data: [], links: []}
      }
    }
  },
 
  mounted: function () {
    gantt.config.xml_date = "%Y-%m-%d";
 
    gantt.init(this.$refs.gantt);
    gantt.parse(this.$props.tasks);
  }
}
</script>
 
<style>
    /* @import "../assets/gantt_trial/codebase/dhtmlxgantt.css"; */
    @import '~dhtmlx-gantt/codebase/dhtmlxgantt.css';
</style>