<template>
  <p>Your score: <span class="score">{{score}}</span></p>
  <p class="rank">{{rank}}</p>
</template>

<script>
export default {
    props:['score'],
    data(){
    return {
        rank:null,
    }
    },
    mounted(){
    if (this.score < 250) {
        //debugger
      this.rank = "Ninja Fingers";
    } 
    else if (this.score < 400) {
      this.rank = "Rapid Reflexes";
    } 
    else {
      this.rank = "...Snail Pace";
    }
    }
}
</script>

<style>
.score{
    font-weight: bold;
}
.rank {
  font-size: 0.9em;
  color: #fff;
  font-weight: bold;
  background: #f3ae43;
  padding: 10px 15px;
  display: inline;
  border-radius: 50px;
}
</style>