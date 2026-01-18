<script lang="ts">
    import FlashCard from "./lib/FlashCard.svelte";

    // Define flash cards data structure
    const flashCards = [

        // Chapitre 1
        // A
        //{ id: 1, question: "la rentrée", answer: "de eerste schooldag" },
        //{ id: 2, question: "rencontrer", answer: "ontmoeten" },
        //{ id: 3, question: "l'amie", answer: "de vriend" },
        //{ id: 4, question: "le frère", answer: "de broer" },
        //{ id: 5, question: "le/la jeune", answer: "de jongere" },
        //{ id: 6, question: "la découverte", answer: "de ontdekking" },
        //{ id: 7, question: "en avion", answer: "met het vliegtuig" },
        //{ id: 8, question: "en train", answer: "met de trein" },
        //{ id: 9, question: "en bateau", answer: "met de boot" },
        //{ id: 10, question: "en voiture", answer: "met de auto" },
        //{ id: 11, question: "pourqoi", answer: "waarom" },
        //{ id: 12, question: "parce que", answer: "omdat" },
        //{ id: 13, question: "mais", answer: "maar" },
        //{ id: 14, question: "incroyable", answer: "ongelofelijk" },
        //{ id: 15, question: "contente", answer: "tevreden" },
        //{ id: 16, question: "en Espagne", answer: "in Spanje" },
        //{ id: 17, question: "en Allemagne", answer: "in Duitsland" },
        //{ id: 18, question: "en Angleterre", answer: "in Engeland" },
        //{ id: 19, question: "aux Pays-Bas", answer: "in Nederland" },
        //{ id: 20, question: "en Belgique", answer: "in België" },
        //// B
        //{ id: 21, question: "le voyage", answer: "de reis" },
        //{ id: 22, question: "le pays", answer: "het land" },
        //{ id: 23, question: "la famille", answer: "de familie" },
        //{ id: 24, question: "le soeur", answer: "de zus" },
        //{ id: 25, question: "le/la jeune", answer: "de jongere" },
        //{ id: 26, question: "la découverte", answer: "de ontdekking" },
        //{ id: 27, question: "en avion", answer: "met het vliegtuig" },
        //{ id: 28, question: "en train", answer: "met de trein" },
        //{ id: 29, question: "en bateau", answer: "met de boot" },
        //{ id: 30, question: "en voiture", answer: "met de auto" },
        //{ id: 31, question: "pourqoi", answer: "waarom" },
        //{ id: 32, question: "parce que", answer: "omdat" },
        //{ id: 33, question: "mais", answer: "maar" },
        //{ id: 34, question: "incroyable", answer: "ongelofelijk" },
        //{ id: 35, question: "contente", answer: "tevreden" },
        //{ id: 36, question: "en Espagne", answer: "in Spanje" },
        //{ id: 37, question: "en Allemagne", answer: "in Duitsland" },
        //{ id: 38, question: "en Angleterre", answer: "in Engeland" },
        //{ id: 39, question: "aux Pays-Bas", answer: "in Nederland" },
        //{ id: 40, question: "en Belgique", answer: "in België" },

        // Chapitre 2
        //// A
        //{ id: 41, question: "le mariage", answer: "het huwelijk" },
        //{ id: 42, question: "la fête", answer: "het feest" },
        //{ id: 43, question: "le cousin, la cousine", answer: "de neef, de nicht" },
        //{ id: 44, question: "tout le monde", answer: "iedereen" },
        //{ id: 45, question: "j'attends", answer: "ik wacht op" },
        //{ id: 46, question: "un/une autre", answer: "een ander" },
        //{ id: 47, question: "là-bas", answer: "daarginds" },
        //{ id: 48, question: "à coté de", answer: "naast" },
        //{ id: 49, question: "souvent", answer: "vaak" },
        //{ id: 50, question: "parfois", answer: "soms" },
        //{ id: 51, question: "mignon(ne)", answer: "schattig" },
        //{ id: 52, question: "pénible", answer: "lastig" },
        //{ id: 53, question: "sympa", answer: "aardig" },
        //{ id: 54, question: "le/la pauvre", answer: "de arme ziel" },
        //{ id: 55, question: "en train de", answer: "bezig met" },
        //{ id: 56, question: "on vient", answer: "we komen" },
        //{ id: 57, question: "je n'ai pas faim", answer: "ik heb geen honger" },
        //{ id: 58, question: "regarder", answer: "kijken" },
        //{ id: 59, question: "partager", answer: "delen" },
        //{ id: 60, question: "changer", answer: "veranderen" },

        //// B
        //{ id: 61, question: "le lapin", answer: "het konijn" },
        //{ id: 62, question: "la tortue", answer: "de schildpad" },
        //{ id: 63, question: "le hamster", answer: "de hamster" },
        //{ id: 64, question: "l'oiseau m", answer: "de vogel" },
        //{ id: 65, question: "le poisson", answer: "de vis" },
        //{ id: 66, question: "le cochon d'Inde", answer: "de cavia" },
        //{ id: 67, question: "je m'occupe de", answer: "ik zorg voor" },
        //{ id: 68, question: "la nourriture", answer: "het voedsel" },
        //{ id: 69, question: "malade", answer: "ziek" },
        //{ id: 70, question: "heureux, heureuse", answer: "gelukkig" },
        //{ id: 71, question: "vieux, vieille", answer: "oud" },
        //{ id: 72, question: "actif, active", answer: "actief" },
        //{ id: 73, question: "gentil(le)", answer: "aardig" },
        //{ id: 74, question: "câlin(e)", answer: "aanhalig" },
        //{ id: 75, question: "intelligent(e)", answer: "slim" },
        //{ id: 76, question: "acheter", answer: "kopen" },
        //{ id: 77, question: "donner", answer: "geven" },
        //{ id: 78, question: "exister", answer: "bestaan" },
        //{ id: 79, question: "aider", answer: "helpen" },
        //{ id: 80, question: "on peut", answer: "we kunnen" },

        //// C (sentences)
        //{ id: 81, question: "Heb je broers en zussen?", answer: "Tu as des freres et soeurs?" },
        //{ id: 82, question: "Ja, ik heb een zusje van tien.", answer: "Oui, j’ai une petite soeur de dix ans." },
        //{ id: 83, question: "Hoe heet zij?", answer: "Comment elle s’appelle?" },
        //{ id: 84, question: "Zij heet Samira.", answer: "Elle s’appelle Samira." },
        //{ id: 85, question: "Hoe is zij?", answer: "Elle est comment?" },
        //{ id: 86, question: "Ze is schattig. Maar soms is ze lastig.", answer: "Elle est adorable. Mais, parfois elle est penible." },
        //{ id: 87, question: "Wat doen jullie graag samen?", answer: "Qu'est-ce que vous aimez faire ensemble?" },
        //{ id: 88, question: "We kijken graag tv.", answer: "On aime regarder la tele." },
        //{ id: 89, question: "Heb jij een huisdier?", answer: "Tu as un animal domestique?" },
        //{ id: 90, question: "Ja, ik heb een hond en twee katten.", answer: "Oui, j’ai un chien et deux chats." },
        //{ id: 91, question: "Mijn hond heet Brownie en hij is erg oud.", answer: "Mon chien s’appelle Brownie et il est tres vieux." },

        //// E
        //{ id: 92, question: "la tante", answer: "de tante" },
        //{ id: 93, question: "le copain, la copine", answer: "de vriend, vriendin" },
        //{ id: 94, question: "le rendez-vous", answer: "de afspraak" },
        //{ id: 95, question: "le portable", answer: "de mobiele telefoon" },
        //{ id: 96, question: "la glace", answer: "het ijsje" },
        //{ id: 97, question: "content(e)", answer: "tevreden" },
        //{ id: 98, question: "interdit(e)", answer: "verboden" },
        //{ id: 99, question: "nul(le)", answer: "waardeloos" },
        //{ id: 100, question: "donc", answer: "dus" },
        //{ id: 101, question: "maintenant", answer: "nu" },
        //{ id: 102, question: "vite", answer: "snel" },
        //{ id: 103, question: "peut-être", answer: "misschien" },
        //{ id: 104, question: "après", answer: "daarna" },
        //{ id: 105, question: "arrêter", answer: "ophouden" },
        //{ id: 106, question: "j'en ai marre", answer: "ik ben het zat" },
        //{ id: 107, question: "présenter", answer: "voorstellen" },
        //{ id: 108, question: "écouter", answer: "luisteren" },
        //{ id: 109, question: "participer à", answer: "meedoen aan" },
        //{ id: 110, question: "trouver", answer: "vinden" },
        //{ id: 111, question: "gagner", answer: "winnen" },

        //// F
        //{ id: 112, question: "la maison", answer: "het huis" },
        //{ id: 113, question: "la cuisine", answer: "de keuken" },
        //{ id: 114, question: "la chambre", answer: "de kamer" },
        //{ id: 115, question: "le salon", answer: "de woonkamer" },
        //{ id: 116, question: "la salle de bains", answer: "de badkamer" },
        //{ id: 117, question: "le lit", answer: "het bed" },
        //{ id: 118, question: "l'armoire v", answer: "de kast" },
        //{ id: 119, question: "la table", answer: "de tafel" },
        //{ id: 120, question: "la chaise", answer: "de stoel" },
        //{ id: 121, question: "la fenêtre", answer: "het raam" },
        //{ id: 122, question: "les loisirs m mv", answer: "de vrije tijd" },
        //{ id: 123, question: "le paysage", answer: "het landschap" },
        //{ id: 124, question: "car", answer: "want" },
        //{ id: 125, question: "je me lève", answer: "ik sta op" },
        //{ id: 126, question: "tôt", answer: "vroeg" },
        //{ id: 127, question: "dormir", answer: "slapen" },
        //{ id: 128, question: "travailler", answer: "werken" },
        //{ id: 129, question: "jouer à la console", answer: "gamen" },
        //{ id: 130, question: "vivre", answer: "leven" },
        //{ id: 131, question: "je vis", answer: "ik leef" },

        //// G (sentences)
        //{ id: 132, question: "Waar woon jij?", answer: "Tu habites ou?" },
        //{ id: 133, question: "Ik woon in Parijs.", answer: "J’habite a Paris." },
        //{ id: 134, question: "Woon jij in een huis?", answer: "Tu habites dans une maison?" },
        //{ id: 135, question: "Nee, ik woon in een flat.", answer: "Non, j’habite dans un appartement." },
        //{ id: 136, question: "Hoe vind jij jouw slaapkamer?", answer: "Comment tu trouves ta chambre?" },
        //{ id: 137, question: "Ik vind mijn slaapkamer leuk, hij is groot.", answer: "J’aime bien ma chambre, elle est grande." },
        //{ id: 138, question: "Er staat een bed in en een bureau.", answer: "Il y a un lit et un bureau." },
        //{ id: 139, question: "Ben jij vaak in jouw slaapkamer?", answer: "Tu es souvent dans ta chambre?" },
        //{ id: 140, question: "Ja, om te kletsen met mijn vrienden.", answer: "Oui, pour discuter avec mes amis." },
        //{ id: 141, question: "Wat doe je in je kamer?", answer: "Qu’est-ce que tu fais dans ta chambre?" },
        //{ id: 142, question: "Ik maak huiswerk en ik luister naar muziek.", answer: "Je fais mes devoirs et j’ecoute de la musique." },

        // Chapitre 8

        // A
        //{ id: 1, question: "le pantalon", answer: "de broek" },
        //{ id: 2, question: "la jupe", answer: "de rok" },
        //{ id: 3, question: "la robe", answer: "de jurk" },
        //{ id: 4, question: "le pull", answer: "de trui" },
        //{ id: 5, question: "les chaussures", answer: "de schoenen" },
        //{ id: 6, question: "la taille", answer: "de kledingmaat" },
        //{ id: 7, question: "essayer", answer: "passen" },
        //{ id: 8, question: "le marché", answer: "de markt" },
        //{ id: 9, question: "le vêtement", answer: "het kledingstuk" },
        //{ id: 10, question: "hésiter", answer: "twijfelen" },
        //{ id: 11, question: "un peu", answer: "een beetje" },
        //{ id: 12, question: "vraiment", answer: "echt" },
        //{ id: 13, question: "moche", answer: "lelijk" },
        //{ id: 14, question: "branché(e)", answer: "in de mode" },
        //{ id: 15, question: "sportif, sportive", answer: "sportief" },
        //{ id: 16, question: "l'anniversaire", answer: "de verjaardag" },
        //{ id: 17, question: "d'abord", answer: "eerst" },
        //{ id: 18, question: "ensuite", answer: "daarna" },
        //{ id: 19, question: "prendre rendez-vous", answer: "afspreken" },
        //{ id: 20, question: "viens!", answer: "kom!" },

        //// A1
        //{ id: 53, question: "de broek", answer: "le pantalon" },
        //{ id: 54, question: "de rok", answer: "la jupe" },
        //{ id: 55, question: "de jurk", answer: "la robe" },
        //{ id: 56, question: "de trui", answer: "le pull" },
        //{ id: 57, question: "de schoenen", answer: "les chaussures" },
        //{ id: 58, question: "de kledingmaat", answer: "la taille" },
        //{ id: 59, question: "passen", answer: "essayer" },
        //{ id: 60, question: "de markt", answer: "le marche" },
        //{ id: 61, question: "het kledingstuk", answer: "le vetement" },
        //{ id: 62, question: "twijfelen", answer: "hesiter" },
        //{ id: 63, question: "een beetje", answer: "un peu" },
        //{ id: 64, question: "echt", answer: "vraiment" },
        //{ id: 65, question: "lelijk", answer: "moche" },
        //{ id: 66, question: "in de mode", answer: "branche(e)" },
        //{ id: 67, question: "sportief", answer: "sportif, sportive" },
        //{ id: 68, question: "de verjaardag", answer: "l'anniversaire" },
        //{ id: 69, question: "eerst", answer: "d'abord" },
        //{ id: 70, question: "daarna", answer: "ensuite" },
        //{ id: 71, question: "afspreken", answer: "prendre rendez-vous" },
        //{ id: 72, question: "kom!", answer: "viens!" },

        / B
        { id: 21, question: "le sac", answer: "de tas" },
        { id: 22, question: "le T-shirt", answer: "het T-shirt" },
        { id: 23, question: "les lunettes de soleil", answer: "de zonnebril" },
        { id: 24, question: "les baskets", answer: "de sportschoenen" },
        { id: 25, question: "les bottes", answer: "de laarzen" },
        { id: 26, question: "faire du shopping", answer: "shoppen, winkelen" },
        { id: 27, question: "avoir besoin de", answer: "nodig hebben" },
        { id: 28, question: "l'argent (de poche)", answer: "het zakgeld" },
        { id: 29, question: "dépenser", answer: "uitgeven" },
        { id: 30, question: "le magasin", answer: "de winkel" },
        { id: 31, question: "la chose", answer: "het ding" },
        { id: 32, question: "utile", answer: "nuttig" },
        { id: 33, question: "rigolo, rigolotte", answer: "lollig" },
        { id: 34, question: "drôle", answer: "grappig" },
        { id: 35, question: "nécessaire", answer: "noodzakelijk" },
        { id: 36, question: "souvent", answer: "vaak" },
        { id: 37, question: "assez", answer: "nogal, genoeg" },
        { id: 38, question: "tout de suite", answer: "direct" },
        { id: 39, question: "la semaine", answer: "de week" },
        { id: 40, question: "mettre", answer: "aantrekken" },

        //// B1
        //{ id: 73, question: "de tas", answer: "le sac" },
        //{ id: 74, question: "het T-shirt", answer: "le T-shirt" },
        //{ id: 75, question: "de zonnebril", answer: "les lunettes de soleil" },
        //{ id: 76, question: "de sportschoenen", answer: "les baskets" },
        //{ id: 77, question: "de laarzen", answer: "les bottes" },
        //{ id: 78, question: "shoppen, winkelen", answer: "faire du shopping" },
        //{ id: 79, question: "nodig hebben", answer: "avoir besoin de" },
        //{ id: 80, question: "het zakgeld", answer: "l'argent (de poche)" },
        //{ id: 81, question: "uitgeven", answer: "depenser" },
        //{ id: 82, question: "de winkel", answer: "le magasin" },
        //{ id: 83, question: "het ding", answer: "la chose" },
        //{ id: 84, question: "nuttig", answer: "utile" },
        //{ id: 85, question: "lollig", answer: "rigolo, rigolotte" },
        //{ id: 86, question: "grappig", answer: "drole" },
        //{ id: 87, question: "noodzakelijk", answer: "necessaire" },
        //{ id: 88, question: "vaak", answer: "souvent" },
        //{ id: 89, question: "nogal, genoeg", answer: "assez" },
        //{ id: 90, question: "direct", answer: "tout de suite" },
        //{ id: 91, question: "de week", answer: "la semaine" },
        //{ id: 92, question: "aantrekken", answer: "mettre" },

        //// C
        //{ id: 41, question: "On va dans ce magasin?", answer: "Gaan we deze winkel in?" },
        //{ id: 42, question: "Bonne idée! Tu veux acheter quelque chose?", answer: "Goed idee! Wil je iets kopen?" },
        //{ id: 43, question: "Oui, je voudrais acheter un nouveau jean.", answer: "Ja, ik wil graag een nieuwe spijkerbroek kopen." },
        //{ id: 44, question: "Comment tu trouves ce jean bleu?", answer: "Hoe vind je deze blauwe spijkerbroek?" },
        //{ id: 45, question: "Il est pas mal. Il coute combien?", answer: "Hij is niet slecht. Wat kost hij?" },
        //{ id: 46, question: "Il coute trente euros (seulement).", answer: "Hij kost (maar) dertig euro." },
        //{ id: 47, question: "Ce n'est pas cher.", answer: "Dat is niet duur." },
        //{ id: 48, question: "Je vais l'essayer.", answer: "Ik ga hem passen." },
        //{ id: 49, question: "Tu fais quelle taille?", answer: "Welke maat heb je?" },
        //{ id: 50, question: "Je fais du S ou du M.", answer: "Ik heb S of M." },
        //{ id: 51, question: "Voilà, un M.", answer: "Hier is een M." },
        //{ id: 52, question: "Dommage, il est trop grand.", answer: "Jammer, hij is te groot." },


        //// C1
        //{ id: 93, question: "Gaan we deze winkel in?", answer: "On va dans ce magasin?" },
        //{ id: 94, question: "Goed idee! Wil je iets kopen?", answer: "Bonne idee! Tu veux acheter quelque chose?" },
        //{ id: 95, question: "Ja, ik wil graag een nieuwe spijkerbroek kopen.", answer: "Oui, je voudrais acheter un nouveau jean." },
        //{ id: 96, question: "Hoe vind je deze blauwe spijkerbroek?", answer: "Comment tu trouves ce jean bleu?" },
        //{ id: 97, question: "Hij is niet slecht. Wat kost hij?", answer: "Il est pas mal. Il coute combien?" },
        //{ id: 98, question: "Hij kost (maar) dertig euro.", answer: "Il coute trente euros (seulement)." },
        //{ id: 99, question: "Dat is niet duur.", answer: "Ce n'est pas cher." },
        //{ id: 100, question: "Ik ga hem passen.", answer: "Je vais l'essayer." },
        //{ id: 101, question: "Welke maat heb je?", answer: "Tu fais quelle taille?" },
        //{ id: 102, question: "Ik heb S of M.", answer: "Je fais du S ou du M." },
        //{ id: 103, question: "Hier is een M.", answer: "Voila, un M." },
        //{ id: 104, question: "Jammer, hij is te groot.", answer: "Dommage, il est trop grand." },        
        

        

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
        //{ id: 168, question: "le village", answer: "het dorp" },
        //{ id: 169, question: "la vile", answer: "de stad" },
        //{ id: 170, question: "la campange", answer: "het platteland" },
        //{ id: 171, question: "l'immeuble", answer: "het flatgebouw" },
        //{ id: 172, question: "l'appartement", answer: "het appartement" },
        //{ id: 173, question: "chez moi", answer: "bij mij thuis" },
        //{ id: 174, question: "la maison", answer: "het huis" },
        //{ id: 175, question: "le jardin", answer: "de tuin" },
        //{ id: 176, question: "le chien", answer: "de hond" },
        //{ id: 177, question: "le chat", answer: "de kat" },
        //{ id: 178, question: "il faut", answer: "je moet" },
        //{ id: 179, question: "prendre", answer: "nemen" },
        //{ id: 180, question: "autre", answer: "andere" },
        //{ id: 181, question: "plus de", answer: "meer dan" },
        //{ id: 182, question: "la chose", answer: "het ding" },
        //{ id: 183, question: "trop de monde", answer: "te veel mensen" },
        //{ id: 184, question: "à côte de", answer: "dichtbij" },
        //{ id: 185, question: "le parc", answer: "het park" },
        //{ id: 186, question: "le/la jeune", answer: "de jongere" },
        //{ id: 187, question: "assez", answer: "genoeg" },

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
