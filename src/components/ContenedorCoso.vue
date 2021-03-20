<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/img/Bluetooth.png')"
          class="my-3"
          contain
          height="9rem"
        />
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Hola... pelawebo...
        </h1>
      </v-col>
      <v-col cols="12">
        <v-dialog
          v-model="dialog"
          persistent
          max-width="290"
        >
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              color="primary"
              dark
              v-bind="attrs"
              v-on="on"
            >
              Tocame
            </v-btn>
          </template>
          <v-card>
            <v-card-title class="headline">
              Esteban es puto?
            </v-card-title>
            <v-card-text>Si lo es</v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn
                color="green darken-1"
                text
                @click="dialog = false"
              >
                Cerrar
              </v-btn>
              <v-btn
                color="green darken-1"
                text
                @click="dialog=false,loading=true"
              >
                Aceptar
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-col>
      <v-col cols="12">
        <v-progress-linear
          indeterminate
          color="cyan"
          v-show="(this.loading)"
        ></v-progress-linear>
      </v-col>
    </v-row>
    
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data () {
      return {
        dialog: false,
        loading: false
      }
    },
    methods: {
    }
  }
</script>
