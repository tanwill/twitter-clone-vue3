<template>
    <div class="flex flex-col">

        <!-- Preview card: whats happening -->
        <SidebarRightPreviewCard title="whats happening">

            <SidebarRightPreviewCardItem v-for="whatsHappening in whatsHappeningItems">
                <div>
                    <h2 class="font-bold text-gray-800 text-md dark:text-white">{{ whatsHappening.title }}</h2>

                    <p class="text-xs text-gray-400">
                        {{ whatsHappening.count }}
                    </p>
                </div>
            </SidebarRightPreviewCardItem>

        </SidebarRightPreviewCard>

        <!-- Preview Card : Who to follow -->
        <SidebarRightPreviewCard title="Who to follow">
            <SidebarRightPreviewCardItem v-for="whoToFollow in whoToFollowItems">
                <div class="flex flex-row items-center justify-between p-2">
                    <div class="flex flex-row">
                        <img class="w-10 h-10 rounded-full" :src="whoToFollow.image" :alt="whoToFollow.name">

                        <div class="flex flex-col ml-2">
                            <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{ whoToFollow.name }}</h1>
                            <p class="text-xs text-gray-400">{{ whoToFollow.handle }}</p>
                        </div>
                    </div>
                    <div class="flex h-full">
                        <button
                            class="px-4 py-2 text-xs font-bold text-white bg-black rounded-full dark:text-black dark:bg-white">Follow</button>
                    </div>
                </div>
            </SidebarRightPreviewCardItem>
        </SidebarRightPreviewCard>

        <footer>
            <ul class="mx-2 my-4 text-xs text-gray-500">
                <li class="inline-block mx-2">
                    <a href="#" class="hover:underline">Privacy Policy</a>
                </li>
                <li class="inline-block mx-2">
                    <a href="#" class="hover:underline">Cookie Policy</a>
                </li>
                <li class="inline-block mx-2">
                    <a href="#" class="hover:underline">Accessability</a>
                </li>
                <li class="inline-block mx-2">
                    <a href="#" class="hover:underline">Ads info</a>
                </li>
                <li class="inline-block mx-2">
                    <a href="#" class="hover:underline">More</a>
                </li>
                <li class="inline-block mx-2">
                    ?? 2022 Twitter, Inc.
                </li>
            </ul>
        </footer>
    </div>
</template>


<script setup>

    const whatsHappeningItems = ref([
        {
            title: 'SpaceX',
            count: '18.8k Tweets'
        },
        {
            title: '#CodingIsFun',
            count: '8.8k Tweets'
        },
        {
            title: '#artforall',
            count: '1.8k Tweets'
        }
    ])

    const whoToFollowItems = ref([
        {
            name: 'User One',
            handle: '@User1',
            image: 'https://picsum.photos/200/200'
        },
        {
            name: 'User Two',
            handle: '@User 2',
            image: 'https://picsum.photos/200/200'
        },
        {
            name: 'User Three',
            handle: '@User 3',
            image: 'https://picsum.photos/200/200'
        }
    ])

</script>