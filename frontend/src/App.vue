<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
// import Greet from "./components/Greet.vue";
</script>

<template>
  <!-- <div class="container">
    <div class="games">
      <button> Game </button>
    </div>
    <div class="news">
      <h2>News</h2>
    </div>
  </div> -->
  <div class="main-screen">
    <div class="content">
      <div class="left-section">
        <h2 class="games-title">Games</h2>
        <div class="game-container">
          <div v-for="n in 3" :key="n" class="single-title">
            <button class="game-button"> Button {{ n }}</button>
            <p class="game-name">game name {{ n }}</p>
          </div>
         
        </div>
      </div>
      
      <div class="right-section">
        <div class="news-spacer"></div>
        <div class="news-container">
            <h2>News</h2>
            <div class="news-list">
              <li> first and foremost, hello This is a list explaing stuff</li>
              <li> news item 2</li>
              <li> news item 3</li>
              <li> news item 3</li>
              <li> news item 3</li>
              <li> news item 3</li>
              <li> news item 3</li>
              <li> news item 3</li>
            </div>
        </div>
      </div>

    </div>
    <div class="footer">
      <span class="version">Version 1.0.0</span>
      <div class="footer-buttons">
        <button @click="goToAdmin">Admin</button>
        <button @click="updateApp">Update</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .main-screen {
    display: flex;
    flex-direction: column;
    height: 95vh;
    min-height: 95vh;
    max-height: 95vh;
    /* overflow-y: auto; */
  }

  .content {
    display: flex;
    width: 100%;
    /* height: 90vh; */
    height: inherit;
    min-height: inherit;
    /* max-height: 90vh; */
  }

  .left-section{
    flex: 1;
    display: flex;
    flex-direction: column;
    margin: 10px;
    /* align-items: center; */
  }

  .games-title {
    align-self: center;
  }

  .game-container {
    flex: 1;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    /* grid-auto-rows: calc(33.33% - 40px); */
    grid-auto-rows: 200px;
    overflow-y: auto;
    gap: 5px;
  }

  .single-title {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .game-button {
    height: 150px;
    width: 150px;
    min-block-size: 150px;
    margin: 10px;
    margin-bottom: 5px;
  }
  .game-name {
    padding: 0px;
    margin: 0;
  }

  .right-section {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .news-spacer {
    flex: .2
  }

  .news-container {
    flex: 1;
    border: 1px solid black;
    /* min-width: 300px; */
    width: 70%;
    max-width: 350px;
    height: 70%;
    max-height: 440px;
    text-align: center;
  }

  .news-list {
    text-align: left;
    padding: 15px;
  }

  .footer {
    display: flex;
    justify-content: space-between;
    margin-inline: 20px;
    /* margin-bottom: 50px; */
  }

  .footer-buttons {
    display: flex;
    gap: 10px;
  }

</style>
