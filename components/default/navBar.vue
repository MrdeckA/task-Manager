<template>
  <div>
    <nav>
      <div class="heading">
        <svg
          class="text-secondary"
          xmlns="http://www.w3.org/2000/svg"
          width="3em"
          height="2em"
          viewBox="0 0 576 512"
        >
          <!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
          <path
            d="M287.9 0C297.1 0 305.5 5.25 309.5 13.52L378.1 154.8L531.4 177.5C540.4 178.8 547.8 185.1 550.7 193.7C553.5 202.4 551.2 211.9 544.8 218.2L433.6 328.4L459.9 483.9C461.4 492.9 457.7 502.1 450.2 507.4C442.8 512.7 432.1 513.4 424.9 509.1L287.9 435.9L150.1 509.1C142.9 513.4 133.1 512.7 125.6 507.4C118.2 502.1 114.5 492.9 115.1 483.9L142.2 328.4L31.11 218.2C24.65 211.9 22.36 202.4 25.2 193.7C28.03 185.1 35.5 178.8 44.49 177.5L197.7 154.8L266.3 13.52C270.4 5.249 278.7 0 287.9 0L287.9 0zM287.9 78.95L235.4 187.2C231.9 194.3 225.1 199.3 217.3 200.5L98.98 217.9L184.9 303C190.4 308.5 192.9 316.4 191.6 324.1L171.4 443.7L276.6 387.5C283.7 383.7 292.2 383.7 299.2 387.5L404.4 443.7L384.2 324.1C382.9 316.4 385.5 308.5 391 303L476.9 217.9L358.6 200.5C350.7 199.3 343.9 194.3 340.5 187.2L287.9 78.95z"
          />
        </svg>
        <h1 class="h2">TAMANA</h1>
      </div>
      <svg
        id="hamburger"
        class="hamburger"
        xmlns="http://www.w3.org/2000/svg"
        height="50px"
        viewBox="0 0 24 24"
        width="40px"
        fill="#000000"
      >
        <path d="M0 0h24v24H0z" fill="none" />
        <path d="M3 18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z" />
      </svg>

      <ul id="items" class="tabs">
        <li class="tab simpleLink"><a href="#" class="link">Accueil</a></li>
        <li class="tab simpleLink"><a href="#" class="link">A Propos</a></li>
        <li class="tab">
          <a href="#" class="link"
            ><v-btn class="bg-danger text-white">Connexion</v-btn></a
          >
        </li>
        <li class="tab">
          <a href="#" class="link"
            ><v-btn class="bg-primary text-white">Inscription</v-btn></a
          >
        </li>
      </ul>
    </nav>
  </div>
</template>
<script>
export default {
  mounted() {
    const hamburger = document.getElementById('hamburger')
    const items=document.getElementById('items')
    hamburger.addEventListener('click', () => {
      items.classList.toggle('displayed')      
    })
  },
}
</script>
<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 2em;
  height: 5em;
  z-index: 1;
}

.heading {
  display: flex;
}

.tabs {
  list-style-type: none;
  display: flex;
  align-items: center;
}

.tab {
  margin-left: 2em;
}
.simpleLink {
  text-decoration: none;
  color: black;
}
.simpleLink :hover {
  background-color: red !important;
  color: white;
  padding: 0.5em 1.5em;
  text-decoration: none;
  border-radius: 2em;
  font-weight: bold;
}
.hamburger {
  display: none;
}
@media screen and (max-width: 800px) {
  nav{
    margin: 0 1em;
  }
  .tabs {
    position: absolute;
    top: 5em;
    left: 0;
    width: 100%;
    height: calc(100vh - 5em);
    background-color: rgb(215, 234, 255);
    align-content: center;
    justify-content: center;
    justify-items: center;
    align-items: center;
    
  }
  .hamburger {
    display: block;
  }

  .nav {
    margin: 0;
    padding: 0;
  }
  .tabs {
    display: flex;
    flex-direction: column;
    margin-left: -100%;
    padding-bottom: 10em;
    transition: all 0.5s ease;
  }
  .tab {
    margin: 2em 0;
  }
  .displayed {
    margin-left: 0;
    transition: all 0.5s ease;
  }
}
</style>