<script setup>
import { RouterLink, RouterView } from 'vue-router'

import Magnify from 'vue-material-design-icons/Magnify.vue'
import Bell from 'vue-material-design-icons/Bell.vue'

import SideMenuItem from './components/SideMenuItem.vue';
</script>

<template>
  <div id="TopNav"
    class="fixed right-0 flex items-center justify-between w-[calc(100%-240px)] h-[56px] border-b border-b-[#32323d]">
    <div class="flex items-center w-full">
      <Magnify class="ml-6 mt-1 pr-2" fill-color="#7E7E88" :size="22" />
      <input type="text"
        class="p-1 bg-transparent outline-none font-[300] placeholder-[#bebec7] text-[#fff] w-full max-w-xl"
        placeholder="Search">
    </div>

    <div class="flex items-center pr-10">
      <div class="mr-4 p-1 hover:bg-gray-600 rounded-full cursor-pointer">
        <Bell fill-color="#fff" :size="22" />
      </div>
      <img
        src="https://yt3.ggpht.com/rfmD2Uydb06xZ-RQiSMo_a42KgSsK1DyxEdOEM3N9EYsXl0DmBkZBFvlpgiGcqj6mFkMrDrGSw=s88-c-k-c0x00ffffff-no-rj"
        alt="profile-icon" class="rounded-full w-8">
    </div>
  </div>

  <div id="SideNav"
    class="fixed w-[240px] h-[100vh] border-r border-r-[#32323d] bg-[#191922]">
    <div class="w-full pl-6 pt-3 cursor-pointer">
      <RouterLink to="/" class="text-white">
        <img src="/images/deezer-logo.png" alt="deezer" width="130">
      </RouterLink>
    </div>

    <div class="mt-[53px]"></div>

    <SideMenuItem iconString="music" :iconSize="20" pageUrl="/" name="Music" />
    <SideMenuItem iconString="podcast" :iconSize="20" pageUrl="/podcasts" name="Podcasts" />
    <SideMenuItem iconString="explore" :iconSize="20" pageUrl="/artist" name="Explore" />
    <SideMenuItem iconString="favourite" :iconSize="20" pageUrl="/favourite" name="Favourites" />

    <div class="text-[#a2a2ad] font-light text-[12px] pl-[62px] mt-[25px]">
      <div class="py-[9px] cursor-pointer hover:text-[#ef5465]">Favourite tracks</div>
      <div class="py-[9px] cursor-pointer hover:text-[#ef5465]">Playlist</div>
      <div class="py-[9px] cursor-pointer hover:text-[#ef5465]">Albums</div>
      <div class="py-[9px] cursor-pointer hover:text-[#ef5465]">Artists</div>
      <div class="py-[9px] cursor-pointer hover:text-[#ef5465]">Podcasts</div>
    </div>
  </div>

  <div class="fixed w-[calc(100%-240px)] h-[calc(100vh-56px)] ml-[240px] mt-[56px] overflow-x-auto">
    <!-- <RouterView /> -->
  </div>
</template>
