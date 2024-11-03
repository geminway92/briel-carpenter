<template>
    <div class="card">
        <div v-if="!showAboutMe" class="content">
            <div class="logo">
                <img src="../assets/logo-gr.jpg">
            </div>
            <div class="description">
                <span>Diseñamos lo que imagines</span>
            </div>

            <div class="email">
                <a href="mailto:grabielcarpenter@gmail.com">grabielcarpenter@gmail.com</a>
                ------------------------------------------
            </div>
        </div>

        <div v-else class="content-about-me">
            <h1>Briel Carpenter</h1>
        </div>

        <div class="about-me" @click="toggleAboutMe">
            <svg class="hammer-icon">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"><!--!Font Awesome Free 6.6.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M413.5 237.5c-28.2 4.8-58.2-3.6-80-25.4l-38.1-38.1C280.4 159 272 138.8 272 117.6l0-12.1L192.3 62c-5.3-2.9-8.6-8.6-8.3-14.7s3.9-11.5 9.5-14l47.2-21C259.1 4.2 279 0 299.2 0l18.1 0c36.7 0 72 14 98.7 39.1l44.6 42c24.2 22.8 33.2 55.7 26.6 86L503 183l8-8c9.4-9.4 24.6-9.4 33.9 0l24 24c9.4 9.4 9.4 24.6 0 33.9l-88 88c-9.4 9.4-24.6 9.4-33.9 0l-24-24c-9.4-9.4-9.4-24.6 0-33.9l8-8-17.5-17.5zM27.4 377.1L260.9 182.6c3.5 4.9 7.5 9.6 11.8 14l38.1 38.1c6 6 12.4 11.2 19.2 15.7L134.9 484.6c-14.5 17.4-36 27.4-58.6 27.4C34.1 512 0 477.8 0 435.7c0-22.6 10.1-44.1 27.4-58.6z"/></svg>
            </svg>
            <span>Sobre mi</span>
        </div>
    </div>
</template>


<script>
export default {
    name: 'AboutMe',
    data() {
        return {
        showAboutMe: false // Propiedad en el padre
        };
    },
    methods: {
    toggleAboutMe() {
      this.showAboutMe = !this.showAboutMe; // Cambia a lo contrario
    }
  }
}
</script>

<style scoped>
.card {
    display: flex;
    background: #DBDCDA;
    /*min-width: 20rem;*/
    width: 25rem;
    height: 100%;
    border-radius: 15px;
}

.content {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin: 2rem;
}

.logo {
    margin-top: 3rem;
}

img {
    width: 70%;
    border-radius: 50%;
}

.description {
    display: flex;
    flex-direction: column;
    color: white;
    font-size: 2rem;
    font-weight: bold;
}

.email {
    display: flex;
    flex-direction: column;
    color: white;
    font-weight: bold;
    align-items: start;
}

.about-me {
    background: white;
    position: absolute;
    display: flex;
    padding: 1rem 1rem;
    border-bottom-right-radius: 15px;
    color: black;
    font-weight: bold;
    gap: 0.5rem;
    cursor: pointer;
}

.hammer-icon {
    width: 1rem;
    height: 1rem;
}

.content-about-me {
    display: flex;
    flex-direction: column;
    width: 100%;
    justify-content: space-between;
    margin: 2rem;
    color: white;
}

.content-about-me h1 {
    text-align: center;
    margin-top: 3rem;
}
</style>