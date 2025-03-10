<template>
  <div id="app">
    <header>
      <img src="data:image/png;base64,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" alt="LOGO"> 
      <h1>Les Bonnes Pièces</h1>
    </header>
    <main>
      <!-- Menu de recherche -->
      <section class="filtres">
        <input v-model="searchQuery" placeholder="Rechercher une pièce..." />
      </section>
      <!-- Category Filter -->
    <select v-model="selectedCategory">
      <option value="">Toutes catégories</option>
      <option value="Freinage">Freinage</option>
      <option value="Moteur">Moteur</option>
    </select>
    <select v-model="selectedDisponible">
      <option value="">Tous</option>
      <option :value="true">Disponible</option>
      <option :value="false">Rupture</option>
    </select>
    <div>
      <button @click="sortOrder = 'asc'">Prix croissant</button>
      <button @click="sortOrder = 'desc'">Prix décroissant</button>
    </div>

      <!-- Table Header -->
      <div class="product-header">
        <div>Nom</div>
        <div>Prix</div>
        <div>Catégorie</div>
        <div>Disponibilité</div>
      </div>

      <!-- Product Cards -->
      <section v-for="p in filteredParts" :key="p.id" class="product-card">
        <div>{{ p.nom }}</div>
        <div>{{ p.prix }} €</div>
        <div>{{ p.categorie }}</div>
        <div>{{ p.disponible ? 'Disponible' : 'Rupture' }}</div>
        <button @click="addToCart(p)" v-if="p.disponible">Ajouter au panier</button>
        <img :src="p.image">
      </section>
    <div class="panier-container">
      <h2>Panier</h2>
      <ul>
        <li v-for="item in panier" :key="item.id">{{ item.nom }} - {{ item.prix }}€</li>
      </ul>
    </div>
      </main>
  </div>
</template>


<script>
export default {
  
  data() {
    return {
      panier : [],
      pieces: [],
      nom:'',
      prix:'',
      categorie:'',
      image:'',
      disponible : true,
      searchQuery : '',
      selectedCategory : '',
      selectedDisponible: '',
      sortOrder: "asc", // Sorting order
    };
  },
  methods : {
    recuperer() {
      fetch('/data/pieces-autos.json')
        .then(response => response.json())
        .then(data => {
          this.pieces = data;
        })
    },
    addToCart(part){
      this.panier.push(part);
      //si on suppose qu'on a un exemplaire de chaque element 
      //et on veut qu'il ne soit plus disponnible si il est ajouter au panier
      //on ajoute
      //part.disponible = false;
    }
  },
  computed : {
    filteredParts() {
      let filtered = this.pieces;
      if(this.searchQuery){
        filtered = filtered.filter(part =>
          part.nom.toLowerCase().includes(this.searchQuery.toLowerCase())
        );
      }
      if(this.selectedCategory){
        filtered = filtered.filter(part => 
          part.categorie === this.selectedCategory
        );
      }
      if(this.selectedDisponible !== ""){
        filtered = filtered.filter(part => 
          part.disponible === this.selectedDisponible
        );
      }
      if (this.sortOrder === "asc") {
        filtered.sort((a, b) => a.prix - b.prix);
      } else {
        filtered.sort((a, b) => b.prix - a.prix);
      }
      return filtered;
    }
  },
  mounted() {
    this.recuperer();
  }
}
</script>

<style>
/* General Styles */
body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f9;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Main Container */
#app {
  width: 80%;
  max-width: 1200px;
  background: white;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  padding: 20px;
  margin-top: 20px;
  position: relative;
}

/* Header */
header {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 15px;
  padding: 20px;
  background: #2c3e50;
  color: white;
  border-radius: 8px;
}

header img {
  width: 50px;
  height: 50px;
}

header h1 {
  font-size: 1.8em;
}

/* Filters */
.filtres {
  margin-bottom: 15px;
}

input, select, button {
  padding: 8px;
  margin: 5px;
  border-radius: 5px;
  border: 1px solid #ccc;
  font-size: 1em;
}

button {
  background-color: #3498db;
  color: white;
  border: none;
  cursor: pointer;
}

button:hover {
  background-color: #2980b9;
}

/* Product Table Header */
.product-header {
  display: flex;
  justify-content: space-around;
  font-weight: bold;
  padding: 10px;
  background: #ecf0f1;
  border-radius: 5px;
  margin-bottom: 10px;
}

/* Product Cards */
.product-card {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 10px;
  margin: 5px 0;
  background: white;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 5px;
}

.product-card img {
  width: 60px;
  height: 60px;
  border-radius: 5px;
}

.product-card button {
  background: #2ecc71;
}

.product-card button:hover {
  background: #27ae60;
}

/* Fixed Cart (Panier) */
.panier-container {
  position: fixed;
  top: 20px;
  right: 20px;
  background: white;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  padding: 15px;
  width: 250px;
  max-height: 300px;
  overflow-y: auto;
}

.panier-container h2 {
  margin: 0 0 10px;
  font-size: 1.4em;
  text-align: center;
}

.panier-container ul {
  list-style: none;
  padding: 0;
}

.panier-container li {
  background: #ecf0f1;
  padding: 8px;
  margin: 5px 0;
  border-radius: 5px;
  font-size: 0.9em;
}

</style>