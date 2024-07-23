<div class="grid h-screen place-items-center p-3 lg:pl-40 lg:pr-40 text-[#f0f0f0] font-mono select-none">
  <div class="bg-[#515151] rounded-xl p-5 mx-3">
    <div class="flex flex-col md:flex-row justify-between items-center space-y-5 md:space-y-0">
      <div class="bg-[#2c2c2c] rounded-xl py-3 px-6 text-[#7900ff] font-bold md:text-3xl text-2xl">Daniel "NiX3r" Iliev</div>
      
      <p class="text-[#2c2c2c]">© 2020-{nowYear} Daniel Iliev, version: 21.08.2002</p>

      <div class="flex">
        <div class="p-2 rounded-full bg-[#2c2c2c] mr-3 hover:bg-[#2d0857]">
          <a href="https://discord.gg/AA9CZEcYHV">
            <img src=".\assets\discord.png" class=" rounded-full h-10 w-10" alt="Discord"/>
          </a>
        </div>

        <div class="p-2 rounded-full bg-[#2c2c2c] mr-3 hover:bg-[#2d0857]">
          <a href="https://github.com/NiX3r">
            <img src=".\assets\github.png" class=" rounded-full h-10 w-10" alt="Github">
          </a>
        </div>

        <div class="p-2 rounded-full bg-[#2c2c2c] mr-3 hover:bg-[#2d0857]">
          <a href="https://www.linkedin.com/in/daniel-iliev-a71466209/">
            <img src=".\assets\linkedin.png" class=" rounded-full h-10 w-10" alt="LinkedIn">
          </a>
        </div>

        <div class="p-2 rounded-full bg-[#2c2c2c] hover:bg-[#2d0857]">
          <a href=".\assets\Profile.pdf" download="CV">
            <img src=".\assets\cv.png" class=" rounded-full h-10 w-10" alt="CV">
          </a>
        </div>
      </div>
    </div>

    <div class="grid grid-cols-12 mt-5 gap-5">
      <div class="col-span-12 lg:col-span-3">
        <div class="bg-[#2c2c2c] rounded-xl">
          <div class="w-full h-64 p-5">
            <img src=".\assets\lion.png" class="rounded-xl object-scale-down h-full w-full" alt="" />
          </div>
        </div>
      </div>
      <div class="col-span-12 lg:col-span-9 h-full">
        <div class="bg-[#2c2c2c] rounded-xl py-3 px-6 h-full">
          <h1 class="text-[#ab61ff] font-bold md:text-2xl lg:text-left text-center text-xl p-8">a passionate software engineer</h1>
          <p class="ml-10">I'm software engineer enthusiastic who's into programming since 2016. I've started learning in C / C++ which lasted me for about 2 years and I felt in love with programming. Then I switched to learning Java and somewhat recently C# and with that came SQL (MySQL). I can read some other languages as well like PHP, JS, CSS, HTML, etc. I've already done some projects for personal use or for commercial use. Some of my projects are available at my page iliev.cz</p>
        </div>
      </div>
    </div>

    <div class="grid grid-cols-12 mt-5 gap-5">
      <div class="col-span-12 lg:col-span-9 h-full">
        <div class="bg-[#2c2c2c] rounded-xl py-3 px-6 h-full">
          <div id="showcase" class="relative w-full h-full" data-carousel="slide" on:mouseenter={() => { clearInterval(interval); }} on:mouseleave={() => { startInterval(); }}>
            <div class="relative overflow-hidden rounded-lg">
              {#each json as item, index}
                <div class:hidden={index !== currentIndex} class="transition-transform duration-[600ms] ease-in-out motion-reduce:transition-none" data-carousel-item>
                  <div class="grid grid-cols-12 gap-6 pr-5">
                    <div class="col-span-12 lg:col-span-8">
                      <div class="flex flex-col md:flex-row justify-start items-center space-y-5 md:space-y-0">
                        <h1 class="text-[#ab61ff] font-bold md:text-2xl lg:text-left text-center text-xl p-4">
                          {item.topic}
                        </h1>
                        {#if (item.git !== "")}
                        <div class="h-10 w-10 rounded-full bg-[#2c2c2c] mr-3 hover:bg-[#515151]">
                          <a href="{item.git}">
                            <img src=".\assets\github.png" class=" rounded-full h-full w-full p-1" alt="GitHub">
                          </a>
                        </div>
                        {/if}
                        {#if (item.web !== "")}
                        <div class="h-10 w-10 rounded-full bg-[#2c2c2c] mr-3 hover:bg-[#515151]">
                          <a href="{item.web}">
                            <img src=".\assets\web.png" class=" rounded-full h-full w-full p-1" alt="GitHub">
                          </a>
                        </div>
                        {/if}
                      </div>
                      <p class="ml-10">{item.description}</p>
                      <div class="text-[#ab61ff] font-bold mt-3 ml-5">Technologies</div>
                      <div class="inline ml-10 mb-5">
                        {#each item.technologies as key}
                          <div class="bg-[#3c3c3c] rounded inline mr-1 pl-1 pr-1">{key}</div>
                        {/each}
                      </div>
                    </div>
                    <div class="col-span-12 lg:col-span-4 mt-8">
                      <div class="w-full h-64 p-5">
                        <img src="{item.image}" class="rounded-xl object-scale-down h-full w-full" alt={item.topic} />
                      </div>
                    </div>
                  </div>
                </div>
              {/each}
            </div>
            <div class="absolute z-30 flex -translate-x-1/2 bottom-5 left-1/2 space-x-3 rtl:space-x-reverse">
              {#each json as item, index}
                <button type="button" class:active={index === currentIndex} class="w-3 h-3 rounded-full" aria-current={index === currentIndex} aria-label="{item.topic}" on:click={() => { goToSlide(index); handleManualNavigation(); }}></button>
              {/each}
            </div>
            <!-- Slider controls -->
            <button type="button" class="absolute top-0 left-0 z-30 flex items-center justify-center h-full px-4 opacity-5 hover:opacity-100 cursor-pointer group focus:outline-none" on:click={() => { prevSlide(); handleManualNavigation(); }} data-carousel-prev>
              <span class="inline-flex items-center justify-center w-10 h-10 rounded-full bg-white/30 dark:bg-gray-800/30 group-hover:bg-white/50 dark:group-hover:bg-gray-800/60 group-focus:ring-4 group-focus:ring-white dark:group-focus:ring-gray-800/70 group-focus:outline-none">
                <svg class="w-4 h-4 text-white dark:text-gray-800 rtl:rotate-180" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 6 10">
                  <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 1 1 5l4 4"/>
                </svg>
                <span class="sr-only">Previous</span>
              </span>
            </button>
            <button type="button" class="absolute top-0 right-0 z-30 flex items-center justify-center h-full px-4 opacity-5 hover:opacity-100 cursor-pointer group focus:outline-none" on:click={() => { nextSlide(); handleManualNavigation(); }} data-carousel-next>
              <span class="inline-flex items-center justify-center w-10 h-10 rounded-full bg-white/30 dark:bg-gray-800/30 group-hover:bg-white/50 dark:group-hover:bg-gray-800/60 group-focus:ring-4 group-focus:ring-white dark:group-focus:ring-gray-800/70 group-focus:outline-none">
                <svg class="w-4 h-4 text-white dark:text-gray-800 rtl:rotate-180" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 6 10">
                  <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m1 9 4-4-4-4"/>
                </svg>
                <span class="sr-only">Next</span>
              </span>
            </button>
            <!-- Indicators -->
             <div class="flex gap-2 absolute bottom-0 -translate-x-1/2 left-1/2 items-center">
                {#each json as item, index}
                  <div class="inline w-3 h-3 rounded-full bg-[#7900ff]" class:bg-[#360a687e]={index !== currentIndex}></div>
                {/each}
             </div>
          </div>
          
        </div>
      </div>
      <div class="col-span-12 lg:col-span-3 h-full">
        <div class=" bg-[#2c2c2c] rounded-xl h-full">
          <div class="w-full h-full p-6">
            <div class=" text-[#ab61ff] font-bold md:text-2xl text-xl text-center">this.GetSkills()</div>

            <div class=" bg-[#360a687e] rounded-full mt-6 h-3 w-full"><div class="one bg-[#7900ff] rounded-full h-3 animate-pulse"></div></div>
            <div class="text-center">Application development</div>

            <div class=" bg-[#360a687e] rounded-full mt-5 h-3 w-full"><div class="two bg-[#7900ff] rounded-full h-3 animate-pulse"></div></div>
            <div class="text-center">Database development</div>

            <div class=" bg-[#360a687e] rounded-full mt-5 h-3 w-full"><div class="five bg-[#7900ff] rounded-full h-3 animate-pulse"></div></div>
            <div class="text-center">Web development</div>
            
            <div class=" bg-[#360a687e] rounded-full mt-5 h-3 w-full"><div class="three bg-[#7900ff] rounded-full h-3 animate-pulse"></div></div>
            <div class="text-center">Graphic user interface</div>

            <div class=" bg-[#360a687e] rounded-full mt-5 h-3 w-full"><div class="four bg-[#7900ff] rounded-full h-3 animate-pulse"></div></div>
            <div class="text-center">Code with fun</div>
          </div>
        </div>
      </div>
    </div>

  </div>
</div>

<style>

@keyframes load-one {
  0%   {width: 0%;}
  90%  {width: 90%;}
}

.one{
  width: 90%;
  animation-name: load-one;
  animation-duration: 3s;
  animation-iteration-count: 1;
}

@keyframes load-two {
  0%   {width: 0%;}
  90%  {width: 80%;}
}

.two{
  width: 80%;
  animation-name: load-two;
  animation-duration: 3s;
  animation-iteration-count: 1;
}

@keyframes load-three {
  0%   {width: 0%;}
  90%  {width: 65%;}
}

.three{
  width: 65%;
  animation-name: load-three;
  animation-duration: 3s;
  animation-iteration-count: 1;
}

@keyframes load-four {
  0%   {width: 0%;}
  90%  {width: 100%;}
}

@keyframes load-five {
  0%   {width: 0%;}
  90%  {width: 50%;}
}

.four{
  width: 100%;
  animation-name: load-four;
  animation-duration: 3s;
  animation-iteration-count: 1;
}

.five{
  width: 50%;
  animation-name: load-five;
  animation-duration: 3s;
  animation-iteration-count: 1;
}

</style>

<script>

  import { onMount, onDestroy } from 'svelte';
  import json from '../../static/assets/projects.json';
  let nowYear = new Date().getFullYear();

  let currentIndex = 0;
  let interval;

  function nextSlide() {
    currentIndex = (currentIndex + 1) % json.length;
  }

  function prevSlide() {
    currentIndex = (currentIndex - 1 + json.length) % json.length;
  }

  function goToSlide(index) {
    currentIndex = index;
  }

  // Set up interval for auto-sliding
  function startInterval() {
    if(interval !== null){
      clearInterval(interval);
    }
    interval = setInterval(nextSlide, 3000); // Change slide every 3 seconds
  }

  // Clear interval on manual navigation
  function handleManualNavigation() {
    clearInterval(interval);
    startInterval();
  }

  // Start the interval when component is mounted
  onMount(() => {
    startInterval();
  });

  // Clear interval when component is destroyed
  onDestroy(() => {
    clearInterval(interval);
  });

</script>