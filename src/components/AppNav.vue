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

        hoverCategoryIndex: 2,
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
            <li v-for="(currentCategory, index) in categories" :class="index == hoverCategoryIndex ? 'hover' : ''">
                {{ currentCategory }}
            </li>
        </ul>
    </nav>


</template>



<style lang="scss">

nav {
    display: flex;
    justify-content: center;
    align-items: center;
   
    ul {
        display: flex;
        list-style-type: none;
        gap: 34px;

        li {
            font-weight: 600;
            cursor: pointer;

            &.hover {
                color: #0282f9;
            }

        }
    }
    
}


</style>