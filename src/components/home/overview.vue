<template>
  <v-container fluid class="google-font">
    <v-row justify="center" align="center" class="px-2">
      <v-col
        md="12"
        class="pa-md-10 pa-5"
        style="background-color: white; border-radius: 15px"
      >
        <p
          class="google-font gdg-h1 mb-2 grey--text text--darken-4"
          style="font-size: 220%"
        >
          What to Expect
        </p>
        <p>
          An annual event hosted by the Google Developers Group across the world
          to bring the technology closer to the developers. It is an all day
          developer conference where we aim to focus on multiple technologies
          through lightning talks, sessions, workshops, etc.
        </p>
        <v-container fluid class="px-0">
          <v-row>
            <v-col
              md="4"
              sm="4"
              cols="12"
              v-for="(item, index) in IWDInfo.what_to_expect"
              :key="index"
            >
              <div
                class="pa-md-6 pa-4"
                style="background-color: #e8f1fb; border-radius: 12px"
              >
                <p style="font-size: 20px; font-weight: 600" class="mt-4">
                  {{ item.label }}
                </p>
                <p>{{ item.value }}</p>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import IWDJSON from '@/assets/data/IWDs.json';
export default {
  name: 'OverviewComponent',
  data: () => ({
    IWDInfo: IWDJSON,
  }),
};
</script>

<style></style>
