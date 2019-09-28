<template>
  <div>
    <div id="slogan" class="text-center">
      <h1>NameGator</h1>
      <br/>
      <h6 class="text-secondary">Gerador de Nomes utilizando Vue.js, GraphQL e Node</h6>
    </div>
    <div id="main">

    </div>
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css"
import "font-awesome/css/font-awesome.css"

export default {
  name: 'app'
}
</script>

<style>
#slogan {
  margin-top: 30px;
  margin-bottom: 30px;
}

#main {
  background-color: #F1F1F1;
  padding-top: 30px;
  padding-bottom: 30px;
}
</style>
