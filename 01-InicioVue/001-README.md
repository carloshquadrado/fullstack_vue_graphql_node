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
### Na tag < div> do título - Adicionadando o ID="slogan" / Na tag < style> adicionando o estilo
```
<div id="slogan" class="text-center">

#slogan {
  margin-top: 30px;
  margin-bottom: 30px;
}
```
### Criar uma nova < div> Main - Adicionadando o ID="main" / Na tag < style> adicionando o estilo
```
    <div id="main">

    </div>
    
#main {
  background-color: #F1F1F1;
  padding-top: 30px;
  padding-bottom: 30px;
}
```
### Dentro da Main - Criar uma nova < div> Container, dentro dela  < div>  row, dentro dela < div> col-md - dívida em duas colunas
```
      <div class="container">
          <div class="row">
            <div class="col-md">
              X
            </div>
            <div class="col-md">
              Y
            </div>
          </div>
      </div>
```
### Dentro do Container - Trocar o X e Y por < div> Card e dentro < div> Card-body
```
Repetir o código abaixo trocando duas vezes uma trocando pelo X e outra Y.

              <div class="card">
                <div class="card-body">
                </div>
              </div>
```

### Antes do < div> Card - Incluir o título Prefixos + Badge Contador e no segundo o título Sufixos
```
<h5>Prefixos <span class="badge badge-info">0</span></h5>

<h5>Sufixos <span class="badge badge-info">0</span></h5>
```
### Dentro da < div> card-body, incluir < ul> list-group e < li> list-group-item para Prefixo e Sufixo
```
Prefixos
                  <ul class="list-group">
                      <li class="list-group-item">
                        A
                      </li>
                      <li class="list-group-item">
                        B
                      </li>
                      <li class="list-group-item">
                        C
                      </li>
                  </ul>  
Sufixos
                 <ul class="list-group">
                      <li class="list-group-item">
                        D
                      </li>
                      <li class="list-group-item">
                        E
                      </li>
                      <li class="list-group-item">
                        F
                      </li>
                  </ul>    
```

### Depois da < ul>, incluir o input para Prefixo e Sufixo
```
                  <br/>
                  <input class="form-control" type="text" placeholder="Digite o Prefixo"/>  

                  <br/>
                  <input class="form-control" type="text" placeholder="Digite o Sufixo"/>  
```                  

### Na tag < script>, incluir a propriedade data
```
Cria uma função que retorna um objeto Prefixo e outro Sufixo

data: function () {
    return {
      prefixos: ['Air','Jet','Flight'],
      sufixos: ['Hub','Station','Mart']
    };
  }
```
