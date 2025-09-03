<script setup>
import Headercomponent from '../components/Headercomponent.vue';
import FooterComponent from '../components/FooterComponent.vue';
import { ref } from 'vue';

const home = ref([
    {
        id: 1,
        title: "ShopEase",
        emogi: null,
        description: null,
        image: "shopease.png",
        category: ["Mobile", "Application", "E-commerce"]
    },
    {
        id: 2,
        title: "Insightly",
        emogi: "💡",
        description: "Developed a SaaS-based analytics dashboard for Insightly, focusing on providing actionable insights through a user-centric design. The dashboard improved data accessibility and was adopted by 80% of users within the first three months.",
        image: null,
        category: ['Web 3.0', 'HTML', 'Dashboard']
    },
    {
        id: 3,
        title: "ShopEase",
        emogi: null,
        description: null,
        image: 'shopease.png',
        category: ["Mobile", "Application", "E-commerce"]
    },
    {
        id: 4,
        title: "Insightly",
        emogi: "💡",
        description: "Developed a SaaS-based analytics dashboard for Insightly, focusing on providing actionable insights through a user-centric design. The dashboard improved data accessibility and was adopted by 80% of users within the first three months.",
        image: null,
        category: ['Web 3.0', 'HTML', 'Dashboard']
    },
]);
</script>

<template>

    <Headercomponent />
    <main>
        <section class="banner">

            <h1>Hi, I’m <span>Alex</span></h1>

            <p>
                a <strong>UI/UX Designer</strong> based in <strong>Los Angeles</strong>. With over <strong>3 years of
                    experience</strong>, I specialize in creating
                user-friendly digital products that solve real-world problems.
            </p>cards
        </section>
        <section class="cards">
            <ul class="card">
                <li v-for="cards in home">

                    <h3>{{ cards.title }}</h3>

                    <p class="emogi" v-if="cards.emogi != null">
                        {{ cards.emogi }}
                    </p>
                    <p class="description" v-if="cards.description != null">{{ cards.description }}</p>
                    
                    <p v-if="cards.image != null">
                        <img :src="'/images/' + cards.image" alt="">
                    </p>
                    <ul>
                        <li v-for="tags in cards.category">
                            {{ tags }}
                        </li>
                    </ul>
                </li>
            </ul>
        </section>

    </main>

    <footer-component>

    </footer-component>

</template>
<style scoped>
section.cards>ul {

    &>li {
        background: white;
        border-radius: 10px;
        padding: 20px;
        margin-bottom: 20px;

        & h3 {
            font-size: 1.5rem;
            padding: 10px 0px;
        }

        & img {
            border-radius: 10px;
        }

        & .emogi {
            font-size: 4rem;
        }
    }

    & ul {
        display: flex;
        margin-top: 20px;

        & li:first-child {
            margin-left: 0;
        }

        & li {
            background: rgb(232, 232, 232);
            color: black;
            margin: 0 10px;
            padding: 4px 8px;
            border-radius: 10px;
            font-size: 0.7rem;
            font-weight: bold;
        }
    }
}
</style>
