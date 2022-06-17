<template>
  <v-container>
    <br>
    <h2>---------- Contact Us ------------</h2>
     <div class="form_container">
       <v-form
    ref="form"
    v-model="valid"
    lazy-validation
  >
   <v-text-field
      v-model="name"
      :rules="emailRules"
      label="Name"
      required
    ></v-text-field>

    <v-text-field
      v-model="message"
      :rules="emailRules"
      label="Message"
      required
    ></v-text-field>

  
    

    <v-btn
      color="warning"
      @click="resetValidation"
    >
      Send
    </v-btn>
  </v-form>
     </div>
  </v-container>
</template>
<script>
 export default {
    data: () => ({
      valid: true,
      name: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => (v && v.length <= 10) || 'Name must be less than 10 characters',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
      select: null,
      items: [
        'Item 1',
        'Item 2',
        'Item 3',
        'Item 4',
      ],
      checkbox: false,
    }),

    methods: {
      validate () {
        this.$refs.form.validate()
      },
      reset () {
        this.$refs.form.reset()
      },
      resetValidation () {
        this.$refs.form.resetValidation()
      },
    },
  }
</script>

<style>

</style>