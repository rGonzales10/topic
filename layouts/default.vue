
<template>
    <div style="display: flex;">
        <div>Richard</div>
        <div style="display: flex; justify-content: end; gap: 20;">
            <!-- <nuxt-link to="/">HOME</nuxt-link>
            <nuxt-link to="/about">ABOUT</nuxt-link> -->
            <a @click="changePage('/')">HOME</a>
            <a @click="changePage('/about')">ABOUT</a>
        </div>
    </div>
    <div style="padding: 20px;">
        <slot />
    </div>
</template>
<script setup>
const router = useRouter();
function changePage(path){
    router.push(path);
}
</script>