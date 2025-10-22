<template>
<div class="container px-4 py-5">
    <h2 class="pb-2 border-bottom text-center">3 Langkah Mudah Memulai</h2>
    <div class="row g-4 py-5 row-cols-1 row-cols-md-3">
      <div class="col text-center">
        <div class="mb-3">
          <div class="d-inline-flex align-items-center justify-content-center bg-success text-white rounded-circle mb-3" style="width: 80px; height: 80px;">
            <i class="bi bi-whatsapp" style="font-size: 2.5rem;"></i>
          </div>
        </div>
        <h4>1. Kirim Pesan</h4>
        <p>Klik tombol "Mulai Percakapan" dan kirim pesan pertama Anda melalui WhatsApp.</p>
      </div>
      <div class="col text-center">
        <div class="mb-3">
          <div class="d-inline-flex align-items-center justify-content-center bg-success text-white rounded-circle mb-3" style="width: 80px; height: 80px;">
            <i class="bi bi-chat-dots" style="font-size: 2.5rem;"></i>
          </div>
        </div>
        <h4>2. Berinteraksi</h4>
        <p>Ajukan pertanyaan atau ikuti menu yang diberikan oleh chatbot kami.</p>
      </div>
      <div class="col text-center">
        <div class="mb-3">
          <div class="d-inline-flex align-items-center justify-content-center bg-success text-white rounded-circle mb-3" style="width: 80px; height: 80px;">
            <i class="bi bi-check2-circle" style="font-size: 2.5rem;"></i>
          </div>
        </div>
        <h4>3. Dapatkan Solusi</h4>
        <p>Dapatkan jawaban dan solusi untuk kebutuhan Anda secara instan.</p>
      </div>
    </div>
    <div class="text-center mt-4">
      <a :href="whatsappLink" target="_blank" class="btn btn-success btn-lg">
        <i class="bi bi-whatsapp me-2"></i> Coba Chatbot Demo
      </a>
    </div>
</div>
</template>

<script>
export default {
  data() {
    return {
      whatsappNumber: import.meta.env.VITE_WHATSAPP_NUMBER
    };
  },
  computed: {
    whatsappLink() {
      return `https://wa.me/${this.whatsappNumber}?text=${encodeURIComponent('Hi, saya mau tanya lebih lanjut')}`;
    }
  }
};
</script>
