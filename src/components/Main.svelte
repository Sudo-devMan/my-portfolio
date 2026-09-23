
<script>
  import Step from './Step.svelte';

  let steps = [
    {name: "RemShare", icon: "fa-solid fa-share-nodes", link: "https://remshare.vercel.app"},
    {name: "ExtraPolation", icon: "fa-solid fa-calculator", link: "https://extra-polation.vercel.app"},
    {name: "Mamochoko", icon: "fa-solid fa-book", link: "https://mamochoko.vercel.app"},
    {name: "DaRentals", icon: "fa-solid fa-house", link: "https://darentals.vercel.app"}
  ]

  let benefits = [
    {name: "a self taught dev", description: "Since grade 9 I have been using various <span class=\"poppins text-violet-400\">online resources to learn</span> programming. Along the way I picked up useful skills that I can use to help businesses of all sizes to grow and expand their reach. I have built all sorts of amazing <span class=\"poppins text-violet-400\">projects along the way for myself and for various clients.</span> "},
    {name: "a ui and ux designer", description: "I can design various types of user interfaces and user experiences using tools like <span class=\"poppins text-violet-400\">Figma and Miro</span>, and implement the designs using React.js, Svelte, and Next.js. Because of my design skills I <span class=\"poppins text-violet-400\">can take any 5/10 website design and bring it back to life</span> with the skills that I have acquired!"},
    {name: "an excellent communicator", description: "I value <span class=\"poppins text-violet-400\">clear and concise verbal communication</span> when it comes to working with people. Because I believe anything can be achieved smoothly without misunderstanding when good communication is involved in the conversation."}
  ]
</script>

<main class="flex flex-col flex-1 p-4">
  <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-3">
    <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Bonjour! Je suis <span class="poppins text-violet-400">Hendrick</span> Mashamaite <br/> Full Stack Backend-first <span class="poppins text-violet-400">Developer</span>
      </h2>
      <p class="text-base md:text-lg">
        Unfortunately <span class="poppins text-violet-400">I am not bilingual</span>. However, I do speak Javascript, Typescript, Python, Java, Bash, SQL, Lua, and MQL5. <span class="poppins text-violet-400">Small list, I know!</span>
      </p>
      <a class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 rounded-full bg-white text-slate-950 cursor-pointer" href="https://wa.me/+27720727038" target="_blank">
        <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"></div>
        <h4 class="relative z-9">Get in touch &rarr;</h4>
      </a>
    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <img src={"images/profile.jpg"} alt="my pic" class="object-cover z-[2] max-h-[70vh]"/>
    </div>
  </section>

  <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        Billion dollar Elon Musk type projects of mine :)
      </h6>
      <h3>
        Wanna see <span class="poppins text-violet-400">my work</span>?
      </h3>
    </div>
    <a href={"https://github.com/Sudo-devMan"} target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200">
        <i class="fa-brands fa-github"></i>
        <p>Check out my GitHub</p>
    </a>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>A file sharing platform made for long distance, bluetooth-less, file sharing created with <strong class="text-violet-400">React.js + Nest.js, AWS S3 for object storage, and Neon for Postgres database</strong></Step>
      <Step step={steps[1]}>A mathematics study material website for high school students. Made with <strong class="text-violet-400">React.js, Express.js, AWS S3 for object storage, and Neon for Postgres database</strong></Step>
      <Step step={steps[2]}>A website for my school. It also features an administration site created with <strong class="text-violet-400">React.js, BootstrapCSS, Django Rest Framework, Supabase for object storage, and Neon for Postgres database</strong></Step>
    </div>
  </section>

  <section id="about" class="py-20 pt-10 sm:pt-16 lg:p-32 flex flex-col gap-16 sm:gap-20 md-gap-24 relative">
    <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
      <h6 class="text-lg sm:text-xl md:text-2xl">Wanna know more?</h6>
      <h3 class="font-semibold text-3xl xm:text-4xl md:text-5xl">
        a bit <span class="poppins text-violet-400">about</span> moi
      </h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
      {#each benefits as benefit, i}
        <div class="flex gap-6">
          
          <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500">
            0{i+1}
          </p>
          <div class="flex flex-col gap-6 sm:gap-8">
            <h3 class="text-2xl sm:text-3xl md:text-5xl">
              {benefit.name}
            </h3>
            <p>{@html benefit.description}</p>
          </div>
        </div>
      {/each}
    </div>
    <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">The <span class="text-violet-400 poppins">Complete</span> Package</h5>
    <div class="flex flex-col overflow-x-scroll gap-10 max-w-[900px] mx-auto w-full">
      <table class="bg-black text-slate-700 rounded text-center">
        <thead class="border-b border-solid border-slate-200">
          <tr class="">
            <th></th>
            <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
            <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
            <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
            <th class="whitespace-nowrap text-white bg-violet-700 p-2 px-4">Me</th>
          </tr>
        </thead>
        <tbody>
          <tr class="border-b border-solid border-slate-200">
            <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Dedication</td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Fast Learner</td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>  <tr class="border-b border-solid border-slate-200">
            <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Team Player</td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>  <tr class="border-b border-solid border-slate-200">
            <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Descipline</td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
      <p>scroll to see more :-) &rarr;</p>
    </div>
    <p class="mx-auto">I will be your best decision ever :)</p>
  </section>
</main>
