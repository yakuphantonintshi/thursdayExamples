<template>
  <div class="container">
  <div class="row">
    <UserDetail firstName="Yakupha" lastName="Ntonintshi" age=21 gender="female"/>

  </div>
  <div class="row">
    <h2>App component</h2>
  </div>
  <div class="row gap-2">
    <Card v-for="(friend, index) in friends" :key="index">
      <template #cardHeader>
        <img :src="img-fluid" :alt="friend.firstName" loading="lazy">

      </template>
      <template #cardBody>
        <p>{{ friend.firstName }} {{ friend.lastName }}</p>

      </template>

    </Card>
  </div>
</div>

</template>

<script>
import UserDetail from '@/components/UserDetail.vue'
import Card from '@/components/Card.vue'

export default {
  name: 'App',
  components: {
    UserDetail,
    Card
  },
  data(){
    return{
      friends: [
        {
          firstName: "Yakupha",
          lastName: "Ntonintshi",
          profile: 'https://yakuphantonintshi.github.io/myimages/Images/my_picture2.jpg'
        },
        {
          firstName: "Simanye",
          lastName: "Somdaka",
          profile: 'https://yakuphantonintshi.github.io/myimages/Images/simanye.jpg'
        },
        {
          firstName: "Khanya",
          lastName: "Pupuma",
          profile: 'https://yakuphantonintshi.github.io/myimages/Images/Khanya.jpg'
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
