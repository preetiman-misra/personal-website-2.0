<script setup lang="ts">
import { ref } from "vue";

const isMenuOpen = ref(false);

const toggleMenu = () => isMenuOpen.value = !isMenuOpen.value;
</script>

<template>
  <nav class="shadow">
    <div class="mx-auto flex justify-between items-center p-6">
      <div>
        <a class="flex justify-start items-center" href="/"><span><svg xmlns="http://www.w3.org/2000/svg" fill="none"
              viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 mr-1">
              <path stroke-linecap="round" stroke-linejoin="round"
                d="M2.25 12l8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25">
              </path>
            </svg>
          </span>Home</a>
      </div>
      <button @click="toggleMenu"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
          stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </button>
    </div>
    <div v-if="isMenuOpen">
      <!-- Blog -->
      <a class="px-6 py-4 border-b border-t border-slate-200 flex justify-start items-center hover:bg-blue-500 hover:text-white"
        href="/blog"><span><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
            stroke="currentColor" class="w-6 h-6 mr-1">
            <path stroke-linecap="round" stroke-linejoin="round"
              d="M12 6.042A8.967 8.967 0 006 3.75c-1.052 0-2.062.18-3 .512v14.25A8.987 8.987 0 016 18c2.305 0 4.408.867 6 2.292m0-14.25a8.966 8.966 0 016-2.292c1.052 0 2.062.18 3 .512v14.25A8.987 8.987 0 0018 18a8.967 8.967 0 00-6 2.292m0-14.25v14.25">
            </path>
          </svg>
        </span>Blog</a>

      <!-- Projects -->
      <a class="px-6 py-4 border-b border-slate-200 flex justify-start items-center hover:bg-blue-500 hover:text-white"
        href="/projects"><span><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
            stroke="currentColor" class="w-6 h-6 mr-1">
            <path stroke-linecap="round" stroke-linejoin="round"
              d="M3.75 9.776c.112-.017.227-.026.344-.026h15.812c.117 0 .232.009.344.026m-16.5 0a2.25 2.25 0 00-1.883 2.542l.857 6a2.25 2.25 0 002.227 1.932H19.05a2.25 2.25 0 002.227-1.932l.857-6a2.25 2.25 0 00-1.883-2.542m-16.5 0V6A2.25 2.25 0 016 3.75h3.879a1.5 1.5 0 011.06.44l2.122 2.12a1.5 1.5 0 001.06.44H18A2.25 2.25 0 0120.25 9v.776">
            </path>
          </svg>
        </span>Projects</a>

      <!-- Art -->
      <a class="px-6 py-4 border-b border-slate-200 flex justify-start items-center hover:bg-blue-500 hover:text-white"
        href="/art"><span>
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
            class="w-6 h-6 mr-1">
            <path stroke-linecap="round" stroke-linejoin="round"
              d="M9.53 16.122a3 3 0 00-5.78 1.128 2.25 2.25 0 01-2.4 2.245 4.5 4.5 0 008.4-2.245c0-.399-.078-.78-.22-1.128zm0 0a15.998 15.998 0 003.388-1.62m-5.043-.025a15.994 15.994 0 011.622-3.395m3.42 3.42a15.995 15.995 0 004.764-4.648l3.876-5.814a1.151 1.151 0 00-1.597-1.597L14.146 6.32a15.996 15.996 0 00-4.649 4.763m3.42 3.42a6.776 6.776 0 00-3.42-3.42">
            </path>
          </svg></span>Art
      </a>

      <!-- Contact -->
      <a class="px-6 py-4 border-b border-slate-200 flex justify-start items-center hover:bg-blue-500 hover:text-white"
        href="/contact"><span><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
            stroke="currentColor" class="w-6 h-6 mr-1">
            <path stroke-linecap="round"
              d="M16.5 12a4.5 4.5 0 11-9 0 4.5 4.5 0 019 0zm0 0c0 1.657 1.007 3 2.25 3S21 13.657 21 12a9 9 0 10-2.636 6.364M16.5 12V8.25">
            </path>
          </svg>
        </span>Contact</a>
    </div>
  </nav>
</template>

