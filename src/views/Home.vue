<template>
  <div class="d-flex flex-column  align-items-center">
    <div class="col-2">
      <img src="https://cdn-icons-png.flaticon.com/512/25/25231.png" alt="logo github" class="img-fluid">
    </div>
    <h1 class="m-4">Bienvenue sur mon Portfolio GitHub</h1>
    <p class="h1">Yvan Brai.</p>
    <div class="container m-4 text-center">
      <p>Etudiant à l'école #Webstart, en developpement web et application mobile depuis 2019.</p>
      <p>Voici le Portfolio de mes projet GitHub, réaliser en Vue JS3, Vue Router, Vue X, et Apollov4 / Graph-QL</p>
      <img src="https://www.cidj.com/sites/default/files/styles/full_offre/public/2020-01/LOGO-e%CC%81cole-webstart.png?itok=YhMS1Kl2" alt="logo  webstart">
    </div>
    <div class="container m-4 text-center">
      <p>Apollo: {{req}}</p>
    </div>
  </div>
</template>

<script>
import gql from 'graphql-tag'

export default {
  apollo: {
    req: gql`
      query {
        viewer {
          name
          repositories(last: 10) {
            nodes {
              name
            }
          }
        }
      }
    `,
  },
  
  name: 'HomeComponent',
}
</script>

<style scoped>

</style>
