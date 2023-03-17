<template>
  <div ref="container"></div>
</template>

<script setup lang="ts">
import {onMounted, ref} from "vue"

import * as THREE from 'three';

const container = ref<HTMLElement|null>(null)

const renderer = new THREE.WebGLRenderer({antialias: true})
renderer.setSize(window.innerWidth, window.innerHeight)

onMounted(()=>{
  container.value?.append(renderer.domElement)
})
</script>
