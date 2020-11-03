<template>
  <q-layout view="lHh Lpr lFf">
    <q-header bordered class="bg-white">
      <q-toolbar class="constrain">
        <q-btn
          flat
          round
          dense
          class="large-screen-only q-mr-sm"
          size="18px"
          to="/camera"
          color="grey-10"
          icon="camera"
        />
        <q-separator class="large-screen-only" vertical spaced />
        <q-toolbar-title class="text-grey-10 font-grand-hotel text-bold">
          Quasargram
        </q-toolbar-title>
        <q-btn
          flat
          round
          dense
          class="large-screen-only"
          size="18px"
          to="/"
          color="grey-10"
          icon="home"
        />
      </q-toolbar>
    </q-header>
    <q-footer bordered class="bg-white text-grey-10 small-screen-only" elevated>
      <q-tabs
        active-color="primary"
        indicator-color="transparent"
        class="text-grey-8"
      >
        <q-route-tab to="/" name="dashboard" icon="dashboard" />
        <q-route-tab to="/camera" name="camera" icon="camera" />
      </q-tabs>
    </q-footer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style lang="sass" scoped>
.q-toolbar
  @media (min-width: $breakpoint-sm-min)
    height: 77px
.q-toolbar__title
  font-size: 30px
  @media (max-width: $breakpoint-xs-max)
    text-align: center
</style>