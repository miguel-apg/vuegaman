<template>
  <v-card ripple dark tile color="primary">
    <v-parallax :src="callout.background.data.full_url">
      <v-row align="center" justify="center">
        <v-col cols="11">
          <v-row align="center" justify="center">
            <v-col cols="12" sm="5" md="4">
              <v-card flat color="transparent">
                <span v-html="callout.callout" />
              </v-card>
            </v-col>
            <v-col cols="12" md="6" v-if="callout.image">
              <v-img contain height="300" :src="callout.image.data.full_url" />
            </v-col>
          </v-row>
        </v-col>
        <v-col> </v-col>
      </v-row>
    </v-parallax>
  </v-card>
</template>

<script>
export default {
  props: {
    callout: {
      name: {
        type: String,
        required: false
      },
      callout: {
        type: String,
        required: false
      },
      image: {
        data: {
          full_url: {
            type: String,
            required: false
          }
        }
      },
      background: {
        data: {
          full_url: {
            type: String,
            required: false
          }
        }
      }
    }
  }
};
</script>

<style></style>
