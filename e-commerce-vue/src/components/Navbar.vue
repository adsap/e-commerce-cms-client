<template>
 <nav class="navbar fixed-top navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid mx-3">
      <a class="navbar-brand ml-2" href="#">E-Commerce CMS</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
          <router-link v-if="$store.state.currentPage === 'add' || $store.state.currentPage === 'edit'"
          class="nav-link" style="color: wheat;" @click.prevent="$store.commit('setPage', 'main')" :to="{ name: 'MainPage' }">
              Main
          </router-link>
          <li v-if="$store.state.currentPage !== 'login'" class="nav-item">
            <a class="nav-link" href="#" style="color: wheat;" @click.prevent="$store.dispatch('logout')">Logout</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {

}
</script>

<style>

</style>
