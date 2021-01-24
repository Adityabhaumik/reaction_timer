<template>
  <h4>Reaction time : {{result}} ms</h4>
  <p class="rank">{{rank}}</p>
</template>

<script>
export default {
    props:['result'],
    data(){
        return{
             rank:null
        } 
       
    },
    mounted(){
        if(this.result <250){
            this.rank='Super Duper Ultra Legendery Fast'
        }
        else if(this.result <300){
            this.rank='Super Duper Fast'
        }
        else if(this.result <400){
            this.rank = 'not fast not sloww mehhh kindaa'
        }
        else{
            this.rank ='Very Bad reaction Time ! Becarefull on the Road '
        }
    }
}
</script>

<style scoped>
h4{
    font-size: 1.4em;
    color: #2de027;
    font-weight: bold;
    /* identical to box height */


  

  
    }

    .rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
    }

</style>