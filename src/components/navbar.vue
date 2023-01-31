<script setup lang="ts">

   let Links = [
    { name:'home',link:'#'},
    { name:'election',link:'#'},
    { name:'result',link:'#'}
   ]

</script>

<template>
   <section
    class="flex w-full px-6 py-2 bg-indigo-100"
   >

    <div
     class="flex bg-white py-2 px-4 justify-between items-center rounded-sm w-full"
    >

        <a href="#" class="flex justify-center items-center space-x-3 uppercase text-lg">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round" d="M8.25 21v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21m0 0h4.5V3.545M12.75 21h7.5V10.75M2.25 21h1.5m18 0h-18M2.25 9l4.5-1.636M18.75 3l-1.5.545m0 6.205l3 1m1.5.5l-1.5-.5M6.75 7.364V3h-3v18m3-13.636l10.5-3.819" />
            </svg>
            <h1>home</h1>
        </a>


        <div 
         class="flex justify-center items-center space-x-3"
        >
            <a
             v-for="link in Links"
             :key="link.name"
             :href="link.link"
             class="uppercase text-lg"
            >
                <h1>{{ link.name }}</h1>
            </a>
        </div>

        <div>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round" d="M10.5 6h9.75M10.5 6a1.5 1.5 0 11-3 0m3 0a1.5 1.5 0 10-3 0M3.75 6H7.5m3 12h9.75m-9.75 0a1.5 1.5 0 01-3 0m3 0a1.5 1.5 0 00-3 0m-3.75 0H7.5m9-6h3.75m-3.75 0a1.5 1.5 0 01-3 0m3 0a1.5 1.5 0 00-3 0m-9.75 0h9.75" />
            </svg>
        </div>
    </div>

   </section>
</template>