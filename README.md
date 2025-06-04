<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Biologie Abitur 2025 – Grundkurs</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  <style>
    .quiz-card { display: none; }
    .quiz-card.active { display: block; }
    .diagram-label {
      cursor: pointer;
      font-weight: bold;
      color: #065f46;
    }
    .diagram-label:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body class="bg-gray-50 text-gray-800">
  <header class="bg-green-600 text-white p-6">
    <h1 class="text-3xl font-bold">Biologie Lernen – NRW Abitur 2025 (Grundkurs)</h1>
    <p class="mt-2">Interaktives Lernen mit Erklärungen, Diagrammen, Lernspielen und Quiz</p>
  </header>

  <nav class="bg-green-100 p-4 flex gap-4 flex-wrap">
    <a href="#physiology" class="text-green-800 font-semibold">🫁 Physiologie</a>
    <a href="#neurobiology" class="text-green-800 font-semibold">🧠 Neurobiologie</a>
    <a href="#ecology" class="text-green-800 font-semibold">🌍 Ökologie</a>
    <a href="#genetics" class="text-green-800 font-semibold">🧬 Genetik & Evolution</a>
    <a href="#flashcards" class="text-green-800 font-semibold">🃏 Lernkarten</a>
    <a href="#quizzes" class="text-green-800 font-semibold">❓ Quiz</a>
    <a href="#games" class="text-green-800 font-semibold">🎮 Spiele</a>
  </nav>

  <main class="p-6 space-y-16">
    <!-- Content Sections with explanations, images, etc. -->
    <section id="physiology">
      <h2 class="text-2xl font-bold mb-4">🫁 Stoffwechselphysiologie</h2>
      <p>Fotosynthese, Zellatmung und ATP-Produktion.</p>
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/3e/CellRespiration.svg" class="w-full max-w-2xl">
      <p class="mt-2"><span class="diagram-label" onclick="alert('ATP-Synthese in der inneren Mitochondrienmembran durch Protonengradienten.')">Klicke hier für ATP-Synthese-Erklärung</span></p>
    </section>

    <section id="neurobiology">
      <h2 class="text-2xl font-bold mb-4">🧠 Neurobiologie</h2>
      <p>Signalübertragung im Nervensystem, Synapsen und Erregungsleitung.</p>
      <img src="https://upload.wikimedia.org/wikipedia/commons/e/ed/Neuron_Hand-tuned.svg" class="w-full max-w-xl">
      <p class="mt-2"><span class="diagram-label" onclick="alert('Reizweiterleitung durch Öffnung von spannungsgesteuerten Ionenkanälen.')">Reizweiterleitung erklären</span></p>
    </section>

    <section id="ecology">
      <h2 class="text-2xl font-bold mb-4">🌍 Ökologie</h2>
      <p>Biotop, Biozönose, Toleranzkurven, Kohlenstoffkreislauf, Biodiversität.</p>
      <img src="https://upload.wikimedia.org/wikipedia/commons/f/fd/Ecosystem_services_diagram_en.svg" class="w-full max-w-2xl">
      <p class="mt-2"><span class="diagram-label" onclick="alert('Energiefluss beginnt mit der Photosynthese der Produzenten.')">Energiefluss erklären</span></p>
    </section>

    <section id="genetics">
      <h2 class="text-2xl font-bold mb-4">🧬 Genetik & Evolution</h2>
      <p>DNA-Replikation, Proteinbiosynthese, Mutationen und Evolutionstheorie.</p>
      <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/DNA_replication_split.svg" class="w-full max-w-xl">
      <p class="mt-2"><span class="diagram-label" onclick="alert('Replikation bedeutet Verdopplung der DNA durch DNA-Polymerase.')">Replikation erklären</span></p>
    </section>

    <!-- Flashcards -->
    <section id="flashcards">
      <h2 class="text-2xl font-bold mb-4">🃏 Glossar Lernkarten</h2>
      <div id="flashcard-app" class="bg-white p-4 shadow rounded-lg max-w-md">
        <p id="term" class="text-xl font-semibold mb-2">Begriff</p>
        <button onclick="revealDefinition()" class="bg-green-600 text-white px-4 py-2 rounded">Definition anzeigen</button>
        <p id="definition" class="mt-4 hidden">Definition...</p>
        <div class="mt-4">
          <button onclick="nextCard()" class="bg-gray-300 px-4 py-2 rounded">Nächste Karte</button>
        </div>
      </div>
    </section>

    <!-- Quizzes -->
    <section id="quizzes">
      <h2 class="text-2xl font-bold mb-4">❓ Quiz</h2>
      <div class="quiz-card active bg-white p-4 rounded shadow max-w-lg">
        <p class="mb-2">Was passiert bei der Glykolyse?</p>
        <button onclick="alert('Richtig! Glukose wird zu Pyruvat abgebaut.')" class="bg-green-600 text-white px-4 py-1 m-1 rounded">Glukose → Pyruvat</button>
        <button onclick="alert('Falsch.')" class="bg-red-500 text-white px-4 py-1 m-1 rounded">ATP → ADP</button>
      </div>
    </section>

    <!-- Interactive Games -->
    <section id="games">
      <h2 class="text-2xl font-bold mb-4">🎮 Lernspiel: Drag-and-Drop DNA</h2>
      <p>Ziehe die Basen zur richtigen Position:</p>
      <div class="flex gap-4 mt-4">
        <div class="bg-gray-100 p-4 rounded shadow">
          <p class="font-bold">DNA-Strang:</p>
          <div class="flex gap-2 mt-2" id="target-bases">
            <div class="bg-white p-2 rounded border w-12 h-12 text-center">A</div>
            <div class="bg-white p-2 rounded border w-12 h-12 text-center">T</div>
            <div class="bg-white p-2 rounded border w-12 h-12 text-center">C</div>
          </div>
        </div>
        <div class="bg-gray-100 p-4 rounded shadow">
          <p class="font-bold">Komplementär:</p>
          <div class="flex gap-2 mt-2">
            <div draggable="true" ondragstart="event.dataTransfer.setData('text','T')" class="bg-blue-200 p-2 rounded cursor-move">T</div>
            <div draggable="true" ondragstart="event.dataTransfer.setData('text','A')" class="bg-blue-200 p-2 rounded cursor-move">A</div>
            <div draggable="true" ondragstart="event.dataTransfer.setData('text','G')" class="bg-blue-200 p-2 rounded cursor-move">G</div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <script>
    const glossary = [
      { term: 'ATP', definition: 'Energieeinheit der Zelle – Adenosintriphosphat' },
      { term: 'Neuron', definition: 'Nervenzelle zur Informationsweiterleitung im Nervensystem' },
      { term: 'Fotosynthese', definition: 'Umwandlung von Lichtenergie in chemische Energie in Pflanzen' },
      { term: 'DNA', definition: 'Desoxyribonukleinsäure – Träger genetischer Information' },
    ];
    let currentIndex = 0;

    function revealDefinition() {
      document.getElementById('definition').textContent = glossary[currentIndex].definition;
      document.getElementById('definition').classList.remove('hidden');
    }

    function nextCard() {
      currentIndex = (currentIndex + 1) % glossary.length;
      document.getElementById('term').textContent = glossary[currentIndex].term;
      document.getElementById('definition').classList.add('hidden');
    }

    window.onload = () => {
      document.getElementById('term').textContent = glossary[0].term;
    };
  </script>
</body>
</html> 
