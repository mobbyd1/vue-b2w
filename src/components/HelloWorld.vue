<template>
  <md-layout md-flex="100">

    <md-layout md-flex="100">

      <md-layout md-flex="30" style="background-color: green; height: 50px">
      </md-layout>

      <md-layout md-flex="40" md-flex-offset="5" style="background-color: blue; height: 50px">
      </md-layout>

      <md-layout>
        <md-list class="align-right">
          <md-list-item>
            <md-button>botao 1</md-button>
          </md-list-item>
          <md-list-item>
            <md-button>botao 2</md-button>
          </md-list-item>
          <md-list-item>
            <md-button>botao 3</md-button>
          </md-list-item>
        </md-list>
      </md-layout>

    </md-layout>

    <md-layout md-flex="100">
      <md-layout>
        <h3>Items</h3>
      </md-layout>
      <md-layout md-flex="10">
        <md-button class="align-right">Enviar</md-button>
      </md-layout>
    </md-layout>

    <md-layout md-flex="50">
      <md-checkbox style="margin-top: 30px!important;"></md-checkbox>
    </md-layout>

    <md-layout md-flex="50">
      <md-input-container>
        <md-input></md-input>
      </md-input-container>
    </md-layout>

    <md-table-card class="table-100">
      <md-table>
        <md-table-header>
          <md-table-row>
            <md-table-head>Dessert (100g serving)</md-table-head>
            <md-table-head md-numeric>Calories (g)</md-table-head>
            <md-table-head md-numeric>Fat (g)</md-table-head>
            <md-table-head md-numeric>Carbs (g)</md-table-head>
            <md-table-head md-numeric>Protein (g)</md-table-head>
          </md-table-row>
        </md-table-header>

        <md-table-body>
          <md-table-row v-for="(row, index) in 5" :key="index">
            <md-table-cell>Dessert Name</md-table-cell>
            <md-table-cell v-for="(col, index) in 4" :key="index" md-numeric>10</md-table-cell>
          </md-table-row>
        </md-table-body>
      </md-table>
    </md-table-card>
  </md-layout>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .table-100 {
    width: 100%;
  }

  .align-right {
    margin-left: 40%;
  }

</style>
