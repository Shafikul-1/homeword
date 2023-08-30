<script setup>
import axios from 'axios'
import { ref } from 'vue'
const tableData = ref([])
console.log(tableData.value);
// const url = 'https://basic-blog.teamrabbil.com/api/post-categories'
// fetch(url)
// .then(response => response.json())
// .then(result => {console.log(result)})
// .catch(error => {console.log(error)})

async function list(){
  let url = 'https://basic-blog.teamrabbil.com/api/post-categories';
  let response = await axios.get(url)
  console.log(response.data[0])
  tableData.value = response.data['data'];  
} 
list()
</script>

<template>
  <table>
    <tbody>
      <tr>
        <td>life</td>
        <td>life</td>
        <td>life</td>
        <td>life</td>
        <td>life</td>
        <td>life</td>
        <td>life</td>
      </tr>
      <!-- <tr v-for="item in tableData">
        <td>{{ item['id'] }}</td>
        <td>{{ item['name'] }}</td>
        <td>{{ item['updated_at'] }}</td>
        <td>{{ item['created_at'] }}</td>
      </tr> -->
    </tbody>
  </table>
      
    <!-- <form @submit.prevent>
        <div class="grid gap-6 mb-6 md:grid-cols-2">
            <div>
                <label for="id" class="block text-md capitalize mb-2  font-medium text-gray-900 dark:text-white">id</label>
                <input type="number" id="id" class="bg-gray-50 border border-gray-300 text-gray-900  rounded-lg focus:ring-blue-500 focus:border-blue-500 block text-md capitalize w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="Id" >
            </div>
            <div>
                <label for="title" class="block text-md capitalize mb-2  font-medium text-gray-900 dark:text-white">title</label>
                <input type="text" id="title" class="bg-gray-50 border border-gray-300 text-gray-900  rounded-lg focus:ring-blue-500 focus:border-blue-500 block text-md capitalize w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="title" >
            </div>
            <div>
                <label for="img" class="block text-md capitalize mb-2  font-medium text-gray-900 dark:text-white">Image </label>
                <input type="url" id="img" class="bg-gray-50 border border-gray-300 text-gray-900  rounded-lg focus:ring-blue-500 focus:border-blue-500 block text-md capitalize w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="Image Url" >
            </div>  
            <div>
                <label for="PhoneNumber" class="block text-md capitalize mb-2  font-medium text-gray-900 dark:text-white">Phone number</label>
                <input type="number" id="PhoneNumber" class="bg-gray-50 border border-gray-300 text-gray-900  rounded-lg focus:ring-blue-500 focus:border-blue-500 block text-md capitalize w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="Phone Number" >
            </div>
            <div>
                <label for="category_id" class="block text-md capitalize mb-2  font-medium text-gray-900 dark:text-white">category id</label>
                <input type="number" id="category_id" class="bg-gray-50 border border-gray-300 text-gray-900  rounded-lg focus:ring-blue-500 focus:border-blue-500 block text-md capitalize w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="Category Id" >
            </div>
            <div>
                <label for="created_at" class="block text-md capitalize mb-2  font-medium text-gray-900 dark:text-white">Created At</label>
                <input type="text" id="created_at" class="bg-gray-50 border border-gray-300 text-gray-900  rounded-lg focus:ring-blue-500 focus:border-blue-500 block text-md capitalize w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="Created At" >
            </div>
        </div>
        <div class="mb-6">
            <label for="updated_at" class="block text-md capitalize mb-2  font-medium text-gray-900 dark:text-white">Updated At</label>
            <input type="text" id="updated_at" class="bg-gray-50 border border-gray-300 text-gray-900  rounded-lg focus:ring-blue-500 focus:border-blue-500 block text-md capitalize w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="Updated At" >
        </div> 
      
        <button type="submit" class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg  w-full sm:w-auto px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">Submit</button>
    </form> -->

</template>
