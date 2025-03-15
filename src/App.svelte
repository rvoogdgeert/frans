<script lang="ts">
    import FlashCard from "./lib/FlashCard.svelte";

    // Define flash cards data structure
    const flashCards = [
        // A
        { id: 1, question: "la famille", answer: "de familie" },
        { id: 2, question: "le père", answer: "de vader" },
        { id: 3, question: "la mère", answer: "de moeder" },
        { id: 4, question: "les parents", answer: "de ouders" },
        { id: 5, question: "la maison", answer: "het huis" },
        { id: 6, question: "la chambre", answer: "de slaapkamer" },
        { id: 7, question: "le lit", answer: "het bed" },
        { id: 8, question: "la table", answer: "de tafel" },
        { id: 9, question: "la chaise", answer: "de stoel" },
        { id: 10, question: "la cuisine", answer: "de keuken" },
        { id: 11, question: "le salon", answer: "de woonkamer" },
        { id: 12, question: "le jardin", answer: "de tuin" },
        { id: 13, question: "le frère", answer: "de broer" },
        { id: 14, question: "la sœur", answer: "de zus" },
        { id: 15, question: "le cousin", answer: "de neef" },
        { id: 16, question: "la cousine", answer: "de nicht" },
        { id: 17, question: "le grand-père", answer: "de opa" },
        { id: 18, question: "la grand-mère", answer: "de oma" },
        { id: 19, question: "drôle", answer: "grappig" },
        { id: 20, question: "chouette", answer: "leuk" },
        { id: 21, question: "bien", answer: "goed" },
        { id: 22, question: "pas mal", answer: "niet slecht" },
        { id: 23, question: "l'ami", answer: "de vriend" },
        { id: 24, question: "l'amie", answer: "de vriendin" },
        { id: 25, question: "le weekend", answer: "het weekend" },
        { id: 26, question: "hier", answer: "gisteren" },
        { id: 27, question: "la semaine", answer: "de week" },
        { id: 28, question: "dernier", answer: "vorige" },
        { id: 29, question: "prochaine", answer: "volgende" },
        { id: 30, question: "jouer", answer: "spelen" },
        { id: 31, question: "le but", answer: "het doelpunt" },
        { id: 32, question: "l'équipe", answer: "het team" },
        { id: 33, question: "perdu", answer: "verloren" },
        { id: 34, question: "gagné", answer: "gewonnen" },

        // B
        { id: 35, question: "janvier", answer: "januari" },
        { id: 36, question: "février", answer: "februari" },
        { id: 37, question: "mars", answer: "maart" },
        { id: 38, question: "avril", answer: "april" },
        { id: 39, question: "mai", answer: "mei" },
        { id: 40, question: "juin", answer: "juni" },
        { id: 41, question: "juillet", answer: "juli" },
        { id: 42, question: "aout", answer: "augustus" },
        { id: 43, question: "septembre", answer: "september" },
        { id: 44, question: "octobre", answer: "oktober" },
        { id: 45, question: "novembre", answer: "november" },
        { id: 46, question: "décembre", answer: "december" },
        { id: 47, question: "lundi", answer: "maandag" },
        { id: 48, question: "mardi", answer: "dinsdag" },
        { id: 49, question: "mercredi", answer: "woensdag" },
        { id: 50, question: "jeudi", answer: "donderdag" },
        { id: 51, question: "vendredi", answer: "vrijdag" },
        { id: 52, question: "samedi", answer: "zaterdag" },
        { id: 53, question: "dimanche", answer: "zondag" },
        { id: 54, question: "le soir", answer: "'s avonds" },
        { id: 55, question: "l'apres-midi", answer: "'s middags" },
        { id: 56, question: "le jour", answer: "de dag" },
        { id: 57, question: "l'anniversaire", answer: "de verjaardag" },
        { id: 58, question: "fêter", answer: "vieren" },
        { id: 59, question: "la chose", answer: "het ding" },
        { id: 60, question: "demander", answer: "vragen" },
        { id: 61, question: "le repas", answer: "de maaltijd" },
        { id: 62, question: "l'endroit", answer: "de plaats" },
        { id: 63, question: "créatif", answer: "creatief" },
        { id: 64, question: "sociable", answer: "sociaal" },
        { id: 65, question: "enthousiaste", answer: "enthousiast" },
        // C
        { question: "Tu as passé un bon weekend?", answer: "Heb je een goed weekend gehad?"},
        { question: "Oui, j'ai fêté mon anniversaire", answer: "Ja, ik heb mijn verjaardag gevierd"},
        { question: "Oui, on a regardé un film", answer: "Ja, wij hebben een film gekeken"},
        { question: "Avec qui?", answer: "Met wie?"},
        { question: "Avec mes copains et Enzo", answer: "Met mijn vrienden en Enzo"},
        { question: "C'est qui, Enzo?", answer: "Wie is dat, Enzo?"},
        { question: "C'est mon cousin", answer: "Dat is mijn neef"},
        { question: "C'était bein?", answer: "Was het leuk?"},
        { question: "Oui, c'était génial", answer: "Ja, het was super"},
        { question: "C'est quand ton anniversaire?", answer: "Wanner ben je jarig?"},
        { question: "C'est la quatre avril", answer: "Op 4 april"},
        // E
        { id: 66, question: "les lunettes", answer: "de bril" },
        { id: 67, question: "les cheveux", answer: "het haar" },
        { id: 68, question: "les yeux", answer: "de ogen" },
        { id: 69, question: "de taille moyenne", answer: "van gemiddelde lengte" },
        { id: 70, question: "porter", answer: "dragen" },
        { id: 71, question: "il mesure 1m75", answer: "het is 1.75m lang" },
        { id: 72, question: "gros/grosse", answer: "dik" },
        { id: 73, question: "cher/chère", answer: "duur, lieve" },
        { id: 74, question: "donc", answer: "dus" },
        { id: 75, question: "peut-être", answer: "misschien" },
        { id: 76, question: "blanc/blanche", answer: "wit" },
        { id: 77, question: "noir(e)", answer: "zwart" },
        { id: 78, question: "bleu(e)", answer: "blauw" },
        { id: 79, question: "rouge", answer: "rood" },
        { id: 80, question: "jaune", answer: "geel" },
        { id: 81, question: "vert(e)", answer: "groen" },
        { id: 82, question: "gris(e)", answer: "grijs" },
        { id: 83, question: "marron", answer: "bruin ogen" },
        { id: 84, question: "brun(e)", answer: "bruin haar" },
        { id: 85, question: "roux/rousse", answer: "rossig haar" },
        { id: 86, question: "blond(e)", answer: "blond" },
        { id: 87, question: "rose", answer: "roze" },
    ];

    // Create a shuffled version of the flashcards
    let shuffledCards = [];

    // Fisher-Yates shuffle algorithm function
    function shuffleArray(array: any) {
        // Create a copy of the original array to avoid modifying it
        const arrayCopy = [...array];
        // Start from the last element and swap it with a randomly selected element
        for (let i = arrayCopy.length - 1; i > 0; i--) {
            // Pick a random index from 0 to i
            const j = Math.floor(Math.random() * (i + 1));
            // Swap elements at i and j
            [arrayCopy[i], arrayCopy[j]] = [arrayCopy[j], arrayCopy[i]];
        }
        return arrayCopy;
    }

    // Initialize shuffled cards when component loads
    shuffledCards = shuffleArray(flashCards);

    // Keep track of the current card index
    let currentCardIndex = 0;

    // State for tracking points system
    let points = 0;
    let attempted = 0;

    // Function to go to the next card
    // Function to go to the next card
    function nextCard() {
        if (currentCardIndex < shuffledCards.length - 1) {
            currentCardIndex++;
        }
    }

    // Function to go to the previous card
    function prevCard() {
        if (currentCardIndex > 0) {
            currentCardIndex--;
        }
    }
    // Function to update points when an answer is submitted
    function handleAnswerSubmit(event: any) {
        const isCorrect = event.detail.isCorrect;
        attempted++;

        if (isCorrect) {
            points++; // Add 1 point for correct answer

            // Set a 2-second delay for correct answers before moving to the next card
            if (currentCardIndex < shuffledCards.length - 1) {
                setTimeout(() => {
                    nextCard();
                }, 2000);
            }
        } else {
            // No point deduction for incorrect answers

            // Set a 5-second delay for incorrect answers before moving to the next card
            if (currentCardIndex < shuffledCards.length - 1) {
                setTimeout(() => {
                    nextCard();
                }, 5000);
            }
        }
    }
</script>

<main>
    <div class="container">
        <h1>Flash Cards Frans</h1>

        <div class="score-container">
            <p>Points: {points} (Attempted: {attempted})</p>
        </div>

        <div class="card-container">
            <FlashCard
                flashCard={shuffledCards[currentCardIndex]}
                on:answerSubmitted={handleAnswerSubmit}
            />
        </div>

        <div class="navigation">
            <button on:click={prevCard} disabled={currentCardIndex === 0}
                >Previous</button
            >
            <span class="card-counter"
                >{currentCardIndex + 1} / {shuffledCards.length}</span
            >
            <button
                on:click={nextCard}
                disabled={currentCardIndex === shuffledCards.length - 1}
                >Next</button
            >
        </div>
    </div>
</main>

<style>
    :global(body) {
        background-color: #10abb4;
        color: #004c50;
        margin: 0;
        padding: 0;
        font-family:
            -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen-Sans,
            Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
    }

    .container {
        display: flex;
        flex-direction: column;
        align-items: center;
        max-width: 800px;
        margin: 0 auto;
        padding: 20px;
        background-color: white;
        border-radius: 12px;
        box-shadow: 0 4px 12px rgba(0, 76, 80, 0.1);
    }

    h1 {
        color: #004c50;
        margin-bottom: 20px;
        font-weight: 700;
        text-align: center;
    }

    .score-container {
        margin-bottom: 20px;
        font-size: 1.2rem;
        font-weight: bold;
        color: #004c50;
        background-color: rgba(16, 171, 180, 0.1);
        padding: 8px 16px;
        border-radius: 8px;
    }

    .card-container {
        width: 100%;
        margin-bottom: 20px;
    }

    .navigation {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        max-width: 400px;
        padding: 10px;
        background-color: rgba(0, 147, 156, 0.05);
        border-radius: 8px;
    }

    button {
        background-color: #00939c;
        color: white;
        border: none;
        padding: 10px 20px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin: 4px 2px;
        cursor: pointer;
        border-radius: 4px;
        transition: all 0.3s ease;
        font-weight: 500;
        box-shadow: 0 2px 4px rgba(0, 76, 80, 0.2);
    }

    button:hover {
        background-color: #10abb4;
        transform: translateY(-2px);
        box-shadow: 0 4px 8px rgba(0, 76, 80, 0.3);
    }

    button:disabled {
        background-color: rgba(0, 147, 156, 0.3);
        cursor: not-allowed;
        box-shadow: none;
        transform: none;
    }

    .card-counter {
        font-size: 1rem;
        color: #502000;
        font-weight: 600;
        background-color: rgba(156, 62, 0, 0.1);
        padding: 4px 10px;
        border-radius: 4px;
    }
</style>
