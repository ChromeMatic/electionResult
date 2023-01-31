<script setup lang="ts">
  import Navbar from './components/navbar.vue';
  import footerComponent from './components/footer.vue';
  
  let Parishes = [
    {
      name:'kingston',
      JSP:'78%',
      PRP:'22',
    },
    {
      name:'Hanover',
      JSP:'68%',
      PRP:'32%',
    },
    {
      name:'St. Andrew',
      JSP:'55.5%',
      PRP:'44.5%',
    },
    {
      name:'St. James',
      JSP:'56%',
      PRP:'44%',
    },
    {
      name:'St Thomas',
      JSP:'70%',
      PRP:'30%',
    },
    {
      name:'St. Mary',
      JSP:'83%',
      PRP:'17%',
    },
    {
      name:'westmoreland',
      JSP:'68%',
      PRP:'32%',
    },
    {
      name:'Portland',
      JSP:'58.5%',
      PRP:'41.5%'
    },
    {
      name:'Manchester',
      JSP:'44.5%',
      PRP:'55.5%'
    }
  ]
</script>

<template>
  <section class="w-full bg-indigo-50">
    <Navbar/>

    <section class="px-8">

      <!-- Election results -->
      <div class="flex flex-col w-full justify-center items-center space-y-8 py-16">

        <img
          class="h-80 w-full object-contain rounded-sm" 
          src="https://fiwiroots.com/images/parishes.jpg" 
          alt="map of jamaica"
        />

        <div class="flex justify-center items-center space-x-16 uppercase leading-6">
          <h1 class="text-2xl bg-white shadow-lg px-8 py-1 rounded-sm">
            JSP 55.55%  of Votes      
          </h1>

          <h1 class="text-2xl">
            PRP  44.45%  of Votes         
          </h1>
        </div>

      </div>

      <!-- Election results in each parish -->
      <div class="w-full grid grid-cols-4 gap-4">
          
        <div
         class="w-full flex flex-col justify-center items-center space-x-4 bg-white py-1 px-2 rounded-sm"
         v-for="parish in Parishes"
        >
          <h1 class="uppercase font-semibold">{{ parish.name }}</h1>

          <div class="flex justify-center items-center space-x-4 font-semibold">
            <h1>
              PRP : {{ parish.PRP }}
            </h1>
            <h1>
              JSP : {{ parish.JSP }}
            </h1>
          </div>

        </div>
      </div>

    </section>

    <footerComponent/>
  </section>
</template>

