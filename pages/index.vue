<template>
  <div class="bg-black">
    <AppHeader />

    <div class="relative min-h-screen">
      <div
        class="absolute -top-8 left-1/2 size-48 md:size-72 -translate-x-1/2 rounded-full bg-gradient-to-r from-[#E70D01]/20 via-[#FF5400]/20 to-[#F77D05]/20 blur-[80px] md:blur-[120px] lg:top-[20rem] lg:size-[26rem] lg:blur-[200px] z-0">
      </div>

      <DotPattern
        class="absolute inset-0 size-full fill-white/20 [mask-image:radial-gradient(white,transparent_85%)] pointer-events-none" />

      <div class="relative flex flex-col items-center min-h-[90vh] p-4 space-y-6 md:space-y-8 pt-24 md:pt-48">
        <HeroSection :isScrolled="isScrolled" class="transition-all duration-500" />
        <CallToAction :isScrolled="isScrolled" />
        <CtaFeatures :isScrolled="isScrolled" />

        <div class="flex flex-col items-center text-sm justify-center mb-6 md:hidden animate-fade-up">
          <span
            class="opacity-0 animate-fade-up animation-delay-0 text-xs text-white p-2 px-4 border border-gray-800 mt-16 shadow-inner backdrop-blur-sm rounded-full mb-2 tracking-wide">
            All your business website needs, in one place
          </span>
        </div>
      </div>
    </div>

    <div class="relative -mt-48 md:-mt-64">
      <DotPattern
        class="absolute inset-0 size-full fill-white/20 [mask-image:radial-gradient(white,transparent_85%)] pointer-events-none" />
      <SeoSection :isScrolled="isScrolled" />
    </div>

    <DividerLine />

    <section class="relative py-12">
      <DotPattern
        class="absolute inset-0 size-full fill-white/20 [mask-image:radial-gradient(white,transparent_85%)] pointer-events-none" />
      <div class="max-w-7xl mx-auto px-4">
        <div class="text-center mb-12">
          <h2 class="text-4xl lg:text-5xl text-white tracking-tighter mb-4 font-mono">
            Not Just Your Partners,<br>Your Success Team
          </h2>
          <p class="text-gray-300 max-w-2xl mx-auto leading-relaxed font-mono text-sm">
            When you win, we win. We dive deep into your vision, pushing the boundaries of modern design and
            development. Every iteration, every solution, every breakthrough is fueled by our investment in your
            success.
          </p>
        </div>

        <div class="grid grid-cols-2 lg:grid-cols-3 gap-4">
          <div v-for="(card, index) in capabilities" :key="index"
            class="group p-4 rounded-2xl border border-white bg-transparent"
            :class="`animate-fade-up animation-delay-${index * 200}`">
            <div class="relative rounded-lg w-fit" style="padding: 8px; margin-bottom: 12px;"
              :class="`text-[${gradientColors[index % 3]}]`">
              <div v-html="card.icon" class="w-6 h-6"></div>
            </div>

            <h3 class="text-sm text-white font-medium mb-2 font-mono">{{ card.title }}</h3>
            <p class="text-xs text-gray-400 leading-relaxed font-mono">{{ card.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <DividerLine />

    <SocialProofLogos />
    <section ref="aiSectionRef" class="relative py-12 fade-in">
      <DotPattern
        class="absolute inset-0 size-full fill-white/20 [mask-image:radial-gradient(white,transparent_85%)] pointer-events-none" />
      <div class="max-w-3xl mx-auto px-4 text-center">
        <p class="text-xl md:text-2xl leading-relaxed text-gray-300 max-w-[90%] md:max-w-full mx-auto">
          <span class="text-gradient">AI isn't just a buzzword here</span>&mdash;it's your competitive advantage.
          By integrating <span class="text-gradient">artificial intelligence</span> into our development workflow,
          we dramatically <span class="text-gradient">reduce timelines</span> while elevating quality.
          From rapid prototyping to intelligent testing, we're bringing tomorrow's web development capabilities to your
          project today.
        </p>
      </div>
    </section>

    <DividerLine />

    <section class="relative py-12">
      <DotPattern
        class="absolute inset-0 size-full fill-white/20 [mask-image:radial-gradient(white,transparent_85%)] pointer-events-none" />
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="mb-12 relative">
          <div class="flex items-center gap-3">
            <div class="relative">
              <DotPattern
                class="absolute inset-0 size-full fill-white/20 [mask-image:radial-gradient(white,transparent_85%)] pointer-events-none" />
              <div class="w-8 h-8 rounded-full border border-gray-600"></div>
              <div
                class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-4 h-4 rounded-full bg-[#F77D05]">
              </div>
            </div>
            <h2 class="text-xl sm:text-2xl font-mono text-white">Solutions</h2>
          </div>
          <p class="text-gray-400 mt-4 max-w-2xl text-sm sm:text-base">
            Our clients trust us to turn their boldest ideas into reality. Every project is an opportunity to exceed
            expectations and push boundaries.
          </p>
        </div>

        <div class="relative">
          <DotPattern
            class="absolute inset-0 size-full fill-white/20 [mask-image:radial-gradient(white,transparent_85%)] pointer-events-none" />
          <div class="px-4 pb-8">
            <div class="grid md:hidden gap-4">
              <div class="rounded-3xl p-6 border border-white backdrop-blur-sm min-h-[200px]">
              </div>
              <div class="rounded-3xl p-6 border border-white backdrop-blur-sm min-h-[200px]">
              </div>
              <div class="rounded-3xl p-6 border border-white backdrop-blur-sm min-h-[180px]">
              </div>
              <div class="rounded-3xl p-6 border border-white backdrop-blur-sm min-h-[180px]">
              </div>
              <div class="rounded-3xl p-6 border border-white backdrop-blur-sm min-h-[250px]">
              </div>
              <div class="rounded-3xl p-6 border border-white backdrop-blur-sm min-h-[150px]">
              </div>
              <div class="rounded-3xl p-6 border border-white backdrop-blur-sm min-h-[150px]">
              </div>
              <div class="rounded-3xl p-6 border border-white backdrop-blur-sm min-h-[150px]">
              </div>
            </div>

            <div class="hidden md:grid grid-cols-12 gap-4 auto-rows-[100px]">
              <div class="col-span-6 row-span-2 rounded-3xl p-6 border border-white backdrop-blur-sm">
              </div>

              <div class="col-span-6 row-span-2 rounded-3xl p-6 border border-white backdrop-blur-sm">
              </div>

              <div class="col-span-3 row-span-2 rounded-3xl p-6 border border-white backdrop-blur-sm">
              </div>

              <div class="col-span-3 row-span-2 rounded-3xl p-6 border border-white backdrop-blur-sm">
              </div>

              <div class="col-span-6 row-span-4 rounded-3xl p-6 border border-white backdrop-blur-sm">
              </div>

              <div class="col-span-2 row-span-2 rounded-3xl p-6 border border-white backdrop-blur-sm">
              </div>

              <div class="col-span-2 row-span-2 rounded-3xl p-6 border border-white backdrop-blur-sm">
              </div>

              <div class="col-span-2 row-span-2 rounded-3xl p-6 border border-white backdrop-blur-sm">
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <DividerLine />

    <section class="relative py-12">
      <DotPattern
        class="absolute inset-0 size-full fill-white/20 [mask-image:radial-gradient(white,transparent_85%)] pointer-events-none" />
      <div class="max-w-6xl mx-auto px-8">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div class="flex gap-6">
            <div class="w-12 h-12 rounded-full bg-gradient-to-r from-[#E70D01] to-[#F77D05] flex-shrink-0"></div>
            <div>
              <p class="text-gray-300 text-lg mb-4">"The team's ability to transform our vision into reality exceeded
                our expectations. Their technical expertise and attention to detail made all the difference."</p>
              <p class="text-white font-mono">John Doe</p>
              <p class="text-sm text-gray-400">CEO, Tech Company</p>
            </div>
          </div>
          <div class="flex gap-6">
            <div class="w-12 h-12 rounded-full bg-gradient-to-r from-[#FF5400] to-[#F77D05] flex-shrink-0"></div>
            <div>
              <p class="text-gray-300 text-lg mb-4">"Working with them was a game-changer for our online presence. They
                delivered a website that perfectly captures our brand's essence."</p>
              <p class="text-white font-mono">Jane Smith</p>
              <p class="text-sm text-gray-400">Marketing Director, Brand Co</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <DividerLine />

    <section ref="bigIdeasSectionRef" class="relative py-12 bg-black/20 fade-in">
      <DotPattern
        class="absolute inset-0 size-full fill-white/20 [mask-image:radial-gradient(white,transparent_85%)] pointer-events-none" />
      <div class="max-w-3xl mx-auto px-8 text-center">
        <p class="text-3xl md:text-4xl font-light leading-relaxed text-white">
          <span class="text-gradient">Big ideas</span> energize us. Exceptional results <span
            class="text-gradient">define us.</span> Together we'll create something extraordinary <span
            class="text-gradient">for your customers.</span>
        </p>
      </div>
    </section>

    <DividerLine />

    <section class="relative py-12 overflow-hidden">
      <DotPattern
        class="absolute inset-0 size-full fill-white/20 [mask-image:radial-gradient(white,transparent_85%)] pointer-events-none" />
      <div class="max-w-6xl mx-auto px-8">
        <div class="absolute inset-0 bg-gradient-to-br from-[#E70D01]/10 to-transparent">
          <div class="absolute bottom-0 left-0 right-0">
            <svg viewBox="0 0 400 100" class="w-full">
              <path d="M0,50 Q100,20 200,50 T400,50" fill="none" stroke="#F77D05" stroke-width="0.5" opacity="0.2" />
              <path d="M0,60 Q100,30 200,60 T400,60" fill="none" stroke="#F77D05" stroke-width="0.5" opacity="0.2" />
            </svg>
          </div>
        </div>

        <div class="relative z-10">
          <h2 class="text-4xl md:text-5xl text-white text-center mb-8">Level Up Your Website</h2>
          <p class="text-gray-300 text-center mb-12 text-xl">Transform your digital presence with our expertise</p>

          <div class="flex flex-wrap justify-center gap-6">
            <div class="px-6 py-3 bg-black/40 backdrop-blur-sm rounded-full border border-white text-white">
              Design & Dev Agency
            </div>
            <div class="px-6 py-3 bg-black/40 backdrop-blur-sm rounded-full border border-white text-white">
              Third Party Integrations
            </div>
            <div class="px-6 py-3 bg-black/40 backdrop-blur-sm rounded-full border border-white text-white">
              Tailored Solutions
            </div>
          </div>

          <div class="mt-12 text-center">
            <a href="#"
              class="inline-block px-8 py-4 bg-gradient-to-r from-[#E70D01] to-[#F77D05] rounded-full text-white font-medium hover:opacity-90 transition-opacity">
              Meet Your Success Team ->
            </a>
          </div>
        </div>
      </div>
    </section>

    <footer class="relative py-16 overflow-hidden">
      <div class="absolute inset-0 z-0">
        <div class="absolute top-0 left-1/2 w-[1200px] h-[1200px] -translate-x-1/2 rounded-full 
           bg-gradient-to-r from-[#E70D01]/20 via-[#FF5400]/15 to-[#F77D05]/15
           blur-[150px] opacity-70">
        </div>
      </div>

      <div class="relative z-10 max-w-7xl mx-auto px-8">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
          <div class="space-y-6">
            <div class="flex items-center gap-3">
              <img src="/public/images/TWALogo-Photoroom.png" alt="The Web Agency" class="w-16 h-16">
              <span class="text-white font-mono">TheWebAgency</span>
            </div>

            <div class="flex gap-4 md:pl-2">
              <a href="#"
                class="p-2 bg-black/40 backdrop-blur-sm rounded-lg border border-gray-800/50 hover:-translate-y-1 transition-transform">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 text-[#F77D05]" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor">
                  <path
                    d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.593-11.018-3.714v-2.155z" />
                </svg>
              </a>
              <a href="#"
                class="p-2 bg-black/40 backdrop-blur-sm rounded-lg border border-gray-800/50 hover:-translate-y-1 transition-transform">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 text-[#FF5400]" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor">
                  <path
                    d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
                </svg>
              </a>
              <a href="#"
                class="p-2 bg-black/40 backdrop-blur-sm rounded-lg border border-gray-800/50 hover:-translate-y-1 transition-transform">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 text-[#E70D01]" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor">
                  <path
                    d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z" />
                </svg>
              </a>
            </div>
          </div>

          <div class="space-y-4">
            <h3 class="text-lg font-mono text-white mb-6">Contact</h3>
            <ul class="space-y-4 text-gray-400">
              <li>5544 McKenzie Drive</li>
              <li>Lake In The Hills, IL, 60156</li>
            </ul>
          </div>

          <div class="space-y-4">
            <h3 class="text-lg font-mono text-white mb-6">Get in Touch</h3>
            <div class="space-y-3">
              <a href="tel:+8478579139"
                class="flex items-center gap-3 px-6 py-3 bg-black/40 backdrop-blur-sm rounded-full border border-gray-800/50 text-gray-300 hover:-translate-y-1 transition-all">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 text-[#F77D05]" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                </svg>
                (847) 857-9139
              </a>

              <a href="mailto:thewebagencydev@gmail.com"
                class="flex items-center gap-3 px-6 py-3 bg-black/40 backdrop-blur-sm rounded-full border border-gray-800/50 text-gray-300 hover:-translate-y-1 transition-all">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 text-[#FF5400]" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                </svg>
                thewebagencydev@gmail.com
              </a>

              <a href="#"
                class="flex items-center gap-3 px-6 py-3 bg-black/40 backdrop-blur-sm rounded-full border border-gray-800/50 text-gray-300 hover:-translate-y-1 transition-all">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 text-[#E70D01]" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>
                Find Us
              </a>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import AppHeader from '~/components/layout/appHeader.vue'
import SocialProofLogos from '~/components/socialProofLogos.vue'

import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)

const aiSectionRef = ref(null)
const bigIdeasSectionRef = ref(null)

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('fade-in-visible')
          observer.unobserve(entry.target)
        }
      })
    },
    {
      threshold: 0.2,
      rootMargin: '50px'
    }
  )

  if (aiSectionRef.value) {
    observer.observe(aiSectionRef.value)
  }
  if (bigIdeasSectionRef.value) {
    observer.observe(bigIdeasSectionRef.value)
  }
})

const handleScroll = () => {
  isScrolled.value = window.scrollY > 100
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})

const capabilities = [
  {
    title: 'Full-Stack Excellence',
    description: 'From frontend pixel perfection to backend brilliance, we craft comprehensive solutions that power your digital presence',
    icon: `<svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M16 18l6-6-6-6M8 6l-6 6 6 6" />
            <path d="M2 12h20" />
          </svg>`
  },
  {
    title: 'AI-Enhanced Development',
    description: 'Harnessing advanced AI to accelerate development cycles, squash bugs instantly, and deliver rapid solutions that keep your project moving at full speed',
    icon: `<svg class="w-8 h-8" viewBox="0 0 512 512" xmlns="http://www.w3.org/2000/svg" fill="none" stroke="currentColor" stroke-width="24">
          <path d="M208,512a24.84,24.84,0,0,1-23.34-16l-39.84-103.6a16.06,16.06,0,0,0-9.19-9.19L32,343.34a25,25,0,0,1,0-46.68l103.6-39.84a16.06,16.06,0,0,0,9.19-9.19L184.66,144a25,25,0,0,1,46.68,0l39.84,103.6a16.06,16.06,0,0,0,9.19,9.19l103,39.63A25.49,25.49,0,0,1,400,320.52a24.82,24.82,0,0,1-16,22.82l-103.6,39.84a16.06,16.06,0,0,0-9.19,9.19L231.34,496A24.84,24.84,0,0,1,208,512Zm66.85-254.84h0Z" />
          <path d="M88,176a14.67,14.67,0,0,1-13.69-9.4L57.45,122.76a7.28,7.28,0,0,0-4.21-4.21L9.4,101.69a14.67,14.67,0,0,1,0-27.38L53.24,57.45a7.31,7.31,0,0,0,4.21-4.21L74.16,9.79A15,15,0,0,1,86.23.11,14.67,14.67,0,0,1,101.69,9.4l16.86,43.84a7.31,7.31,0,0,0,4.21,4.21L166.6,74.31a14.67,14.67,0,0,1,0,27.38l-43.84,16.86a7.28,7.28,0,0,0-4.21,4.21L101.69,166.6A14.67,14.67,0,0,1,88,176Z" />
          <path d="M400,256a16,16,0,0,1-14.93-10.26l-22.84-59.37a8,8,0,0,0-4.6-4.6l-59.37-22.84a16,16,0,0,1,0-29.86l59.37-22.84a8,8,0,0,0,4.6-4.6L384.9,42.68a16.45,16.45,0,0,1,13.17-10.57,16,16,0,0,1,16.86,10.15l22.84,59.37a8,8,0,0,0,4.6,4.6l59.37,22.84a16,16,0,0,1,0,29.86l-59.37,22.84a8,8,0,0,0-4.6,4.6l-22.84,59.37A16,16,0,0,1,400,256Z" />
        </svg>`
  },
  {
    title: 'Performance Optimization',
    description: 'We fine tune every aspect of your website for peak performance, delivering lightning fast experiences that keep your users engaged',
    icon: `<svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z" />
          </svg>`
  },
  {
    title: 'Responsive Design',
    description: 'Seamlessly adaptive interfaces that captivate your audience across every device and screen size, ensuring no user is left behind',
    icon: `<svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <rect x="2" y="3" width="14" height="18" rx="2" />
            <rect x="16" y="8" width="6" height="13" rx="2" />
          </svg>`
  },
  {
    title: 'SEO Forward',
    description: 'Built in search engine optimization that puts your business at the forefront of digital discovery, driving organic growth and clicks from day one',
    icon: `<svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <circle cx="11" cy="11" r="8" />
            <path d="M21 21l-4.35-4.35" />
            <path d="M11 8v6M8 11h6" />
          </svg>`
  },
  {
    title: 'Brand Architecture',
    description: 'We transform your brand into a cohesive digital identity, creating memorable interactions that resonate with your audience',
    icon: `<svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M12 19l7-7 3 3-7 7-3-3z" />
            <path d="M18 13l-1.5-7.5L2 2l3.5 14.5L13 18l5-5z" />
            <path d="M2 2l7.586 7.586" />
            <circle cx="11" cy="11" r="2" />
          </svg>`
  }
]

const gradientColors = ['#E70D01', '#FF5400', '#F77D05']
</script>

<style scoped>
html {
  scroll-behavior: smooth;
}

.text-gradient {
  background: linear-gradient(to right, #E70D01, #FF5400, #F77D05);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.fade-in {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.6s ease-out, transform 0.6s ease-out;
}

.fade-in-visible {
  opacity: 1;
  transform: translateY(0);
}

* {
  font-family: "JetBrains Mono", serif;
  font-optical-sizing: auto;
  font-weight: 200;
  font-style: normal;
}

.opacity-0 {
  opacity: 0;
}

.animate-fade-up {
  animation-fill-mode: forwards;
}

.animation-delay-2000 {
  animation-delay: 2000ms;
}

@keyframes fade {
  from {
    opacity: 0;
  }

  to {
    opacity: 1;
  }
}

.text-gradient {
  background: linear-gradient(to right, #E70D01, #FF5400, #F77D05);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.animate-fade {
  animation: fade 0.5s ease-out forwards;
}

.group {
  position: relative;
  transition: transform 0.3s ease;
}

.group:hover {
  transform: translateY(-4px);
}

.group::before {
  content: '';
  position: absolute;
  inset: -1px;
  /* or your desired border width */
  background: linear-gradient(to right, rgba(231, 13, 1, 0.2), rgba(255, 84, 0, 0.2), rgba(247, 125, 5, 0.2));
  border-radius: inherit;
  z-index: -1;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.group:hover::before {
  opacity: 1;
}
</style>
