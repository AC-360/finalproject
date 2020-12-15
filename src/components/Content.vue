<template>
  <div>
    <form>
          <input type="text" placeholder="5-Digit Zip Code">
          <button id="farenheit" v-on:click="farenheit">Farenheit</button>
      <button id="celsius" v-on:click="celcius">Celsius</button>
    </form>
    <h1>{{theName}}</h1>
    <h2>{{theTemp.temp}}</h2>
    <img id="wImg" v-bind:src="'https:openweathermap.org/img/wn/' + theWeather[0].icon + '.png'" alt="Weather">
    <p id="description">{{theWeather[0].main}}</p>
  </div>
</template>

<script>
export default {
  name: 'Content', //Setting name to show in template
  props: ['theWeather','theTemp','theName']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  div{
    color: gray;
  }
  #wImg{
    width: 25%;
    height: 25%;
    background-color: lightblue;
  }
  #description{
    font-size: 150%;
  }
</style>
