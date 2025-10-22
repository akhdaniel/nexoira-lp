<script setup>
import { ref, onMounted } from 'vue';

const heroImages = [
  '/image1.png',
  '/image2.png',
  '/image3.png',
  '/image4.png',
  '/image5.png',
  '/image6.png',
  '/image7.png',
];

const currentHeroImage = ref('');

onMounted(() => {
  const randomIndex = Math.floor(Math.random() * heroImages.length);
  currentHeroImage.value = heroImages[randomIndex];
});
</script>

<template>
  <div class="container col-xxl-8 px-4 pt-0 py-lg-5">
    <div class="row flex-lg-row-reverse align-items-center g-5 py-lg-5">
      <div class="col-12 col-lg-6">
        <img :src="currentHeroImage" class="d-block mx-lg-auto img-fluid" alt="Chatbot Illustration" width="700" height="500" loading="lazy">
      </div>
      <div class="col-lg-6">
        <h1 class="display-5 fw-bold lh-1 mb-3">Nexoira: Otomatisasi Interaksi WhatsApp Anda</h1>
        <p class="lead">Tingkatkan layanan pelanggan dan efisiensi bisnis Anda dengan chatbot AI canggih yang terintegrasi langsung dengan WhatsApp. Siap melayani 24/7.</p>
        <div class="d-grid gap-2 d-md-flex justify-content-md-start">
          <a href="https://app.nexoira.chat" class="btn btn-success btn-lg px-4 me-md-2"><i class="bi bi-box-arrow-up-right me-2"></i>Coba Gratis!</a>
          <a href="#features" class="btn btn-outline-secondary btn-lg px-4">Lihat Fitur</a>
        </div>
      </div>
    </div>
  </div>
</template>
