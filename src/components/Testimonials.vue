<template>
  <div class="container px-4 py-5">
    <h2 class="pb-2 border-bottom text-center">Apa Kata Mereka?</h2>
    <div class="row g-4 py-5 row-cols-1 row-cols-lg-3">
      <div class="col" v-for="(testimonial, index) in randomTestimonials" :key="index">
        <div class="card h-100 shadow-sm">
          <div class="card-body">
            <p class="card-text">"{{ testimonial.quote }}"</p>
          </div>
          <div class="card-footer bg-transparent border-top-0">
            <footer class="blockquote-footer text-end">{{ testimonial.author }}, <cite title="Source Title">{{ testimonial.title }}</cite></footer>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      testimonials: [
        {
          quote: "Chatbot ini benar-benar mengubah cara kami berinteraksi dengan pelanggan. Respons cepat dan otomatisasi membuat semuanya lebih efisien. Luar biasa!",
          author: "Budi Santoso",
          title: "CEO Toko Online"
        },
        {
          quote: "Awalnya ragu, tapi setelah mencoba, saya sangat terkesan. Penjualan meningkat dan beban tim customer service kami berkurang drastis.",
          author: "Siti Aminah",
          title: "Owner Butik Fashion"
        },
        {
          quote: "Fitur analitiknya sangat membantu kami memahami kebutuhan pelanggan. Setup-nya juga sangat mudah dan cepat. Recommended!",
          author: "Ahmad Dahlan",
          title: "Manajer Marketing"
        },
        {
          quote: "Layanan pelanggan kami menjadi jauh lebih baik berkat chatbot ini. Sangat responsif dan mudah diintegrasikan.",
          author: "Dewi Lestari",
          title: "Customer Service Manager"
        },
        {
          quote: "Investasi terbaik tahun ini! Chatbot ini menghemat waktu dan sumber daya kami secara signifikan.",
          author: "Joko Susilo",
          title: "Direktur Operasional"
        },
        {
          quote: "Saya tidak bisa membayangkan bekerja tanpa chatbot ini lagi. Efisiensi dan akurasi yang ditawarkan sangat membantu bisnis kami.",
          author: "Rina Fitri",
          title: "Startup Founder"
        },
        {
          quote: "Produk yang luar biasa! Membantu kami dalam mengelola pertanyaan pelanggan 24/7 tanpa henti.",
          author: "Eko Prasetyo",
          title: "Head of Support"
        }
      ]
    };
  },
  computed: {
    randomTestimonials() {
      const shuffled = [...this.testimonials].sort(() => 0.5 - Math.random());
      return shuffled.slice(0, 3);
    }
  }
};
</script>

<style scoped>
.card {
  background-color: #f8f9fa;
  border: 1px solid #dee2e6;
}
.blockquote-footer {
  color: #6c757d;
}
</style>
