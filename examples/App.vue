<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Demo />
    <div style="display: flex" @click="click">
      <x-card imgSrc="lhc-o.jpg" summary="2021,龙马精神！" />
      <x-card imgSrc="lhc-s.jpg" summary="送你一朵小红花！">
        <template v-slot:footer>
          <div class="footer">
            <div class="level">新晋女神</div>
            <div class="prive">99999999</div>
          </div>
        </template>
      </x-card>
      <x-card
        imgSrc="lhc-t.jpg"
        :width="370"
        :imgHeught="90"
        summary="2022,念念相忘！"
      />
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  components:{
  },
 methods:{
   click(){
   
  //  console.log(new Date);
   }
 }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.footer {
  padding: 0 8px;
  font-size: 12px;
  text-align: left;
}

.level {
  color: #9199A1;
  margin-bottom: 8px;
}

.prive {
  color: #f01414;
}


</style>
