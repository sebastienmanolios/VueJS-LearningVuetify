<template>
  <v-container>
    <v-raw>
      <v-col>
        <h1>Signup</h1>
        <v-form>
          <v-text-field label="Email" type="email"></v-text-field>
          <v-autocomplete :items="browser" label="Which browser do you use?"></v-autocomplete>
          <v-file-input label="Attach file profile"></v-file-input>
          <v-text-field label="Birthday" v-model="birthday" readonly></v-text-field>
          <v-date-picker v-model="birthday"></v-date-picker>
          <v-checkbox label="Agree to terms & conditions"></v-checkbox>  
          <v-switch label="Agree to terms & conditions"></v-switch>  
          <v-btn color="primary" type="submit">Submit</v-btn>
        </v-form>
      </v-col>
    </v-raw>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      birthday: '',
     browser: [
       'Chrome',
       'Firefox',
       'Safari',
       'Edge',
       'Brave'
     ]
    }
  },
}
</script>