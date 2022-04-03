<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <div class="bg-gray-100">
    <div class="max-w-7xl mx-auto py-16 px-4 sm:px-6 lg:py-24 lg:px-8 lg:grid lg:grid-cols-3 lg:gap-x-8">
      <div>
        <h2 class="text-base font-semibold text-indigo-600 uppercase tracking-wide">Unicast <span class="text-orange-500">Technologies</span></h2>
        <p class="mt-2 text-3xl font-extrabold text-gray-900">What Made us Unique</p>
      </div>
      <div class="mt-12 lg:mt-0 lg:col-span-2">
        <dl class="space-y-10 sm:space-y-0 sm:grid sm:grid-cols-2 sm:grid-rows-4 sm:grid-flow-col sm:gap-x-6 sm:gap-y-10 lg:gap-x-8">
          <div v-for="feature in features" :key="feature.name" class="relative">
            <dt>
              <CheckIcon class="absolute h-6 w-6 text-green-500" aria-hidden="true" />
              <p class="ml-9 text-lg leading-6 font-medium text-gray-900">{{ feature.name }}</p>
            </dt>
            <dd class="mt-2 ml-9 text-base text-gray-500">
              {{ feature.description }}
            </dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>

<script>
import { CheckIcon } from '@heroicons/vue/outline'

const features = [
  {
    name: 'High Speed Internet Connection',
    description: 'Get fast speed, watch any movies without your internet buffering.',
  },
  { name: 'Best Rate Per Month', description: 'Pay cheap compare to the market.' },
  {
    name: 'Support Care',
    description: 'If you have any question we are here 24 Hrs to solve your problem.',
  },
  { name: 'Reliable Internet', description: 'Get reliable internet.' },
 
]

export default {
  components: {
    CheckIcon,
  },
  setup() {
    return {
      features,
    }
  },
}
</script>