<template>
  <div class="row mainapp">
    <div class="col-md-2">
      <div class="navbar">
        <br>
        <div class="mainnav">

          <div class="nav-item">
            <span class="fa fa-dashboard"></span>
            &nbsp;
            <router-link to="/">Dashboard</router-link>
          </div>

          <div class="nav-item">
            <span class="fa fa-id-card"></span>
            &nbsp;
            <router-link to="/Staff">Staff</router-link>
          </div>

          <div class="nav-item">
            <span class="fa fa-user-graduate"></span>
            &nbsp;
            <router-link to="/students">Students</router-link>
          </div>

          <div class="nav-item">
            <span class="fa fa-book-open"></span>
            &nbsp;
            <router-link to="/about">About</router-link>
          </div>

        </div>
      </div>
    </div>

    <div class="col-md-10">
      <router-view/>
    </div>

  </div>
</template>

<script>

import {Vue, Options} from 'vue-class-component';

@Options({

  methods: {
    check_user_login: function () {
      let status = localStorage.getItem('status');
      if(status) {
        if(status == 'loggedin') {
          
        }
        else {
          
        }
      }
      else {
        localStorage.setItem("loggedout");
        }
    },
  },
  
  beforeMount() {
  }
  
})

export default class App extends Vue {}

</script>

<style>

@import url('./assets/static/css/bootstrap.min.css');
@import url('./assets/static/css/fonts/stylesheet.css');

body {
  font-family: Rubik, sans-serif;
  background-image: url('./assets/static/images/bg1.jpg');
  background-size: cover;
  overflow-x: hidden;
  background-repeat: no-repeat;
  background-attachment: fixed;
}

body .col-md-2, body .col-md-10 {
  overflow-x: hidden !important;
}

body .col-md-2 {
  z-index: 1;
}


.navbar {
  background: rgba(0, 0, 0, 0.5);
  border-right: 2px solid #c3c3c3;
  position: fixed;
  top: 0;
  bottom: 0;
  width: 250px;
  overflow: hidden;
}

.navbar .mainnav {
  position: fixed;
  top: 50px;
  width: 250px;
}

.navbar .mainnav .nav-item {
  padding: 20px;
  border-bottom: 2px solid #c3c3c3;
  font-size: 20px;
  font-weight: bold;
}

.navbar .mainnav .nav-item a,
.navbar .mainnav .nav-item span {
  color: #fff;
  text-decoration: none;
}

.navbar .mainnav .nav-item:hover
 {
  background-color: #42b983;
  transition: 0.5s;
  border-bottom-color: #42b983;
}

</style>
