<template>
  <div>
    <ul>
      <li v-for="user in users" :key="user.id">
        {{ user.name }}
      </li>
    </ul>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "IndexPage",
  data() {
    return {
      users: [],
    };
  },
  components: {},
  // methods: {
  //   async getUsers() {
  //     const { data } = await axios.get(
  //       "https://jsonplaceholder.typicode.com/users"
  //     );
  //     this.users = data;
  //   },
  // },
  asyncData() {
    return axios
      .get("https://jsonplaceholder.typicode.com/users")
      .then(({ data }) => {
        return { users: data };
      });
  },
  // mounted() {
  //   this.getUsers();
  // },
};
</script>

<style></style>
