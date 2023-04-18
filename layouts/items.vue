<template>
    <div class="items-container">
      <div v-for="(item, index) in items" :key="index" class="item">
        <img :src="item.imageUrl" alt="">
        <p>{{ item.text }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        items: [
          { imageUrl: 'path/to/image1.jpg', text: 'Item 1 text' },
          { imageUrl: 'path/to/image2.jpg', text: 'Item 2 text' },
          { imageUrl: 'path/to/image3.jpg', text: 'Item 3 text' },
          // Add more items here as needed
        ]
      };
    }
  };
  </script>
  
  <style>
  .items-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
  }
  
  .item {
    width: calc(33.33% - 10px);
    margin-bottom: 20px;
    text-align: center;
  }
  
  .item img {
    max-width: 100%;
  }
  </style>
  