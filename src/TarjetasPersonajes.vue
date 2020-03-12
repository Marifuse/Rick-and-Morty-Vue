<template>
    <div id="main-container">
        <!-- Contenedor img y personaje -->
        <section class="container">
            <div class="p-list">
                <img v-bind:src="image"/>
                <h2>{{nombre}}</h2>
            </div>                
        </section>
    </div>
</template>

<script>
// Código donde se pone el tipo de nombre e imagen
export default {
    name: "TarjetasPersonajes",
    props: {
        nombre: String,
        image: String
    }
}
</script>

<style scoped>
    /* Contenedor de TarjetasPersonajes */
    .container {
        width: 20em;
        margin: auto;       
    }
    .p-list {
        display: flex;
        padding: 1em;
    }
    /* Imagen contenida en App */
    img {
        width: 6em;
        border-radius: 50%;
    }
    /* Nombre contenido en App */
    h2 {
        padding-left: 1em;
        padding-top: 0.5em;
        color: darkgreen;
    }
</style>

