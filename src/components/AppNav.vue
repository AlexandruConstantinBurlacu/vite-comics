<script>
  export default {
    name: 'AppNav',

    data() {
    return {
        categories: [
        "CHARACTERS", "COMICS", "MOVIES", "TV",
        "GAMES", "COLLECTIBLES", "VIDEOS", "FANS",
        "NEWS", "SHOP"
        ],
    }
  }

  }

</script>



<template>
    
    <nav>
        <div class="logo">
            <img src="\vue-dc-comics-1\vue-dc-comics-1\img\dc-logo.png" alt="DC Logo">
        </div>

        <ul class="selection">
            <li v-for="currentCategory in categories">
                {{ currentCategory }}
            </li>
        </ul>
    </nav>


</template>



<style lang="scss">

nav {
    display: flex;
    justify-content: center;
}


</style>