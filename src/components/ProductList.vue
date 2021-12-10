<template>
<div id="pd_list" class="row">
    <div class="card" 
    style="width: 15rem;"
     v-for="item in products" :key="item.id">

  <img :src="item.imgUrl" 
  class="card-img-top" 
  :alt="item.title">

  <div class="card-body">
    <p class="card-title">{{item.title}}</p>
    <p class="card-text">Rp. {{item.price}}</p>
    <a href="#" class="btn btn-primary">Go Add</a>
  </div>
</div>
</div>
</template>

<script>
import products from "../mock/products.json";

export default {
    name: "ProductList",
    data(){
        return{
            products,
        }
    }
};
</script>

<style>
#pd_list{
    font-family: sans-serif;
    text-align: center;
    color: #2c3e50;
}
.card{
    border: none;
}

</style>