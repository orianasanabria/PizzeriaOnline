<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Pizzería</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNavAltMarkup"
        aria-controls="navbarNavAltMarkup"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <router-link class="nav-link" to="/">Inicio</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/">Inventario</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/">Ventas</router-link>
            </li>
          </ul>
        </div>
      </div>
      <div class="cart-icon"></div>
    </div>
  </nav>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
.cart-icon {
  width: 24px;
  height: 24px;
  line-height: 24px;
  &::before {
    content: "shopping_cart";
    font-family: "Material Icons";
    font-size: 1.5rem;
    color: #fff;
  }
}
</style>
