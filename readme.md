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

Creamos una nueva app de Vue, a esta le pasamos (entre otroselementos), el elementeo donde se cargará la app,
la data que esta utilizará y como opcionales filtros, etc