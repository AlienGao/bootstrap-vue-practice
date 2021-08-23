<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand href="#">
        <img src="https://placekitten.com/g/30/30" alt="Kitten">
      </b-navbar-brand>
      <b-nav-form class="mx-auto">
        <b-input-group size="sm">
          <b-form-input placeholder="Search"></b-form-input>
          <b-input-group-append is-text>
            <b-icon icon="search"></b-icon>
          </b-input-group-append>
        </b-input-group>
      </b-nav-form>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-navbar-nav>
            <b-nav-item href="#">Link</b-nav-item>
            <b-nav-item href="#">Disabled</b-nav-item>
          </b-navbar-nav>

          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown right>
            <!-- Using 'button-content' slot -->
            <template v-slot:button-content>
              <em>User</em>
            </template>
            <b-dropdown-item href="#">Profile</b-dropdown-item>
            <b-dropdown-item href="#">Sign Out</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <div class="d-none d-lg-block">小于lg屏幕时隐藏</div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
      }
    },
    methods: {
    }
  }
</script>

<style scoped>
</style>