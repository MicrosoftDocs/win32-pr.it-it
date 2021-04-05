---
title: Considerazioni di progettazione e motivazioni aziendali accessibili per i video
description: Questo articolo si riferisce agli sviluppatori e ai produttori di contenuti del gioco che vogliono raggiungere il mercato della community di accessibilità aggiungendo funzionalità di accessibilità di base per aiutare gli utenti con disabilità o problemi.
ms.assetid: 95580b75-fb8e-b8a9-2137-40d6c60ae35d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74499068877a400a94eb0ca32c2a1aff4bcf6c6d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728594"
---
# <a name="making-video-games-accessible-business-justifications-and-design-considerations"></a>Rendere accessibili i videogiochi: le motivazioni aziendali e le considerazioni di progettazione

Gli editori e gli sviluppatori di giochi amano concentrarsi sulle funzionalità che riceveranno i titoli rilevati dalla community di giochi mainstream, ad esempio grafica e audio. Tuttavia, c'è un altro pubblico, desidero partecipare anche a questi giochi. Questi giocatori provengono dalla community di accessibilità una community di persone con disabilità, oltre a quelle che interessano il loro benessere.

Questo articolo si riferisce agli sviluppatori e ai produttori di contenuti del gioco che vogliono raggiungere il mercato della community di accessibilità aggiungendo funzionalità di accessibilità di base per aiutare gli utenti con disabilità o problemi. Verranno discussi gli argomenti seguenti:

-   [Che cos'è l'accessibilità?](#what-is-accessibility)
-   [Perché l'accessibilità è importante?](#why-is-accessibility-important)
-   [Stato di accessibilità nel settore dei giochi](#the-state-of-accessibility-in-the-games-industry)
-   [La necessità di giochi accessibili](#the-need-for-accessible-games)
-   [Problemi visivi](#visual-impairments)
-   [Problemi uditivi](#auditory-impairments)
-   [Problemi di mobilità](#mobility-impairments)
-   [Problemi vocali](#vocal-impairments)
-   [Conclusione](#conclusion)
-   [Altre risorse](#more-resources)

## <a name="what-is-accessibility"></a>Che cos'è l'accessibilità?

Spesso, quando gli utenti considerano l'accessibilità, pensano a cose come le rampe per la carrozzella e la didascalia chiusa sulla televisione. Questo è dovuto al fatto che questi tipi di funzionalità di accessibilità si distinguono e vengono usati da utenti con particolari esigenze. Tuttavia, le funzionalità di accessibilità non sono progettate solo per quelle con le disabilità più gravi. Tra gli utenti di computer statunitensi che variano da 18 a 64 anni, il 57% (74,2 milioni) può trarre vantaggio dall'uso della tecnologia accessibile a causa di disabilità e problemi che potrebbero influire sull'uso del computer. ("[Il mercato per la tecnologia accessibile: la vasta gamma di capacità e il suo effetto sull'uso del computer](https://www.microsoft.com/enable/research/phase1.aspx)", Microsoft Corporation) La possibilità di trasformare il volume di un telefono pubblico consente agli utenti con una lieve perdita di udito di usarli. Una guida della mano su una rampa di scale consente a una persona che non è associata alla mobilità di scalarli più facilmente.

In alcuni casi, le funzionalità normali di un prodotto sono le funzionalità che possono aiutare gli utenti con difficoltà. Ad esempio, un utente con problemi visivi può utilizzare le impostazioni di contrasto in un televisore per semplificare la visualizzazione della schermata. Una persona con malattia di Parkinson può utilizzare una composizione tocco per semplificare la chiamata telefonica.

Le funzionalità di accessibilità in genere tendono a offrire uno dei cinque tipi di disabilità:

-   Cecità visiva, impossibilità di distinguere i colori, la visione sfocata e così via.
-   Udito acustico, sordità.
-   Problemi di sintesi vocale, differenze di linguaggio.
-   Mobilità: polso, ARM, gambe e problemi di mano.
-   Problemi di apprendimento cognitivo e problemi di ragionamento, inclusa la dislessità.

Nel contesto dei giochi video, l'aggiunta dell'accessibilità significa rendere un titolo utilizzabile a qualcuno con una di queste disabilità.

## <a name="why-is-accessibility-important"></a>Perché l'accessibilità è importante?

Esistono motivi sociali e finanziari per i quali gli sviluppatori di giochi dovrebbero pensare di rendere accessibili i loro prodotti.

Per i figli e i giovani adulti con disabilità che variano da lievi a gravi, i giochi video possono offrire diversi vantaggi. I ricercatori della Wheeling Jesuit University hanno recentemente scoperto che la riproduzione di giochi sportivi o giochi di combattimento aiuta a distrarre i figli e i giovani adulti affetti da dolori cronici (il Journal Edmonton, 13 febbraio 2006). Inoltre, i giochi video sono stati rivelati utili per aiutare i bambini ad affrontare la chirurgia in modo più efficace e con un minor numero di effetti collaterali rispetto ai tranquillizzanti (la pressione associata, il 19 dicembre 2004). I giochi vengono usati anche per il trattamento del cancro; l'esercizio, estremamente importante per il ripristino dopo la chemioterapia, è stato incoraggiato attraverso l'uso di giochi come la rivoluzione Dance Dance (c) quando i figli rifiutano di partecipare ad altre forme di attività fisiche.

Inoltre, consentire agli utenti con problemi (in particolare gli elementi figlio) di partecipare alle attività che la maggior parte degli utenti ha goduto e di ottenere per la concessione può contribuire a ridurre il dolore emotivo e la sensazione di essere estranei.

I motivi sociali non sono gli unici motivi per cui gli sviluppatori di giochi devono introdurre le funzionalità di accessibilità nei propri titoli. Le funzionalità di accessibilità possono aumentare le vendite incoraggiando gli utenti con disabilità ad acquistare un titolo accessibile. Maggiori vendite possono derivare anche da giocatori che vogliono supportare una società che supporta la community di accessibilità. Infine, il PR positivo dal supporto e dai gruppi di advocacy per l'accessibilità è disponibile la pubblicità gratuita.

La richiesta di accessibilità continuerà a crescere man mano che la popolazione dei giochi invecchia. Man mano che le persone crescono meno recenti, le difficoltà possono diventare più gravi. Inoltre, è probabile che gli utenti sviluppino nuove difficoltà e problemi di cui hanno età. L'aggiunta di funzionalità di accessibilità di base ai titoli consente agli editori e agli sviluppatori di continuare a creare ricavi da questi clienti.

## <a name="the-state-of-accessibility-in-the-games-industry"></a>Stato di accessibilità nel settore dei giochi

Per la maggior parte del settore dei giochi, l'accessibilità nei giochi video è una priorità bassa. Un motivo è dovuto a una mancanza di consapevolezza tra gli sviluppatori sui problemi di accessibilità: gli sviluppatori che non sono disabilitati potrebbero non essere consapevoli dei modi in cui è possibile rendere un titolo più accessibile per gli utenti con disabilità o difficoltà.

Un altro motivo è che gli sviluppatori hanno una quantità limitata di tempo e risorse. Le analisi dei vantaggi economici spesso concludono che i problemi di accessibilità non sono degni di attenzione e di investimento del settore dei giochi, a causa dei presupposti seguenti:

-   Il costo di implementazione delle funzionalità di accessibilità non vale la pena restituire.
-   Non esiste un numero sufficiente di destinatari per rendere utile lo sviluppo dell'accessibilità.

Questi presupposti sono errati. Rendere accessibili i giochi è molto utile per gli investimenti.

## <a name="the-need-for-accessible-games"></a>La necessità di giochi accessibili

In 2003, Microsoft Corporation ha commissionato Forrester Research, Inc., per condurre uno studio completo per misurare il mercato attuale e potenziale della tecnologia accessibile nel Stati Uniti e comprendere il modo in cui viene attualmente utilizzata la tecnologia di accessibilità. Lo studio ha determinato che il 57% degli utenti di computer è probabilmente o con molta probabilità di trarre vantaggio dall'uso della tecnologia accessibile. E la richiesta futura di accessibilità viene proiettata solo per crescere ("[tecnologia accessibile nel calcolo: analisi della consapevolezza, dell'uso e potenziale futuro](https://www.microsoft.com/enable/research/phase2.aspx)" Microsoft Corporation).

**Figura 1. Incremento stimato del numero di utenti di tecnologie accessibili da 2003 a 2010**

![incremento stimato del numero di utenti di tecnologie accessibili da 2003 a 2010](images/accessibility-growth.gif)

Lo studio ha inoltre determinato che l'uso delle funzionalità di accessibilità non è stato limitato a utenti con particolari esigenze. Tra gli utenti di computer che utilizzano opzioni e utilità di accessibilità predefinite:

-   32% non hanno capacità o problemi.
-   68% hanno una disabilità o una difficoltà lieve o grave.

L'osservazione empirica suggerisce che non si tratta solo di una tendenza limitata ai PC. Le funzionalità di accessibilità vengono spesso usate dagli utenti senza alcuna disabilità solo per migliorare l'esperienza di gioco. È ad esempio possibile che un giocatore stia compensando una disabilità temporanea, ad esempio un pollice rotto, problemi ambientali, come il rumore di fondo, o altri fattori di situazione.

Dato il potenziale aumento dell'utilizzo della tecnologia di accessibilità, è fondamentale per educare la gestione, i progettisti, gli sviluppatori e i tester. Molte aziende stanno cercando modi per espandersi in nuovi mercati al di fuori della 18-32 demografica maschile. Mentre gli editori mullano su come convincere Little Suzy a interpretare giochi o nonne e nonni per prelevare un controller, c'è un mercato costituito da persone che vogliono disperatamente giocare ai giochi mainstream che non sono stati osservati. I potenziali ricavi da ottenere da una quantità relativamente ridotta di risorse che forniscono le funzionalità di accessibilità di base in un titolo sono molto tangibili.

L'inclusione delle funzionalità di accessibilità di base in un titolo può aumentare le vendite tramite un "effetto domino", ad esempio raggiungendo i giocatori che normalmente non sarebbero in grado di riprodurre il titolo o avrebbero diminuito significativamente la loro esperienza. Raggiungendo questi giocatori, si raggiunge anche la community di accessibilità, nota per una rapida condivisione delle informazioni sui prodotti accessibili e il suo fedele supporto di aziende che promuovono l'accessibilità. Per estensione, le aziende che hanno un ruolo attivo in questa community traggono vantaggio dall'esposizione positiva dei supporti.

Senza includere le funzionalità di accessibilità, è possibile eseguire il rischio di potenziali boicottamenti e cause, oltre alla conseguente perdita di vendite. Molti rivenditori e compagnie aeree sono stati citati per mancanza di accessibilità e, nel settore tecnologico, la community cieca boicottava Internet Explorer 4 per la mancanza di accessibilità.

Di seguito sono riportate diverse categorie di disabilità. Ogni categoria include alcuni suggerimenti relativamente facili da implementare che possono rendere un titolo accessibile a un pubblico più ampio.

## <a name="visual-impairments"></a>Problemi visivi

*"La mia presentazione è stata seguita da una sessione di domande e risposte vivace e un momento significativo si è verificato quando uno dei dipendenti ha posto una domanda sull'accessibilità nei \[ nostri \] giochi... Questo personale di 28 anni è un appassionato che ha usato per giocare al \[ gioco \] con un ampio cerchio di amici. Dato che è daltonico, tuttavia, è stato difficile per lui raccontare ai bravi Guy dei cattivi e il gioco diventava troppo frustrante. Quando la nuova versione... il problema è stato risolto e i \[ \] suoi amici hanno deciso di acquistare il gioco di un concorrente. "un dirigente del settore Anonimo*

Il termine "problemi visivi" porta spesso a mente un utente che è completamente cieco. Tuttavia, è sorprendente tenere presente che il 8,7% del popolamento maschile è influenzato da un certo livello di cecità dei colori ("in[che modo le persone ereditano daltonismo? Con quale frequenza?](https://www.webexhibits.org/causesofcolor/2C.mdl), "WebExhibits.org). Un altro 1,2% di persone è interessato da forme più gravi di problemi visivi ("[informazioni sulle disabilità: foglio dei fatti visivi di disaccoppiamenti](https://nichcy.org/disability/specific/visualimpairment)", il centro di diffusione nazionale per gli elementi figlio con disabilità). Ciò significa che quasi uno dei dieci potenziali giocatori ha problemi che influiscono sulla loro vista che possono influire negativamente sull'esperienza di gioco.

Per comprendere i problemi visivi, si supponga che:



| Sei un giocatore      | In questo scenario                                                                                                                                                                         |
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Con visione normale   | È luminosa e soleggiata, quindi non è possibile visualizzare gli oggetti scuri sullo schermo. <br/> Si dispone di un set di televisori precedente, pertanto non è possibile visualizzare oggetti e testo di piccole dimensioni a causa della scarsa qualità dell'immagine. <br/> |
| Con visione disaccoppiata | Il testo del gioco è talmente piccolo che non è possibile leggerlo. <br/> Il colore è cieco, quindi non è possibile sapere quale pulsante premere quando il gioco indica di premere il pulsante rosso. <br/>                   |



 

Con pochi semplici passaggi e funzionalità, è possibile risolvere questi problemi e migliorare l'esperienza di gioco sia per i giocatori con visione normale che per i giocatori con problemi visivi.

1.  Test dei titoli nei televisori neri e bianchi. Prendere nota di tutte le istanze in cui non è possibile distinguere elementi, giocatori, obiettivi e comandi e modificare di conseguenza la tavolozza dei colori.
2.  Offrire ai giocatori un'opzione per aumentare le dimensioni del testo sullo schermo. Consente inoltre di modificare la velocità di scorrimento del testo. È importante ricordare che l'esperienza console è di 10 metri, non per l'esperienza di gioco a 2 piedi per molti sviluppatori di PC. Anche per i giocatori senza problemi di visione, l'interfaccia utente e il testo di piccole dimensioni possono essere difficili da leggere a lunghe distanze.
3.  Fornire funzionalità di sintesi vocale che possono esprimere tutto il testo del gioco, inclusi i menu di gioco che tengono traccia dello stato attivo sui pulsanti. Consente all'utente di controllare la velocità, il pitch e il sesso della voce. Per impedire che la sintesi vocale venga annullata da altri rumori del gioco, offrire agli utenti la possibilità di modificare il volume di sintesi vocale, rumore di ambiente, suoni del gioco attivi e musica. Includere anche l'opzione per riprodurre suoni distinti durante la transizione tra le voci di menu e i pulsanti.
4.  Infine, offrire ai giocatori l'opzione per modificare le impostazioni di luminosità e contrasto nel gioco. Fornire agli utenti la possibilità di scegliere le proprie combinazioni di colori personalizzate in modo che i colori del testo, dello sfondo e dell'HUD possano essere configurati in base alle esigenze di un utente.

## <a name="auditory-impairments"></a>Problemi uditivi

*"I ricordi di Half-Life tornare a rimandarci come un altro capolavoro tecnologico \[ Halo \] è inutile per il Gamer sordo... Ci auguriamo che non sia possibile pregare. che se Halo 2 vedrà mai la luce del giorno in cui verrà completamente sottotitolo. "www.DeafGamers.com*

Il successivo tipo di problemi più diffusi che possono influenzare la riproduzione del gioco è dovuto a problemi uditivi. Negli Stati Uniti, oltre 28 milioni persone sono interessate da una sorta di problemi di udito. Sebbene le anomalie uditive siano spesso associate a Age, 17 di ogni 1.000 figli sotto la età di 18 sono interessati da un problema di udito ("[statistiche sui disturbi uditivi, infezioni auricolari e sordità](https://www.nidcd.nih.gov/health/statistics/pages/hearing.aspx)", Istituto nazionale sulla sordità e altri problemi di comunicazione). Quando si considera che i giocatori di oggi stanno diventando più vecchi e perdono la loro udienza a una velocità sempre crescente, è chiaro che la richiesta di accessibilità audio aumenterà solo.

Per comprendere i problemi di disaccoppiamento uditivo, si supponga che:



| Sei un giocatore           | In questo scenario                                                                                                                                                                                                                                                            |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Con udienza normale       | Non si vuole disturbare nessuno in modo da giocare con il suono disattivato, ma non è possibile riprodurre il gioco perché le direzioni sono fornite solo nell'audio. <br/>                                                                                                                               |
| Con problemi di udito | Si tratta di un gioco a gran parte, ma non si può dire che l'utente è sotto tiro perché non è possibile sentire le armi.<br/> Il gioco ha molto rumore di ambiente e non è possibile udire le istruzioni verbali fornite. <br/>                                                     |
| Chi è sordo               | Il commento audio è così flessibile, non è possibile ascoltarlo, neanche in una stanza silenziosa. <br/> Tutti gli obiettivi sono assegnati all'utente in audio e non è possibile determinare ciò che si dovrebbe fare. <br/> Tutte le storie sono fornite verbalmente e non è possibile seguire la procedura. <br/> |



 

Con alcune attività relativamente secondarie, è possibile rendere il gioco utilizzabile e divertente per i giocatori con audizione normale e per i giocatori che hanno problemi uditivi.

1.  Chiudere la didascalia tutte le finestre di dialogo. Sono inclusi il contenuto del gioco e gli cinematici. Fornire al giocatore la possibilità di attivare e disattivare queste didascalie.
2.  Quando un effetto acustico fornisce informazioni essenziali, fornire un meccanismo testuale o tattile (vibrazione) anche per i commenti. Se, ad esempio, in genere una bomba nel gioco rende più veloce il rumore di un bip vicino alla propria esplosione, fornire un indicatore visivo (ad esempio una barra temporale) che consente anche al giocatore di conoscere quanto tempo rimane prima dell'esplosione.
3.  Se il gioco supporta online Play, è possibile offrire ai giocatori la possibilità di inviare messaggi di testo e di usare la propria voce per fornire informazioni tra i membri del team e altri giocatori online. Una cuffia non è utile per un utente che non è in grado di ascoltare e, sempre più, i giocatori stanno cercando di giocare con altri utenti con cui possono comunicare e strategie online.

## <a name="mobility-impairments"></a>Problemi di mobilità

*"I videogiochi offrono alle persone con disabilità l'opportunità di riconnettersi con i loro coetanei e le sue capacità perse o mai. La mia esperienza personale deriva dal fatto che la mia depressione è stata paralizzata al periodo di 14 anni, visitando il centro ricreativo nell'ospedale e l'unico interesse che ho dovuto uscire dalla mia depressione era quello di riprodurre il sistema di videogame. Ho perso l'interesse quando ho imparato a non poterlo riprodurre... " Robert Florio*

I problemi di mobilità sono forse il più difficile tra le diverse difficoltà per ottenere statistiche aziendali. Ciò è dovuto principalmente al fatto che queste difficoltà possono essere causate da patologie, patologie neurologiche, perdita di elementi/cifre, paralisi e così via, che possono avere un certo livello di influenza sull'esperienza di un giocatore video. Queste difficoltà possono essere congenite oppure possono verificarsi in un secondo momento.

Per comprendere i problemi di disaccoppiamento uditivo, si supponga che:



| Sei un giocatore                                 | In questo scenario                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Senza problemi di mobilità                     | Il controller del gioco è costituito da un numero così elevato di pulsanti, ovvero un giocatore occasionale, che non si desidera apprendere come utilizzarlo. <br/>                                                                                                                                                                          |
| Con problemi di mobilità temporanei            | Si ha un pollice rotto, quindi non è possibile usare levetta nel controller. <br/> Si ha un piede rotto, quindi non è possibile usare il riquadro danza per un titolo di danza.<br/>                                                                                                                                     |
| Con problemi di mobilità permanenti e gravi | Si è perso un ARM, pertanto non è possibile usare un controller a due mani. <br/> Si dispone della malattia di Parkinson, delle mani agitate e che consente di attivare accidentalmente i pulsanti sul controller. <br/> L'utente è paralizzato dall'arresto del collo, quindi non è possibile usare un controller di gioco standard. <br/> |



 

Prendere in considerazione tutti questi giochi è complesso, ma è possibile tenere presente alcuni aspetti semplici quando si sviluppano i giochi.

1.  Ridurre a icona l'uso del pulsante e pensare alle interfacce di menu per i comandi. Questa operazione è particolarmente utile per utenti che potrebbero mancare cifre o una mano. È utile anche per gli utenti paralizzati che usano controller personalizzati.
2.  Consentire ai giocatori di personalizzare la configurazione del controller e la sensibilità del pulsante/levetta. Ciò consentirà agli utenti con problemi di competenze motorie di personalizzare il controller per ridurre al minimo l'effetto della loro disabilità durante il gioco. Consente inoltre un migliore supporto dei controller personalizzati per le persone affette da disabilità.
3.  Se il gioco usa un tipo specifico di periferica (Dance Pad, Light Gun e così via), consentire ad altri controller di eseguire le stesse funzioni. Ad esempio, un gioco come Dance Dance Revolution (c) consente anche a singoli utenti con restrizioni per la carrozzella di giocare insieme ai loro amici tramite un normale controller di mano.

## <a name="vocal-impairments"></a>Problemi vocali

Le difficoltà vocali costituiscono una percentuale relativamente ridotta della community di disabilità. Le statistiche specifiche sono difficili da visualizzare, ma l'evidenza mostra che la maggior parte delle difficoltà vocali è collegata ad altre disabilità (ad esempio, il motore o problemi di udito). Tuttavia, poiché un maggior numero di editori di giochi inizia a esplorare l'uso di conferenze vocali e riconoscimento vocale nei propri titoli, le persone con problemi vocali inizieranno a vedere la qualità dell'esperienza di gioco in calo. Per ovviare a questo problema, è possibile implementare funzionalità di accessibilità di base.

Per comprendere i problemi di disaccoppiamento uditivo, si supponga che:



| Sei un giocatore             | In questo scenario                                                                                                                                                                                                                                           |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Senza problemi vocali    | Si sta giocando a un gioco che richiede comandi vocali per controllare i caratteri e non è possibile giocare perché non è presente un microfono. <br/> Si sta giocando tardi e non si vuole disturbare nessuno, in modo da non poter usare Communicator. <br/> |
| Chi ha un disaccoppiamento vocale | Si sta giocando a un gioco che richiede comandi vocali per controllare i caratteri e non è possibile giocare perché il gioco non è in grado di riconoscere ciò che si sta dicendo.                                                                                                               |
| Chi non può parlare      | Il gioco che si sta giocando richiede un input vocale, pertanto non è possibile riprodurlo. <br/> Il gioco online che si sta svolgendo prevede di coordinare la strategia tramite Communicator, in modo da non poter riprodurre in modo efficace. <br/>                                               |



 

Fortunatamente, sono disponibili alcune semplici correzioni che possono rendere il gioco utilizzabile e divertente per questi giocatori.

1.  Se un gioco usa il riconoscimento vocale, fornire ai giocatori un'opzione per scegliere i comandi da un menu o una combinazione di pulsanti.
2.  Se il titolo supporta anche il multiplayer online, offrire ai giocatori la possibilità di una macro personalizzabile con messaggi audio o (anche meglio per quelli con problemi di udito). È anche possibile fornire il supporto della tastiera per la chat.

## <a name="conclusion"></a>Conclusione

A questo punto, si potrebbe pensare che non sia possibile ospitare tutti questi giocatori in tutti questi scenari. Anche se si intende implementare ogni suggerimento in questo documento, non è possibile garantire che un titolo sia completamente accessibile a tutti. Tuttavia, seguendo queste linee guida sull'accessibilità, è possibile rendere il titolo molto più accattivante per la community di accessibilità. E che possono aumentare solo le vendite.

Per rendere un titolo più accessibile, gli sviluppatori e i publisher devono trovare persone con diversi tipi di disabilità per testare l'usabilità dei giochi. Questo approccio fornisce informazioni di prima mano sul fatto che un gioco sia accessibile o meno a un determinato gruppo di destinatari. Un ulteriore vantaggio, con diverse risorse di sviluppo e testing, può offrire informazioni aggiuntive che possono migliorare la riproduzione dei giochi per tutti i giocatori. Soprattutto, coinvolgere la community di accessibilità e ottenere informazioni su questi potenziali clienti. Si tenga un gioco bash per il titolo presso un centro servizi sordi locale, l'ospedale Children o il centro veterano. Incoraggiare gli sviluppatori e i tester a collaborare con le organizzazioni locali che collaborano con persone con disabilità, per partecipare a una classe di linguaggio di firma o per iscriversi a newsletter correlate all'accessibilità per restare al passo con la community. Sollecitare commenti e suggerimenti sui titoli precedenti da giocatori disabili in scuole e istituti locali.

Nessuno mi piace sentire un estraneo. Includendo la community di accessibilità nei test dei giochi e nella progettazione, sarà possibile commercializzare il titolo a un pubblico molto più ampio ed eseguire le operazioni più appropriate per la community e per il suo fondo.

## <a name="more-resources"></a>Altre risorse

Sono disponibili numerose risorse Web che illustrano l'accessibilità dei giochi video, oltre a numerose società incentrate sui videogiochi disabilitati. Inoltre, il gruppo di tecnologie accessibile in Microsoft può essere contattato con domande sull'accessibilità correlate al PC all'indirizzo: ablecat@microsoft.com . È possibile inviare domande sull'accessibilità correlate a Xbox a: xaccess@microsoft.com .

Siti di disabilità generali:

-   [Accessibilità del gioco](https://www.game-accessibility.com/)
-   [Sito di accessibilità Microsoft](https://www.microsoft.com/enable/)
-   [Accessibilità](/previous-versions/windows/internet-explorer/ie-developer/accessibility/gg701968(v=vs.85))

Siti di disaccoppiamento uditivi:

-   [DeafGamers.com](https://www.deafgamers.com/)
-   [Libreria di risorse sorda](https://www.deaflibrary.org/)

Siti di problemi visivi:

-   [Istituto d'occhio nazionale](https://www.nei.nih.gov/)
-   [Vischeck](https://www.vischeck.com/)
-   [WebExhibits.org](https://www.webexhibits.org/causesofcolor/2.mdl)

Siti di problemi di mobilità:

-   [RobertFlorio.com](https://www.robertflorio.com/games)
-   [WebAIM](https://webaim.org/articles/motor/)

Siti di disaccoppiamento vocale:

-   [American Speech-Language-Audition Association](https://www.asha.org/public/speech/)

 

