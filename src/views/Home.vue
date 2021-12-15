<template>
  <div id="app" class="container">
    <h1>{{name}}</h1>
    <ul>
      <li v-for="recipe in recipes" :key="recipe.name">
        <ul>
          <li v-for="ingredient in recipe.ingredients" :key="ingredient">
            {{ingredient}}
          </li>

          <li v-for="step in recipe.steps" :key="step">
            {{step}}
          </li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Home",
  mounted() {

  },
  data() {
    return {
     name:'recipes',
     recipes: [
       {
         'name': 'Mjúk piparkaka',
         'ingredients': [
          '200 gr Naturli smjörlíki við stofuhita',
          '2 dl sykur',
          '6 dl hveiti',
          '2 tsk lyftiduft',
          '1,5 tsk matarsódi', 
          '1 msk kanill',
          '2 tsk engiferkrydd',
          '2 tsk negull',
          'Örlítið salt',
          '6 dl vegan mjólk',
          '2 tsk vanilludropar',
          '1 msk eplaedik',
          '2 msk týtuberjasulta'
         ],
         'steps': [
           'Hitið ofninn í 175°C. Minn er ekki með blæstri svo ég set á undir og yfir hita.',
           'Þeytið smjörlíkið og sykurinn í stórri skál þar til það verður létt og svolítið ljóst.',
           'Sigtið út í skálina hveiti, lyftiduft, matarsóda, salt og kryddin.',
           'Hellið útí mjólk, vanilludropum og eplaediki og hrærið þar til deigið er laust við kekki.',
           'Bætið sultunni útí og blandið varlega saman við deigið.',
           'Smyrjið tvö smelluform og skiptið deiginu í þau.',
           'Bakið í 40-60 mínútur. Það fer svolítið eftir ofninum hversu lengi kakan er að bakast en ég byrja að fylgast með henni eftir sirka hálftíma.',
           'Látið botnana kólna áður en þið setjið kremið á.'
         ]
       }
     ]
    };
  },
  methods: {
    
  },
  created: function () {

  },
};
</script>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 100%;
  grid-template-rows: 80px auto 50px;
}

.item {
  /* border:1px solid black; */
}
/* img {
  display: block;
  margin: auto;
  width: 20rem;
} */

.movieInfo {
  grid-row: 2;
  grid-column: 1;
  display: grid;
  grid-template-columns: 3fr auto;
  grid-template-rows: 25% 25% 25% 25%;
  /* border:1px solid white; */
  /* margin: auto;
  max-width:90%;
  min-height: 300px; */
  /* border: 1px solid black; */
  /* background: lightcoral; */
  /* border: 5px solid red; */
}

form {
  margin-top: 1rem;
}

input {
  width: 70%;
  height: 2rem;
  margin-top: 0.5rem;
  margin-bottom: 1rem;
}

ul {
  padding-top: 1rem;
  font-size: 1.5rem;
  text-align: left;
}

ul > li:nth-child(even) {
  color: grey;
}

ul button {
  margin: 0 10px;
}

ul a {
  margin: 0 10px;
}

ul a:hover {
  /* display:none; */
}
.poster {
  grid-template-columns: 1;
  grid-row: 1/4;
  /* float:left;
border: 5px solid red; */
  /* width:50px; */
}

.poster img {
  max-width: 200px;
}

.movieInfo .text {
  /* grid-column:2; */
}
.movieInfo .movie-title {
  grid-row: 1;
  grid-column: 2;
  align-self: top;
  margin-top: 5px;
  margin-bottom: 5px;
  /* border: 1px solid white; */
}

.movieInfo .genre {
  margin-top: 0;
  margin-bottom: 10px;
  font-style: italic;
  color: darkgray;
}

.movieInfo .plot {
  font-size: 0.9rem;
  margin: 0 15px;
  text-align: left;
  /* text-justify: inter-word; */
}

.movieInfo .year {
  margin: 0 0 10px 0;
}

.search-box {
  grid-row: 4;
}

.header {
  grid-row: 1;
  align-self: top;
}
</style>
