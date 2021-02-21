<template>
  <v-app>
    <Header />
    <br />
    <v-main id="container">
      <h1>Reusable Components</h1>
      <TextField :fields="text_sample" />
      <SelectField :fields="select_sample" />
      <RadioField :fields="radio_sample" />
      <TimeField :fields="time_sample" />
      <DateField :fields="date_sample" />
    </v-main>
  </v-app>
</template>

<script>
import Header from './components/Header';
import TextField from './components/inputs/TextField';
import SelectField from './components/inputs/SelectField';
import RadioField from './components/inputs/RadioField';
import TimeField from './components/inputs/TimeField';
import DateField from './components/inputs/DateField';

export default {
  name: 'App',
  components: {
    Header,
    TextField,
    SelectField,
    RadioField,
    TimeField,
    DateField
  },

  data: () => ({
    text_sample: {
      label: 'Enter Text',
      text: ''
    },
    select_sample: {
      label: 'Select Item',
      answers: ['Red', 'Blue', 'Green', 'Black'],
      selected: ''
    },
    radio_sample: {
      answers: ['Yes', 'No', 'Maybe'],
      selected: 'No'
    },
    date_sample: {
       label: 'Birthday',
       // you can define a default date e.g date = Date.now()
    },
    time_sample: {
      label: 'Curfew',
      // you can define a default time with correct format
    }
  }),
};
</script>
<style>
#container {
  text-align: center;
  margin: 0 auto;
  width: 360px;
}
</style>
