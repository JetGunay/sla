<template>
  <div class="fixed top-[5%] z-40">
    <div class="fixed flex shadow-lg p-3 m-2 bg-white top-[12.5%]">
      <ul>
        <template v-for="r in rlarr" :key="r">
          <li
            v-if="r.access"
            class="group p-2 flex items-center justify-center"
          >
            <router-link
              :to="r.to"
              class="link flex items-center ease-in-out duration-300"
            >
              <div class="relative inline-block group">
                <div class="flex flex-col items-center">
                  <IconLayout
                    :classes="r.iconclass"
                    :svgclass="r.svgclass"
                    :svgd="r.svgd"
                  />
                  <span
                    class="absolute left-[2.5rem] w-max hidden group-hover:flex p-2 text-xs text-white whitespace-no-wrap rounded-md bg-black shadow-md"
                    >{{ r.title }}</span
                  >
                </div>
              </div>
            </router-link>
          </li>
        </template>
        <li class="group p-2 flex items-center justify-center border-t-[1px]">
          <MenuC />
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
// import store from "@/store";
import { ref } from "vue";
import MenuC from "./MenuC.vue";
import IconLayout from "./IconLayout.vue";

// const user = computed(() => {
//   console.log(store.state.user);
//   return store.state.user;
// });

const rlarr = ref([
  {
    to: { name: "dashboard" },
    title: "Dashboard",
    svgclass: "w-7 h-7",
    svgd: "M2.25 12l8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25",
    iconclass: "relative",
    access: true,
  },
  {
    to: { name: "form" },
    title: "form",
    svgclass: "w-7 h-7",
    svgd: "M9 12h3.75M9 15h3.75M9 18h3.75m3 .75H18a2.25 2.25 0 002.25-2.25V6.108c0-1.135-.845-2.098-1.976-2.192a48.424 48.424 0 00-1.123-.08m-5.801 0c-.065.21-.1.433-.1.664 0 .414.336.75.75.75h4.5a.75.75 0 00.75-.75 2.25 2.25 0 00-.1-.664m-5.8 0A2.251 2.251 0 0113.5 2.25H15c1.012 0 1.867.668 2.15 1.586m-5.8 0c-.376.023-.75.05-1.124.08C9.095 4.01 8.25 4.973 8.25 6.108V8.25m0 0H4.875c-.621 0-1.125.504-1.125 1.125v11.25c0 .621.504 1.125 1.125 1.125h9.75c.621 0 1.125-.504 1.125-1.125V9.375c0-.621-.504-1.125-1.125-1.125H8.25zM6.75 12h.008v.008H6.75V12zm0 3h.008v.008H6.75V15zm0 3h.008v.008H6.75V18z",
    iconclass: "relative",
    access: true,
  },
  {
    to: { name: "dashboard" },
    title: "Users",
    svgclass: "w-7 h-7",
    svgd: "M18 18.72a9.094 9.094 0 003.741-.479 3 3 0 00-4.682-2.72m.94 3.198l.001.031c0 .225-.012.447-.037.666A11.944 11.944 0 0112 21c-2.17 0-4.207-.576-5.963-1.584A6.062 6.062 0 016 18.719m12 0a5.971 5.971 0 00-.941-3.197m0 0A5.995 5.995 0 0012 12.75a5.995 5.995 0 00-5.058 2.772m0 0a3 3 0 00-4.681 2.72 8.986 8.986 0 003.74.477m.94-3.197a5.971 5.971 0 00-.94 3.197M15 6.75a3 3 0 11-6 0 3 3 0 016 0zm6 3a2.25 2.25 0 11-4.5 0 2.25 2.25 0 014.5 0zm-13.5 0a2.25 2.25 0 11-4.5 0 2.25 2.25 0 014.5 0z",
    iconclass: "relative",
    access: true,
  },
]);
</script>

<style></style>
