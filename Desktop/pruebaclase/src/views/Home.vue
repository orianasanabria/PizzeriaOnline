<template>
  <div class="home">
    <div class="container">
      <div class="row">
        <div class="col-12 mt-5">
          <h1><em>Pizzería</em></h1>
        </div>
        <div class="col-12 mt-5">
          <div class="pizza-card">
            <div class="row">
              <div v-for="pizza in pizzas" :key="pizza.name" class="col-4 mb-5">
                <div class="card h-100">
                  <img :src="pizza.img" class="card-img-top" alt="" />
                  <div class="card-body">
                    <h5 class="card-title text-capitalize">
                      <strong>Pizza {{ pizza.name }}</strong>
                    </h5>

                    <p class="card-text">
                      {{ pizza.desc }}
                    </p>
                    <ul class="list-group list-group-flush">
                      <li
                        v-for="(ing, i) in pizza.ing"
                        :key="i"
                        class="list-group-item text-capitalize"
                      >
                        {{ ing.name }}
                      </li>
                    </ul>
                    <hr />
                    <p class="text-center mb-3">
                      <strong>Precio: ${{ pizza.price }}</strong>
                    </p>

                    <div class="row">
                      <div class="col-6">
                        <input
                          v-model="cantidad"
                          class="w-100 h-100"
                          type="text"
                        />
                      </div>
                      <div class="col-6">
                        <a href="#" class="btn btn-primary ms-3 w-75"
                          >Agregar</a
                        >
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapActions, mapState } from "vuex";
export default {
  name: "Home",
  data() {
    return {
      cantidad: "",
    };
  },
  methods: {
    ...mapActions(["getData"]),
  },
  computed: {
    get: function () {
      return "Algo";
    },
    set: function (v) {
      return console.log(v);
    },
    ...mapState(["pizzas"]),
  },
  created() {
    this.getData();
  },
};
</script>

<style></style>
