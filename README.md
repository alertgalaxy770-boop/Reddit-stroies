# Reddit



<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AI Story Video Generator</title>
<script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 font-sans">

<!-- Navbar -->
<nav class="bg-white shadow p-4 flex justify-between items-center">
  <h1 class="text-2xl font-bold text-purple-600">StoryAI</h1>
  <button class="bg-purple-600 text-white px-4 py-2 rounded hover:bg-purple-700">Login</button>
</nav>

<!-- Hero Section -->
<section class="text-center py-16">
  <h2 class="text-4xl font-bold mb-4">Turn Reddit Stories into AI Videos</h2>
  <p class="text-gray-700 mb-6">Paste your story, choose a voice, and generate narration instantly in your browser.</p>
  <button class="bg-purple-600 text-white px-6 py-3 rounded hover:bg-purple-700">Create Free Video</button>
</section>

<!-- Generate Project Section -->
<section class="max-w-3xl mx-auto bg-white p-8 rounded shadow">
  <h3 class="text-2xl font-bold mb-4">Generate AI Narration</h3>
  <textarea id="storyInput" class="w-full border rounded p-2 mb-4" rows="6" placeholder="Paste your Reddit story here..."></textarea>

  <label class="block mb-2 font-semibold">Choose Voice:</label>
  <select id="voiceSelect" class="w-full border rounded p-2 mb-4">
    <!-- Voices will populate automatically -->
  </select>

  <button id="generateBtn" class="bg-purple-600 text-white px-6 py-2 rounded hover:bg-purple-700">Generate Narration</button>

  <div id="audioContainer" class="mt-6 hidden">
    <h4 class="font-semibold mb-2">Your narration is playing via browser TTS!</h4>
    <p class="text-gray-600 text-sm">Click generate to hear audio.</p>
  </div>
</section>

<!-- Footer -->
<footer class="text-center py-6 text-gray-600">
  &copy; 2026 StoryAI. All rights reserved.
</footer>

<!-- JS for Browser TTS -->
<script>
const generateBtn = document.getElementById("generateBtn");
const storyInput = document.getElementById("storyInput");
const voiceSelect = document.getElementById("voiceSelect");
const audioContainer = document.getElementById("audioContainer");

// Populate voices
function populateVoices() {
  const voices = speechSynthesis.getVoices();
  voiceSelect.innerHTML = "";
  voices.forEach(v => {
    if(v.lang.startsWith("en")) {
      const option = document.createElement("option");
      option.value = v.name;
      option.textContent = ${v.name} (${v.lang});
      voiceSelect.appendChild(option);
    }
  });
}

// Some browsers fire this event when voices are ready
speechSynthesis.onvoiceschanged = populateVoices;

// Generate narration
generateBtn.addEventListener("click", () => {
  const text = storyInput.value.trim();
  const selectedVoice = voiceSelect.value;

  if(!text) {
    alert("Please enter a story!");
    return;
  }

  const utterance = new SpeechSynthesisUtterance(text);
  const voice = speechSynthesis.getVoices().find(v => v.name === selectedVoice);
  if(voice) utterance.voice = voice;

  speechSynthesis.speak(utterance);
  audioContainer.classList.remove("hidden");
});

// Initial population
window.onload = () => {
  populateVoices();
};
</script>

</body>
</html>



code this into a full website like wava ai make it exactly the same in htl code

all in 1 line/ file
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AI Story Video Generator</title>
<script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 font-sans">

<!-- Navbar -->
<nav class="bg-white shadow p-4 flex justify-between items-center">
  <h1 class="text-2xl font-bold text-purple-600">StoryAI</h1>
  <button class="bg-purple-600 text-white px-4 py-2 rounded hover:bg-purple-700">Login</button>
</nav>

<!-- Hero Section -->
<section class="text-center py-16">
  <h2 class="text-4xl font-bold mb-4">Turn Reddit Stories into AI Videos</h2>
  <p class="text-gray-700 mb-6">Paste your story, choose a voice, and generate narration instantly in your browser.</p>
  <button class="bg-purple-600 text-white px-6 py-3 rounded hover:bg-purple-700">Create Free Video</button>
</section>

<!-- Generate Project Section -->
<section class="max-w-3xl mx-auto bg-white p-8 rounded shadow">
  <h3 class="text-2xl font-bold mb-4">Generate AI Narration</h3>
  <textarea id="storyInput" class="w-full border rounded p-2 mb-4" rows="6" placeholder="Paste your Reddit story here..."></textarea>

  <label class="block mb-2 font-semibold">Choose Voice:</label>
  <select id="voiceSelect" class="w-full border rounded p-2 mb-4">
    <!-- Voices will populate automatically -->
  </select>

  <button id="generateBtn" class="bg-purple-600 text-white px-6 py-2 rounded hover:bg-purple-700">Generate Narration</button>

  <div id="audioContainer" class="mt-6 hidden">
    <h4 class="font-semibold mb-2">Your narration is playing via browser TTS!</h4>
    <p class="text-gray-600 text-sm">Click generate to hear audio.</p>
  </div>
</section>

<!-- Footer -->
<footer class="text-center py-6 text-gray-600">
  &copy; 2026 StoryAI. All rights reserved.
</footer>

<!-- JS for Browser TTS -->
<script>
const generateBtn = document.getElementById("generateBtn");
const storyInput = document.getElementById("storyInput");
const voiceSelect = document.getElementById("voiceSelect");
const audioContainer = document.getElementById("audioContainer");

// Populate voices
function populateVoices() {
  const voices = speechSynthesis.getVoices();
  voiceSelect.innerHTML = "";
  voices.forEach(v => {
    if(v.lang.startsWith("en")) {
      const option = document.createElement("option");
      option.value = v.name;
      option.textContent = ${v.name} (${v.lang});
      voiceSelect.appendChild(option);
    }
  });
}

// Some browsers fire this event when voices are ready
speechSynthesis.onvoiceschanged = populateVoices;

// Generate narration
generateBtn.addEventListener("click", () => {
  const text = storyInput.value.trim();
  const selectedVoice = voiceSelect.value;

  if(!text) {
    alert("Please enter a story!");
    return;
  }

  const utterance = new SpeechSynthesisUtterance(text);
  const voice = speechSynthesis.getVoices().find(v => v.name === selectedVoice);
  if(voice) utterance.voice = voice;

  speechSynthesis.speak(utterance);
  audioContainer.classList.remove("hidden");
});

// Initial population
window.onload = () => {
  populateVoices();
};
</script>

</body>
</html>


