<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-white text-grey-10" bordered>
      <q-toolbar class="constrain">
        <q-btn
          class="large-screen-only q-mr-sm"
          to="/camera"
          dense
          flat
          round
          size="18px"
          icon="eva-camera-outline"
        />
        <q-separator vertical spaced class="large-screen-only" />
        <q-toolbar-title class="text-grand-hotel text-bold">
          Quasagram
        </q-toolbar-title>
        <q-btn
          class="large-screen-only"
          to="/"
          dense
          flat
          round
          size="18px"
          icon="eva-home-outline"
        />
      </q-toolbar>
    </q-header>
    <q-footer class=" small-screen-only bg-white" bordered>
      <q-tabs
        indicator-color="transparent"
        class="text-grey-10"
        active-color="primary"
      >
        <!-- ctrl alt shift a -->
        <q-route-tab to="/" icon="eva-home-outline" />
        <!-- label="Home" -->

        <q-route-tab to="/camera" icon="eva-camera-outline" />
      </q-tabs>
    </q-footer>
    <q-page-container class="bg-grey-1">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: "MainLayout",
  components: {},
  data() {
    return {};
  }
};
</script>

<style lang="sass">
.q-toolbar
  @media (min-width:$breakpoint-sm-min)
      height: 77px


.q-toolbar__title
  font-size: 30px
  @media (max-width:$breakpoint-xs-max)
      text-align: center

.q-footer
  .q-tab__icon
    font-size: 30px
</style>
