<template>
  <v-card>
    <v-card-title>Defi Settings</v-card-title>
    <v-card-text>
      <h3>Active Defi modules</h3>
      <p class="text--secondary">
        Only data for the selected modules will be queried. If no modules are
        selected, querying for all the supported modules will be disabled.
      </p>
      <defi-module-selector />
      <h3 class="mt-6">Selected accounts</h3>
      <p class="text--secondary">
        If no accounts are selected for a protocol, data for all accounts will
        be queried for that protocol.
      </p>
      <defi-address-selector />
    </v-card-text>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import DefiAddressSelector from '@/components/defi/wizard/DefiAddressSelector.vue';
import DefiModuleSelector from '@/components/defi/wizard/DefiModuleSelector.vue';

@Component({
  components: { DefiAddressSelector, DefiModuleSelector }
})
export default class DefiSettings extends Vue {}
</script>

<style scoped></style>
