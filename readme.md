# Vue JS
https://vuejs.org/

Para comenzar a utilizar, copiamos el script:
<!-- production version, optimized for size and speed -->
<script src="https://cdn.jsdelivr.net/npm/vue"></script>
Al final del body


# Inicialización de app en Vue
Creamos un div principal con el id: #app

<div id="app">
    <h1>Hola {{ nombre }} </h1>
</div>

let app =  new Vue({
    el: '#app', 
    data: {
        nombre: 'Matias'
    },
    filters: {
        uppercase: function(str) {
            return str.toUpperCase()
        }, 
        lowercase: function(str) {
            return str.toLowerCase()
        },
    }
})

Creamos una nueva app de Vue, a esta le pasamos (entre otroselementos), el elemento donde se cargará la app,
la data que esta utilizará y como opcionales filtros,

Al ser una aplicación reactiva, todo lo que cambie en la API (O backend), cambiara inmediatamente en el front 

# Manejo de eventos

Podemos utilizar el atributo v-on:evento="funcion" para cargar una funcion (previemente creada en nuestro objeto vue)
<button v-on:click="sumar"> Sumar 1 </button>

Es posible llamar una funcion con el shortcut
<button @click="sumar"> Sumar 1 </button>

He incluso cargar codigo js directamente
<button @click="contador++"> Sumar 1 </button>

Ahora, en nuestro objeto Vue, cargamos las funciones de la siguiente manera;

let app =  new Vue({
    el: '#app', 
    data: {
        contador: 0
    },
    methods: {
        sumar: function() {
            this.contador++
        }
    }
})

# Condicionales e iteradores

# Componentes
