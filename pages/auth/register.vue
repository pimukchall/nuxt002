<template>
  <div class="d-flex justify-center">
    <v-card width="700" height="500">
      <v-card-title> Register </v-card-title>
      <v-card-text>
        <v-row>
          <v-col cols="6">
            <v-text-field v-model="form.fname" label="First name" outlined>
            </v-text-field>
          </v-col>
          <v-col cols="6">
            <v-text-field v-model="form.lname" label="Surname" outlined>
            </v-text-field>
          </v-col>
          <v-col cols="6">
            <v-text-field v-model="form.username" label="Username" outlined></v-text-field>
          </v-col>
          <v-col cols="6">
            <v-text-field v-model="form.email" label="Email" outlined></v-text-field>
          </v-col>
          <v-col cols="6">
            <v-text-field v-model="form.password" label="Password" :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
              :type="show1 ? 'text' : 'password'" @click:append="show1 = !show1" outlined>
            </v-text-field>
          </v-col>
          <v-col cols="6">
            <v-text-field v-model="confirmPass" label="Confirm Password" :append-icon="show2 ? 'mdi-eye' : 'mdi-eye-off'"
              :type="show2 ? 'text' : 'password'" @click:append="show2 = !show2" outlined>
            </v-text-field>
          </v-col>
        </v-row>
      </v-card-text>
      <v-card-actions>
        <v-spacer></v-spacer>
        <div>
          <span v-bind:title="message">
            <v-btn @click="gotoHome" color="primary">register</v-btn>
          </span>
        </div>
      </v-card-actions>
    </v-card>
  </div>
</template>
<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      message: 'You registered on ' + new Date().toLocaleString(),
      show1: false,
      show2: false,
      confirmPass: '',
      form: {
        fname: '',
        lname: '',
        email: '',
        password: '',
      },
    }
  },
  methods: {    
    gotoHome() {
      this.$router.push('/')
    }
  },
}
</script>