<template>
  <div id="app">
    <div class="container">
      <h1>Simon Says</h1>

      <div class="simon">
        <ul>
          <li class="blue"></li>
          <li class="red"></li>
          <li class="green"></li>
          <li class="yellow"></li>
        </ul>
      </div>

      <div class="status">
        <h2>Status</h2>

        <h3>Round: {{}}</h3>

        <button>Start</button>
      </div>

      <div class="options">
        <h2>Options</h2>
        <div class="game-difficulty" action="">
          <input type="radio" checked /> Easy <br />
          <input type="radio" /> Normal <br />
          <input type="radio" /> Hard
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
};
</script>

<style lang="sass">
*
  padding: 0
  box-sizing: border-box

#app
  font-family: Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: center
  color: #2c3e50
  margin-top: 60px

div
  display: block

button
  font-size: 18px
  padding: 10px 20px
  cursor: pointer

.container
  display: block
  width: 500px
  margin: 0 auto

.simon
  position: relative
  float: left
  width: 300px
  height: 300px
  margin-right: 50px

.status
  text-align: left

.options
  text-align: left

ul
  list-style: none

.blue,
.red,
.green,
.yellow
  width: 300px
  height: 300px
  position: absolute
  border-radius: 150px 150px 150px 150px

  &:hover
    filter: opacity(.8);
    border: 5px solid black

.blue
  background-color: blue
  clip: rect(0, 150px, 150px, 0)

.red
  background-color: red
  clip: rect(0, 300px, 150px, 150px)

.green
  background-color: green
  clip: rect(150px, 300px, 300px, 150px)

.yellow
  background-color: yellow
  clip: rect(150px, 150px, 300px, 0)


.game-difficulty
  input
    display: inline-block
</style>
