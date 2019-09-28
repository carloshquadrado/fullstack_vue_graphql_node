# Aula 001

## Criando o Ambiente com o VueJS
```
vue create .
    OBS: Fazer na pasta do Projeto
Current directory? Y
Pick a preset: default (babel, eslint)
```

## Limpando o arquivo padrão App.vue

### Tag < script>< /script>
```
Remover a linha da importação do componente HelloWorld dentro da tag <script>
Remover as linhas da renderização do componente HelloWorld dentro da tag <script>


import HelloWorld from './components/HelloWorld.vue '

  components: {
    HelloWorld
  }

Ficando  da seguinte forma:
export default {
  name: 'app'
}
```

### Tag < template>< /template>
```
Remover o bloco abaixo, retirando o logo e o título.

  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>

Ficando da seguinte forma:
<template>

</template>
```
### Tag < style>< /style>
```
Remover o bloco abaixo, retirando a estilização CSS.

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

Ficando da seguinte forma:
<style>

</style>
```

## < template > - Inclusão de < div> , título e padrões Bootstrap
### Tag < div>< /div>
``` 
Criar uma tag div dentro da template pois é obrigatório o projeto ter uma div "root", sem ela o projeto dá erro
```
### Título+Bootstrap
```
Criar dentro da tag <div> o seguinte trecho:

Usar a centralização do bootstrap
    <div class="text-center">
Título do Projeto com tag <h1>    
      <h1>NameGator</h1>
    </div>
```
### Instalar Bootstrap e Font-Awesome
```
Ver o processo no README.md do projeto
```
### Importar na tag < script> o Bootstrap e Font-Awesome
```
import "bootstrap/dist/css/bootstrap.css"
import "font-awesome/css/font-awesome.css"
```

### Na tag < template> - Adicionar o texto secundário, utilizando também uma função do Bootstrap
```
      <br/>
      <h6 class="text-secondary">Gerador de Nomes utilizando Vue.js, GraphQL e Node</h6>
```
