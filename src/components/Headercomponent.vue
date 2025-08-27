<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
  <header>
    <nav>
      <ul>
        <li class="atual">
          <RouterLink to="/"> Home </RouterLink>
        </li>
        <li>
          <RouterLink to="/about">About</RouterLink>
        </li>
        <li>
          <RouterLink to="/projects"> Projects </RouterLink>
        </li>
        <li>
          <RouterLink to="/connect"> Connect </RouterLink>
        </li>

      </ul>
    </nav>
  </header>

</template>

<style>
  header {
    padding: 5vw 10vw;
    font-size: 0.8rem;

    & ul {
      display: flex;
      width: fit-content;
      margin: 0 auto;
      background: rgba(255, 255, 255, 0.5);
      padding: 5px;
      border-radius: 50px;
      border: 1px solid rgb(211, 211, 211);

      & li {
        padding: 8px 15px;
      }

      & .router-link-active {
        background: black;
        color: white;
        border-radius: 30px;
        padding: 5px 5px;
      }
    }
  }
</style>