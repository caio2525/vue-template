<template>
  <v-app>
    
    <v-app-bar app>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-toolbar-title>Nav Bar</v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer 
      v-if="!$vuetify.breakpoint.mdAndUp" 
      app  
      temporary 
      v-model="isOpen"
    >
      <template #prepend>
        <h2>Teste Prepend</h2>
      </template>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6">
            Application
          </v-list-item-title>
          <v-list-item-subtitle>
            subtext
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
      
    </v-navigation-drawer>

    <v-navigation-drawer 
      v-if="$vuetify.breakpoint.mdAndUp" 
      app  
      permanent 
      v-model="permanent"
    >
      
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6">
            Application
          </v-list-item-title>
          <v-list-item-subtitle>
            subtext
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
      <template #prepend>
        <header class="prepend-header">
          <v-toolbar-content class="prepend-header-content">Prepend</v-toolbar-content>
        </header>
        
      </template>
    </v-navigation-drawer>


    <v-main>
      <v-button @click="toggle">Drawer</v-button>
      {{isOpen}}
      <Nuxt />
    </v-main>

  </v-app>
</template>

<script>
//$vuetify.breakpoint.lgAndUp
  export default{
    data(){
      return({
        isOpen: false,
        permanent: true,
      })
    },
    methods:{
      toggle(){
        this.isOpen = true
      }
    },
    computed:{
      
    }
  }
</script>

<style>
.drawer-class{
  background-color: brown;
}

.prepend-header{
  height: 64px;
  border: 1px solid black;
}

.prepend-header-content{
  height: 64px;
}
</style>
