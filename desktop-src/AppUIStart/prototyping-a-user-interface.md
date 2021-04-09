---
title: Prototipazione di un'interfaccia utente
description: In questo argomento viene illustrata la creazione di un prototipo di un'interfaccia utente che consente di ridurre al minimo i difetti di progettazione e garantire un'esperienza utente corretta.
ms.assetid: 16e3fabb-9cd1-4517-8f19-b1d80c956ee0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148c01d31c3bee34b555ab2ce10565229a7d1fb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955068"
---
# <a name="prototyping-a-user-interface"></a>Prototipazione di un'interfaccia utente

In questo argomento viene illustrata la creazione di un prototipo di un'interfaccia utente che consente di ridurre al minimo i difetti di progettazione e garantire un'esperienza utente corretta.

## <a name="introduction"></a>Introduzione

In alcuni casi, quando un progetto si sposta in futuro, presupposti ridotti e decisioni ben intenzionate ma insufficienti si accumulano, trasformando ore di lavoro in un'esperienza utente scadente. Gli smart team eliminano gli errori prima della spedizione usando una tecnica denominata prototipazione interfaccia utente. Combinati con gli studi di usabilità, i prototipi mantengono i team diretti nella direzione giusta.

## <a name="why-prototype"></a>Vantaggi del prototipo

Il prototipo è un mezzo per esplorare le idee prima di investirle. Tutti i tecnici e gli artigiani esperti creano prototipi del proprio lavoro prima di compilare qualsiasi elemento, ovvero architetti che creano modelli fuori carta o cartone o con strumenti di realtà virtuale. I tecnici aeronautici usano i tunnel del vento. I generatori di Bridge creano modelli di stress. Il software e i progettisti Web creano le simulazioni del modo in cui gli utenti interagiranno con i loro progetti.

Il prototipo è il modo migliore per risparmiare tempo e risorse. Il valore di un prototipo è che si tratta di una facciata, ad esempio un set di Hollywood, in cui viene costruita solo la parte iniziale della compilazione. Rispetto al prodotto reale, i prototipi sono semplici ed economici da creare. Pertanto, per un investimento minimo, è possibile trovare problemi di usabilità e progettazione e l'interfaccia utente modificata prima di sostanziali investimenti nel progetto e nelle tecnologie finali.

Quando si esaminano le esigenze di un progetto specifico, è possibile che vengano rilevati i motivi per la creazione di un prototipo diverso dal risparmio di denaro. L'obiettivo è esplorare un nuovo modello di interfaccia? Apportare modifiche a una parte della progettazione esistente? Esaminare una nuova tecnologia? Prima di iniziare, è importante chiarire il motivo per cui si sta creando ciò che si sta creando. A partire da Clear Goals consente di rendere il lavoro diretto ed efficace. I motivi per la creazione di prototipi rientrano in tre categorie di base:

-   Modello di prova.

    Tra alcuni team ci sono disaccordi sulla direzione futura di un progetto. Un prototipo può essere usato per dimostrare che un'idea o un nuovo approccio ha un merito o un valore. Un prototipo può essere utile per illustrare il funzionamento di un'idea, esprimere le proprie qualità in modo visivo e interattivo e/o motivare i membri del team a pensare al problema da un'altra prospettiva.

-   Esplorazione della progettazione.

    Se si progetta un software interattivo, l'unico modo per esplorare la modalità di utilizzo di un elemento consiste nel creare una simulazione e interagire con esso. Talvolta la simulazione è legata a uno studio di usabilità, in cui le parti del prototipo possono essere valutate in modo strutturato. In alcuni casi è semplicemente un modo per esprimere chiaramente a uno sviluppatore il modo in cui un elemento dovrebbe funzionare. In molti casi, è possibile che una finestra di progettazione stia semplicemente sperimentando, nel tentativo di ottenere un senso per l'approccio che potrebbe funzionare. Chiunque nel team può utilizzare i prototipi per esplorare i problemi di progettazione, anche se i progettisti sono in genere i più qualificati. Le esplorazioni di progettazione devono essere indirizzate al tentativo di risolvere problemi specifici riconosciuti nel prodotto.

-   Esplorazione tecnica.

    Gli sviluppatori che analizzano gli approcci di implementazione a un problema spesso provano diverse tecniche di codifica per verificare se funzionano correttamente. L'uso di COM+, DHTML (Dynamic HTML), Microsoft Win32 o approcci di codifica specifici all'interno di ogni tecnologia presenta compromessi diversi. In alcuni casi un prototipo rappresenta un'esplorazione della tecnologia che funzionerà correttamente per supportare una determinata funzionalità dell'interfaccia utente.

A volte vengono creati prototipi per una combinazione di questi motivi. Se un team è sufficientemente pianificato, può allocare tempo per uno sviluppatore e una finestra di progettazione o project manager per interagire con un prototipo. In questi casi, è estremamente importante definire chiaramente gli obiettivi e i contributi che ciascun membro del team deve prendere. Chiunque debba essere chiaro sugli obiettivi, su cosa è in gioco e su quale sarà il potenziale risultato.

## <a name="who-is-involved"></a>Chi è impegnato?

Il prototipo può essere eseguito in modo informale da chiunque, indipendentemente dal loro background o ruolo nel progetto. È facile creare un prototipo semplice ma efficace acquisendo una bitmap da Adobe Photoshop, inserendolo nello strumento per la creazione e la gestione di siti Web di Microsoft FrontPage e aggiungendo pulsanti o collegamenti attivi. Questi prototipi leggeri sono solo fino a questo punto e possono diventare difficili da usare per interazioni complesse.

Per i prototipi più formali di team più grandi, uno sviluppatore o un project manager collaborerà spesso con una finestra di progettazione e un tecnico di usabilità. Insieme generano idee, compilano un prototipo che rappresenta le idee ottimali e poi entrano nel Lab per vedere quanto è efficace per la risoluzione dei problemi degli utenti. Gli sviluppatori potrebbero essere impegnati se possono risparmiare tempo o se sono necessarie competenze tecniche. Spesso la finestra di progettazione o la project manager eseguiranno la maggior parte degli script o della codifica per compilare il prototipo.

## <a name="when-should-a-prototype-be-built"></a>Quando deve essere compilato un prototipo?

A seconda dell'ambito del prototipo e del livello di dettaglio richiesto, i prototipi possono essere creati in qualsiasi momento durante il progetto. Spesso vengono creati all'inizio del progetto, durante la fase di pianificazione e specifica, prima che gli sviluppatori scrivano il codice di produzione. Questo è il momento in cui la necessità di eseguire l'esplorazione è maggiore e quando il tempo necessario per l'investimento è la maggior parte possibile. Se gli sviluppatori anziché i responsabili del programma o i progettisti eseguono la creazione di prototipi, il tempo di pianificazione diventa ancora più importante a causa della necessità di assicurarsi che il lavoro investito nel prototipo venga considerato nella pianificazione dello sviluppo. La pianificazione di qualsiasi versione dell'interfaccia utente deve includere un certo livello di prototipazione.

In ritardo in un progetto, i prototipi più piccoli possono contribuire alla risoluzione di problemi tecnici e di progettazione difficili. Una rapida simulazione HTML del comportamento di una finestra di dialogo o di una pagina Web può contribuire a rispondere a una domanda dello sviluppatore o a un altro compagno di squadra per conoscere l'esperienza desiderata. In alcuni casi, un gestore di programmi o un progettista forte può implementare il comportamento nel software di sviluppo Microsoft JScript e approssimarsi alla maggior parte della logica di programmazione che gli sviluppatori dovranno considerare.

Il tempo necessario per creare un prototipo può variare notevolmente, a seconda dell'ambito e della precisione dell'aspetto del risultato finale. Un prototipo informale potrebbe indicare alcune ore di lavoro di una sola persona; un lavoro più organizzato può coinvolgere settimane di lavoro da un intero team.

## <a name="where-should-the-focus-be"></a>Dove si trova lo stato attivo?

In un prototipo, compilare solo la maggior parte della progettazione necessaria. È possibile fare in modo che i pulsanti non funzionino o che il testo non venga mai aggiornato. Fino a quando le interazioni richieste possono essere rilevate, è bene usare Smoke e Mirrors per il resto. Di seguito sono riportati alcuni motivi per cui è necessario concentrarsi attentamente sulle attività:

-   Costo della compilazione del prototipo.

    Il costo necessario per la creazione del prototipo dovrebbe essere ridotto al minimo. La sfida per la creazione di prototipi consiste nel riconoscere l'investimento minimo necessario per rispondere in modo efficace alle domande sul progetto. Questo è il punto in cui gli studi di usabilità sono essenziali, perché identificano chiaramente le parti dell'interfaccia utente che richiedono la maggior parte del lavoro. Anche senza gli studi sull'usabilità, definire chiaramente quali problemi degli utenti vengono risolti o quali attività sono state migliorate con la progettazione nel prototipo.

-   Durata limitata.
-   I prototipi dovrebbero avere durate chiaramente definite. L'obiettivo finale è una presentazione in una riunione del team? Una riunione di revisione esecutiva? Una verifica delle specifiche? Uno studio sull'usabilità? Identificazione della soluzione che risolve un problema utente Una volta soddisfatte le esigenze di questi obiettivi specifici, è consigliabile riservare il prototipo. Il concetto di base è che il codice o le bitmap generate in un prototipo rimarranno indietro. Potrebbero esserci eccezioni in cui il codice o gli oggetti visivi risiedono nel prodotto, ma l'aspettativa dovrebbe essere che questo non sia il caso.
-   Rischio di sovraccaricare il team.

    La visualizzazione di prototipi per sviluppatori e colleghi può risultare complessa. Un prototipo troppo complesso o elaborato, che sfoggia oggetti visivi straordinari e animazioni, può sopraffare gli utenti. È necessario avere sempre un senso per quanto riguarda la velocità e la quantità di prototipi che devono essere presi in considerazione.

## <a name="what-is-the-scope"></a>Qual è l'ambito?

Poiché viene determinato lo stato attivo per il prototipo, tenere presente quanto segue:

-   Esigenze del cliente.

    Partendo da una comprensione dei problemi principali o delle esigenze degli utenti (ad esempio, un ingegnere di usabilità fornito) fornisce un'idea di quali parti della progettazione dell'interfaccia utente garantiscano la maggior parte dell'esplorazione.

-   Attività di studio sull'usabilità.

    Se si crea il prototipo per uno studio di usabilità, discutere con il progettista dell'usabilità le attività specifiche che faranno parte dello studio e la progettazione intorno a tali elementi.

-   Input del team.

    Comunica con gli sviluppatori principali del team come le idee nel prototipo sono disponibili insieme. Ottenere un senso di base per quanto ragionevole, cosa è possibile e cosa non è più considerato per la prossima versione. In alcuni casi, si consiglia di andare oltre quello che dicono è possibile per un aspetto della progettazione se è un punto chiave e il team deve essere sottoposto a test. Tuttavia, non eseguire questa operazione con tutti gli aspetti del prototipo perché esiste una linea sottile tra il push dei limiti e il sovraccarico del team. Se il desiderio è quello di ispirare il team mostrando loro una visione per diverse versioni, è possibile procedere. Tuttavia, se il requisito prevede la definizione di modifiche specifiche per la versione successiva, concentrare gli sforzi su tali modifiche. Assicurarsi di richiamare le modifiche specifiche in modo modulare e mostrare agli sviluppatori un percorso per la compilazione delle progettazioni.

-   Larghezza rispetto a profondità.

    Per i prototipi di dimensioni maggiori, c'è la considerazione aggiuntiva della larghezza e della profondità. Ogni funzionalità della progettazione può funzionare solo un po' o deve essere scelta una funzionalità per il prototipo con quasi tutte le parti e le opzioni? Provare a non eseguire entrambe le operazioni perché il risultato potrebbe essere un prototipo grande e ingombrante che è difficile da modificare e di cui è difficile eliminarlo.

## <a name="flexible-prototypes"></a>Prototipi flessibili

Un modo per concentrare le risorse di creazione di prototipi consiste nel concentrarsi sulla progettazione intelligente. È possibile creare prototipi più efficaci consentendo a una parte del codice del prototipo di esercitare diverse idee. Anziché avere cinque prototipi diversi, provare a creare un prototipo con le opzioni per cambiare i diversi attributi del prototipo.

La barra degli strumenti è posizionata a sinistra o in alto? È necessario visualizzare 10 elementi nell'home page o 20? Un prototipo valido dispone di un pannello Opzioni incorporato che consente di modificare i parametri dell'aspetto o del funzionamento del prototipo. Mantenendo i pannelli delle opzioni nascosti nel prototipo, provare a evitare che un partecipante all'usabilità li ritrovi accidentalmente durante un test.

Il problema consiste nel mantenere il prototipo semplice, ma ancora utile per poter essere visualizzato a un compagno di squadra, è possibile dimostrare diverse opzioni ed è possibile ottenere commenti e suggerimenti.

## <a name="beta-vs-prototype"></a>Beta rispetto a Prototype

Le versioni beta non sono qualificate come prototipi, perché si tratta di attività di progettazione complete. Se viene rilevato un errore critico in una funzionalità di una versione beta, è improbabile che venga ignorato, anche se potrebbe essere il migliore interesse del prodotto. Gli sviluppatori, i tester e i progettisti hanno già investito molto tempo e la pressione per vivere con decisioni negative è molto elevata. Le versioni beta sono certamente utili per individuare bug e difetti, ma sono raramente utili per eseguire studi controllati sul valore di specifiche direzioni di progettazione.

## <a name="tools-and-technologies"></a>Tools and Technologies

Sono disponibili diversi strumenti e tecnologie che è possibile utilizzare per la creazione di prototipi, ciascuno dei quali presenta vantaggi e svantaggi. Prendere in considerazione il tipo di lavoro di progettazione sottoposto a prototipo e gli obiettivi del tentativo di creazione di prototipi prima di decidere quale strumento o tecnologia è quello più adatto.

-   Microsoft Visual Basic o C#.

    Si tratta della tecnologia più veloce per la creazione di prototipi di interfaccia utente in stile Windows. L'oggetto Web browser facilita l'integrazione di HTMLUI con componenti di tipo Windows standard. Sebbene sia vero che uno sviluppatore che ha sperimentato Microsoft Visual Studio potrebbe essere in grado di generare l'interfaccia utente più velocemente in C/C++, questo crea la tentazione di riutilizzare il codice dal prototipo dell'interfaccia utente nel codice di produzione. Il reparto IT accetta la disciplina per riconoscere che gli obiettivi di un prototipo di interfaccia utente rapido e Dirty sono fortemente divergenti rispetto alla progettazione di alta qualità. Verificare che il tipo di codice da scrivere sia chiaro e che il team o il Manager conosca cosa verrà rimosso.

-   Microsoft Expression Blend + SketchFlow.

    SketchFlow è uno strumento visivo per la progettazione, la creazione di prototipi e la creazione di interfacce utente sofisticate per le applicazioni desktop e Web di Windows Presentation Foundation (WPF) e Microsoft Silverlight. Le applicazioni vengono compilate disegnando forme, disegnando controlli quali pulsanti e caselle di riepilogo, facendo in modo che le parti di un'applicazione rispondano ai clic del mouse e ad altri input utente e applicando lo stile a tutti gli elementi.

-   Adobe Director o Adobe Flash.

    Director è un diffuso strumento di prototipazione dell'interfaccia utente tra le finestre di progettazione. È particolarmente utile per le progettazioni GUI multimediali o non standard o per i prototipi che richiedono animazioni significative. Si tratta di una flessibilità elevata che rende più complessa l'interfaccia utente in stile interfaccia utente rispetto a Visual Basic. Tuttavia, un utente esperto del Director può generare Windows o un'interfaccia utente Web senza difficoltà.

-   HTML.

    FrontPage e altri editor HTML consentono la creazione rapida di prototipi semplici. Per esprimere un'idea, spesso è possibile creare bitmap che illustrino una sequenza di interazione dell'utente e inserirle in FrontPage. Queste immagini possono essere usate per simulare la modalità di interazione con la progettazione. JScript e DHTML si riportano a un altro livello, consentendo una logica e un'interazione molto sofisticate. Se si usa HTML per creare un prototipo di un sito Web, l'avviso appena descritto per C/C++ si applica anche in questo caso, non rientrare nella trappola del codice prototipo rapido con la progettazione della qualità di produzione.

 

 




