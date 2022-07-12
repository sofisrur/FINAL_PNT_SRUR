<template>

  <section class="src-components-texto">

    Color: <input type="text" v-model="color">
    Fondo: <input type="text" v-model="fondo">
    Size: <input type="text" v-model="size">
    <hr>
    Texto: <input type="text" :style="{color: color, background:fondo, fontSize: size}" v-model="ingreso">
    <p>{{contar}}</p>  



  <table>
    <tr>
            <th>Numero de Pregunta</th>
            <th>Respuesta</th>
          </tr>
          <tr>
            <td>1</td>
            <td>B</td>
          </tr>
          <tr>
            <td>2</td>
            <td>C</td>
          </tr>
          <tr>
            <td>3</td>
            <td>B</td>
          </tr>
           <tr>
            <td>4</td>
            <td>D</td>
          </tr>
           <tr>
            <td>5</td>
            <td>B, D</td>
          </tr>
        </table>
  </section>

</template>

<script>

  export default  {
    name: 'src-components-texto',
    props: [],
    mounted () {

    },
    
    
    data () {
      return {
        ingreso : " ",
        color : " ",
        fondo:" ",
        size: " "
      }
    },
    methods: {
       noEsp: function(value){
            return !value.includes(" ")
        }
    
    },
    computed: {
       contar:function(){
        var resultado = this.ingreso.split(" ")
        return "Cantidad de palabras: " + resultado.length
      },

    }
}


</script>

<style scoped lang="scss">

</style>
