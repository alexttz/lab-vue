<template>
    <header class="header">
        <h1>This is Header</h1>
    </header>
    <!--
        A diretiva v-for itera sobre um array ou objeto e renderiza o bloco de código
        para cada item. A diretiva :key é usada para fornecer uma chave única para
        cada item, o que ajuda o Vue a otimizar a renderização.
        A classe CSS "todo-item" estiliza cada item da lista.
        obj.title exibe o título de cada item do array "todos".
    -->
    
    <div v-for="obj in todos" :key="obj.id" class="todo-item">
        <img v-if="obj.imgSrc" :src="obj.imgSrc" :alt="obj.title">
        {{ obj.title }}
    </div>
</template>

<script>
export default {

    /*
    Definimos o array "todos" dentro de data().
    Este array contém uma lista de objetos, onde cada objeto representa uma tarefa (todo).
    Cada objeto de tarefa tem propriedades como "userId", "id", "title", "completed" e opcionalmente "imgSrc".
    No template, usamos a diretiva v-for para iterar sobre o array "todos"
    e exibir o título e a imagem de cada tarefa na tela.
    */
    data() {
        return {
            todos: [
                {
                    "userId": 1,
                    "id": 1,
                    "title": "delectus aut autem",
                    "completed": false,
                    "imgSrc": "https://placehold.co/600x400",
                },
                {
                    "userId": 1,
                    "id": 2,
                    "title": "quis ut nam facilis et officia qui",
                    "completed": false,
                    "imgSrc": "https://placehold.co/600x400",
                },
                {
                    "userId": 1,
                    "id": 3,
                    "title": "fugiat veniam minus",
                    "completed": false
                },
                {
                    "userId": 1,
                    "id": 4,
                    "title": "et porro tempora",
                    "completed": true
                },
                {
                    "userId": 1,
                    "id": 5,
                    "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
                    "completed": false
                }
            ]
        }
    }
}

</script>

<style>


.header {
    background-color: #42b983;
    padding: 20px;
    color: white;
    text-align: center;
}

.todo-item {
    margin-bottom: 10px;
    padding: 10px;
    border: 1px solid #ccc;
}
.todo-item img {
    max-width: 100px;
    display: block;
    margin-bottom: 5px;
}
</style>