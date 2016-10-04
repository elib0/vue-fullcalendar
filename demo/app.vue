<template>
  <div>
  	<p>
  		Here is the demo of vue-fullcalendar, no jquery fullcalendar.js required!
  	</p>
    <full-calendar class="test-fc" :events="fcEvents" day-click="" lang="es"></full-calendar>
  </div>
</template>
<script>
let demoEvents = [
    {
      title    : 'Sunny 728-730',
      start    : '2016-10-20',
      end      : '2016-11-01',
      cssClass : 'family'
    },
    {
      title : 'Sunny 726-727',
      start : '2016-10-29',
      end : '2016-11-15',
      cssClass : ['home', 'work']
    },
    {
      title : 'Sunny 727-728',
      start : '2016-07-27',
      end : '2016-07-28'
    },
    {
      title : 'Sunny 728-730',
      start : '2016-07-28',
      end : '2016-07-30'
    },
  ]

export default {
	data () {
		return {
      name:'Sunny!',
      fcEvents : demoEvents
    }
	},
  events : {
    'changeMonth' (start, end, current) {
      console.log('changeMonth', start, end, current)
    },
    'dayClick' (day) {
      console.log(day)
    }
  },
  components : {
    'full-calendar' : require('src/fullCalendar')
  }
}
</script>
<style lang='scss'>
  .app{
    color:green;
  }
  .family{
    background: #337ab7 !important;
  }

  .work{
    background: #5cb85c !important;
  }
</style>