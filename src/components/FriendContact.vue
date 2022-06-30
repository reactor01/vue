<template>
  <li>
    <header>
      <h1>{{ friend.name }}</h1>
    </header>
    <button @click="toggleDetails">Show Details</button>
    <ul v-if="detailsAreVisiable">
      <li><strong>Phone:</strong> {{ friend.phone }}</li>
      <li><strong>Email:</strong> {{ friend.email }}</li>
    </ul>
  </li>
</template>

<script>
export default {
  data() {
    return {
      detailsAreVisiable: false,
      friend: {
        id: "_id23232",
        name: "Manuel Lorenz",
        phone: "0213123 213 3",
        email: "julie@localhost.com",
      },
    };
  },
  methods: {
    toggleDetails() {
      this.detailsAreVisiable = !this.detailsAreVisiable;
    },
  },
};
</script>
