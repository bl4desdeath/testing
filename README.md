<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Music and Memory Experiment</title>
  <style>
    body {
      background-color: #d3d3d3; /* light gray */
      color: #000000;
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 2em;
      padding: 20px;
      text-align: center;
    }
    .hidden {
      display: none;
    }
    iframe {
      width: 100%;
      height: 600px;
      border: none;
    }
    audio {
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <h1>Welcome to the Music and Memory Experiment</h1>
  
  <div id="step1">
    <p>Please fill out the following form to enter your age:</p>
    <iframe src="https://forms.gle/s6o4JAw6ciAPV4q39"></iframe>
    <button onclick="nextStep(2)">Next</button>
  </div>

  <div id="step2" class="hidden">
    <p>Read the following paragraph in silence:</p>
    <p>Bees are small flying insects known for their role in pollination and honey production. They live in organized colonies, with a queen, worker bees, and drones each having specific roles. The queen lays eggs, while worker bees gather nectar, make honey, and care for the hive. Bees use their fuzzy bodies to transfer pollen from flower to flower, helping plants reproduce. Their buzzing sound comes from rapidly beating wings that also allow them to hover and change direction mid-air. Bees communicate through a special waggle dance that shows the direction and distance to food. Despite their tiny size, they are vital to ecosystems and agriculture. Without bees, many fruits, vegetables, and nuts would become scarce. Bees face threats from pesticides, habitat loss, and climate change. Protecting them means supporting a balanced and healthy environment for all living things. There are over 20,000 known species of bees, ranging from the common honeybee to solitary species like the mason bee. Each species plays a unique role in its ecosystem, with some specializing in pollinating specific types of plants. Bumblebees, for example, are especially good at pollinating crops like tomatoes through a process called buzz pollination. Bees have excellent memory and can recognize human faces and specific flowers. Their sense of smell is incredibly sensitive, allowing them to find nectar even in low concentrations. Honeybees produce wax from glands on their abdomen to construct intricate honeycombs for storing honey and raising young. A single bee can visit thousands of flowers in a day. Despite their hard work, honeybees only produce about a twelfth of a teaspoon of honey in their lifetimes. Many plants depend entirely on bees for pollination, making these insects essential for biodiversity. Urban beekeeping has become popular in recent years, helping increase awareness about the importance of bees. Beekeepers must monitor hives for diseases like colony collapse disorder, which has caused major bee population declines. Some governments have introduced bans on harmful pesticides to help protect pollinators. Flower-rich gardens and wildflower strips along fields offer bees safe feeding areas. Education about bees in schools and communities helps encourage conservation. By planting native flowers and reducing chemical use, individuals can contribute to the survival of bee populations.</p>
    <button onclick="nextStep(3)">Take The Quiz</button>
  </div>

  <div id="step3" class="hidden">
    <p>Please complete the quiz below.:</p>
    <p>PLEASE REMEMBER YOUR RESULT.</p>
    <iframe src="https://forms.gle/kHMc6pUioEaJ1YB48"></iframe>
    <button onclick="assignMusic()">Next</button>
  </div>

  <div id="step4" class="hidden">
    <p>Read the following paragraph while music plays:</p>
    <p>Lena, a clever inventor, and Kai, a daring sky-pilot, lived in a floating city above the clouds. One morning, Lena discovered a map hidden inside an old mechanical bird she'd been repairing. The map pointed to the lost island of Aerith, said to hold the secrets of ancient sky energy. Eager for adventure, Kai fueled up his airship, and they set off into the unknown. Storms battered their path, forcing Lena to jury-rig a broken wing with a lightning rod and spare brass gears. Wind howled through the rigging as Kai fought the controls, his eyes fixed on the swirling horizon. They passed through pockets of strange weather—sudden hail, eerie calm, and even flashes of green lightning. At night, Lena studied the map by lantern light, tracing forgotten symbols etched in silver ink. They encountered a flock of iron-feathered sky-crows, which nearly shredded their balloon canopy before Kai veered into a tunnel of clouds. As they reached the storm’s eye, a massive cloud serpent rose from the mist, guarding the entrance to Aerith. Lena distracted it with a flash bomb while Kai dove through a narrow canyon of clouds. The serpent’s roar echoed through the sky, shaking the airship’s hull. Safely inside, they found Aerith glowing with bioluminescent vines and levitating stones. Strange birds with translucent wings circled above, singing haunting melodies in the wind. The island’s gravity shifted unpredictably, forcing Lena and Kai to tread carefully across floating platforms. In the heart of the island, a temple pulsed with power, sealed by an ancient puzzle. Lena deciphered the symbols while Kai kept watch for danger. Each symbol glowed as it clicked into place, releasing a hum that vibrated the very air. Just as they solved the final piece, the serpent returned enraged. It crashed through the outer walls of the temple, shattering columns of crystal. Kai fought it off with aerial maneuvers, while Lena retrieved a crystal humming with energy. She clung to the deck as the ground trembled and Aerith began to collapse into itself. With the island collapsing, they escaped moments before it vanished into the clouds. A wave of wind pushed them higher, and they soared silently for a moment in the open blue. Back home, the crystal powered their city for a generation. The city’s engines sang a new song, brighter and steadier than before. The two friends stood at the edge of the skyport, already dreaming of the next adventure. As the sun dipped behind the clouds, their silhouettes stood tall against the orange light, hearts alight with discovery.</p>
    <audio id="assignedAudio" controls autoplay loop></audio>
    <button onclick="nextStep(5)">Take The Quiz</button>
  </div>

  <div id="step5" class="hidden">
    <p>Please complete the second quiz below:</p>
    <p>PLEASE REMEMBER YOUR RESULT.</p>
    <iframe src="https://forms.gle/yv8Eh8jJyBjKx5LHA"></iframe>
    <button onclick="nextStep(6)">Next</button>
  </div>

<div id="step6" class="hidden">
  <p>Paste a YouTube link to a song of your choice:</p>
  <input type="text" id="userSong" placeholder="Paste your YouTube URL here">
  <button onclick="playUserSong()">Submit and Continue</button>
</div>

<div id="step7" class="hidden">
    <p>Read the following paragraph while your chosen song plays:</p>
    <p><em>[Insert Third Paragraph Text Here]</em></p>
 <div id="youtubeContainer"></div>
  <button onclick="nextStep(8)">Continue to Final Quiz</button>
</div>


  <div id="step8" class="hidden">
    <p>Please complete the third quiz below:</p>
    <p>PLEASE REMEMBER YOUR RESULT.</p>
    <iframe src="https://docs.google.com/forms/d/e/untitled/viewform?embedded=true"></iframe>
    <button onclick="nextStep(9)">Final Step</button>
  </div>

  <div id="step9" class="hidden">
    <p>Enter your quiz scores and provide feedback:</p>
    <iframe src="https://forms.gle/pW17vYh1QDzkrF3d9"></iframe>
    <p>Thank you for participating!</p>
  </div>

  <script>
    function nextStep(step) {
      for (let i = 1; i <= 9; i++) {
        document.getElementById('step' + i).classList.add('hidden');
      }
      document.getElementById('step' + step).classList.remove('hidden');
    }

    function assignMusic() {
      const musicLinks = [
        'https://example.com/classical.mp3',
        'https://example.com/electronic.mp3',
        'https://example.com/pop.mp3',
        'https://example.com/lofi.mp3',
        'https://example.com/instrumental.mp3'
      ];
      const randomIndex = Math.floor(Math.random() * musicLinks.length);
      const audio = document.getElementById('assignedAudio');
      audio.src = musicLinks[randomIndex];
      nextStep(4);
    }

function playUserSong() {
  const url = document.getElementById('userSong').value.trim();
  const youtubeContainer = document.getElementById('youtubeContainer');

  // Extract YouTube Video ID
  const match = url.match(/(?:youtube\.com\/(?:watch\?v=|embed\/)|youtu\.be\/)([^\s&?]+)/);

  if (!match || !match[1]) {
    alert('Please enter a valid YouTube URL.');
    return;
  }

  const videoId = match[1];
  const embedUrl = `https://www.youtube.com/embed/${videoId}?autoplay=1&loop=1&playlist=${videoId}&rel=0`;

  youtubeContainer.innerHTML = `
    <iframe width="0" height="0" src="${embedUrl}" 
      frameborder="0" allow="autoplay; encrypted-media" 
      allowfullscreen></iframe>
  `;

  nextStep(7);
}


  </script>
</body>
</html>
