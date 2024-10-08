<script setup>
import logo from "../img/logo-watchstore3-9-24_1725292445.webp";

const menuItems = [
  "Giới thiệu",
  "XU HƯỚNG 2024",
  "Menu",
  "Nam",
  "Nữ",
  "Luxury",
  "Cũ Cao Cấp",
];
</script>
<template>
  <v-app>
    <v-app-bar color="white">
      <v-main class="remove-padding">
        <v-container class="">
          <v-row class="justify-center align-center">
            <v-col cols="2">
              <v-img :src="logo" alt="Logo" max-width="150"></v-img>
            </v-col>

            <v-col cols="7">
              <v-list class="d-flex justify-space-around">
                <v-list-item v-for="(item, index) in menuItems" :key="index">
                  <v-list-item-title>{{ item }}</v-list-item-title>
                </v-list-item>
              </v-list>
            </v-col>

            <v-col cols="2">3</v-col>

            <v-col cols="1">4</v-col>
          </v-row>
        </v-container>
      </v-main>
    </v-app-bar>
  </v-app>
</template>

<style scoped>
.remove-padding {
  padding: 0;
}
.remove-magin {
  margin: 0 !important;
}
</style>
