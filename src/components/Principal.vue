<template>
  <div id="Principal">
    <h1 v-text="tituloprincipal"></h1>
    <div class= "container">
      <div class="row">
      <div class="col">
      <div class="card" style="width: 18rem;">
        <img src="https://media.rawg.io/media/games/456/456dea5e1c7e3cd07060c14e96612001.jpg" class="card-img-top" alt="...">
        <div class="card-body">
          <h5 class="card-title">Nombre Juego</h5>
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item">Rating: </li>
          <li class="list-group-item">Released: </li>
          <li class="list-group-item">Updated: </li>
        </ul>
        <div class="card-body">
           <button type="button" class="btn btn-dark">Opinar</button>
        </div>
      </div>
      </div>
      <div class="col">
      <div class="card" style="width: 18rem;">
        <img src="https://media.rawg.io/media/games/456/456dea5e1c7e3cd07060c14e96612001.jpg" class="card-img-top" alt="...">
        <div class="card-body">
          <h5 class="card-title">Nombre Juego</h5>
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item">Rating 4.48 </li>
          <li class="list-group-item">Released: </li>
          <li class="list-group-item">Updated: </li>
        </ul>
        <div class="card-body">
           <button type="button" class="btn btn-dark">Opinar</button>
        </div>
      </div>
      </div>
      <div class="col">
      <div class="card" style="width: 18rem;">
        <img src="https://media.rawg.io/media/games/456/456dea5e1c7e3cd07060c14e96612001.jpg" class="card-img-top" alt="...">
        <div class="card-body">
          <h5 class="card-title">Nombre Juego</h5>
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item">Rating: </li>
          <li class="list-group-item">Released: </li>
          <li class="list-group-item">Updated: </li>
        </ul>
        <div class="card-body">
           <button type="button" class="btn btn-dark">Opinar</button>
        </div>
      </div>
      </div>
    </div>
  </div>
  <br>
  <div class= "container">
    <div class="row">
    <div class="col">
    <div class="card" style="width: 18rem;">
      <img src="https://media.rawg.io/media/games/456/456dea5e1c7e3cd07060c14e96612001.jpg" class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">Nombre Juego</h5>
      </div>
      <ul class="list-group list-group-flush">
        <li class="list-group-item">Rating: </li>
        <li class="list-group-item">Released: </li>
        <li class="list-group-item">Updated: </li>
      </ul>
      <div class="card-body">
         <button type="button" class="btn btn-dark">Opinar</button>
      </div>
    </div>
    </div>
    <div class="col">
    <div class="card" style="width: 18rem;">
      <img src="https://media.rawg.io/media/games/456/456dea5e1c7e3cd07060c14e96612001.jpg" class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">Nombre Juego</h5>
      </div>
      <ul class="list-group list-group-flush">
        <li class="list-group-item">Rating: </li>
        <li class="list-group-item">Released: </li>
        <li class="list-group-item">Updated: </li>
      </ul>
      <div class="card-body">
         <button type="button" class="btn btn-dark">Opinar</button>
      </div>
    </div>
    </div>
    <div class="col">
    <div class="card" style="width: 18rem;">
      <img src="https://media.rawg.io/media/games/456/456dea5e1c7e3cd07060c14e96612001.jpg" class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">Nombre Juego</h5>
      </div>
      <ul class="list-group list-group-flush">
        <li class="list-group-item">Rating: </li>
        <li class="list-group-item">Released: </li>
        <li class="list-group-item">Updated: </li>
      </ul>
      <div class="card-body">
         <button type="button" class="btn btn-dark">Opinar</button>
      </div>
    </div>
    </div>
  </div>
  </div>
</div>
</template>

<script>
  export default {
    name: 'Principal',
    data(){
    return{
      tituloprincipal: 'Lista de Juegos Disponibles',
      jsonjuego:{},
      mostrar: false,
      error: '',
      }
    },
    props:{
      nombrejuego: String,
    }, //fin props
    created(){
      console.log('Invocando hook created');
      fetch(`https://api.rawg.io/api/pages?key=9cf8b48ffdf14d289549aab8192bec6a&dates`)
        .then( response => response.json() )
            .then( json=>{
                            console.log(json);
                            this.jsonjuego = json;
                            this.mostrar=true;
                            } );
      console.log('fin hook created');
      console.log('jsonjuego')
    },//fin created
  }
</script>

<style scoped>

</style>
