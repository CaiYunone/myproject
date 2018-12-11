<template>
  <div>

  </div>
</template>
<script>
  import {getRecommend} from '../assets/recommend'
  import {ERR_OK} from "../assets/config";

  export default {
    data(){
      return{

      }
    },
    created(){
      this._getRec()
    },
    methods:{
      _getRec(){
        getRecommend().then(res=>{
          if(res.code===ERR_OK){
            console.log(res.data.slider)
          }
        })
      }
    }
  }
</script>
