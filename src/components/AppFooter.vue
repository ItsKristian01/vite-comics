
<script>
export default {
    data() {
        return {
            footInfo: [
                {
                    title: "DC COMICS",
                    links: ["Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
                },
                {
                    title: "SHOP",
                    links: ["Shop DC", "Shop DC Collectibles"]
                },
                {
                    title: "DC",
                    links: ["Terms of Use", "Privacy policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us",]
                },
                {
                    title: "SITES",
                    links: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"]
                },
            ],
        }
    },
};
</script>

<template>
    <footer>
        <div class="foot-head">
            <h3 v-for="(info, index) in footInfo">{{ footInfo[index].title }}
                <ul>
                    <li v-for="link in footInfo[index].links">{{ link }}</li>
                </ul>
            </h3>
        </div>

        <section class="foot-nav">

            <button class="sign-btn">
                <a>SIGN-UP NOW!</a>
            </button>


            <div class="icons">
                <a class="follow" href="">
                    FOLLOW US
                </a>
                
                <a href="">
                    <img src="../assets/img/footer-facebook.png" alt="">
                </a>
                <a href="">
                    <img src="../assets/img/footer-twitter.png" alt="">
                </a>
                <a href="">
                    <img src="../assets/img/footer-youtube.png" alt="">
                </a>
                <a href="">
                    <img src="../assets/img/footer-pinterest.png" alt="">
                </a>
                <a href="">
                    <img src="../assets/img/footer-periscope.png" alt="">
                </a>
            </div>

        </section>
    </footer>
</template>

<style scoped lang="scss">
footer {
    .foot-head {
        padding: 4rem;
        background-image: url("../assets/img/footer-bg.jpg");
        display: flex;
        gap: 2rem;

        h3 {
            margin-bottom: 20px;
            color: white;
        }

        ul {
            margin-top: 10px;
            color: hsl(0deg 0% 58.43%);
            list-style: none;

            li {
                margin-bottom: 10px;
            }
        }
    }

    .foot-nav {
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 1rem;
        padding: 2.5rem;
        background-color: hsl(0deg 0% 18.82%);

        .sign-btn {
            background-color: hsl(0deg 0% 18.82%);
            padding: 1rem;
            border: 2px solid hsl(208.91deg 98.41% 49.22%);

            a {
                color: white;
            }
        }

        .icons {
            display: flex;
            gap: 1rem;
            .follow {
                margin-right: 20px;
                margin-top: 10px;
                text-decoration: none;
                color: hsl(208.91deg 98.41% 49.22%);
                font-size: 20px;
                
            }
        }
    }
}
</style>