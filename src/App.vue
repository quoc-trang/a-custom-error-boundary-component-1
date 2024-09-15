<script setup>
import BlogPost from "@/components/BlogPost.vue";
</script>
<template>
  <div class="max-w-4xl p-4 mx-auto">
    <Suspense>
      <BlogPost />
    </Suspense>
  </div>
</template>
