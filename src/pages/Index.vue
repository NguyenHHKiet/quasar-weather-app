<template>
  <q-page class="flex column">
    <div class="col q-pt-lg q-px-md">
      <q-input v-model="search" aria-placeholder="Search" dark borderless>
        <template v-slot:before>
          <q-icon name="event" />
        </template>

        <template v-slot:append>
          <q-btn round dense flat icon="search" />
        </template>
      </q-input>
    </div>

    <template v-if="weatherData">
      <div class="col text-white text-center">
        <div class="text-h4 text-weight-light">
          Manchester
        </div>
        <div class="text-h6 text-weight-light">
          Rain
        </div>
        <div class="text-h1 text-weight-thin q-my-lg relative-position">
          <span>8</span>
          <span class="text-h4 relative-position degree">&deg;</span>
        </div>
      </div>

      <div class="col text-center">
        <img src="https://cdn.pixabay.com/photo/2020/09/27/03/38/woman-5605529_640.jpg" alt="Bill" />
      </div>
    </template>
    <template v-else>
      <div class="col column text-center text-white">
        <div class="col text-h2 text-weight-thin">Quasar<br />Weather</div>
        <q-btn color="teal">
          <q-icon left size="3em" name="map" />
          <div>Find my location</div>
        </q-btn>
      </div>
    </template>

    <div class="col skyline"></div>
  </q-page>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'PageIndex',
  components: {},
  data() {
    return {
      search: '',
      weatherData: null
    }
  }
});

</script>

<style lang="scss">
.q-page {
  background: linear-gradient(to bottom, #136aBa, #267871);
}

.degree {
  top: -44px;
}

.skyline {
  flex: 0 0 100px;
  background: url(../assets/sklyline.png);
  background-size: contain;
  background-position: center bottom;
}
</style>
