<template>
    <div>
    <div class="flex text-start">
      <SideBar />
      <div class="w-full flex flex-col">
        <div>
          <NavbarAdmin />
        </div>
        <div class="mx-5 my-10">
          <!-- button -->
          <router-link to="/member">
            <button class="border-2 border-solid rounded-full">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-10 w-10"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                stroke-width="2"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M15 19l-7-7 7-7"
                />
              </svg>
            </button>
          </router-link>
          <!-- title -->
          <h1 class="text-4xl font-medium my-5">Edit Membership</h1>
          <!-- form -->
          <div class="my-10">
            <div>

              <div class="grid my-5 grid-cols-3 gap-2">
                <div>
                  <div class="my-0">
                    <label class="block mb-2 text-lg font-medium text-gray-900">
                      Name
                    </label>
                    <input
                      v-model="Name"
                      type="text"
                      class="w-96 h-10 text-sm text-gray-900 bg-gray-50 border border-gray-300 text-start align-text-top"
                    />
                  </div>
                </div>
              </div>

              <div class="grid my-5 grid-cols-3 gap-2">
                <div>
                  <div class="my-0">
                    <label class="block mb-2 text-xl font-medium text-gray-900">
                      Email
                    </label>
                    <input
                      v-model="Email"
                      type="text"
                      class="w-96 h-10 text-sm text-gray-900 bg-gray-50 border border-gray-300 text-start align-text-top"
                    />
                  </div>
                </div>
              </div>
              <div class="grid my-5 grid-cols-3 gap-2">
                <div>
                  <div class="my-0">
                    <label class="block mb-2 text-xl font-medium text-gray-900">
                      Status
                    </label>
              <div class="relative inline-block text-left">
  <div>
    <button type="button" class="inline-flex justify-center w-96 rounded-md border border-gray-300 shadow-sm px-4 py-2 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-100 focus:ring-indigo-500" id="menu-button" aria-expanded="true" aria-haspopup="true">
      Non Active
      <!-- Heroicon name: solid/chevron-down -->
      <svg class="-mr-1 ml-2 h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
        <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
      </svg>
    </button>
  </div>
  <div class="origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 focus:outline-none" role="menu" aria-orientation="vertical" aria-labelledby="menu-button" tabindex="-1">
    <div class="py-1" role="none">
      <!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
      <a href="#" class="text-gray-700 block px-4 py-2 text-sm" role="menuitem" tabindex="-1" id="menu-item-1">Active</a>
      <a href="#" class="text-gray-700 block px-4 py-2 text-sm" role="menuitem" tabindex="-1" id="menu-item-2">Non Active</a>
    </div>
  </div>
</div>
<div class="grid my-5 grid-cols-3 gap-2">
                <div>
                  <div class="my-0">
                    <label class="block mb-2 text-xl font-medium text-gray-900">
                      Contact
                    </label>
                    <input
                      v-model="Email"
                      type="text"
                      class="w-96 h-10 text-sm text-gray-900 bg-gray-50 border border-gray-300 text-start align-text-top"
                    />
                  </div>
                </div>
              </div>
              
              <div class="grid my-5 grid-cols-3 gap-2">
                <div>
                  <div class="my-0">
                    <label class="block mb-2 text-xl font-medium text-gray-900">
                      Duration
                    </label>
              <div class="relative inline-block text-left">
  <div>
    <button type="button" class="inline-flex justify-center w-96 rounded-md border border-gray-300 shadow-sm px-4 py-2 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-100 focus:ring-indigo-500" id="menu-button" aria-expanded="true" aria-haspopup="true">
      Duration
      <!-- Heroicon name: solid/chevron-down -->
      <svg class="-mr-1 ml-2 h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
        <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
      </svg>
    </button>
  </div>
  <div class="origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 focus:outline-none" role="menu" aria-orientation="vertical" aria-labelledby="menu-button" tabindex="-1">
    <div class="py-1" role="none">
      <!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
      <a href="#" class="text-gray-700 block px-4 py-2 text-sm" role="menuitem" tabindex="-1" id="menu-item-1">1 Month</a>
      <a href="#" class="text-gray-700 block px-4 py-2 text-sm" role="menuitem" tabindex="-1" id="menu-item-2">4 Month</a>
      <a href="#" class="text-gray-700 block px-4 py-2 text-sm" role="menuitem" tabindex="-1" id="menu-item-3">8 Month</a>
    </div>
  </div>
</div>
<div class="grid my-5 grid-cols-3 gap-2">
                <button
                  @click="addClass()"
                  class="absolute-right-200 bg-red-600 text-white rounded-md gap-1 h-14 w-24 text-center px-1"
                >
                  <span class="text-xl">SAVE</span>
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  </div>
  </div>
  </div>
  </div>
  </div>
    </div>
  
</template>

<script>
import SideBar from "../../components/SideBar.vue";
import NavbarAdmin from "../../components/NavbarAdmin.vue";
import axios from "axios";

export default {
  components: { SideBar, NavbarAdmin },
  name: "addOfflineClass",
  data() {
    return {
      category_id: null,
      class_name_id: null,
      date: null,
      image: null,
      trainer_id: null,
      price: null,
      description: "",
      things: "",
      time_start: null,
      time_end: null,
    };
  },
  computed: {
    listTrainer() {
      return this.$store.state.trainer.trainerList;
    },
    listCategory() {
      return this.$store.state.category.categoryList;
    },
    listClass_name() {
      return this.$store.state.classname.class_nameList;
    },
  },
  methods: {
    fetchtrainer() {
      this.$store.dispatch(`trainer/fetchList`);
    },
    fetchCategory() {
      this.$store.dispatch(`category/fetchList`);
    },
    fetchClassName() {
      this.$store.dispatch(`classname/fetchList`);
    },
    async addClass() {
      await axios
        .post("https://gym-capstone.hasura.app/api/rest/addclass", {
          class_name_id: this.class_name_id,
          type_id: 1,
          date: this.date,
          time_start: this.time_start,
          time_end: this.time_end,
          image: this.image,
          trainer_id: this.trainer_id,
          price: this.price,
          description: this.description,
          things: "",
        })
        .then((response) => {
          this.alertAddSucces(response);
          this.$router.push({ name: "offlineClass" });
        })
        .catch((error) => {
          this.alertAddError(error);
        });
    },
    alertAddSucces() {
      this.$swal({
        position: "center",
        icon: "success",
        title: "Berhasil Menambahkan",
        showAlertLoginSucces: false,
        timer: 1500,
      });
    },
    alertAddError() {
      this.$swal({
        position: "center",
        icon: "error",
        title: "Gagal!!!",
        showAlertLoginError: false,
        timer: 1500,
      });
    },
  },
  mounted() {
    this.fetchtrainer();
    this.fetchCategory();
    this.fetchClassName();
  },
};
</script>
