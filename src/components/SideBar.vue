<template>
  <div class="lg:h-screen">
    <div
      class="bg-[#8c8c8e12] flex-col gap-4 w-72 h-60 p-30 flex justify-center items-center"
    >
      <div class="avatar">
        <div class="w-24 rounded-full ring ring-white ring-offset-base-100 ring-offset-2">
          <img class="" src="@/assets/images/me.jpg" />
        </div>
      </div>
      <div>
        <h2 class="font-bold">Théo Grosjean</h2>
        <h3 class="font-bold text-gray-700">Developpeur</h3>
      </div>
    </div>
    <div
      class="bg-[#8c8c8e05] flex-col w-72 px-8 py-4 flex justify-center items-center"
    >
        <ul class="w-full">
            <li class="flex justify-between"><h6 class="font-bold">Age :</h6><span class="text-gray-400">26</span></li>
            <li class="flex justify-between"><h6 class="font-bold">Localisation :</h6><span class="text-gray-400">Nancy</span></li>
            <li class="flex justify-between"><h6 class="font-bold">Mobilité :</h6><span class="text-gray-400">Grand-Est</span></li>
        </ul>
        <div class="divider"></div>
        <div class="flex flex-col justify-between gap-6">
            <div class="flex flex-col gap-2">
                <div class="flex justify-between">
                    <h6 class="font-bold">VueJs</h6>
                    <span class="text-gray-300">80%</span>
                </div>
                <progress class="progress h-1 progress-primary w-56" value="80" max="100"></progress>
            </div>
            <div class="flex flex-col gap-2">
                <div class="flex justify-between">
                    <h6 class="font-bold">Docker</h6>
                    <span class="text-gray-300">60%</span>
                </div>
                <progress class="progress h-1 progress-primary w-56" value="60" max="100"></progress>
            </div>
            <div class="flex flex-col gap-2">
                <div class="flex justify-between">
                    <h6 class="font-bold">Cobol</h6>
                    <span class="text-gray-300">40%</span>
                </div>
                <progress class="progress h-1 progress-primary w-56" value="40" max="100"></progress>
            </div>
            <div class="flex flex-col gap-2">
                <div class="flex justify-between">
                    <h6 class="font-bold">Python</h6>
                    <span class="text-gray-300">80%</span>
                </div>
                <progress class="progress h-1 progress-primary w-56" value="80" max="100"></progress>
            </div>
            <div class="flex flex-col gap-2">
                <div class="flex justify-between">
                    <h6 class="font-bold">HTML</h6>
                    <span class="text-gray-300">90%</span>
                </div>
                <progress class="progress h-1 progress-primary w-56" value="90" max="100"></progress>
            </div>
            <div class="flex flex-col gap-2">
                <div class="flex justify-between">
                    <h6 class="font-bold">CSS</h6>
                    <span class="text-gray-300">80%</span>
                </div>
                <progress class="progress h-1 progress-primary w-56" value="80" max="100"></progress>
            </div>
            <div class="flex flex-col gap-2">
                <div class="flex justify-between">
                    <h6 class="font-bold">JavaScript</h6>
                    <span class="text-gray-300">80%</span>
                </div>
                <progress class="progress h-1 progress-primary w-56" value="80" max="100"></progress>
            </div>
            <div class="flex flex-col gap-2">
                <div class="flex justify-between">
                    <h6 class="font-bold">Django</h6>
                    <span class="text-gray-300">60%</span>
                </div>
                <progress class="progress h-1 progress-primary w-56" value="60" max="100"></progress>
            </div>
            <div class="flex flex-col gap-2">
                <div class="flex justify-between">
                    <h6 class="font-bold">TailwindCSS</h6>
                    <span class="text-gray-300">80%</span>
                </div>
                <progress class="progress h-1 progress-primary w-56" value="80" max="100"></progress>
            </div>
            <div class="flex flex-col gap-2">
                <div class="flex justify-between">
                    <h6 class="font-bold">C#</h6>
                    <span class="text-gray-300">50%</span>
                </div>
                <progress class="progress h-1 progress-primary w-56" value="50" max="100"></progress>
            </div>
        </div>
    </div>
    <div class="bg-[#8c8c8e0a] flex-col gap-4 w-72 h-6 p-30 flex justify-center items-center"
>
<svg class="text-white" xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24"><path d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.593-11.018-3.714v-2.155z"/></svg>
    </div>
  </div>
</template>

<script>
export default {
  name: "SideBar",
};
</script>

<style scoped>
svg {
    color :white
}
</style>
