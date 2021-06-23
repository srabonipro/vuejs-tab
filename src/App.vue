<template>
<div>
  <h1 class="text-danger">Learning About Dynamic Component</h1> <br>
  <div class="d-flex gap-2 justify-content-center">
    <button @click="activeTab = 'TabA'" class="btn btn-secondary">TabA</button>
    <button @click="activeTab = 'TabB'" class="btn btn-secondary">TabB</button>
    <button @click="activeTab = 'TabC'" class="btn btn-secondary">TabC</button>
  </div>

  <component :is="activeTab"></component>

  <!-- <TabA v-if="activeTab === 'TabA'" />
  <TabB v-if="activeTab === 'TabB'" />
  <TabC v-if="activeTab === 'TabC'" /> -->

</div>
</template>

<script>
import TabA from './components/TabA.vue';
import TabB from './components/TabB.vue';
import TabC from './components/TabC.vue';

export default {
  name: 'App',
  components: {
    TabA,
    TabB,
    TabC,
  },
  data() {
    return {
      activeTab: 'TabA'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.the-card {
    width: 500px;
    border: 1px solid #006f88;
    min-height: 200px;
    margin: 22px auto;
}
.the-card__title {
    background: #167db1;
    padding: 5px 11px;
    color: #fff;
}
.the-card__body {
    padding: 11px;
}
.the-card__body img {
    height: 150px;
}
ul {
    list-style-type: none;
    margin-right: 25px;
}
.the-card__footer {
    background: #e3e3e3;
    padding: 5px 11px;
    text-align: center;
}
</style>
