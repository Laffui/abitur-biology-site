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
  </style>
</head>
<body class="bg-gray-50 text-gray-800">
  <header class="bg-green-600 text-white p-6">
    <h1 class="text-3xl font-bold">Biologie Lernen – NRW Abitur 2025 (Grundkurs)</h1>
    <p class="mt-2">Themen: Physiologie, Neurobiologie, Ökologie, Genetik & Evolution</p>
  </header>

  <nav class="bg-green-100 p-4 flex gap-4 flex-wrap">
    <a href="#physiology" class="text-green-800 font-semibold">🫁 Physiologie</a>
    <a href="#neurobiology" class="text-green-800 font-semibold">🧠 Neurobiologie</a>
    <a href="#ecology" class="text-green-800 font-semibold">🌍 Ökologie</a>
    <a href="#genetics" class="text-green-800 font-semibold">🧬 Genetik & Evolution</a>
    <a href="#flashcards" class="text-green-800 font-semibold">🃏 Lernkarten</a>
    <a href="#quizzes" class="text-green-800 font-semibold">❓ Quiz</a>
  </nav>

  <main class="p-6 space-y-16">
    <section id="physiology">
      <h2 class="text-2xl font-bold mb-4">🫁 Stoffwechselphysiologie</h2>
      <p>Vertiefung in Fotosynthese, Zellatmung, Enzyme, Energiegewinnung und Stoffwechselregulation.</p>
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/3e/CellRespiration.svg" alt="Zellatmung Diagramm" class="my-4 w-full max-w-2xl">
      <p>Oben siehst du eine Übersicht der Zellatmung (Glykolyse, Citratzyklus, Atmungskette).</p>
    </section>

    <section id="neurobiology">
      <h2 class="text-2xl font-bold mb-4">🧠 Neurobiologie</h2>
      <p>Lerne Aufbau und Funktion von Nervenzellen, Synapsen und Erregungsweiterleitung.</p>
      <img src="https://upload.wikimedia.org/wikipedia/commons/e/ed/Neuron_Hand-tuned.svg" alt="Neuron Diagramm" class="my-4 w-full max-w-xl">
      <p>Diagramm zeigt den Aufbau einer Nervenzelle – wichtig für das Verständnis von Ruhe- und Aktionspotenzial.</p>
    </section>

    <section id="ecology">
      <h2 class="text-2xl font-bold mb-4">🌍 Ökologie</h2>
      <p>Ökologische Nischen, Populationen, Energiefluss und Einfluss des Menschen auf Ökosysteme.</p>
      <img src="https://upload.wikimedia.org/wikipedia/commons/f/fd/Ecosystem_services_diagram_en.svg" alt="Energiefluss Ökosystem" class="my-4 w-full max-w-2xl">
    </section>

    <section id="genetics">
      <h2 class="text-2xl font-bold mb-4">🧬 Genetik & Evolution</h2>
      <p>DNA, Proteinbiosynthese, Genregulation, Mutationen und Evolutionsmechanismen.</p>
      <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/DNA_replication_split.svg" alt="DNA-Replikation" class="my-4 w-full max-w-xl">
    </section>

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

    <section id="quizzes">
      <h2 class="text-2xl font-bold mb-4">❓ Quiz: Zellatmung</h2>
      <div class="quiz-card active bg-white p-4 rounded shadow max-w-lg">
        <p class="mb-2">1. Welches Molekül liefert am meisten ATP bei der Zellatmung?</p>
        <button onclick="alert('Richtig!')" class="bg-green-600 text-white px-4 py-1 m-1 rounded">NADH</button>
        <button onclick="alert('Falsch – NADH liefert mehr als FADH₂')" class="bg-red-500 text-white px-4 py-1 m-1 rounded">FADH₂</button>
        <button onclick="alert('Falsch – Glukose ist Ausgangsstoff')" class="bg-red-500 text-white px-4 py-1 m-1 rounded">Glukose</button>
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
