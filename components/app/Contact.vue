<template>
  <div class="d-flex flex-column mt-16">
    <span class="text-subtitle-1 font-weight-bold">Reach me via:</span>
    <span class="text-body-2">{{ contactNo }}</span>
    <span class="text-body-2">{{ email }}</span>
  </div>
  <div class="d-flex mt-2">
    <VTooltip
      v-for="(link, i) in links"
      :key="i"
      location="bottom"
    >
      <template v-slot:activator="{ props }">
        <a
          target="_blank" 
          :href="link.href"
          v-bind="props"
          class="mr-4 link-btn-hover link-btn-large"
        >
          <VIcon
            variant="plain"
            :icon="link.icon"
          />
        </a>

      </template>
      <span class="text-caption">{{ link.name }}</span>
    </VTooltip>
  </div>
</template>

<script setup>
import { ref } from 'vue';

// const contactNo = ref("+639219964993");
// const email = ref("gonzales.louieb@gmail.com");
// const links = ref([
//   {
//     name: 'LinkedIn',
//     href: 'https://www.linkedin.com/in/louiebgonzales/',
//     icon: 'mdi-linkedin',
//   },
//   {
//     name: 'Facebook',
//     href: 'https://www.facebook.com/louiebgonza1es',
//     icon: 'mdi-facebook',
//   },
// ]);

const contactNo = ref("+639847561829");
const email = ref("dummy.email@gmail.com");
const links = ref([
  {
    name: 'LinkedIn',
    href: 'https://www.linkedin.com/in/dummy-act/',
    icon: 'mdi-linkedin',
  },
  {
    name: 'Facebook',
    href: 'https://www.facebook.com/dummy-act',
    icon: 'mdi-facebook',
  },
]);

</script>

<style scoped>
.link-btn-hover {
  transition: color 100ms linear, opacity 100ms linear;
  color: #424242;
  opacity: 0.5;
}
.link-btn-hover:hover {
  color: #0D47A1; /* Primary Color */
  opacity: 1;
}

.link-btn-large {
  font-size: 24px;
}

.default-font {
  font-family: "Noto Sans", sans-serif !important;
}
</style>