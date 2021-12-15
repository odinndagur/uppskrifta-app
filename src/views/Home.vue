<template>
  <div id="app" class="container">
    {{recipes}}
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
