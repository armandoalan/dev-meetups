<template>
  <v-app>
    <v-navigation-drawer absolute temporary v-model="sideNav">
      <v-list>
        <v-list-tile v-for="item in menuItems" 
        :key="item.title"
        router 
        :to= "item.link">
          <v-list-tile-action>
            <v-icon>{{item.icons}}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>{{item.title}}</v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
     <v-toolbar clipped-left dark class="primary" app>
    <v-toolbar-side-icon @click.native.stop= "sideNav = !sideNav" class="hidden-sm-and-up"></v-toolbar-side-icon>
      <v-toolbar-title>
        <router-link to="/" tag="span" style="cursor: pointer">Meetup</router-link>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-xs-only">
          <v-btn flat v-for="item in menuItems" 
          :key="item.title"
          router 
          :to="item.link">
            <v-icon left >{{item.icons}}</v-icon> {{item.title}}
          </v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <main>
      <router-view></router-view>
    </main>
</v-app>
</template>

<script>
  export default {
    data () {
      return {
        sideNav: false,
        menuItems: [
          {icons: 'supervisor_account', title: 'View Meetups', link: '/meetups'},
          {icons: 'room', title: 'Organize Meetups', link: '/meetup/new'},
          {icons: 'person', title: 'Profile', link: '/profile'},
          {icons: 'face', title: 'Sign up', link: '/signin'},
          {icons: 'lock_open', title: 'Sign in', link: '/signup'}
        ]
      }
    }
  }
</script>
