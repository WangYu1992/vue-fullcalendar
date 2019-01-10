<template>
  <div>
    <full-calendar locale="zh-cn" :events="events" @eventMouseover="eventMouseover" @eventClick="eventClick">
		<template slot="fc-event-card" scope="p">
			<!-- {{p}} -->
            <p>{{ p.event.title }}</p>
        </template>
	</full-calendar>
  </div>
</template>

<script>
import fullCalendar from "./components/fullCalendar.vue";
export default {
  components: {
    fullCalendar
  },
  data() {
    return {
      events: [
        {
          title: "event1",
		  start: "2019-1-10",
		},
		{
			title: 'event4',
			start: '2019-1-10',
		},
		{
          title: "event2",
		  start: "2019-1-11",
        },
		{
			title: 'event5',
			start: '2019-1-10',
		},
		{
			title: 'event6',
			start: '2019-1-10'
		},
		{
			title: 'event7',
			start: '2019-1-10'
		},
		{
			title: 'event8',
			start: '2019-1-10',
			
		},
        
        {
          title: "event3",
          start: "2019-1-12"
        },
      ]
    };
  },
  methods: {
	  eventClick (event, jsEvent, pos) {
		  console.log(event, jsEvent, pos)
	  },
	  eventMouseover (event, jsEvent, pos) {
		//   console.log(event, jsEvent, pos)
	  }
  }
};
</script>

<style>
</style>
