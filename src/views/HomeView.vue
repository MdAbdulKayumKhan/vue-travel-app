<script>
import { ref } from "@vue/reactivity";
export default {
  name: "UserList",
  data() {
    const users = ref(null);

    fetch("https://jsonplaceholder.typicode.com/users")
      .then((response) => response.json())
      .then((data) => (users.value = data));

    return { users };
  },
};
</script>

<template>
  <div v-for="user in users" :key="user.id" class="grid grid-clos-2 grid-rows-3 gap-4 grid-flow-row-dense">
  <div class="block p-6 rounded-lg shadow-lg bg-white max-w-sm">
    <h5 class="text-gray-900 text-xl leading-tight font-medium mb-2">{{user.name}}</h5>
    <p class="text-gray-700 text-base mb-4">
      {{user.email}}
    </p>
    <p class="text-gray-700 text-base mb-4">
      {{user.website}}
    </p>
    <button type="button" class=" inline-block px-6 py-2.5 bg-blue-600 text-white font-medium text-xs leading-tight uppercase rounded shadow-md hover:bg-blue-700 hover:shadow-lg focus:bg-blue-700 focus:shadow-lg focus:outline-none focus:ring-0 active:bg-blue-800 active:shadow-lg transition duration-150 ease-in-out">Button</button>
  </div>
</div>
</template>
