<script setup>
import logo from "../img/logo-watchstore3-9-24_1725292445.webp";
import SvgIcon from "@jamescoyle/vue-icon";
import { mdiMagnify, mdiCart, mdiHeartOutline } from "@mdi/js";

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
  <v-app-bar color="white">
    <v-main class="remove-padding">
      <v-container class="remove-padding">
        <v-row class="justify-center align-center">
          <v-col cols="2" class="pa-0 responsive-logo">
            <v-img :src="logo" alt="Logo"></v-img>
          </v-col>
          <v-col cols="7">
            <v-list class="d-flex flex-wrap justify-space-around">
              <v-list-item
                v-for="(item, index) in menuItems"
                :key="index"
                class="pa-0"
              >
                <v-list-item-title>{{ item }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-col>
          <v-col cols="2">
            <v-row class="search-input">
              <v-col cols="10" class="remove-padding d-flex align-center">
                <input
                  type="text"
                  placeholder="Tìm kiếm"
                  class="custom-input"
                />
              </v-col>
              <v-col
                cols="2"
                class="d-flex align-center justify-center remove-padding"
              >
                <svg-icon
                  type="mdi"
                  :path="mdiMagnify"
                  width="24"
                  height="24"
                  class=""
                ></svg-icon>
              </v-col>
            </v-row>
          </v-col>
          <v-col cols="1" class="pa-0">
            <svg-icon
              type="mdi"
              :path="mdiCart"
              width="24"
              height="24"
              class="ml-3 mr-3"
            ></svg-icon>
            <svg-icon
              type="mdi"
              :path="mdiHeartOutline"
              width="24"
              height="24"
              class=""
            ></svg-icon>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app-bar>
</template>

<style scoped>
.remove-padding {
  padding: 0 !important;
}
.remove-magin {
  margin: 0 !important;
}
.responsive-logo {
  min-width: 120px;
  min-height: 24px;
  width: 100%;
  height: auto;
}

.custom-input {
  border: none;
  width: 100%;
  padding: 6px 8px;
  outline: none;
}

.custom-input:focus {
  border-color: none;
  box-shadow: none;
}
.v-icon {
  cursor: pointer;
}
.search-input {
  border: 1px solid #ccc;
  border-radius: 4px;
  outline: none;
  transition: border-color 0.3s ease, box-shadow 0.3s ease;
}

.search-input:focus-within {
  border-color: #1976d2;
  box-shadow: 0 0 5px rgba(25, 118, 210, 0.5);
}
</style>
