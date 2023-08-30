<script setup>
import axios from 'axios'
import { ref } from 'vue'
import { RouterLink } from 'vue-router';
const tableData = ref([])
async function list(){
  let url = 'https://basic-blog.teamrabbil.com/api/post-newest';
  let response = await axios.get(url)
  console.log(response.status)
  tableData.value = response.data;  
} 
list()
</script>
<template> 
    <RouterLink to="/"  v-for="item in tableData" :key="item.id" class="m-2 max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
          <img class="rounded-t-lg" :src="item['img']" alt="" />
      <div class="p-5">
          <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{{ item['title'] }}</h5>
          <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">{{ item['short'] }}</p>
      </div>
    </RouterLink>
</template>
