<script>
  import { onMount } from 'svelte';

  const images = [
    "/generated/image-professional-hvac-technician-installing--1765401627068-0.webp",
    "/generated/image-skilled-plumber-repairing-pipes-under-si-1765401629976-1.webp",
    "/generated/image-electrician-working-on-electrical-panel--1765401632320-2.webp",
    "/generated/image-hvac-technician-in-branded-uniform-check-1765401634810-3.webp",
    "/generated/image-service-technician-in-company-van-drivin-1765401637268-4.webp"
  ];

  let showCookieBanner = $state(true);
</script>

<svelte:head>
  <title>Probook - AI-Powered Dispatch for Home Services</title>
  <meta name="description" content="Increase home service revenue with AI-powered technician-to-job matching. Trusted by 24+ companies with an 18% average ticket lift." />
</svelte:head>

<div class="font-sans text-[#111] antialiased bg-white selection:bg-black selection:text-white">
  <!-- Header -->
  <header class="fixed top-0 left-0 w-full z-50 flex justify-between items-center px-6 py-5 bg-white/90 backdrop-blur-sm border-b border-gray-100">
    <div class="flex items-center gap-2">
      <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M5.0473 17.8386L5.69453 18.9586V18.9601H18.3003L18.9314 17.84H6.34063L6.82626 16.9993H19.4308L20.078 15.8807H7.47237L7.95715 15.0414H16.0358L16.0366 15.0429L16.0375 15.0414H20.5603L20.5612 15.0429L21.2084 13.9228L21.208 13.922L21.2084 13.9213H21.2075L14.9084 3.00677L14.9106 3.00296L14.9062 3.00296L13.6177 3.00296L5.0473 17.8386ZM14.261 4.12767L13.7751 4.96887L18.9438 13.9213H19.9139L14.261 4.12767ZM13.1286 6.08808L12.6467 6.9225L16.6749 13.9006L16.6634 13.9213H17.6511L13.1286 6.08808ZM11.9999 8.04225L8.60411 13.9213H15.3899L11.9999 8.04225ZM6.99833 3.30006C7.33866 3.10343 7.7248 2.99993 8.11786 3L2.30033 13.0776C2.10357 12.7371 2 12.3508 2 11.9575C2 11.5643 2.10357 11.178 2.30033 10.8375L6.17916 4.12006C6.37543 3.77951 6.65798 3.49669 6.99833 3.30006ZM9.08869 3H10.3816L3.43223 15.0384L2.785 13.9184L9.08869 3ZM11.3509 3H12.6424L4.56262 16.9963L3.91691 15.8777L11.3509 3ZM21.7064 13.0598C21.8988 12.7254 22 12.3463 22 11.9605C22 11.5746 21.8988 11.1956 21.7064 10.8611L17.8039 4.10233C17.6108 3.7681 17.3331 3.49057 16.9987 3.2976C16.6644 3.10463 16.2852 3.00302 15.8992 3.00296H15.8741L21.6931 13.082L21.7064 13.0598ZM17.7995 19.7994H6.17916C6.37472 20.1412 6.65692 20.4253 6.99728 20.6232C7.33763 20.8212 7.72414 20.9258 8.11786 20.9269H15.8829C16.2737 20.9261 16.6572 20.8212 16.994 20.6231C17.3309 20.4249 17.6089 20.1406 17.7995 19.7994Z"
          fill="currentColor"
        />
      </svg>
      <span class="text-xl font-medium tracking-tight">Probook</span>
    </div>
    <nav class="hidden md:flex items-center gap-8 text-sm font-medium">
      <a href="#customers" class="hover:opacity-70 transition-opacity">Customers</a>
      <a href="#about" class="hover:opacity-70 transition-opacity">About</a>
      <a href="#careers" class="hover:opacity-70 transition-opacity">Careers</a>
      <a href="#contact" class="bg-black text-white px-4 py-2 rounded-sm hover:bg-gray-800 transition-colors">Book a Demo</a>
    </nav>
  </header>

  <!-- Hero Section -->
  <section class="pt-40 pb-20 px-6 max-w-[1400px] mx-auto">
    <div class="max-w-4xl mb-24">
      <h1 class="text-6xl md:text-7xl font-medium tracking-tight leading-[1.1] mb-8">
        Increase home service<br>revenue with AI
      </h1>
      <div class="flex flex-col md:flex-row justify-between items-start md:items-end gap-8">
        <p class="text-lg md:text-xl max-w-md leading-relaxed text-gray-800">
          AI-powered technician-to-job matching that optimizes sales conversions and delivers an 18% average ticket lift.
        </p>
        <button class="bg-black text-white px-6 py-3 text-sm font-medium rounded-sm hover:bg-gray-800 transition-colors">
          See Probook in Action
        </button>
      </div>
    </div>

    <!-- Hero Images Grid -->
    <div class="grid grid-cols-2 md:grid-cols-5 gap-4">
      {#each images as src, i}
        <div class="aspect-[3/4] overflow-hidden bg-gray-100 rounded-sm">
          <img {src} alt="Home service technician {i + 1}" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
        </div>
      {/each}
    </div>
  </section>

  <!-- Stats Section -->
  <section class="py-32 px-6 max-w-[1400px] mx-auto">
    <div class="text-center mb-20">
      <h2 class="text-2xl md:text-3xl font-medium mb-6 leading-snug">
        Trusted by 24+ home service companies nationwide
      </h2>
      <p class="text-gray-600 text-lg max-w-2xl mx-auto">
        From HVAC to plumbing to electrical, Probook optimizes dispatch operations for multi-truck service companies across America.
      </p>
    </div>

    <!-- Stats Grid -->
    <div class="grid grid-cols-1 md:grid-cols-3 gap-12 max-w-4xl mx-auto">
      <div class="text-center">
        <div class="text-5xl md:text-6xl font-medium mb-3">18%</div>
        <p class="text-gray-600">Average ticket lift</p>
      </div>
      <div class="text-center">
        <div class="text-5xl md:text-6xl font-medium mb-3">50%</div>
        <p class="text-gray-600">Reduction in dispatcher workload</p>
      </div>
      <div class="text-center">
        <div class="text-5xl md:text-6xl font-medium mb-3">22%</div>
        <p class="text-gray-600">Decrease in drive time</p>
      </div>
    </div>
  </section>

  <!-- Dark Section 1: AI Matching -->
  <section class="bg-[#111] text-white py-32 px-6">
    <div class="max-w-[1400px] mx-auto">
      <div class="flex flex-col md:flex-row justify-between items-start mb-20 gap-8">
        <h2 class="text-4xl md:text-5xl font-medium tracking-tight max-w-xl">
          AI-powered matching<br>that drives revenue
        </h2>
        <p class="text-gray-400 text-lg max-w-md leading-relaxed">
          The difference between a $300 band-aid fix and a $20,000 system replacement comes down to matching the right technician to the right job.
        </p>
      </div>

      <!-- Interactive Box -->
      <div class="w-full aspect-video bg-[#1a1a1a] rounded-sm mb-16 flex items-center justify-center relative overflow-hidden">
        <img src="/generated/image-operations-dispatcher-reviewing-schedule-1765401639704-5.webp" alt="Dispatcher operations" class="w-full h-full object-cover opacity-60" />
        <div class="absolute inset-0 bg-gradient-to-t from-[#1a1a1a] via-transparent to-[#1a1a1a]/50"></div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-12 border-t border-white/10 pt-12">
        <div>
          <h3 class="text-lg font-medium mb-3">Optimize for dollars</h3>
          <p class="text-gray-400 leading-relaxed">Match high-performing technicians to the best revenue opportunities.</p>
        </div>
        <div>
          <h3 class="text-lg font-medium mb-3">Data-driven decisions</h3>
          <p class="text-gray-400 leading-relaxed">Replace gut feelings with objective performance metrics.</p>
        </div>
        <div>
          <h3 class="text-lg font-medium mb-3">AutoPilot mode</h3>
          <p class="text-gray-400 leading-relaxed">Let AI build your dispatch board automatically.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Dark Section 2: Efficiency -->
  <section class="bg-[#111] text-white py-32 px-6 border-t border-white/5">
    <div class="max-w-[1400px] mx-auto">
      <div class="flex flex-col md:flex-row justify-between items-start mb-20 gap-8">
        <h2 class="text-4xl md:text-5xl font-medium tracking-tight">
          More revenue,<br>happier teams
        </h2>
        <p class="text-gray-400 text-lg max-w-md leading-relaxed">
          Probook delivers a triple win: increased revenue, reduced dispatcher workload, and satisfied customers with accurate arrival windows.
        </p>
      </div>

      <!-- Interactive Box -->
      <div class="w-full aspect-[2/1] bg-[#1a1a1a] rounded-sm flex items-center justify-center relative overflow-hidden">
        <img src="/generated/image-home-service-company-team-meeting-with-p-1765401644371-7.webp" alt="Team meeting" class="w-full h-full object-cover opacity-50" />
        <div class="absolute inset-0 bg-gradient-to-r from-[#1a1a1a] via-transparent to-[#1a1a1a]"></div>
      </div>
    </div>
  </section>

  <!-- Light Gray Section -->
  <section class="bg-[#f5f5f5] py-24 px-6">
    <div class="max-w-[1400px] mx-auto grid grid-cols-1 md:grid-cols-3 gap-12">
      <div>
        <h3 class="text-lg font-medium mb-3 text-[#111]">Maximize technician revenue</h3>
        <p class="text-gray-600 leading-relaxed">Funnel top performers to the best opportunities for higher conversion rates.</p>
      </div>
      <div>
        <h3 class="text-lg font-medium mb-3 text-[#111]">Reduce dispatcher burden</h3>
        <p class="text-gray-600 leading-relaxed">Cut daily workload by 50% while handling more calls with fewer staff.</p>
      </div>
      <div>
        <h3 class="text-lg font-medium mb-3 text-[#111]">Improve customer satisfaction</h3>
        <p class="text-gray-600 leading-relaxed">Deliver accurate arrival windows and better technician-customer matching.</p>
      </div>
    </div>
  </section>

  <!-- Built for Home Services -->
  <section class="bg-[#f0f0f0] py-32 px-6">
    <div class="max-w-[1400px] mx-auto">
      <div class="mb-16">
        <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6 text-[#111]">
          Built for home service operations
        </h2>
        <p class="text-gray-600 text-lg max-w-2xl leading-relaxed">
          Probook combines real-time performance data with AI optimization to match technicians to jobs based on skills, location, and revenue potential.
        </p>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-start">
        <!-- Visual -->
        <div class="bg-[#111] aspect-video rounded-xl flex items-center justify-center relative overflow-hidden">
          <img src="/generated/image-happy-homeowner-shaking-hands-with-profe-1765401642059-6.webp" alt="Customer satisfaction" class="w-full h-full object-cover" />
        </div>

        <!-- List -->
        <div class="space-y-12 pt-4">
          <div class="group cursor-pointer">
            <h3 class="text-xl font-medium mb-3 text-[#111]">Objective performance metrics</h3>
            <p class="text-gray-600 leading-relaxed">Track exact dollar amounts and technician performance with daily updated metrics visible to your entire dispatch team.</p>
          </div>
          <div class="group cursor-pointer">
            <h3 class="text-xl font-medium mb-3 text-[#111]">Identify A-player technicians</h3>
            <p class="text-gray-600 leading-relaxed">Use data-driven insights to recruit and retain top performers who thrive with objective metrics.</p>
          </div>
          <div class="group cursor-pointer">
            <h3 class="text-xl font-medium mb-3 text-[#111]">Standardize operations</h3>
            <p class="text-gray-600 leading-relaxed">Create consistent dispatching practices that scale as your business grows.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Testimonials Section -->
  <section class="bg-white py-32 px-6" id="customers">
    <div class="max-w-[1400px] mx-auto">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-20 text-[#111] text-center">
        What our customers say
      </h2>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
        <!-- Testimonial 1 -->
        <div class="bg-[#f5f5f5] p-8 rounded-sm">
          <p class="text-lg mb-6 leading-relaxed text-gray-800">
            "Probook gave us a triple win: more revenue, happier dispatchers, and satisfied customers."
          </p>
          <div class="border-t border-gray-300 pt-4">
            <p class="font-medium">Jim Sloan</p>
            <p class="text-sm text-gray-600">General Manager, TR Miller Heating, Cooling & Plumbing</p>
          </div>
        </div>

        <!-- Testimonial 2 -->
        <div class="bg-[#f5f5f5] p-8 rounded-sm">
          <p class="text-lg mb-6 leading-relaxed text-gray-800">
            "Since integrating Probook into our operations, we've seen our average ticket value soar by an impressive 18%."
          </p>
          <div class="border-t border-gray-300 pt-4">
            <p class="font-medium">Alyssa Porta</p>
            <p class="text-sm text-gray-600">Operations Director, Lion Home Service</p>
          </div>
        </div>

        <!-- Testimonial 3 -->
        <div class="bg-[#f5f5f5] p-8 rounded-sm">
          <p class="text-lg mb-6 leading-relaxed text-gray-800">
            "If you take Probook away, I quit. It has made our dispatching more efficient, allowing us to handle more calls without increasing staff."
          </p>
          <div class="border-t border-gray-300 pt-4">
            <p class="font-medium">Andrea Williams</p>
            <p class="text-sm text-gray-600">Lead Dispatcher, Blake Brothers</p>
          </div>
        </div>

        <!-- Testimonial 4 -->
        <div class="bg-[#f5f5f5] p-8 rounded-sm">
          <p class="text-lg mb-6 leading-relaxed text-gray-800">
            "Probook has halved the amount of work we do daily. The results speak for themselves."
          </p>
          <div class="border-t border-gray-300 pt-4">
            <p class="font-medium">Krystin Hines</p>
            <p class="text-sm text-gray-600">Lead Dispatcher, Lion Home Service</p>
          </div>
        </div>
      </div>

      <!-- Customer Results -->
      <div class="bg-[#111] text-white p-12 rounded-sm">
        <h3 class="text-2xl font-medium mb-8">TR Miller Results</h3>
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
          <div>
            <div class="text-3xl font-medium mb-2">$190K</div>
            <p class="text-gray-400 text-sm">Additional revenue in June alone</p>
          </div>
          <div>
            <div class="text-3xl font-medium mb-2">22.3%</div>
            <p class="text-gray-400 text-sm">Reduction in drive time</p>
          </div>
          <div>
            <div class="text-3xl font-medium mb-2">50.1%</div>
            <p class="text-gray-400 text-sm">Increase in billable hours</p>
          </div>
          <div>
            <div class="text-3xl font-medium mb-2">61.8%</div>
            <p class="text-gray-400 text-sm">More jobs per day for top performers</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Integration Section -->
  <section class="bg-[#fffcf8] py-32 px-6">
    <div class="max-w-[1400px] mx-auto">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-20 text-[#111]">
        Seamless integration
      </h2>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
        <!-- Card 1 -->
        <div>
          <div class="w-14 h-14 bg-[#111] text-white flex items-center justify-center rounded-sm mb-8">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
              <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5 21 12m0 0-7.5 7.5M21 12H3" />
            </svg>
          </div>
          <h3 class="text-lg font-medium mb-3 text-[#111]">ServiceTitan integration</h3>
          <p class="text-gray-600 leading-relaxed">Official partner integration with the leading field service management platform.</p>
        </div>

        <!-- Card 2 -->
        <div>
          <div class="w-14 h-14 bg-[#111] text-white flex items-center justify-center rounded-sm mb-8">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6A2.25 2.25 0 0 1 6 3.75h2.25A2.25 2.25 0 0 1 10.5 6v2.25a2.25 2.25 0 0 1-2.25 2.25H6a2.25 2.25 0 0 1-2.25-2.25V6ZM3.75 15.75A2.25 2.25 0 0 1 6 13.5h2.25a2.25 2.25 0 0 1 2.25 2.25V18a2.25 2.25 0 0 1-2.25 2.25H6A2.25 2.25 0 0 1 3.75 18v-2.25ZM13.5 6a2.25 2.25 0 0 1 2.25-2.25H18A2.25 2.25 0 0 1 20.25 6v2.25A2.25 2.25 0 0 1 18 10.5h-2.25a2.25 2.25 0 0 1-2.25-2.25V6ZM13.5 15.75a2.25 2.25 0 0 1 2.25-2.25H18a2.25 2.25 0 0 1 2.25 2.25V18A2.25 2.25 0 0 1 18 20.25h-2.25A2.25 2.25 0 0 1 13.5 18v-2.25Z" />
            </svg>
          </div>
          <h3 class="text-lg font-medium mb-3 text-[#111]">Nexstar network</h3>
          <p class="text-gray-600 leading-relaxed">Trusted by Nexstar members and aligned with industry best practices.</p>
        </div>

        <!-- Card 3 -->
        <div>
          <div class="w-14 h-14 bg-[#111] text-white flex items-center justify-center rounded-sm mb-8">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 13.5l10.5-11.25L12 10.5h8.25L9.75 21.75 12 13.5H3.75z" />
            </svg>
          </div>
          <h3 class="text-lg font-medium mb-3 text-[#111]">Fast deployment</h3>
          <p class="text-gray-600 leading-relaxed">Get up and running quickly with dedicated deployment support.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Careers Section -->
  <section class="bg-white py-32 px-6" id="careers">
    <div class="max-w-[1400px] mx-auto">
      <div class="max-w-3xl mx-auto text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6 text-[#111]">
          Join the fastest-growing AI startup in New York
        </h2>
        <p class="text-gray-600 text-lg leading-relaxed">
          We're a small, high-performing team solving complex problems in a $700B industry. All positions are full-time in New York City.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-6 max-w-4xl mx-auto">
        <div class="border border-gray-200 p-6 rounded-sm hover:border-gray-400 transition-colors">
          <h3 class="text-lg font-medium mb-2">Founding Account Executive</h3>
          <p class="text-gray-600 text-sm mb-4">Sales · New York City</p>
          <a href="#contact" class="text-sm font-medium hover:underline">Learn more →</a>
        </div>

        <div class="border border-gray-200 p-6 rounded-sm hover:border-gray-400 transition-colors">
          <h3 class="text-lg font-medium mb-2">Deployment Strategist</h3>
          <p class="text-gray-600 text-sm mb-4">Operations · New York City</p>
          <a href="#contact" class="text-sm font-medium hover:underline">Learn more →</a>
        </div>

        <div class="border border-gray-200 p-6 rounded-sm hover:border-gray-400 transition-colors">
          <h3 class="text-lg font-medium mb-2">Software Engineer - Backend</h3>
          <p class="text-gray-600 text-sm mb-4">Engineering · New York City</p>
          <a href="#contact" class="text-sm font-medium hover:underline">Learn more →</a>
        </div>

        <div class="border border-gray-200 p-6 rounded-sm hover:border-gray-400 transition-colors">
          <h3 class="text-lg font-medium mb-2">Software Engineer - ML</h3>
          <p class="text-gray-600 text-sm mb-4">Engineering · New York City</p>
          <a href="#contact" class="text-sm font-medium hover:underline">Learn more →</a>
        </div>

        <div class="border border-gray-200 p-6 rounded-sm hover:border-gray-400 transition-colors">
          <h3 class="text-lg font-medium mb-2">Software Engineer - Product</h3>
          <p class="text-gray-600 text-sm mb-4">Engineering · New York City</p>
          <a href="#contact" class="text-sm font-medium hover:underline">Learn more →</a>
        </div>

        <div class="border border-gray-200 p-6 rounded-sm hover:border-gray-400 transition-colors bg-[#f5f5f5]">
          <h3 class="text-lg font-medium mb-2">General Application</h3>
          <p class="text-gray-600 text-sm mb-4">All Departments · New York City</p>
          <a href="#contact" class="text-sm font-medium hover:underline">Apply now →</a>
        </div>
      </div>
    </div>
  </section>

  <!-- CTA Banner -->
  <section class="px-6 py-12" id="contact">
    <div class="max-w-[1400px] mx-auto border border-gray-100 rounded-xl p-8 md:p-12 flex flex-col md:flex-row justify-between items-center gap-8 bg-white shadow-sm">
      <div class="flex items-center gap-6">
        <div class="flex gap-1 h-8">
           <div class="w-2 bg-black h-full"></div>
           <div class="w-2 bg-black h-full"></div>
           <div class="w-2 bg-black h-full"></div>
           <div class="w-2 bg-black h-full opacity-50"></div>
        </div>
        <h2 class="text-2xl md:text-3xl font-medium tracking-tight">See the revenue lift for yourself</h2>
      </div>
      <button class="bg-black text-white px-8 py-3 text-sm font-medium rounded-sm hover:bg-gray-800 transition-colors whitespace-nowrap">
        Book a Demo
      </button>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-white pt-20 pb-10 px-6 border-t border-gray-100" id="about">
    <div class="max-w-[1400px] mx-auto">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-12 md:gap-24 mb-20">
        <div class="col-span-1 md:col-span-2">
          <div class="flex items-center gap-2 mb-2">
            <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M5.0473 17.8386L5.69453 18.9586V18.9601H18.3003L18.9314 17.84H6.34063L6.82626 16.9993H19.4308L20.078 15.8807H7.47237L7.95715 15.0414H16.0358L16.0366 15.0429L16.0375 15.0414H20.5603L20.5612 15.0429L21.2084 13.9228L21.208 13.922L21.2084 13.9213H21.2075L14.9084 3.00677L14.9106 3.00296L14.9062 3.00296L13.6177 3.00296L5.0473 17.8386ZM14.261 4.12767L13.7751 4.96887L18.9438 13.9213H19.9139L14.261 4.12767ZM13.1286 6.08808L12.6467 6.9225L16.6749 13.9006L16.6634 13.9213H17.6511L13.1286 6.08808ZM11.9999 8.04225L8.60411 13.9213H15.3899L11.9999 8.04225ZM6.99833 3.30006C7.33866 3.10343 7.7248 2.99993 8.11786 3L2.30033 13.0776C2.10357 12.7371 2 12.3508 2 11.9575C2 11.5643 2.10357 11.178 2.30033 10.8375L6.17916 4.12006C6.37543 3.77951 6.65798 3.49669 6.99833 3.30006ZM9.08869 3H10.3816L3.43223 15.0384L2.785 13.9184L9.08869 3ZM11.3509 3H12.6424L4.56262 16.9963L3.91691 15.8777L11.3509 3ZM21.7064 13.0598C21.8988 12.7254 22 12.3463 22 11.9605C22 11.5746 21.8988 11.1956 21.7064 10.8611L17.8039 4.10233C17.6108 3.7681 17.3331 3.49057 16.9987 3.2976C16.6644 3.10463 16.2852 3.00302 15.8992 3.00296H15.8741L21.6931 13.082L21.7064 13.0598ZM17.7995 19.7994H6.17916C6.37472 20.1412 6.65692 20.4253 6.99728 20.6232C7.33763 20.8212 7.72414 20.9258 8.11786 20.9269H15.8829C16.2737 20.9261 16.6572 20.8212 16.994 20.6231C17.3309 20.4249 17.6089 20.1406 17.7995 19.7994Z"
                fill="currentColor"
              />
            </svg>
            <h3 class="text-xl font-medium">Probook</h3>
          </div>
          <p class="text-gray-500 text-lg mb-6">AI-Powered Dispatch for Home Services</p>
          <p class="text-gray-600 text-sm max-w-md">
            Based in New York City, we're the fastest-growing AI startup transforming the $700B home services industry.
          </p>
        </div>

        <div>
          <ul class="space-y-4 text-sm font-medium">
            <li><a href="#customers" class="hover:underline">Customers</a></li>
            <li><a href="#careers" class="hover:underline">Careers</a></li>
            <li><a href="#contact" class="hover:underline">Contact</a></li>
          </ul>
        </div>

        <div>
          <h4 class="text-sm font-medium mb-4">Partners</h4>
          <ul class="space-y-4 text-sm text-gray-600">
            <li>Nexstar Network</li>
            <li>ServiceTitan</li>
          </ul>
        </div>
      </div>

      <div class="flex flex-col md:flex-row justify-between items-end text-[10px] text-gray-400 uppercase tracking-wider gap-4">
        <div class="flex gap-8">
          <span>Probook 2025</span>
        </div>
        <div class="flex gap-8">
          <a href="#" class="hover:text-gray-600">Terms of use</a>
          <a href="#" class="hover:text-gray-600">Privacy Policy</a>
        </div>
      </div>
    </div>
  </footer>

  <!-- Cookie Banner -->
  {#if showCookieBanner}
    <div class="fixed bottom-6 right-6 max-w-sm bg-white border border-gray-100 shadow-xl p-6 rounded-sm z-50 text-xs text-gray-600">
      <p class="mb-4 leading-relaxed">
        We use cookies. See our <a href="#" class="underline text-black">Privacy Policy</a> for more information.
      </p>
      <button onclick={() => showCookieBanner = false} class="bg-black text-white px-4 py-2 rounded-sm font-medium hover:bg-gray-800 transition-colors">
        Got it
      </button>
    </div>
  {/if}
</div>

<style>
  :global(body) {
    font-family: 'Inter', sans-serif;
  }
  .perspective-1000 {
    perspective: 1000px;
  }
  .transform-style-3d {
    transform-style: preserve-3d;
  }
</style>

