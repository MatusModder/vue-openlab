<script>
const data = {
  data() {
    return {
list: [
        {id: 1, label: 'Tesco', items: ['Rozok 5ks','Melon 1ks','Maso 3kg','Voda 2l']},
        {id: 2, label: 'Billa', items: ['Jogurt 8ks','Banan 1kg','Chicken 1.5kg']},
        {id: 3, label: 'Lidl', items: ['Nanuk 5ks','Paprika 1ks','Macbook 5kg','Mydlo 2ks']},
      ],
      clicked: false,
      counter: 0,
      toggle: false
    }
  }
}
export default data
</script>

<template>


  <main>
    <h1>Čúús!</h1>
    <div v-for="item in list" :key="item.id">
      <li>
        {{ item.label }}
          <ul v-for="i in item.items" :key="i">
          {{ i }}
          </ul>
      </li>
    </div>
    <button @click="clicked=true">Openlab je SUPER!!!</button>
    <p v-if="clicked == true">https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwiEsZnL_tL4AhV2SPEDHRqxCckQwqsBegQIBBAB&url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DdQw4w9WgXcQ&usg=AOvVaw0aHtehaphMhOCAkCydRLZU</p>
      <button @click="counter+=1">CPS test</button>
      <p>{{ counter }}</p>
      <button @click="toggle=!toggle">Tajná správa</button>
      <p v-if="toggle==true">Dajte mi hviezdičku na <a href="https://github.com/MatusModder">GitHube!</a></p>
  </main>
</template>

<style>
@import './assets/base.css';

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }

  #app {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 0 2rem;
  }

  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .logo {
    margin: 0 2rem 0 0;
  }
}
</style>
