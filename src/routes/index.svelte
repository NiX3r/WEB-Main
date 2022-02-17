<div class="container mx-auto mt-3 mb-3 md:mt-20 text-[#f0f0f0] font-mono">
  <div class="bg-[#515151] rounded-3xl p-7 mx-3">
    <div class="flex flex-col sm:flex-row justify-between items-center space-y-5 sm:space-y-0">
      <div class="bg-[#2c2c2c] rounded-full py-3 px-6 text-[#7900ff] font-bold md:text-3xl text-2xl"><div class=" animate-pulse">Daniel Iliev</div></div>

      <div class="flex">
        <div class="p-2 rounded-full bg-[#2c2c2c] mr-3 hover:bg-[#2d0857]">
          <a href="https://discord.com/invite/g892nvr">
            <img src=".\assets\discord.png" class=" rounded-full h-10 w-10" alt="Discord"/>
          </a>
        </div>

        <div class="p-2 rounded-full bg-[#2c2c2c] mr-3 hover:bg-[#2d0857]">
          <a href="https://github.com/nCodesDotEU">
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

    <div class="grid grid-cols-12 mt-6 gap-6">
      <div class="col-span-12 lg:col-span-3">
        <div class=" bg-[#2c2c2c] rounded-3xl">
          <div class="w-full h-64 p-5">
            <img src="https://picsum.photos/seed/cuako/200/200" class="rounded-xl object-cover h-full w-full" alt="" />
          </div>
        </div>
      </div>
      <div class="col-span-12 lg:col-span-9 h-full">
        <div class="bg-[#2c2c2c] rounded-2xl py-3 px-6 h-full">
          <h1 class="text-[#ab61ff] font-bold md:text-2xl lg:text-left text-center text-xl p-8">a passionate programmer</h1>
          <p class=" ml-10">I'm a young student who's been interested in programming since 2016. I've started learning in C / C++ which lasted me for about 2 years and I felt in love with it. Then I switched to learning Java and somewhat recently C# and with it came SQL connected with it. I can read some other languages as well lik PHP, JS, CSS, HTML, etc. I've already done some projects just for fun or for companies. For example I've developed app for managing house revision connected to remote MySQL server.</p>
        </div>
      </div>
    </div>

    <div class="grid grid-cols-12 mt-6 gap-6">
      <div class="col-span-12 lg:col-span-9 h-full">
        <div class="bg-[#2c2c2c] rounded-2xl py-3 px-6 h-full">
          <div class="grid grid-cols-12 gap-6 pr-5">
            <div class="col-span-12 lg:col-span-8">
              <h1 class="text-[#ab61ff] font-bold md:text-2xl lg:text-left text-center text-xl p-4">{topic}</h1>
              <p class=" ml-10">{description}</p>
              <div class=" text-[#ab61ff] font-bold mt-3 ml-5">Technologies</div> <p class=" ml-10 mb-5">{technologies}</p>
            </div>
            <div class="col-span-12 lg:col-span-4 mt-8">
              <div class="w-full h-64 p-5">
                <img src="{picture}" class="rounded-xl object-cover h-full w-full" alt="" />
              </div>
            </div>
            
          </div>

          <div class="flex flex-row justify-between items-center space-y-5 lg:space-y-0 pr-5 pl-5">
            <div on:click={left}>
              <img class="md:h-10 md:w-10 h-7 w-7" src="./assets/left-arrow.png" alt="Left arrow">
            </div>
            <div class="p-2 rounded-full bg-[#515151] mr-3">
              <a href="{git}">
                <img src="./assets/github.png" class=" rounded-full md:h-10 md:w-10 h-7 w-7" alt="Github">
              </a>
            </div>
            <div class="p-2 rounded-full bg-[#515151] mr-3">
              <a href="{web}">
                <img src="./assets/web.png" class=" rounded-full md:h-10 md:w-10 h-7 w-7" alt="Github">
              </a>
            </div>
            <div on:click={right}>
              <img class="md:h-10 md:w-10 h-7 w-7" src="./assets/right-arrow.png" alt="Left arrow">
            </div>
          </div>

        </div>
      </div>
      <div class="col-span-12 lg:col-span-3 h-full">
        <div class=" bg-[#2c2c2c] rounded-3xl h-full">
          <div class="w-full h-full p-6">
            <div class=" text-[#ab61ff] font-bold md:text-2xl text-xl text-center">this.GetSkills()</div>

            <div class=" bg-[#7809f77e] rounded-full mt-6 h-3 w-full"><div class="one bg-[#7900ff] rounded-full h-3 animate-pulse"></div></div>
            <div class="text-center">Application development</div>

            <div class=" bg-[#7809f77e] rounded-full mt-5 h-3 w-full"><div class="two bg-[#7900ff] rounded-full h-3 animate-pulse"></div></div>
            <div class="text-center">Databases implementation</div>

            <div class=" bg-[#7809f77e] rounded-full mt-5 h-3 w-full"><div class="three bg-[#7900ff] rounded-full h-3 animate-pulse"></div></div>
            <div class="text-center">Graphic user interface</div>

            <div class=" bg-[#7809f77e] rounded-full mt-5 h-3 w-full"><div class="one bg-[#7900ff] rounded-full h-3 animate-pulse"></div></div>
            <div class="text-center">Communication</div>

            <div class=" bg-[#7809f77e] rounded-full mt-5 h-3 w-full"><div class="four bg-[#7900ff] rounded-full h-3 animate-pulse"></div></div>
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

.four{
  width: 100%;
  animation-name: load-four;
  animation-duration: 3s;
  animation-iteration-count: 1;
}

</style>

<script>

  import json from '../../static/assets/projects.json';

  let index = 0;
  let description;
  let topic;
  let git;
  let web;
  let picture;
  let technologies;
  setData();

  let interval;
  interval = setInterval(() => {
      right();
      setData();
    }, 10000);

  function left(){
    if(index === 0){
      index = json.length - 1;
    }
    else{
      index--;
    }
    setData();
  }

  function right(){
    if(index === json.length - 1){
      index = 0;
    }
    else{
      index++;
    }
    setData();
  }

  function setData(){
    description = json[index].description;
    topic = json[index].topic;
    git = json[index].git;
    web = json[index].web;
    picture = json[index].image;
    // @ts-ignore
    technologies = json[index].technologies;
  }

</script>