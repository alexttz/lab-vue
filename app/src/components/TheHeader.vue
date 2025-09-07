<template>
    <header class="header">
        <h1>This is Header</h1>
    </header>
    <!--
        A diretiva
      v-for faz uma varredura em um array ou objeto
        e repete o bloco de código para cada item encontrado.
        A diretiva v-bind:key é usada para fornecer uma chave única para cada item.
        classe CSS "todo-item" estiliza cada item da lista.
        obj.title exibe o título de cada item do array "todos"  .
    -->
    
    <div v-for="obj in todos"
        v-bind:key="obj.id"
        class="todo-item">

        {{ obj.title }}

    </div>

</template>

<script>
export default {

    /*
    Definimos dois arrays "todos" dentro do data.
    O primeiro array é um array de arrays,
    enquanto o segundo array é um array de objetos.
    Ambos os arrays contêm objetos com propriedades "userId", "id", "title" e "completed".
    No template, usamos a diretiva v-for para iterar sobre o array "todos"
    e exibir o título de cada objeto na tela.
    */
    data() {
        return {
            todos: [
                [
                    {
                        "userId": 1,
                        "id": 1,
                        "title": "delectus aut autem",
                        "completed": false
                    },
                    {
                        "userId": 1,
                        "id": 2,
                        "title": "quis ut nam facilis et officia qui",
                        "completed": false
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
                ],
                {
                    "userId": 1,
                    "id": 1,
                    "title": "delectus aut autem",
                    "completed": false
                },
                {
                    "userId": 1,
                    "id": 2,
                    "title": "quis ut nam facilis et officia qui",
                    "completed": false
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

.todo-item {
    background-color: #f9f9f9;
    border: 1px solid #ddd;
    padding: 10px;
    margin: 5px 0;
}   

.header {
    background-color: #42b983;
    padding: 20px;
    color: white;
    text-align: center;
}
</style>