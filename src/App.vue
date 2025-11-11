<template>
  <nav>
    <router-link to="/">Home </router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/gallery">Gallery</router-link>
  </nav>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

@media (max-width: 780px) {
  .packages-details-item {
    width: 40% !important;
  }

  .packages-details a {
    width: 30% !important;
  }

  .packages img {
    width: 20% !important;
  }

  .checkout-con {
    flex-direction: column !important;
    align-items: center !important;
  }

  .item-selected {
    width: 84% !important;
    margin-bottom: 15px;
    margin-top: 10px;
  }

  .cart,
  .item-selected {
    height: 300px !important;
  }

  .cart {
    width: 100% !important;
  }
}

.main {
  padding: 10px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000;
  width: 100%;
  height: 100%;
}

body,
html {
  height: 100% !important;
  width: 100% !important;
  background-color: #000;
}

nav {
  padding: 30px;
  background: linear-gradient(90deg, #8d7ecf, #cd47da);
}

nav a {
  font-weight: 700;
  color: #fff;
}

nav a.router-link-exact-active {
  color: #000;
}

.item-con {
  display: flex;
  justify-content: space-evenly;
}

.item {
  border: 1px solid;
  width: 15%;
}

.slide-con {
  display: flex;
}

.slide-image {
  width: 20%;
  margin: 20px;
}

.slide-image img {
  width: 100%;
}

.packages,
.packages:nth-child(2n) {
  color: #fff;
}

.packages {
  display: flex;
  padding: 10px;
  height: 260px;
  border-bottom: 1px solid #cd47da;
}

.packages img {
  width: 15%;
}

.packages-details {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
}

.packages-details a {
  text-decoration: none;
  color: #fff;
  width: 8%;
  margin-left: 20px;
}

.packages-details-item {
  width: 11%;
}

.packages-details button {
  align-self: flex-end;
  background: linear-gradient(90deg, #8d7ecf, #a96bd9, #cd47da);
  border: 1px solid #fff;
  width: 100%;
  border-radius: 22px;
  margin-left: 10px;
}

.packages-details button:nth-child(2n) {
  background-color: #2b2d2b;
  color: #fff;
}

.btn {
  border: 1px solid #000 !important;
}

h3[data-v-ebbc34ee] {
  margin: 40px 0 0;
}

ul[data-v-ebbc34ee] {
  list-style-type: none;
  padding: 0;
}

li[data-v-ebbc34ee] {
  display: inline-block;
  margin: 0 10px;
}

a[data-v-ebbc34ee] {
  color: #42b983;
}

.header {
  margin: 20px 0 20px;
}

.g-con {
  height: 100%;
}

.container {
  color: #fff;
}

.gallery-con {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

.gallery-con img {
  margin: 5px;
  width: 20%;
}

.gallery-con img:hover {
  width: 25%;
  border: 2px solid #a96bd9;
}

@media (max-width: 780px) {
  .gallery-con {
    height: 100%;
  }

  .gallery-con img {
    width: 45%;
  }

  .gallery-con img:hover {
    width: 47%;
  }
}
</style>
