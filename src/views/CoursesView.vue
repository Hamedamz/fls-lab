<script setup>
const courses = [
  {
    number: "CSCI 599",
    title: "Introduction to Holodecks",
    syllabus: "https://web-app.usc.edu/soc/syllabus/20223/30034.pdf",
  },
];
</script>

<template>
  <div>
    <h1 class="mb-8 text-4xl font-black text-white">Courses</h1>

    <ol>
      <li v-for="(course, i) in courses" :key="i" class="mb-4">
        <span class="text-white">{{ i + 1 }}</span>
        <span class="text-cyan-500">.</span>

        {{ course.number }}, {{ course.title }}

        <a v-if="course.syllabus" :href="course.syllabus" target="_blank">
          syllabus
        </a>
      </li>
    </ol>
  </div>
</template>
