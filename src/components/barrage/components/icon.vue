
<template>
  <div v-if="options.show"
    class="barrage-Icon"  
    :class="options.div ? options.div.className :''" 
    :style="{...(options.div ? options.div.style : {})}">
      <i class="icon" 
        v-if="options.i ? options.i.showIcon : false" 
        :style="{...(options.i ? options.i.style : {})}" 
        :class="options.i ? options.i.className : ''">
        <img :src="options.i.icon" alt="" />
      </i>
  </div>
</template>
<script>
export default {
    props : {
        options : {
            type : Object,
            default : ()=> ({})
        }
    }
}
</script>
<style lang="less" scoped>
.barrage-Icon{
    display: inline-block;
    .icon{
        position: relative;
        display: inline-block;
        width: 0.22rem;
        height: 0.2rem;
        vertical-align: middle; 
        margin-bottom: 0.03rem;
        img{
            width: 100%;
            height: 100%;
        }
    }
}
</style>
