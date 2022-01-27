<template>
  <Calendar
      :min-date="new Date()"
      :attributes="attrs"
      @dayclick="onDayClick"
      v-model="customer.birthday"
      is-required
      mode="date"
  />
</template>


<script>
import { Calendar } from 'v-calendar';
import axios from "axios";

export default {
  components:{
    Calendar
  },
  data() {
    return {
      attrs: [
        {
          key: 'today',
          highlight: true,
          dates: new Date(),
        }
      ],

      days: [],
      customer: {
        name: 'Nathan Reyes',
        birthday: '1983-01-21',
      },
      modelConfig: {
        type: 'string',
        mask: 'YYYY-MM-DD', // Uses 'iso' if missing
      },
    };
  },

  methods: {
    onDayClick(day) {
      this.selectedDay = day;
      let availableHours = ['09:00','10:00', '11:00', '12:00', '13:00', '14:00', '15:00', '16:00', '17:00'];
      axios.get('https://death-api-im7m6.ondigitalocean.app/api/appointments')
          .then(response => this.available = response.data)
      console.log(availableHours);
      console.log(this.available);
      /*const idx = this.days.findIndex(d => d.id === day.id);
      if (idx >= 0) {
        this.days.splice(idx, 1);
      } else {
        this.days.push({
          id: day.id,
          date: day.date,
        });
      }*/
    },
  },

}

</script>