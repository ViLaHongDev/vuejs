<script setup>
    import { computed, ref } from 'vue';

    const month = ref(1);
    // const point = ref(0);

    // const rank = computed(
    //   () => {
    //     if(point.value >= 9) return 'Xuất sắc'
    //     if(point.value >= 8) return 'Giỏi'
    //     if(point.value >= 6.5) return 'Khá'
    //     if(point.value >= 5) return 'Trung bình'
    //     return 'Yếu'
    // })
    

</script>

<template>
    <!-- <div>
      <h1>Nhập điểm của bạn:</h1>
      <input type="number" v-model="point" max="10" min="0">
      <p v-if="point >= 9">Xuất sắc</p>
      <p v-else-if="point >= 8">Giỏi</p>
      <p v-else-if="point >= 6.5">Khá</p>
      <p v-else-if="point >= 5">Trung bình</p>
      <p v-else>Yếu</p>
    </div> --> 
    
    <!-- <div>
      <input type="number" v-model="point" max="10" min="0">
      <p>{{ rank }}</p>
    </div> -->

    <div>
        <h3>Nhập tháng của bạn:</h3>
        <input type="number" v-model.number="month">
        <p v-if="month < 1 || month > 12" style="color: red;">Vui lòng nhập tháng 1 đến 12</p>
        <p v-else-if="month >= 1 && month <= 3">Mùa xuân</p>
        <p v-else-if="month <= 6">Mùa hạ</p>
        <p v-else-if="month <= 9">Mùa thu</p>
        <p v-else>Mùa đông</p>
    </div>

</template>

<style scoped>

</style>
