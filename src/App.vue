<template>
  <div>

    <app-alert
      v-if="alert"
      title="Внимание!"
      text="Это действие запрещено для данной страницы. Закройте её немедленно!"
      type="danger"
      :closable="true"
      @close="alert = false"
    ></app-alert>

    <div class="card">
      <button class="btn primary" @click="toggleAlert">
        {{ alert ? 'Скрыть сообщение' : 'Показать сообщение' }}
      </button>
    </div>

  </div>
</template>

<script>

import AppAlert from "./components/AppAlert.vue";

export default {
  data() {
    return {
      alert: false
    }
  },
  methods: {
    toggleAlert() {
      this.alert = !this.alert
    }
  },
  components: {
    AppAlert
  }, 
};
</script>

<style>
  
</style>
