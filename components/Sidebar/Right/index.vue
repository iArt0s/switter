<template>
  <div class="flex flex-col">

    <!--     What's happening -->
    <SidebarRightPreviewCard
        title="What's hahappening"
    >

      <SidebarRightPreviewCardItem
          v-for="whatsHappening in whatsHappeningItems"
      >
        <div class="">
          <h2 class="font-bold text-gray-800 text-md dark:text-white">{{ whatsHappening.title }}</h2>
          <p class="text-xs text-gray-400">{{ whatsHappening.count }}</p>
        </div>


      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>

    <!--    Who to follow-->
    <SidebarRightPreviewCard
        title="Who to follow"
    >
      <SidebarRightPreviewCardItem
          v-for="whoToFollow in whoToFollowItems"
      >
        <div class="flex items-center flex-row justify-between p-2">
          <div class="flex  flex-row">
            <img class="w-10 h-10 rounded-full" :src="whoToFollow.image" :alt="whoToFollow.name">

            <div class="flex flex-col ml-2">
              <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{ whoToFollow.name }}</h1>
              <p class="text-xs text-gray-900">{{ whoToFollow.handle }}</p>
            </div>
          </div>
          <div class="flex h-full">
            <button class="px-4 py-2 text font text-white bg-black dark:text-black dark:bg-white rounded-full">Follow</button>
          </div>
        </div>

      </SidebarRightPreviewCardItem>

    </SidebarRightPreviewCard>
  </div>
</template>
<script setup>
const whatsHappeningItems = ref([
  {
    title: 'Spacex',
    count: '18.8k Tweets'
  },
  {
    title: '#Coding Nuxt is cool',
    count: '10k Tweets'
  },
  {
    title: 'SafeSpace',
    count: '8.8k Tweets'
  },
])

const whoToFollowItems = ref([
  {
    name: 'John Doe',
    handle: '@John3000',
    image: 'https://picsum.photos/200/200'
  },
  {
    name: 'John Doe',
    handle: '@John3000',
    image: 'https://picsum.photos/200/200'
  },
  {
    name: 'John Doe',
    handle: '@John3000',
    image: 'https://picsum.photos/200/200'
  },
])
</script>
