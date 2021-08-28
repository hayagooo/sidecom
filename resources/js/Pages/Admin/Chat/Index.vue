<template>
    <div>
        {{ label }}
        <div v-if="chatData.length > 0">
            <div v-for="item, index in chatData" :key="index">
                <div class="border-2 border-indigo-600">
                    <h3 class="text-xl">{{ item.message }}</h3>
                    <p>from {{ item.user.name }}</p>
                </div>
            </div>
        </div>
        <div v-else>
            <h2>Tidak ada chat terbaru</h2>
        </div>
    </div>
</template>

<script>
export default {
    props: ['userData', 'chatData'],
    data() {
        return {
            label: 'Chat Sidecom'
        }
    }
}
</script>
