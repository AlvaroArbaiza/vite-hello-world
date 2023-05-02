<script>
export default {
    name: "AppHero",
    data() {
        return {
            imgName: "soci.jpg"
        }
    },
    methods: {
        getImgPath(imgPath) {

            return new URL(imgPath, import.meta.url).href;
        }
    }
};
</script>

<template>
    <div id="container">
        <div>

            <h2>Pensa fuori dagli schemi!</h2>
            <h3>(immagine inserita da background)</h3>
        </div>
    </div>
    <div class="assets">
        <h3>Immagine inserita dalla cartella assets</h3>
        <img src="../assets/R.jpg" alt="sfondo di paesaggio">
    </div>
    <div class="assets">
        <h3>Immagine inserita dalla cartella public</h3>
        <img src="/img/a.jpg" alt="sfondo di dev">
    </div>
    <div class="assets">
        <h3>Immagine inserita dinamicamente con un metodo</h3>
        <img :src="getImgPath(`../assets/${imgName}`)" alt="sfondo di paesaggio">
    </div>
</template>

<style scoped>
h2 {
    font-size: 3rem;
    color: greenyellow;
}

#container {
    width: 100%;
    height: 300px;
    display: flex;
    justify-content: center;
    align-items: center;
    background: url(http://jimkulakowski.com/web-design/img/parallax-backgrounds/space.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    margin: 10px 0;
}

.assets {
    position: relative;
}

.assets>h3 {
    position: absolute;
    top: 50%;
    right: 50%;
    transform: translate(50%, -50%);
    background-color: rgba(0, 0, 0, 0.201);
    border-radius: 20px;
}

img {
    max-width: 100%;
}

h3 {
    color: rgb(185, 222, 255);
    font-size: 2.8rem;
}
</style>