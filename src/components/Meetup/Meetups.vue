<template>
 <v-container>
   <v-layout row wrap>
     <v-flex xs12 sm10 md8 offset-sm1 offset-md2>
       <v-card class="info">
         <v-container fluid>
           <v-layout row wrap>
             <v-flex xs5 sm4 md3>
               <v-card-media 
               src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/52/New_York_Midtown_Skyline_at_night_-_Jan_2006_edit1.jpg/800px-New_York_Midtown_Skyline_at_night_-_Jan_2006_edit1.jpg1"
               height="130px"
               ></v-card-media>
             </v-flex>
             <v-flex xs7 sm8 md9>
               <v-card-title primaty-title>
                 <div>
                  <h5 class="white--text mb-0">My meetup</h5>
                  <div>17th july 9 Pm</div>
                </div>
               </v-card-title>
               <v-card-actions>
                 <v-btn flat to="/meetups/1">
                   <v-icon left light>arrow_forward</v-icon>
                   View Meetup</v-btn>
               </v-card-actions>
             </v-flex>
           </v-layout>
         </v-container>
       </v-card>
     </v-flex>
   </v-layout>
 </v-container>
</template>
