<template>
    <h1>Hey, {{ name }}</h1> <!-- {{ name }} é conhecido como mustache-->
    <input type="text" v-model="name"> <!-- exemplo de data-binding (ligação dos dados)-->

    <!--Da mesma forma, possível é fazer um bind alternativo-->
    <h6 v-bind:style="decoration">css com objetos</h6>

    <!-- v-bind: também pode ser abreviado para : como facilitador-->
    <!--tudo dentro das chaves únicas são interpretadas como javascript-->
    <h6 :style="{ textDecoration: decoration }">css com parâmetro e variável</h6>

    <!--acima textDecoration é um parâmetro, enquanto embaixo é um valor js-->
    <h6 :style="{ textDecoration }">css com variável direta</h6>

    <!-- v-bind, novamente-->
    <a :href="link">Link do meu GitHub</a>
</template>
  
<script>
export default {
    data: () => ({
        name: 'Ryu', //declaração de variável
        decoration: 'underline',
        link: 'https://github.com/Henrycklol',
        textDecoration: 'underline'
    })
}
</script>
  