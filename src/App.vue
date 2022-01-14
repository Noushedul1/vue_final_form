<template>
  <div>
    <div>
      <pre>
        {{JSON.stringify(formValues,null,2)}}
      </pre>
    </div>
    <form @submit="submitForm">
      <div>
        <label>Firstname : </label>
        <input type="text" v-model="formValues.firstname">
      </div>
      <div>
        <label>Lastname : </label>
        <input type="text" v-model="formValues.lastname">
      </div>
      <div>
        <label>Password : </label>
        <input type="text" v-model="formValues.password">
      </div>
      <div>
        <label>Email : </label>
        <input type="email" v-model="formValues.email">
      </div>
      <div>
        <label>Select course : </label>
        <select v-model="formValues.selectCourse" multiple>
          <option value="">SELECT COURSE</option>
          <option value="html">HTML</option>
          <option value="css">CSS</option>
          <option value="php">PHP</option>
          <option value="mysql">MYSQL</option>
          <option value="vue">VUE</option>
          <option value="laravel">LARAVEL</option>
        </select>
      </div>
      <div>
        <label>Select country : </label>
        <select v-model="formValues.selectCountry">
          <option value="">SELECT COUNTRY</option>
          <option value="bd">Bangladesh</option>
          <option value="usa">USA</option>
          <option value="uk">UK</option>
        </select>
      </div>
      <div>
        <p>Gender : </p>
        <input type="radio" v-model="formValues.gender">
        <label>Male </label>
        <input type="radio" v-model="formValues.gender">
        <label>Female </label>
      </div>
      <div>
        <label>Skill set : </label>
        <input type="checkbox" value="html" v-model="formValues.skillSet">
        <label>HTML</label>
        <input type="checkbox" value="css" v-model="formValues.skillSet">
        <label>CSS</label>
        <input type="checkbox" value="js" v-model="formValues.skillSet">
        <label>JS</label>
      </div>
      <div>
        <label>Years o Experience </label>
        <input type="radio" value="0-2" v-model="formValues.yearsofExperience">
        <label>0-2</label>
        <input type="radio" value="0-4" v-model="formValues.yearsofExperience">
        <label>0-4</label>
        <input type="radio" value="10+" v-model="formValues.yearsofExperience">
        <label>10+</label>
      </div>
      <div>
        <label>Agree for remote job? </label>
        <input type="checkbox" v-model="formValues.remorejob" true-value="yes" false-value="no">
      </div>
      <div>
        <button>Submit</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {

  },
  data() {
    return {
      formValues: {
        firstname: '',
        lastname: '',
        password: '',
        email: '',
        selectCource: [],
        gender: '',
        remotejob: 'no',
        selectCountrt: '',
        skillSet: [],
        yearsofExperience: ''
      }
    }
  },
  methods: {
    submitForm(event) {
      event.preventDefault();
      console.log('form value', this.formValues);
    }
  }
}
</script>

<style>

</style>