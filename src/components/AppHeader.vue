
<script>
export default {
    data() {
        return {
            navItems: [
                {
                    title: "CHARACTERS",
                    activeItem: false,
                },
                {
                    title: "COMICS",
                    activeItem: true,
                },
                {
                    title: "MOVIES",
                    activeItem: false,
                },
                {
                    title: "TV",
                    activeItem: false,
                },
                {
                    title: "GAMES",
                    activeItem: false,
                },
                {
                    title: "COLLECTIBLES",
                    activeItem: false,
                },
                {
                    title: "VIDEOS",
                    activeItem: false,
                },
                {
                    title: "FANS",
                    activeItem: false,
                },
                {
                    title: "NEWS",
                    activeItem: false,
                },
                {
                    title: "SHOP",
                    activeItem: false,
                },
            ]
        }
    },
};
</script>

<template>
    <header>
        <nav>
            <img src="../assets/img/dc-logo.png" alt="DC Logo">
            <ul>
                <li v-for="items in navItems" :key="items.title">
                    <a :clas="{ active: items.activeItem }" class="border" href="">{{ items.title }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style scoped lang="scss">
header {
    padding: 2rem;

    nav {
        display: flex;
        justify-content: space-between;

        img {
            width: 90px;
        }
    }
}

ul {
    display: flex;
    align-items: center;
    list-style: none;
    gap: 1rem;


    a {
        color: hsl(23.33deg 10.23% 34.51%);
        text-decoration: none;

        &:hover {
            color: hsl(206.67deg 96.12% 59.61%);

            &.border {
                border-bottom: 5px solid hsl(208.91deg 98.41% 49.22%);
                width: 2px;
                padding: 4rem;
            } 
        }

        &.active {
            color: hsl(206.67deg 96.12% 59.61%);
        }
    }
}</style>