<template>
  <v-container fluid>
    <v-row>
      <v-col cols="12" md="6" class="column">
        Esquerdo
        {{$vuetify.breakpoint.lgAndUp}}
      </v-col>
      <v-col 
        md="6"
        class="d-none d-md-flex column"
       
      >
        Direito
        <p>Teste</p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
//{v-if="!$vuetify.breakpoint.smAndDown"}
  export default{
    name: 'LoginPage'
  }
</script>

<style>
.hide-column{
  display: none;
}

.column{
  border: 1px solid blue;
}

</style>
