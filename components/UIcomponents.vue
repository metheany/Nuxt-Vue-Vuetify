<template>
  <div>
    <div>
      <v-app>
        <div>
          Alert
          <v-alert
            :value="true"
            type="success"
          >
            This is a success alert.
          </v-alert>

          <v-alert
            :value="true"
            type="info"
          >
            This is a info alert.
          </v-alert>

          <v-alert
            :value="true"
            type="warning"
          >
            This is a warning alert.
          </v-alert>

          <v-alert
            :value="true"
            type="error"
          >
            This is a error alert.
          </v-alert>
        </div>


        <div>
          Badge

          <div class="text-xs-center">
            <v-badge left>
              <span slot="badge">6</span>
              <v-icon
                large
                color="grey lighten-1"
              >
                shopping_cart
              </v-icon>
            </v-badge>

            <v-badge color="red">
              <span slot="badge">!</span>
              <v-icon
                large
                color="grey"
              >
                mail
              </v-icon>
            </v-badge>
          </div>
        </div>

        <div>
          Bottom nav

          <v-card height="200px" flat>
            <div class="headline text-xs-center pa-5">
              Active: {{ bottomNav }}
            </div>
            <v-bottom-nav
              :active.sync="bottomNav"
              :value="true"
              absolute
              color="transparent"
            >
              <v-btn
                color="teal"
                flat
                value="recent"
              >
                <span>Recent</span>
                <v-icon>history</v-icon>
              </v-btn>

              <v-btn
                color="teal"
                flat
                value="favorites"
              >
                <span>Favorites</span>
                <v-icon>favorite</v-icon>
              </v-btn>

              <v-btn
                color="teal"
                flat
                value="nearby"
              >
                <span>Nearby</span>
                <v-icon>place</v-icon>
              </v-btn>
            </v-bottom-nav>
          </v-card>
        </div>

        <div>
          Bottom sheet
          <div class="text-xs-center">
            <v-bottom-sheet v-model="sheet">
              <v-btn
                slot="activator"
                color="purple"
                dark
              >
                Click me
              </v-btn>

              <v-list>
                <v-subheader>Open in</v-subheader>
                <v-list-tile
                  v-for="tile in tiles"
                  :key="tile.title"
                  @click="sheet = false"
                >
                  <v-list-tile-avatar>
                    <v-avatar size="32px" tile>
                      <img
                        :src="`https://cdn.vuetifyjs.com/images/bottom-sheets/${tile.img}`"
                        :alt="tile.title"
                      >
                    </v-avatar>
                  </v-list-tile-avatar>
                  <v-list-tile-title>{{ tile.title }}</v-list-tile-title>
                </v-list-tile>
              </v-list>
            </v-bottom-sheet>
          </div>
        </div>
      </v-app>
    </div>
  </div>
</template>

<script>
  export default {

    data: () => ({

      sheet: false,
      tiles: [
        { img: 'keep.png', title: 'Keep' },
        { img: 'inbox.png', title: 'Inbox' },
        { img: 'hangouts.png', title: 'Hangouts' },
        { img: 'messenger.png', title: 'Messenger' },
        { img: 'google.png', title: 'Google+' }
      ]
    }),

    // data () {
    //   return {
    //     bottomNav: 'recent'
    //   }
    // }
  }
</script>

<style scoped>

</style>
