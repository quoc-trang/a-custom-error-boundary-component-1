<script setup lang="ts">
import { ref } from "vue";
import BlogPostComments from "@/components/BlogPostComments.vue";
import ErrorBoundary from "@/components/ErrorBoundary.vue";

const post = ref({
  title: "Sample Blog Post",
  author: "John Doe",
  date: "May 23, 2024",
  content:
    "This is a sample blog post content. It contains information about a specific topic and is designed to be informative and engaging.",
});
</script>
<template>
  <div>
    <h1 class="mb-4 text-4xl font-bold text-primary">{{ post.title }}</h1>
    <p class="mb-6 text-sm text-gray-600">
      Written by {{ post.author }} on {{ post.date }}
    </p>
    <div class="prose">
      <p>{{ post.content }}</p>
    </div>
  </div>

  <ErrorBoundary>
    <BlogPostComments />
    <template #error="{ error, clearError }">
      <p class="pt-5 font-bold">⚠️ {{ error.message }}</p>
      <button class="mt-2" @click="clearError">Try Again</button>
    </template>
  </ErrorBoundary>
</template>
