<template>
  <div id="app">
    <div class="container">
      <h1 class="heading">Avalon Perez</h1>
      <img src="@/assets/pink.png" class="container__img" alt />
      <nav class="container__nav">
        <ul class="nav">
          <li><a href="#" class="nav__link">home</a></li>
          <li><a href="#" class="nav__link">about</a></li>
          <img src="@/assets/pink.png" class="nav__img" alt />
          <li><a href="#" class="nav__link">gallery</a></li>
          <li><a href="#" class="nav__link">contact</a></li>
        </ul>
      </nav>
    </div>
    <ul class="social-links">
      <li>
        <a href="#" class="social-links__link">
          <img
            src="@/assets/instagram-brands.svg"
            alt
            class="social-links__img"
          />
        </a>
      </li>
      <li>
        <a href="#" class="social-links__link">
          <img
            src="@/assets/twitter-square-brands.svg"
            alt
            class="social-links__img"
          />
        </a>
      </li>
      <li>
        <a href="#" class="social-links__link">
          <img
            src="@/assets/snapchat-square-brands.svg"
            alt
            class="social-links__img"
          />
        </a>
      </li>
      <li>
        <a href="#" class="social-links__link">
          <img
            src="@/assets/envelope-square-solid.svg"
            alt
            class="social-links__img"
          />
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App"
};
</script>

<style lang="scss">
@font-face {
  font-family: QuickSand;
  src: url("./assets/fonts/Quicksand-VariableFont_wght.ttf");
}

*,
*::before,
*::after {
  box-sizing: border-box;
}

html {
  font-size: 62.5%;
}

body {
  font-size: 1.6rem;
  font-family: QuickSand, sans-serif;
  padding: 0;
  margin: 0;
  background: linear-gradient(to right, #bd0f4d 50%, #cb2964 50%);
  display: flex;
  justify-content: center;
  align-items: center;
}
#app {
  position: relative;
}

.heading {
  margin: 3rem 0;
  padding: 0;
  font-weight: 100;
  letter-spacing: 0.5rem;
  color: white;
  text-align: center;
}

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;

  &__img {
    width: 80vw;
    box-shadow: 0 0 2rem 0.2rem rgba(black, 0.3);
  }

  &__nav {
    width: 100vw;

    display: flex;
    align-items: center;
    justify-content: center;
    margin: 1.5rem 0 0;
  }
}

.nav {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  padding: 0;

  &__link {
    color: white;
    text-transform: uppercase;
    text-decoration: none;
    letter-spacing: 0.3rem;
    font-size: 1rem;
    margin: 0 0.5rem;

    &:hover {
      opacity: 0.5;
    }
  }

  &__img {
    border-radius: 50%;
    border: 0.1rem solid rgba(white, 0.3);
    height: 3rem;
    width: 3rem;
    margin: 0 0.5rem;
  }
}

.social-links {
  display: flex;
  justify-content: space-between;
  width: 60vw;
  position: fixed;
  top: auto;
  left: 0;
  right: 0;
  bottom: 0;
  list-style-type: none;
  margin: 0 auto;

  &__link {
    display: block;
    font-size: 3rem;
    padding: 0.2rem;
    margin: 0.3rem 0 0;
    color: white;
    transition: 0.3s ease-in-out;

    &:hover {
      opacity: 0.5;
    }
  }

  &__img {
    height: 2rem;
  }
}

@media (min-width: 1200px) {
  .heading {
    font-size: 4rem;
    margin: 3rem 0 5rem;
    letter-spacing: 1rem;
  }

  .nav {
    margin: 0 0 0 10rem;
    &__img {
      height: 7rem;
      width: 7rem;
      margin: 0 4rem;
    }

    &__link {
      font-size: 2rem;
      margin: 0 2rem;
      letter-spacing: 1rem;
    }
  }
  .container {
    &__nav {
      margin: 3rem 0 0;
    }
    &__img {
      width: 60vh;
    }
  }
  .social-links {
    height: fit-content;
    top: 0;
    bottom: 0;
    right: 0;
    left: 90vw;
    flex-direction: column;
    margin: auto 2rem auto 0;

    &__link {
      margin: 2rem 0 0;
    }

    &__img {
      height: 4rem;
    }
  }
}
</style>
