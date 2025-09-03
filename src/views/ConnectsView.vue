<script setup>
import Headercomponent from '../components/Headercomponent.vue';
import FooterComponent from '../components/FooterComponent.vue'; 
import { ref } from 'vue';  

const social = ref([
    {
        id: 1,
        title: "Instagram",
        icon: "fa-brands fa-instagram",
    },
    {
    id: 2,
        title: "Behance",
        icon: "fa-brands fa-behance",
    },
    {
    id: 3,
        title: "Dribble",
        icon: "fa-brands fa-dribbble",
    },
    {
    id: 4,
        title: "LinkedIn",
        icon: "fa-brands fa-linkedin-in",
    },
    
])
</script>

<template>
<Headercomponent></Headercomponent>
    <main>
        <section class="banner">

            <h1><span>Connect</span></h1>

            <p>
                I’m always open to new opportunities and collaborations. Whether you’re looking to start a project or just want to chat, feel free to reach out.
            </p>
        </section>

        <section class="connect">
            <ul class="white-itens">
                <li v-for="connect in social">
                    <a href="#"><span :class="'fa-brands fa-instagram' + connect.icon"></span>{{connect.title}}</a>
                </li>
            </ul>
        </section>
    </main>
<footer-component></footer-component>
</template>

<style scoped>
section.connect {
    & ul {
        & li {
            text-align: center;
            & span {
                font-weight:bold ;
                padding: 0 15px 0 0;
            }
        } 
    }
}
</style>
