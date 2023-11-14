<template>
  <v-container fluid>
    <v-card>
      <v-card-title>Settings</v-card-title>
      <v-card-text>
        <v-form>
          <v-row>
            <v-col cols="12" md="2">
              <v-text-field
                :counter="10"
                label="aerender binary path"
                required
                hide-details
                variant="underlined"
                :disabled="loading"
              />
            </v-col>
            <v-col cols="12" md="2">
              <v-text-field
                :counter="10"
                label="output path"
                required
                hide-details
                variant="underlined"
                :disabled="loading"
              />
            </v-col>
            <v-col cols="12" md="2">
              <v-btn
                :loading="loading"
                :disabled="loading"
                @click="save"
                color="primary"
                prepend-icon="mdi-send"
                class="flex-grow-1"
              >
                Submit
              </v-btn>
            </v-col>
          </v-row>
        </v-form>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
// import { ipcRenderer } from 'electron';

export default {
  data: () => ({
    loading: false,
  }),
  methods: {
    save() {
      this.loading = true;
      setTimeout(() => (this.loading = false), 3000);
    },
  },
};
</script>