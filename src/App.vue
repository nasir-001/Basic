<template>
  <div id="app">
    <Navbar />
    <!-- <AccountDropdown /> -->
    <div class="bg-gray-50 flex">
        <div class="px-8 py-12 max-w-md mx-auto lg:max-w-full max-w-xl lg:w-1/2 lg:py-24 lg:px-12">
            <div class="xl:max-w-md xl:ml-auto">
                <img class="h-10" src="/img/logo.png" alt="Workcation">
                <img class="mt-6 lg:hidden rounded-lg shadow-xl sm:mt-8 w-full sm:object-cover sm:object-center" src="/img/woman.jpg" alt="Woman working in beach">
                <h1 class="mt-6 text-2xl font-bold text-gray-900 leading-tight sm:text-4xl lg:text-3xl sm:mt-8 xl:text-4xl">
                    You can work from anywhere. 
                    <br class="hidden lg:inline"><span class="text-brand-blue">Take advantage of it.</span>
                </h1>
                <p class="mt-2 text-gray-600 sm:text-xl">
                    Workcation helps you find work-friendly 
                    rentals in beautiful location so you can enjoy 
                    some nice weather even when you're not on vaction.
                </p>
                <div class="mt-4 sm:mt-6">
                    <a href="#" class="inline-block uppercase tracking-wider active:bg-indigo-600 hover:bg-indigo-400 focus:outline-none active:shadow-outline bg-indigo-500 text-white bg-indigo-400 font-semibold text-sm px-5 py-3 rounded-lg outline-none shadow-outline; sm:text-base shadow-lg">Book your escape</a>
                    <a href="#" class="inline-block uppercase tracking-wider hover:bg-gray-300 active:bg-gray-500 bg-gray-500 focus:outline-none active:shadow-outline font-semibold text-sm px-5 py-3 rounded-lg outline-none text-gray-900 ml-2 sm:text-base">Learn more</a>
                </div>
            </div>
        </div>
    
        <div class="hidden lg:block lg:w-1/2 w-full lg:relative">
            <img class="absolute inset-0 m-auto rounded-lg mr-12 h-72  w-full object-center object-cover" src="/img/woman.jpg" alt="Woman working in beach">
        </div>
    </div>

    <div class="max-w-md sm:max-w-xl lg:max-w-6xl mx-auto px-8 lg:px-12 py-8">
        <h2 class="text-xl text-gray-900">Popular destinations</h2>
        <p class="text-gray-600">A selection of great work-friendly cities with lots to see and explore</p>
        <div class="flex flex-wrap -mx-4">
            <div class="mt-6 w-full px-4 lg:w-1/2 xl:w-1/3" v-bind:key="destination" v-for="destination in popularDestinations">
                <DestinationCard :destination="destination" />
            </div>
            
        </div>
    </div>
    <div class="px-10 pb-10">
        <div class="text-gray-900  mx-auto lg:max-w-full max-w-xl lg:w-1/2">
            <div class="rounded-lg overflow-hidden">
                <img class="w-full object-cover shadow-xl" src="/img/apartment.jpg" alt="Building">
            </div>

            <div class="relative px-4 -mt-20 xs:-mt-10">
                <div class="bg-gray-200 p-6 rounded-lg shadow-2xl">
                    <div class="flex items-baseline">
                        <span class="inline-block text-lg bg-teal-200 text-teal-800  text-xs px-2 rounded-full uppercase font-semibold tracking-wide">New</span>
                        <div class="ml-2 text-gray-600 text-sm uppercase font-semibold tracking-wide">
                            3 beds &bull; 2 baths
                        </div>
                    </div> 
                    <h4 class="mt-1 font-semibold text-lg leading-snug">Modern home in the city</h4>
                    <div class="mt-1">
                        $1,900 
                        <span class="text-gray-600 text-sm">/wk</span>
                    </div>
                    <div class="mt-2">
                        <span class="fas fa-star fa-sm text-teal-600"></span>
                        <span class="fas fa-star fa-sm text-teal-600"></span>
                        <span class="fas fa-star fa-sm text-teal-600"></span>
                        <span class="fas fa-star fa-sm text-teal-600"></span>
                        <span class="fas fa-star fa-sm text-gray-600"></span>
                        <!-- <span class="text-teal-600 font-semibold">4/5 stars</span> -->
                        <span class="text-gray-600 text-sm">34 reviews</span>
                    </div>
                </div>
            </div>
            
            
        </div>
    </div>
  </div>
</template>

<script>
import DestinationCard from './components/DestinationCard'
import Navbar from './components/Navbar'
// import AccountDropdown from './components/AccountDropdown'

export default {
  name: 'App',
  components: {
      DestinationCard,
      Navbar,
    //   AccountDropdown,
  },
  data() {
    return {
      popularDestinations: [
        {
          city: 'Toronto',
          averagePrice: 120,
          propertyCount: 86,
          imageUrl: "/img/apartment.jpg",
          imageAlt: 'Apartment',
        },
        {
          city: 'Toronto',
          averagePrice: 100,
          propertyCount: 76,
          imageUrl: "/img/1.jpg",
          imageAlt: 'Apartment',
        },
        {
          city: 'Toronto',
          averagePrice: 150,
          propertyCount: 66,
          imageUrl: "/img/2.jpg",
          imageAlt: 'Apartment',
        },
        {
          city: 'Toronto',
          averagePrice: 200,
          propertyCount: 56,
          imageUrl: "/img/3.jpg",
          imageAlt: 'Apartment',
        },
        {
          city: 'Toronto',
          averagePrice: 120,
          propertyCount: 60,
          imageUrl: "/img/4.jpg",
          imageAlt: 'Apartment',
        },
        {
          city: 'Toronto',
          averagePrice: 320,
          propertyCount: 70,
          imageUrl: "/img/5.jpg",
          imageAlt: 'Apartment',
        },
        {
          city: 'Toronto',
          averagePrice: 500,
          propertyCount: 76,
          imageUrl: "/img/6.jpg",
          imageAlt: 'Apartment',
        },
        {
          city: 'Toronto',
          averagePrice: 120,
          propertyCount: 40,
          imageUrl: "/img/7.jpg",
          imageAlt: 'Apartment',
        },
        {
          city: 'Toronto',
          averagePrice: 300,
          propertyCount: 56,
          imageUrl: "/img/4.jpg",
          imageAlt: 'Apartment',
        },
      ]
    }
  }
}
</script>

<style>

</style>
