<template>
<div>
  <div>
    <h1 class="title">Calculator</h1>
  </div>
  <hr>
  <div>
    <b-container fluid>
      <b-row class="text-center">
        <b-col cols="2" class="text-center"></b-col>
        <b-col cols="4" class="text-center">
          <form>
            <div class="field">
              <label class="lable">First Number</label>
              <b-form-input name="num1" v-model="num1" v-validate="'required|digits'" class="input" type="text"></b-form-input>
            </div>
            <div class="field" style="margin-top:12px;">
              <label class="label">Second Number</label>
              <b-form-input name="num2" v-model="num2" class="input" v-validate="'required|digits'" type="text"></b-form-input>
            </div>
          </form>
        </b-col>
        <b-col cols="4" class="text-left">
          <div><label class="label">Addition: {{ add }}</label></div>
          <div><label class="lable">Multiplication: {{ mul }}</label></div>
          <div><label class="label">Subtraction: {{ sub }}</label></div>
          <div><label class="label">Division: {{ div }}</label></div>
        </b-col>
      </b-row>
    </b-container>
  </div>

  &nbsp;
  <div>
    <b-button variant="primary" v-on:click="postreq()">Calculate</b-button>
  </div>
</div>
</template>

<script>

export default {
  name: 'app',
  components: {
 
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
