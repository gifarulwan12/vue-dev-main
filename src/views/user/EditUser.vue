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
          <router-link to="/user">
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
          <h1 class="text-2xl font-medium my-5">Edit User</h1>
          <!-- form -->
          <div class="my-0">
            <div>

              <div class="grid my-0 grid-cols-3 gap-2">
                <div>
                  <div class="my-0">
                    <label class="block mb-2 text-l font-medium text-gray-900">
                      Name
                    </label>
                    <input
                      v-model=Name
                      type="text"
                      class="w-96 h-10 text-sm text-gray-900 bg-gray-50 border border-gray-300 text-start align-text-top"
                    />
                  </div>
                </div>
              </div>

              <div class="grid my-5 grid-cols-3 gap-2">
                <div>
                  <div class="my-0">
                    <label class="block mb-2 text-l font-medium text-gray-900">
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
                    <label class="block mb-2 text-l font-medium text-gray-900">
                      Email
                    </label>
                    <input
                      v-model="Contact"
                      type="text"
                      class="w-96 h-10 text-sm text-gray-900 bg-gray-50 border border-gray-300 text-start align-text-top"
                    />
                  </div>
                </div>
              </div>
                              <div class="grid my-5 grid-cols-3 gap-2">
                <div>
                  <div class="my-0">
                    <label class="block mb-2 text-l font-medium text-gray-900">
                      Jumlah Kelas
                    </label>
                    <input
                      v-model="Duration"
                      type="text"
                      class="w-96 h-10 text-sm text-gray-900 bg-gray-50 border border-gray-300 text-start align-text-top"
                    />
                  </div>
                </div>
              </div>
              </div>
                <div class="flex justify-end">
                            <button @click="edituser()" class="p-2.5 px-3 text-sm font-medium text-white bg-red-600 rounded border border-red-600 hover:bg-red-100 hover:text-red-600" type="button">Save</button>
                        </div>
              </div>
            </div>
          </div>
        </div>
      </div>
</template>

<script>
import SideBar from '../../components/SideBar.vue'
import NavbarAdmin from '../../components/NavbarAdmin.vue'
import axios from 'axios'
export default {
    components: { SideBar, NavbarAdmin },
    data() {
        return {
            name: '',
            contact: '',
            email:'',
            class:'',
        }
    },
    methods: {
        addmember() {
            axios
            .put(`https://6303a9c20de3cd918b3b8fee.mockapi.io/user:id`,
            {name:this.name, email:this.email, status:this.status, contact:this.contact, duration:this.duration})
            .then((response) => {console.log(response)})
            .catch((error) => {console.log(error, "edit")})
        },
    },
}
</script>

<style
SideBar>

</style>    