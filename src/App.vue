<template>
  <div id="app">
    <div id="nav">
      <div class="headerTop">
        <div class="listeMenu">
          <router-link to="/" class="liensNav">
            <img src="./assets/logo.svg" alt="logo twitch" class="logo" />
          </router-link>
          <router-link :to="{name: 'topgames'}" class="liensNav">Top Games.</router-link>
          <router-link :to="{name: 'topstreams'}" class="liensNav">Top Streams</router-link>
          <div class="liensNav">
            <form class="formSubmit">
              <input type="text" class="inputRecherche" />
              <button type="submit">
                <img src="./assets/search.svg" alt="icone loupe" class="logoLoupe" />
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
    <div class="menuResBtn">
      <img src="./assets/menuIco.svg" alt="icone menu" class="menuIco" />
    </div>
    <router-view />
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  color: #000;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

body {
  background-color: #ecf0f1;
}

#app {
  text-align: center;
}

/* 
/////////////////////////
PARTIE HEADER
/////////////////////////
*/
.headerTop {
  background-color: #6441a4;
  height: 50px;
  z-index: 1000;
  width: 100%;
  margin-bottom: 20px;
  /* position: fixed; */
}

#nav a {
  font-weight: bold;
  color: #000;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: #fff;
}

.listeMenu {
  height: 50px;
  display: flex;
  align-items: center;
  width: 100%;
}

.liensNav {
  list-style-type: none;
  padding: 0 20px;
}

.liensNav:nth-child(4) {
  margin: 0 auto;
  flex-shrink: 1;
  width: 600px;
}

/* .lien{

} */

.logo {
  margin-top: 5px;
}

.formSubmit {
  display: flex;
  flex-shrink: 1;
}

.logoLoupe {
  width: 20px;
}

.inputRecherche {
  width: 50%;
  background-color: #fff;
  border: 2px solid #fff;
  border-top-left-radius: 5px;
  border-bottom-left-radius: 5px;
}

.liensNav button {
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  padding: 4px 20px;
  border: none;
}

.menuResBtn {
  display: none;
  position: fixed;
  top: 10px;
  right: 20px;
  color: #fff;
  width: 50px;
  height: 50px;
  cursor: pointer;
}

.menuIco {
  width: 25px;
}
</style>
