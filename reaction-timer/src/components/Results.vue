<template>
  <div class="result">
  <p>Reaction time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
    </div>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank : null
    }
  },
  mounted() {
    if (this.score < 250) {
      this.rank = 'Faster than light'
    } else if (this.score < 400) {
      this.rank = 'Rapid Reflexes'
    } else {
      this.rank = 'As slow as a Snail....'
    }
  }
}
</script>

<style>
  .result{
    width: 190px;
padding: 10px;
background: #E8CF24;
overflow:auto;
display:block;
margin: 40px auto;

font-family: Verdana, Geneva, sans-serif; 
font-size: 1.4rem;
font-weight: bold;

border: 1px solid #cccccc;
-moz-border-radius: 7px;
-webkit-border-radius: 7px;
border-radius: 7px;

-moz-box-shadow: 2px 2px 2px #cccccc;
-webkit-box-shadow: 2px 2px 2px #cccccc;
box-shadow: 2px 2px 2px #cccccc;
}
  .rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
  }
</style>
