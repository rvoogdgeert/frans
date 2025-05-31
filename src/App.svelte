<script lang="ts">
    import FlashCard from "./lib/FlashCard.svelte";

    // Define flash cards data structure
    const flashCards = [
        // 5A
        //{ id: 1, question: "le frère", answer: "de broer" },
        //{ id: 2, question: "la sœur", answer: "de zus" },
        //{ id: 3, question: "le cousin", answer: "de neef" },
        //{ id: 4, question: "la cousine", answer: "de nicht" },
        //{ id: 5, question: "le grand-père", answer: "de opa" },
        //{ id: 6, question: "la grand-mère", answer: "de oma" },
        //{ id: 7, question: "drôle", answer: "grappig" },
        //{ id: 8, question: "chouette", answer: "leuk" },
        //{ id: 9, question: "bien", answer: "goed" },
        //{ id: 10, question: "pas mal", answer: "niet slecht" },
        //{ id: 11, question: "l'ami", answer: "de vriend" },
        //{ id: 12, question: "l'amie", answer: "de vriendin" },
        //{ id: 13, question: "le weekend", answer: "het weekend" },
        //{ id: 14, question: "hier", answer: "gisteren" },
        //{ id: 15, question: "la semaine", answer: "de week" },
        //{ id: 16, question: "dernier", answer: "vorige" },
        //{ id: 17, question: "prochaine", answer: "volgende" },
        //{ id: 18, question: "jouer", answer: "spelen" },
        //{ id: 19, question: "le but", answer: "het doelpunt" },
        //{ id: 20, question: "l'équipe", answer: "het team" },
        //{ id: 21, question: "perdu", answer: "verloren" },
        //{ id: 22, question: "gagné", answer: "gewonnen" },

        //// 5B
        //{ id: 23, question: "janvier", answer: "januari" },
        //{ id: 24, question: "février", answer: "februari" },
        //{ id: 25, question: "mars", answer: "maart" },
        //{ id: 26, question: "avril", answer: "april" },
        //{ id: 27, question: "mai", answer: "mei" },
        //{ id: 28, question: "juin", answer: "juni" },
        //{ id: 29, question: "juillet", answer: "juli" },
        //{ id: 30, question: "aout", answer: "augustus" },
        //{ id: 31, question: "septembre", answer: "september" },
        //{ id: 32, question: "octobre", answer: "oktober" },
        //{ id: 33, question: "novembre", answer: "november" },
        //{ id: 34, question: "décembre", answer: "december" },
        //{ id: 35, question: "lundi", answer: "maandag" },
        //{ id: 36, question: "mardi", answer: "dinsdag" },
        //{ id: 37, question: "mercredi", answer: "woensdag" },
        //{ id: 38, question: "jeudi", answer: "donderdag" },
        //{ id: 39, question: "vendredi", answer: "vrijdag" },
        //{ id: 40, question: "samedi", answer: "zaterdag" },
        //{ id: 41, question: "dimanche", answer: "zondag" },
        //{ id: 42, question: "le soir", answer: "'s avonds" },
        //{ id: 43, question: "l'apres-midi", answer: "'s middags" },
        //{ id: 44, question: "le jour", answer: "de dag" },
        //{ id: 45, question: "l'anniversaire", answer: "de verjaardag" },
        //{ id: 46, question: "fêter", answer: "vieren" },
        //{ id: 47, question: "la chose", answer: "het ding" },
        //{id: 48, question: "demander", answer: "vragen" },
        //{id: 49, question: "le repas", answer: "de maaltijd" },
        //{id: 50, question: "l'endroit", answer: "de plaats" },
        //{id: 51, question: "créatif", answer: "creatief" },
        //{id: 52, question: "sociable", answer: "sociaal" },
        //{id: 53, question: "enthousiaste", answer: "enthousiast" },

        ////5C
        //id: 54, question: "Tu as passé un bon weekend?", answer: "Heb je een goed weekend gehad?"},
        //{id: 55, question: "Oui, j'ai fêté mon anniversaire", answer: "Ja, ik heb mijn verjaardag gevierd"},
        //{id: 56, question: "Oui, on a regardé un film", answer: "Ja, wij hebben een film gekeken"},
        //{ id: 57, question: "Avec qui?", answer: "Met wie?" },
        //{id: 58, question: "Avec mes copains et Enzo", answer: "Met mijn vrienden en Enzo",},
        //{ id: 59, question: "C'est qui, Enzo?", answer: "Wie is dat, Enzo?" },
        //{ id: 60, question: "C'est mon cousin", answer: "Dat is mijn neef" },
        //{ id: 61, question: "C'était bein?", answer: "Was het leuk?" },
        //{ id: 62, question: "Oui, c'était génial", answer: "Ja, het was super" },
        //{id: 63, question: "C'est quand ton anniversaire?", answer: "Wanneer ben je jarig?" },
        //{ id: 64, question: "C'est la quatre avril", answer: "Op 4 april" },

        //// 5E
        //{ id: 65, question: "les lunettes", answer: "de bril" },
        //{ id: 66, question: "les cheveux", answer: "het haar" },
        //{ id: 67, question: "les yeux", answer: "de ogen" },
        //{ id: 68, question: "de taille moyenne", answer: "van gemiddelde lengte" },
        //{ id: 69, question: "porter", answer: "dragen" },
        //{ id: 70, question: "il mesure 1m75", answer: "hij is 1.75m lang" },
        //{ id: 71, question: "gros/grosse", answer: "dik" },
        //{ id: 72, question: "cher/chère", answer: "duur, lieve" },
        //{ id: 73, question: "donc", answer: "dus" },
        //{ id: 74, question: "peut-être", answer: "misschien" },
        //{ id: 75, question: "blanc/blanche", answer: "wit" },
        //{ id: 76, question: "noir(e)", answer: "zwart" },
        //{ id: 77, question: "bleu(e)", answer: "blauw" },
        //{ id: 78, question: "rouge", answer: "rood" },
        //{ id: 79, question: "jaune", answer: "geel" },
        //{ id: 80, question: "vert(e)", answer: "groen" },
        //{ id: 81, question: "gris(e)", answer: "grijs" },
        //{ id: 82, question: "marron", answer: "bruin ogen" },
        //{ id: 83, question: "brun(e)", answer: "bruin haar" },
        //{ id: 84, question: "roux/rousse", answer: "rossig haar" },
        //{ id: 85, question: "blond(e)", answer: "blond" },
        //{ id: 86, question: "rose", answer: "roze" },

        ////// 6A
        //{ id: 87, question: "", answer: "blauw" },
        //{ id: 88, question: "", answer: "rood" },
        //{ id: 89, question: "", answer: "geel" },
        //{ id: 90, question: "", answer: "hij is 1.75m lang" },
        //{ id: 91, question: "", answer: "dik" },
        //{ id: 92, question: "", answer: "duur, lieve" },
        //{ id: 93, question: "", answer: "dus" },
        //{ id: 94, question: "", answer: "misschien" },
        //{ id: 95, question: "", answer: "wit" },
        //{ id: 96, question: "", answer: "zwart" },
        //{ id: 97, question: "", answer: "blauw" },
        //{ id: 98, question: "", answer: "rood" },
        //{ id: 99, question: "", answer: "geel" },
        //{ id: 100, question: "", answer: "groen" },
        //{ id: 101, question: "", answer: "grijs" },
        //{ id: 102, question: "", answer: "bruin ogen" },
        //{ id: 103, question: "", answer: "bruin haar" },
        //{ id: 104, question: "", answer: "rossig haar" },
        //{ id: 105, question: "", answer: "blond" },
        //{ id: 106, question: "", answer: "roze" },
        //{ id: 107, question: "", answer: "roze" },

        ////// 6B
        //{ id: 108, question: "", answer: "roze" },
        //{ id: 109, question: "", answer: "roze" },
        //{ id: 110, question: "", answer: "groen" },
        //{ id: 111, question: "", answer: "grijs" },
        //{ id: 112, question: "", answer: "bruin ogen" },
        //{ id: 113, question: "", answer: "bruin haar" },
        //{ id: 114, question: "", answer: "rossig haar" },
        //{ id: 115, question: "", answer: "blond" },
        //{ id: 116, question: "", answer: "roze" },
        //{ id: 117, question: "", answer: "roze" },
        //{ id: 118, question: "", answer: "roze" },
        //{ id: 119, question: "", answer: "roze" },
        //{ id: 120, question: "", answer: "groen" },
        //{ id: 121, question: "", answer: "grijs" },
        //{ id: 122, question: "", answer: "bruin ogen" },
        //{ id: 123, question: "", answer: "bruin haar" },
        //{ id: 124, question: "", answer: "rossig haar" },
        //{ id: 125, question: "", answer: "blond" },
        //{ id: 126, question: "", answer: "roze" },
        //{ id: 127, question: "", answer: "roze" },
        //{ id: 128, question: "", answer: "roze" },

        ////// 6C
        //{ id: 128, question: "", answer: "roze" },
        //{ id: 129, question: "", answer: "roze" },
        //{ id: 130, question: "", answer: "groen" },
        //{ id: 131, question: "", answer: "grijs" },
        //{ id: 132, question: "", answer: "bruin ogen" },
        //{ id: 133, question: "", answer: "bruin haar" },
        //{ id: 134, question: "", answer: "rossig haar" },
        //{ id: 135, question: "", answer: "blond" },
        //{ id: 136, question: "", answer: "roze" },
        //{ id: 137, question: "", answer: "roze" },
        //{ id: 138, question: "", answer: "roze" },
        //{ id: 139, question: "", answer: "roze" },
        //{ id: 140, question: "", answer: "groen" },
        //{ id: 141, question: "", answer: "grijs" },
        //{ id: 142, question: "", answer: "bruin ogen" },
        //{ id: 143, question: "", answer: "bruin haar" },
        //{ id: 144, question: "", answer: "rossig haar" },
        //{ id: 145, question: "", answer: "blond" },
        //{ id: 146, question: "", answer: "roze" },
        //{ id: 147, question: "", answer: "roze" },
        //{ id: 148, question: "", answer: "roze" },

        ////// 6E
        //{ id: 148, question: "", answer: "roze" },
        //{ id: 149, question: "", answer: "roze" },
        //{ id: 150, question: "", answer: "groen" },
        //{ id: 151, question: "", answer: "grijs" },
        //{ id: 152, question: "", answer: "bruin ogen" },
        //{ id: 153, question: "", answer: "bruin haar" },
        //{ id: 154, question: "", answer: "rossig haar" },
        //{ id: 155, question: "", answer: "blond" },
        //{ id: 156, question: "", answer: "roze" },
        //{ id: 157, question: "", answer: "roze" },
        //{ id: 158, question: "", answer: "roze" },
        //{ id: 159, question: "", answer: "roze" },
        //{ id: 160, question: "", answer: "groen" },
        //{ id: 161, question: "", answer: "grijs" },
        //{ id: 162, question: "", answer: "bruin ogen" },
        //{ id: 163, question: "", answer: "bruin haar" },
        //{ id: 164, question: "", answer: "rossig haar" },
        //{ id: 165, question: "", answer: "blond" },
        //{ id: 166, question: "", answer: "roze" },
        //{ id: 167, question: "", answer: "roze" },
        //{ id: 168, question: "", answer: "roze" },

        //// 6F
        { id: 168, question: "le village", answer: "het dorp" },
        { id: 169, question: "la vile", answer: "de stad" },
        { id: 170, question: "la campange", answer: "het platteland" },
        { id: 171, question: "l'immeuble", answer: "het flatgebouw" },
        { id: 172, question: "l'appartement", answer: "het appartement" },
        { id: 173, question: "chez moi", answer: "bij mij thuis" },
        { id: 174, question: "la maison", answer: "het huis" },
        { id: 175, question: "le jardin", answer: "de tuin" },
        { id: 176, question: "le chien", answer: "de hond" },
        { id: 177, question: "le chat", answer: "de kat" },
        { id: 178, question: "il faut", answer: "je moet" },
        { id: 179, question: "prendre", answer: "nemen" },
        { id: 180, question: "autre", answer: "andere" },
        { id: 181, question: "plus de", answer: "meer dan" },
        { id: 182, question: "la chose", answer: "het ding" },
        { id: 183, question: "trop de monde", answer: "te veel mensen" },
        { id: 184, question: "à côte de", answer: "dichtbij" },
        { id: 185, question: "le parc", answer: "het park" },
        { id: 186, question: "le/la jeune", answer: "de jongere" },
        { id: 187, question: "assez", answer: "genoeg" },

        //// 7A
        //{ id: 188, question: "", answer: "roze" },

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
