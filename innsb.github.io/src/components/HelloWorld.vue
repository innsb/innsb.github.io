<template>
  <div class="hello">
    
    
      <div class="container justify-content-center">
    <div id="demo" class="row justify-content-center w-50 m-auto">
      <div class="column justify-content-center" id="divBtn">
        <!-- Table visibility switch -->
        <div class="custom-control custom-switch d-flex justify-content-center">
          <input type="checkbox" class="custom-control-input" id="customSwitch1" v-on:click="showTbl = !showTbl">
          <label class="custom-control-label" for="customSwitch1">Вкл/Выкл всю таблицу</label>
          <!-- Table visibility switch -->
        </div><br>
        <div class="col-lg-6 " id="btn10">
          <button class="btn btn-success m-1" @click="append('1')">1</button>
          <button class="btn btn-success m-1" @click="append('2')">2</button>
          <button class="btn btn-success m-1" @click="append('3')">3</button>
          <button class="btn btn-success m-1" @click="append('4')">4</button>
          <button class="btn btn-success m-1" @click="append('5')">5</button>
          <button class="btn btn-success m-1" @click="append('6')">6</button>
          <button class="btn btn-success m-1" @click="append('7')">7</button>
          <button class="btn btn-success m-1" @click="append('8')">8</button>
          <button class="btn btn-success m-1" @click="append('9')">9</button>
          <button class="btn btn-success m-1" @click="append('0')">0</button>
        </div>
      </div>
      <div id="divInput" class="m-2 form-group w-auto position-relative">
        <form id="search">
          <label class="" for=""></label>
          <div class="input-group">
            <input name="query" v-model="searchQuery" class="form-control" placeholder="ИНН">
            <div class="btn btn-success input-group-append" @click="clear()">X</div>
          </div>
          <small id="" class="form-text text-muted">Введите первые 2 цифры</small>
        </form>
        <div>
        </div>
      </div>
      <!-- Grid Table -->
      <demo-grid v-if="showTbl || isSearchQuery" class="m-2" :data="gridData" :columns="gridColumns" :filter-key="searchQuery">
      </demo-grid>
      <!-- Grid Table -->
    </div>
  </div>


  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
/*   main.css  */
body {
  flex-direction: column;
  font-family: 'Open Sans', sans-serif;
  font-size: 14px;
  color: #444;
}
#demo {
 max-width: 400px;
  width: 400px;
}
#divBtn {
  /* display: block; */
  /* flex-flow: row wrap; */
  justify-items : center;
  align-content: center;
  align-items: center;
  justify-content: center;
  margin: auto;
}
#btn10 {
  display: flex;
  flex-flow: row wrap;
  justify-items : center;
  align-content: center;
  align-items: center;
  justify-content: center;
  /* width: 330px; */
  /* height: 250px; */
  padding: 1;
  margin: auto;
  /* position: relative; */

}
@media (max-width: 330px) {
  #btn10 {
    padding: 0;
  }
}


</style>
