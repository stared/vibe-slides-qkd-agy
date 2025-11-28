---
theme: seriph
background: ./cyberpunk_background_anime_1764262562697.png
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Device Independent QKD
  Presentation for Hong Kong Audience
drawings:
  persist: false
transition: slide-left
title: Device Independent QKD
---

# Device Independent QKD

<div class="text-2xl opacity-80">
Trusting the Quantum World, Not the Devices
</div>

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/pmigdal/nano-slides" target="_blank" alt="GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

---
layout: two-cols
---

<template v-slot:default>
# The Problem: Trust

Traditional QKD relies on trusting the devices.

- **Source**: Must emit perfect qubits.
- **Detectors**: Must measure exactly as specified.
- **Reality**: Devices are imperfect and hackable.

What if the devices were built by your enemy?
</template>

<template v-slot:right>
<div class="flex flex-col items-center justify-center h-full">
  <img src="./eve_anime_character_1764262460827.png" class="h-60 rounded-xl shadow-lg" />
  <p class="text-sm mt-2 opacity-70">Eve could have built your devices!</p>
</div>
</template>

---
layout: center
class: text-center
---

# The Players

<div class="grid grid-cols-3 gap-8 mt-8">
  <CharacterProfile 
    name="Alice" 
    role="The Sender" 
    image="./alice_v5.png" 
    color="blue" 
  />
  <CharacterProfile 
    name="Bob" 
    role="The Receiver" 
    image="./bob_v4.png" 
    color="green" 
  />
  <CharacterProfile 
    name="Eve" 
    role="The Eavesdropper" 
    image="./eve_anime_character_1764262460827.png" 
    color="purple" 
  />
</div>

---

# The Setup

<div class="grid grid-cols-2 gap-4">
<div>

We use an **Entangled Source** that distributes particles to Alice and Bob.

They measure these particles using random settings.

Crucially, they don't need to trust the source or the measurement devices!

</div>
<div class="flex justify-center">
  <img src="./quantum_source_anime_1764262533751.png" class="h-60 rounded-lg shadow-blue-500/50 shadow-lg" />
</div>
</div>

---

# Bell's Inequality: The Litmus Test

<div class="flex items-center justify-between mt-8">
  <div class="w-1/2 pr-4">
    <p class="mb-4">
      If the devices are behaving classically (or are pre-programmed by Eve), they must obey <b>Bell's Inequality</b>.
    </p>
    <div class="my-4">
      $$ S \leq 2 $$
    </div>
    <p class="mt-4">
      But quantum mechanics allows:
    </p>
    <div class="text-xl font-bold text-blue-400">
      $$ S = 2\sqrt{2} \approx 2.82 $$
    </div>
  </div>
  <div class="w-1/2">
    <img src="./measurement_device_anime_1764262548611.png" class="rounded-lg shadow-lg" />
  </div>
</div>

---
layout: center
class: text-center
---

# Device Independence

<div class="text-xl">
If $S > 2$, we <b>know</b> the system is quantum and entangled.
</div>

<div class="mt-8 opacity-80">
This guarantees secrecy, even if the devices were built by Eve herself!
</div>

<div class="mt-12 grid grid-cols-2 gap-8 w-2/3 mx-auto">
  <div class="p-4 bg-white/10 rounded-xl">
    <div class="text-4xl mb-2">🔒</div>
    <div>Secure Key</div>
  </div>
  <div class="p-4 bg-white/10 rounded-xl">
    <div class="text-4xl mb-2">🚫</div>
    <div>No Eavesdropping</div>
  </div>
</div>

---
layout: center
class: text-center
---

# Thank You!

<div class="flex justify-center gap-4 mt-8">
  <img src="./alice_v5.png" class="h-32 rounded-full opacity-80" />
  <img src="./bob_v4.png" class="h-32 rounded-full opacity-80" />
</div>

<div class="mt-8 text-sm opacity-50">
  Created with Slidev & Nano Banana Pro
</div>
