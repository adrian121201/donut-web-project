<template>
  <v-app dark>
   
    <v-app-bar fixed app class="elevation-0" height="auto" style="padding-top: 15px; padding-bottom: 15px;">

       
      <v-toolbar-title style="font-family: 'Titan One', sans-serif; color: #612009;"> DONUT DISTURB  <v-icon style="font-size: 45px;" color="#612009">mdi-chart-donut-variant</v-icon></v-toolbar-title>

      <v-spacer />


      <router-link to="/">
        <v-btn text class="hidden-sm-and-down" style="font-family: Arial, Helvetica, sans-serif; color: #612009;">
        HOME
        </v-btn>
      </router-link>
      
      <v-btn text class="hidden-sm-and-down" style="font-family: Arial, Helvetica, sans-serif; color: #612009;" @click="scrollToSection('#our-story')">
        OUR STORY
      </v-btn>

      <router-link to="/products">
        <v-btn text class="hidden-sm-and-down" style="font-family: Arial, Helvetica, sans-serif; color: #612009;">
        OUR PRODUCTS
        </v-btn>
      </router-link>
      

      <v-btn text class="hidden-sm-and-down" style="font-family: Arial, Helvetica, sans-serif; color: #612009;" @click="scrollToSection('#contact-us')">
        CONTACT US
      </v-btn>
       
      <v-btn icon class="hidden-sm-and-down">
      <v-icon size="24" color="#612009">mdi-heart-outline</v-icon>
      </v-btn>

      <v-btn icon class="hidden-sm-and-down">
      <v-icon size="24" color="#612009">mdi-facebook</v-icon>
      </v-btn>

      <v-btn icon class="hidden-sm-and-down">
       <v-icon size="24" color="#612009">mdi-twitter</v-icon>
      </v-btn>

      <v-btn icon class="hidden-sm-and-down">
      <v-icon size="24" color="#612009">mdi-instagram</v-icon>
      </v-btn>

      <v-btn icon class="hidden-sm-and-down">
        <v-icon size="24" color="#612009">mdi-account-circle</v-icon>
      </v-btn>


      <v-btn icon class="hidden-md-and-up" @click.stop="drawer = !drawer">
        <v-icon color="#612009">mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>
    
    <v-navigation-drawer v-model="drawer" app temporary class="elevation-0">
      <v-list-item-group>
        <v-list-item>
          <v-icon size="24" color="#612009">mdi-account-circle</v-icon>
        </v-list-item>
        <v-list-item>
          <v-list-item-title color="#612009">HOME</v-list-item-title>
        </v-list-item>
        <v-list-item>
          <v-list-item-title color="#612009">OUR STORY</v-list-item-title>
        </v-list-item>
        <v-list-item>
          <v-list-item-title color="#612009">OUR MENU</v-list-item-title>
        </v-list-item>
        <v-list-item>
          <v-list-item-title color="#612009">CONTACT US</v-list-item-title>
        </v-list-item>
        <v-list-item>
          <v-icon size="24" color="#612009">mdi-facebook</v-icon>
        </v-list-item>
        <v-list-item>
          <v-icon size="24" color="#612009">mdi-twitter</v-icon>
        </v-list-item>
        <v-list-item>
          <v-icon size="24" color="#612009">mdi-instagram</v-icon>
        </v-list-item>
      </v-list-item-group>
    </v-navigation-drawer>
   

    <div style="margin-top: 50px;">
    <v-container fluid fill-height class="pa-0">
      <v-row no-gutters>
        <v-col>
          <v-img :src="require('@/assets/introWallpaper.jpg')">
            <v-container style="margin-top: 20vh;">
              <v-row>
                <v-col cols="12" class="text-left">
                  <h1 style="margin-bottom: 20px; max-width: 400px; font-family: 'Titan One', sans-serif; color: #612009;">Discover Our Delicious Donuts Today!</h1>
                  <p style="max-width: 600px; color: #6D4C41; font-family: Arial, Helvetica, sans-serif;">
                    We believe in turning ordinary moments into extraordinary memories, one delectable donut at a time. Step into a world where the aroma of freshly baked goodness fills the air, and every bite is a journey into a realm of pure delight.
                  </p>
                </v-col>
                <v-col cols="12" class="text-left">
                   <button class="d-intro-btn"><span>EXPLORE</span></button>

                    <router-link to="/products">
                    <button class="c-intro-btn"><span>MENU</span></button>
                    </router-link>

                </v-col>
              </v-row>
            </v-container>
          </v-img>
        </v-col>
      </v-row>
    </v-container>
  </div>

    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

   
    <v-footer height="auto" style="background-color: #612009; padding-top: 80px; padding-bottom: 50px;">
      <v-container>
        <v-row justify="space-between">
          <v-col cols="12" md="3">
            <v-btn style="background-color: white; height: auto; border-radius: 50%; padding: 16px; min-width: 0;">
              <v-icon style="font-size: 4em;" color="#612009">mdi-chart-donut-variant</v-icon>
            </v-btn>
          </v-col>

          <v-col cols="12" md="3">
            <div>
              <div style="color: white; font-family: 'Titan One', sans-serif; margin-bottom: 10px;">Contact us</div>
              <div style="color: white; margin-bottom: 10px;"><v-icon color="white">mdi-email</v-icon>donutdisturb@gmail.com</div>
              <div style="color: white;"><v-icon color="white">mdi-phone</v-icon>+639534203251</div>
            </div>
          </v-col>

          <v-col cols="12" md="3">
            <div>
              <div style="color: white; font-family: 'Titan One', sans-serif; margin-bottom: 10px;">Our Locations</div>
              <div style="color: white; margin-bottom: 10px;"><v-icon color="white">mdi-map-marker</v-icon>Dolores San Fernando, Pampanga</div>
              <div style="color: white;"><v-icon color="white">mdi-office-building</v-icon>Building 452, 2nd Floor.</div>
            </div>
          </v-col>

          <v-col cols="12" md="3">
            <div>
             
              <div style="color: white; font-family: 'Titan One', sans-serif; margin-bottom: 10px;">Follow us on other platforms</div>
              
              <v-btn style="background-color: white; border-radius: 50%; ; height: auto; min-width: 0; padding: 10px;"><v-icon color="#612009">mdi-facebook</v-icon></v-btn>
              <v-btn style="background-color: white; border-radius: 50%; ; height: auto; min-width: 0; padding: 10px; margin-left: 5px;"><v-icon color="#612009">mdi-twitter</v-icon></v-btn>
              <v-btn style="background-color: white; border-radius: 50%; ; height: auto; min-width: 0; padding: 10px; margin-left: 5px;"><v-icon color="#612009">mdi-instagram</v-icon></v-btn>
              <v-btn style="background-color: white; border-radius: 50%; ; height: auto; min-width: 0; padding: 10px; margin-left: 5px;"><v-icon color="#612009">mdi-linkedin</v-icon></v-btn>
            </div>
    
          </v-col>
        </v-row>

        <v-row style="margin-top: 100px;">
          <v-col class="text-center" cols="12">
            <div style="color: white; font-family: 'Titan One', sans-serif; font-size: 20px; margin-bottom: 10px;">Donut Disturb</div>
            <div style="color: white; font-size: 14px;">&copy; 2023 Donut Disturb. All Rights Reserved.</div>
          </v-col>
        </v-row>

      </v-container>
    </v-footer>


    
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
    };
  },
  mounted() {
 
    document.addEventListener('contextmenu', this.handleRightClick);
  },
  beforeDestroy() {
   
    document.removeEventListener('contextmenu', this.handleRightClick);
  },
  methods: {
    handleRightClick(event) {
      event.preventDefault();
   
    },
    scrollToSection(sectionId) {
      const section = document.querySelector(sectionId);
      if (section) {
        const sectionRect = section.getBoundingClientRect();

        window.scrollTo({
          top: sectionRect.top + window.scrollY,
          behavior: 'smooth',
        });
      } else {
        console.error('Section not found:', sectionId);
      }
    },
    
  },
  
};
</script>




<style>

.d-intro-btn {
  cursor: pointer;
  border: 1px solid #612009;
  padding: 0.9rem 2rem;
  margin: 0;
  font-family: inherit;
  font-size: inherit;
  position: relative;
  display: inline-block;
  letter-spacing: 0.05rem;
  font-weight: bold;
  font-size: 14px;
  font-family: Arial, Helvetica, sans-serif;
  border-radius: 500px;
  overflow: hidden;
  background: rgb(235, 235, 235); 
  color:  rgb(235, 235, 235);
}

.d-intro-btn span {
  position: relative;
  z-index: 10;
  transition: color 0.4s;
}

.d-intro-btn:hover span {
  color: #612009; 
}

.d-intro-btn::before,
.d-intro-btn::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
}

.d-intro-btn::before {
  background: #612009; 
  width: 120%;
  left: -10%;
  transform: skew(30deg);
  transition: transform 0.4s cubic-bezier(0.3, 1, 0.8, 1);
}

.d-intro-btn:hover::before {
  transform: translate3d(100%, 0, 0);
}


.c-intro-btn {
  cursor: pointer;
  border: 1px solid #612009;
  padding: 0.9rem 2rem;
  margin: 0;
  margin-top: 30px;
  margin-left: 10px;
  font-family: inherit;
  font-size: inherit;
  position: relative;
  display: inline-block;
  letter-spacing: 0.05rem;
  font-weight: bold;
  font-size: 14px;
  font-family: Arial, Helvetica, sans-serif;
  border-radius: 500px;
  overflow: hidden;
  background: #612009; 
  color: #612009; 
}

.c-intro-btn span {
  position: relative;
  z-index: 10;
  transition: color 0.4s;
}

.c-intro-btn:hover span {
  color: white; 
}

.c-intro-btn::before,
.c-intro-btn::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
}

.c-intro-btn::before {
  background:  rgb(235, 235, 235);
  width: 120%;
  left: -10%;
  transform: skew(30deg);
  transition: transform 0.4s cubic-bezier(0.3, 1, 0.8, 1);
}

.c-intro-btn:hover::before {
  transform: translate3d(100%, 0, 0);
}

</style>