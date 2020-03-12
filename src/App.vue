<template>
    <div id="main">
        <!-- Sección que contiene la imagen y el nombre del personaje -->
        <section class="container">
            <!-- Función que recorre el arreglo del componente TarjetasPersonajes -->
            <article class="personajes-list" v-for="(personaje, index) in personajes" :key="index">
                <TarjetasPersonajes 
                v-bind:image = "personaje.image"
                v-bind:nombre = "personaje.name">
                </TarjetasPersonajes>  
            </article>             
        </section>
    </div>
</template>

<script>
// Codigo con el import
import TarjetasPersonajes from "./TarjetasPersonajes.vue";
export default {
    name: "App",
    components: { TarjetasPersonajes },
    data() {
        return {
             personajes: [
                {
                    name: 'Rick Sanchez',         
                    image: 'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
                },
                {
                    name: 'Morty Smith',         
                    image: 'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
                },
                {
                    name: 'Summer Smith',         
                    image: 'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
                },
                {
                    name: 'Beth Smith',         
                    image: 'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
                },
                {
                    name: 'Jerry Smith',         
                    image: 'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
                }
            ]
        }
    }
}
</script>

<style>
    /* Estilo HTML */
    body {
        margin: 0;
        background-image: url(https://rickandmortypod.com/wp-content/uploads/2018/11/cropped-RM_page-header_background1-3.png);
        background-size: cover;
    }
    /* Contenedor imagen y nombre */
    #main {
        padding: 5em;
        padding-top: 2em;
    }
</style>

