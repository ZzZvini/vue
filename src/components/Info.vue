<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades ! </p>
        <p>Utilizo as seguintes teclonogias: </p>
            <ul>
                <li>JAVASCRIPT</li>
                <li>PHP</li>
                <li>PHYTON</li>
            </ul>
        <p v-show="mostrar_email">Mande uma mensagem para {{ email }}</p>
        <p>Para acessar meu portifolio <a v-bind:href="meu_link" target="_blank"> basta clicar aqui!</a></p>
        <Picture />
    </div>
</template>

<script>
    import Picture from './Picture.vue'

    export default {
        name: 'Info',
        components :{
            Picture
        },
        data(){
            return{
                esta_trabalhando: true,
                mostrar_email: true,
                email: 'vinicios@hotmail.com',
                meu_link:'https://github.com/ZzZvini'
            }
        }
    }
</script>