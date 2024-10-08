<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">

import Vue from 'vue';


export default Vue.extend({
  name: 'MainLayout',
  components: {  },
  data() {
    return {
      leftDrawerOpen: false,
    }
  }
});

</script>
