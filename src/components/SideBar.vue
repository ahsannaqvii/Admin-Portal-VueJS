<template>
  <v-app id="inspire">
    <v-main class="grey lighten-3">
      <v-container>
        <v-row>
          <v-col cols="2">
            <v-sheet rounded="lg"  min-height="100vh">
              <v-list color="transparent">
                <v-list-item
                  v-for="[icon, link] in links" :key="icon"
                  link
                >
                 <v-list-item-icon>
          <v-icon>{{ icon }}</v-icon>
        </v-list-item-icon>
                  <v-list-item-content>
                    <v-list-item-title>
                      {{ link }}
                    </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>

                <v-divider class="my-2"></v-divider>

                <v-list-item
                  link
                  color="grey lighten-4"
                >
                  <v-list-item-content>
                    <v-list-item-title>
                      Refresh
                    </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-sheet>
          </v-col>

          <router-view></router-view>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
  export default {  
    name:"SideBar",
    data: () => ({
      links:[["mdi-microsoft-windows", "Dashboard"],
        ["mdi-account", "Profile"],
        ["mdi-clipboard-list-outline", "Products"],
        ["mdi-card-account-details-outline", "Orders"],
        ["mdi-cog", "System Setting"],
    ]}),
  }
</script>