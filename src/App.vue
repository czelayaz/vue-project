<script setup>
  import movieCard from './components/movieCard.vue';
</script>

<template>
  <main class="main">
    <div class="navbar-menu">
      <nav class="navbar">
        <div class="navbar-left">
          <img class="logo" src="./assets/images/video-player.png" alt="project-logo">
          <ul>
            <li>
              <a href="">Movies</a>
            </li>
            <li>
              <a href="">Series</a>
            </li>
          </ul>
        </div>
        <div class="navbar-center">
          <form action="search-form">
            <input type="text" class="search-input" placeholder="Search Movie">
            <button type="submit" class="search-button"><img src="" alt="search"></button>
          </form>
        </div>
        <div class="nabvar-right">
          <ul>
            <li>
              <a href="/">Log in</a>
            </li>
            <li>
              <a href="/">Register</a>
            </li>
          </ul>
        </div>

      </nav>
    </div>
    <div class="content">
        <movieCard />
        <movieCard />
        <movieCard />
        <movieCard />
        <movieCard />
    </div>
  </main>
</template>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background: linear-gradient(to bottom right, black, #2563eb);
}

.content {
  max-width: 1200px;
  padding: 40px 20px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px,1fr));
  gap: 40px;
  justify-items: center;
}

nav {
  display: flex;
  justify-content: space-between;
  padding: 0 24px;
  height: 60px;
  border-bottom: 1px solid black;
}

.logo {
  padding-top: 8px;
  width: 45px;
  height: 45px;
}

.navbar-left {
  display: flex;
}

.navbar-left ul {
  margin-left: 24px;
}

.navbar-left ul, .nabvar-right ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  align-items: center;
  height: 60px;
}

.navbar-left a, .nabvar-right a {
  text-decoration: none;
  color: gray;
}

/*
.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}

.wrapper__content {
  width: 100%;
  max-width: 34rem;
  margin: 0 auto;
  padding: 3rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  backdrop-filter: blur(16px);
  background: linear-gradient(
    to bottom right,
    rgba(59, 130, 246, 0.3),
    rgba(37, 99, 235, 0.3),
    rgba(29, 78, 216, 0.3)
  );
  border-radius: 1.5rem;
  box-shadow:
    0 10px 15px -3px rgba(0, 0, 0, 0.1),
    0 4px 6px -2px rgba(0, 0, 0, 0.05);
  border: 1px solid rgba(191, 219, 254, 0.5);
}

.title {
  text-align: center;
  font-size: 3rem;
  margin: 0;
}
*/
</style>
