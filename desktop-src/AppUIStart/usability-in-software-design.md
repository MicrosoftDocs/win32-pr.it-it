---
title: Usabilità nella progettazione software
description: Questo argomento introduce il concetto di usabilità e il motivo per cui deve essere una parte importante di qualsiasi progetto di progettazione software.
ms.assetid: 912b3224-e36d-44d6-98fa-a7f28e68a2d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482fd749a797c58656d987e1bde9e995ac58b8fdf98a6c056cd327e846665749
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589131"
---
# <a name="usability-in-software-design"></a>Usabilità nella progettazione software

Questo argomento introduce il concetto di usabilità e il motivo per cui deve essere una parte importante di qualsiasi progetto di progettazione software.

-   [Introduzione](#introduction)
-   [Definizione dell'usabilità](#defining-usability)
    -   [Facilità d'uso](#ease-of-use)
    -   [Usabilità e utilità](#usability-vs-utility)
    -   [Gradimento rispetto all'uso](#liking-it-vs-using-it)
    -   [Confronto tra individuazione e Learning'efficienza](#discovery-vs-learning-vs-efficiency)
    -   [Gli slogan non funzionano](#slogans-do-not-work)
-   [Perché l'usabilità è importante?](#why-is-usability-important)
    -   [Perché è opportuno?](#why-should-you-care)
    -   [Qual è il costo?](#what-does-it-cost)
    -   [Come si aumenta l'usabilità?](#how-do-i-increase-usability)
    -   [Perché è consigliabile coinvolgere gli utenti?](#why-should-i-involve-users)
    -   [Non è possibile seguire solo le linee guida?](#cant-i-just-follow-guidelines)
    -   [È necessario creare un lab di usabilità?](#do-i-need-to-build-a-usability-lab)
    -   [Come si Informazioni di base?](#how-do-i-get-started)

## <a name="introduction"></a>Introduzione

Il termine "usabilità" nel contesto della creazione di software rappresenta un approccio che pone l'utente, anziché il sistema, al centro del processo. Questa filosofia, nota come progettazione centrata sull'utente, incorpora le preoccupazioni degli utenti e la difesa fin dall'inizio del processo di progettazione e impone che le esigenze dell'utente siano le più importanti di qualsiasi decisione di progettazione.

L'aspetto più visibile di questo approccio è il test di usabilità, in cui gli utenti lavorano e interagiscono con l'interfaccia del prodotto e condividono le proprie opinioni e preoccupazioni con i progettisti e gli sviluppatori.

## <a name="defining-usability"></a>Definizione dell'usabilità

La sezione definisce il significato dell'usabilità nel contesto dello sviluppo software e la relativa relazione con altri aspetti del processo di sviluppo.

### <a name="ease-of-use"></a>Facilità d'uso

L'usabilità è una misura di quanto sia semplice usare un prodotto per eseguire attività prescritte. Questo è diverso dai concetti correlati di utilità e likeability.

### <a name="usability-vs-utility"></a>Usabilità e utilità

Un attributo centrale che determina la qualità di un prodotto è l'utilità. Questo misura se gli usi effettivi di un prodotto possono raggiungere gli obiettivi che i progettisti intendono raggiungere. Il concetto di utilità si ramifica ulteriormente nell'utilità e nell'usabilità. Anche se questi termini sono correlati, non sono intercambiabili.

L'utilità si riferisce alla capacità del prodotto di eseguire una o più attività. Maggiore è il numero di attività progettate per l'esecuzione del prodotto, maggiore è l'utilità.

Si considerino i tipici elaboratori di testo Microsoft MS-DOS della fine degli anni '80. Tali programmi hanno fornito molte potenti funzionalità di modifica e manipolazione del testo, ma richiedevano agli utenti di apprendere e ricordare decine di sequenze di tasti di carattere in grado di eseguirle. Applicazioni come queste possono essere usate con un'utilità elevata (offrono agli utenti la funzionalità necessaria) ma una usabilità bassa (gli utenti devono dedicare molto tempo e impegno per apprendere e usarle). Al contrario, un'applicazione semplice e ben progettata, ad esempio una calcolatrice, può essere molto semplice da usare, ma non offrire molta utilità.

Entrambe le qualità sono necessarie per l'accettazione del mercato ed entrambe fanno parte del concetto generale di utilità. Ovviamente, se un programma è altamente utilizzabile ma non ha alcun valore, nessuno lo userà. E gli utenti che hanno presentato un potente programma difficile da usare probabilmente resistono o cercano alternative.

I test di usabilità consentono di determinare quanto sia semplice per gli utenti eseguire determinate attività. Tuttavia, non consente direttamente di determinare se il prodotto stesso ha valore o utilità. Gli utenti possono aggiungere commenti correlati all'utilità durante i test di usabilità, ma qualsiasi commento deve essere verificato con altri metodi di ricerca più affidabili.

### <a name="liking-it-vs-using-it"></a>Gradimento rispetto all'uso

La likeability è sempre un tratto auspicabile in un prodotto. Se gli utenti come il prodotto, è più probabile che lo usino e lo consiglino ad altri utenti. Come per l'utilità, è tuttavia consigliabile prestare attenzione a non confondere la likeability con l'usabilità.

Agli utenti piace spesso un prodotto per motivi non correlati all'utilità e all'usabilità. Possono essere attratti dal suo stile o allo stato che ritiene che il prodotto conferirà loro. Gli utenti in genere desiderano prodotti altamente utilizzabili, ma non è consigliabile presupporre che un prodotto ben apprezzato sia utilizzabile.

L'usabilità indica se una persona può usare il prodotto per eseguire le attività che devono eseguire. I test di usabilità misurano principalmente le prestazioni, non le preferenze. È tuttavia possibile usare questionari standardizzati per misurare le preferenze tra i prodotti.

### <a name="discovery-vs-learning-vs-efficiency"></a>Confronto tra individuazione e Learning'efficienza

Esistono molti aspetti dell'usabilità, ma tradizionalmente il termine si riferisce in modo specifico agli attributi di individuazione, apprendimento ed efficienza.

-   L'individuazione comporta la ricerca e la ricerca della funzionalità di un prodotto in risposta a una particolare esigenza. I test di usabilità possono determinare il tempo necessario a un utente per trovare una funzionalità e il numero di errori (scelte erre sulla posizione) che l'utente effettua lungo la strada.
-   Learning si riferisce al processo tramite il quale l'utente comprende come usare una funzionalità individuata per completare un'attività. I test di usabilità possono determinare il tempo necessario per questo processo e anche il numero di errori commersi dall'utente durante l'apprendimento della funzionalità.
-   L'efficienza si riferisce al punto in cui l'utente ha "masterato" la funzionalità e la usa senza richiedere altre informazioni. I test di usabilità possono determinare il tempo necessario all'utente esperto per eseguire i passaggi necessari per usare la funzionalità.

Questi tre aspetti di base dell'usabilità sono fortemente influenzati dalla natura dell'attività in fase di esecuzione e dalla frequenza con cui l'utente la esegue. Alcune funzionalità vengono usate raramente o sono così complesse che l'utente essenzialmente le rileva ogni volta; Per queste funzionalità, Microsoft sviluppa spesso procedure guidate per guidare l'utente nel processo.

### <a name="slogans-do-not-work"></a>Gli slogan non funzionano

Gli sviluppatori di software a volte pensano che semplici parole d'ordine come "rendere il prodotto più utilizzabile" possano aiutare a risolvere i problemi di usabilità. Anche se è importante un atteggiamento positivo verso l'usabilità, solo i test di usabilità adeguati con gli utenti comuni, nel contesto del prodotto specifico in fase di creazione, possono fornire agli sviluppatori le informazioni necessarie per creare un prodotto in grado di soddisfare le esigenze degli utenti. "Rendere il prodotto più utilizzabile" dovrebbe essere lo strumento di ogni sviluppatore di software, ma ha senso solo se lo sviluppatore sa cosa significa usabilità. Il test con gli utenti comuni è il modo più affidabile per scoprirlo.

## <a name="why-is-usability-important"></a>Perché l'usabilità è importante?

La sezione risponde ad alcune domande comuni sull'importanza dell'usabilità e su come incorporare principi di progettazione centrati sull'utente nel processo di sviluppo.

### <a name="why-should-you-care"></a>Perché è opportuno?

Se le considerazioni sull'usabilità non sono già state incorporate nel processo di progettazione del prodotto, ci si potrebbe chiedere perché è necessario o auspicabile. Dopo tutto, è certamente possibile rilasciare un prodotto funzionante senza bug senza eseguire alcuna operazione di usabilità. Tuttavia, l'incorporamento di principi di progettazione centrati dall'utente può portare a un prodotto molto migliorato in diverse aree.

Il motivo migliore per eseguire test di usabilità è ridurre il numero di chiamate di supporto degli utenti. La scarsa usabilità è un motivo principale per cui gli utenti chiamano linee di supporto tecnico software e ogni responsabile della società di software e di Information Services sa quanto può essere costoso il supporto dei prodotti. Inoltre, l'addebito degli utenti per il supporto aumenta la potenziale insoddisfazione per il prodotto. Se gli utenti trovano facile usare il prodotto, non dovranno chiamare il supporto tecnico con la frequenza necessaria.

Per il software prodotto per uso interno, il motivo migliore per rendere l'usabilità una parte importante del processo di sviluppo è ridurre i costi di training. Un prodotto altamente utilizzabile è molto più facile da apprendere per gli utenti rispetto a un prodotto per cui l'usabilità non era una priorità elevata. Gli utenti apprendono le funzionalità più rapidamente e mantengono le proprie conoscenze più a lungo, il che è direttamente correlato alla riduzione dei costi di training e del tempo.

I test di usabilità consentono di migliorare l'accettazione dell'utente. L'accettazione deriva da diversi fattori, tra cui usabilità, utilità e likeability. Per i prodotti al dettaglio, l'accettazione dell'utente spesso correla direttamente l'acquisto ripetuto o la fedeltà, il che significa che è probabile che l'utente consigli il prodotto ad altri utenti. Per le applicazioni interne, l'accettazione da parte dell'utente è correlata alla disponibilità a usare il software per eseguire le attività per le quali è stato progettato, in modo da aumentare la produttività. L'aumento dell'usabilità è uno dei fattori che possono contribuire a una maggiore accettazione da parte degli utenti.

L'usabilità può aiutare a distinguere i prodotti da quelli dei concorrenti. Se due prodotti sono sostanzialmente uguali nell'utilità, il prodotto con usabilità migliore sarà probabilmente considerato superiore. Inoltre, le Windows di programmazione di base hanno livellato il campo di gioco per l'interfaccia utente di base, in modo che molti programmi che servono funzioni simili hanno un aspetto e un'azione simili. Queste analogie significano che piccole differenze nell'usabilità possono avere un grande effetto sulle preferenze dell'utente.

Infine, ogni prodotto viene testato per l'usabilità alla fine. Gli utenti eseguono test di usabilità sul prodotto ogni volta che lo usano e eseguono il loro verdetto attraverso il loro uso continuo o la loro mancanza. Testare il prodotto prima di rilasciarlo sul mercato può contribuire a garantire che le esperienze degli utenti con il prodotto siano positive.

### <a name="what-does-it-cost"></a>Qual è il costo?

Gli sviluppatori di software e i project manager spesso si preoccupano che l'avvio di un processo di progettazione centrato su utenti e l'esecuzione di test di usabilità adeguati richiedano quantità inaccettabili di tempo e denaro. La realtà è che il costo in tempo e denaro speso per concentrarsi sull'utente è spesso relativamente ridotto, e certamente lo è rispetto al costo di non farlo.

Si consideri, ad esempio, il costo in tempo e denaro necessario per eseguire revisioni di progettazione in ritardo nel ciclo di sviluppo anziché in precedenza, quando il prodotto è ancora in tavola. L'attesa del periodo beta per esporre gli utenti al prodotto ai fini dei test di usabilità può comportare lo smontaggio di parti del programma che hanno richiesto molto tempo per lo sviluppo. E attendere che il prodotto sia effettivamente rilasciato e quindi apportare modifiche basate su feedback negativi o sul supporto di una progettazione scadente potrebbe rendere il costo notevolmente superiore a causa di costi elevati per il supporto del prodotto o di scarsa ricezione da parte degli utenti.

Uno studio di usabilità ragionevole può in genere essere eseguito in circa due settimane o meno e può ridurre notevolmente il tempo e il costo delle modifiche in ritardo nel ciclo di sviluppo. Il costo dell'esecuzione dei test varia a seconda della natura del prodotto e delle parti dell'interfaccia testate.

I test di usabilità sono simili ai test del codice. I project manager hanno esito positivo per il test del codice durante la pianificazione di un progetto di sviluppo. Non lo vedono come qualcosa in più che deve essere intasato nella pianificazione del progetto e nel budget. I project manager accettano invece il test del codice come costo dell'attività aziendale perché l'alternativa è molto più costosa. Lo stesso vale per i test di usabilità.

### <a name="how-do-i-increase-usability"></a>Come si aumenta l'usabilità?

Quando si legge e si comprende l'importanza dell'usabilità, gli sviluppatori di software talvolta sono tentati di aggiungere l'usabilità, come se fosse un ingrediente che può essere semplicemente aggiunto a un prodotto per renderlo più utilizzabile. Al contrario, l'usabilità deve far parte del processo di progettazione stesso, anziché una "cosa" che viene aggiunta al processo qui o in quel punto. Il motivo per cui gli esperti di usabilità si riferiscono a "attenzione dell'utente" e "progettazione incentrata sull'utente" è che l'usabilità dipende dal mantenimento delle esigenze degli utenti centrali per il processo di progettazione. La progettazione centrata sull'utente per necessità non implica solo la semplice esecuzione di un set di regole che regolano il posizionamento di pulsanti e menu in un'interfaccia. I test di usabilità sono un'opportunità per controllare il lavoro di progettazione. Non è un modo per "aggiungere" l'usabilità a un prodotto.

Gould, Boies e Lewis (1991) identificano quattro importanti set di progettazione centrati su utenti:

-   Concentrarsi in anticipo sugli utenti.

    Gli sviluppatori devono concentrarsi sulla comprensione delle esigenze degli utenti nelle prime fasi del processo di progettazione.

-   Progettazione integrata.

    Tutti gli aspetti della progettazione devono evolversi in parallelo, anziché in sequenza. Mantenere la progettazione interna del prodotto coerente con le esigenze dell'interfaccia utente.

-   Test anticipati e continui.

    L'unico approccio attualmente fattibile alla progettazione software è empirico: la progettazione funziona se gli utenti reali ne decidono il funzionamento. L'incorporamento dei test di usabilità durante il processo di sviluppo offre agli utenti la possibilità di fornire feedback sulla progettazione prima del rilascio del prodotto.

-   Progettazione iterativa.

    I problemi di grandi dimensioni spesso mascherano i problemi di piccole dimensioni. I progettisti e gli sviluppatori devono rivedere la progettazione in modo iterativo tramite round di test.

### <a name="why-should-i-involve-users"></a>Perché è consigliabile coinvolgere gli utenti?

Gli sviluppatori devono riconoscere che non sono utenti tipici. Hanno una conoscenza e una comprensione più approfondita del sistema che stanno sviluppando rispetto all'utente medio. Gli aspetti dell'interfaccia poco chiari o confusi per la maggior parte degli utenti potrebbero quindi essere perfettamente chiari per qualcuno che ha lavorato al progetto. Alcuni sviluppatori di software sono in grado di empatizzare con l'utente medio fino a un certo punto, ma non esiste alcun sostituto per le interazioni reali degli utenti effettivi con il prodotto.

Di conseguenza, concentrandosi sulle esigenze degli utenti tipiche in anticipo e rivedendo la progettazione basata spesso sui test degli utenti, gli sviluppatori software incentrati sugli utenti producono progettazioni migliori e, di conseguenza, prodotti migliori.

Con una progettazione migliore viene fornita una migliore accettazione da parte degli utenti. Il vantaggio del software per la vendita al dettaglio è ovvio: aumento delle vendite. L'accettazione è importante anche con il software sviluppato per l'uso interno: una maggiore attenzione alla progettazione incentrata sull'utente comporta una maggiore produttività e una minore necessità di supporto. Coinvolgere visibilmente gli utenti fin dall'inizio dello sviluppo dimostra anche un interesse per le proprie esigenze e preoccupazioni, il che aumenta la disponibilità a contribuire allo sviluppo.

### <a name="cant-i-just-follow-guidelines"></a>Non è possibile seguire semplicemente le linee guida?

Microsoft ha sviluppato un set di linee guida di interfaccia per la piattaforma Windows computing per garantire che i programmi Windows hanno un aspetto coerente. Altre aziende hanno sviluppato linee guida simili per altre piattaforme informatiche ed esperti di usabilità come Jakob Nielsen hanno scritto ampiamente sulla progettazione di pagine Web utilizzabili. Con la grande quantità di informazioni disponibili su questi argomenti, i progettisti a volte ritengono che la rigorosa aderenza alle linee guida e agli standard sia tutto ciò che è necessario per produrre prodotti utilizzabili.

Il problema di questo approccio è che le linee guida sono intrinsecamente generali. Le linee guida devono essere applicabili a un'ampia gamma di casi e pertanto non sempre prescrivere il miglior corso di azione per la particolare applicazione in fase di sviluppo. L'aderenza a un set ben scritto di linee guida può essere utile nella progettazione di un'interfaccia coerente, ma non può garantire la sua usablility a meno che non venga testata con utenti reali. Quando si usano le linee guida, non usarle come un libro di riferimento in cui le linee guida puntano verso il meglio di tutti i risultati. Due sviluppatori possono implementare la stessa linea guida in due modi diversi ed entrambe le implementazioni potrebbero non essere ugualmente appropriate per la situazione. In alcuni casi, una rigorosa aderenza alle linee guida può portare a risultati scarsi o a conflitti tra le linee guida. Solo la progettazione basata su utenti può contribuire a risolvere questi problemi prima che diventino problemi.

Un altro modo di pensare a questo è: consentire alla progettazione centrata sull'utente di essere l'arbitraggio delle decisioni di progettazione, non delle linee guida dell'interfaccia utente.

### <a name="do-i-need-to-build-a-usability-lab"></a>È necessario creare un lab di usabilità?

Non presupporre che il test di usabilità significhi eseguire il commit in un costoso lab, con fotocamere montate su un controsoffitto, mirror unidirevi e altri strumenti di gruppo di messa a fuoco. Per essere certi che le aziende che esercitino molti test spesso trovino comodo creare lab dedicati e i consulenti per l'usabilità hanno spesso un'ampia gamma di strutture e apparecchiature per offrire ai propri clienti. È tuttavia possibile eseguire test di usabilità validi e utili in un'ampia gamma di impostazioni e circostanze.

Un approccio consiste nell'avere semplicemente un tester?qualcuno esperto nell'esecuzione di studi sui partecipanti umani e nella raccolta di dati?siede dietro un utente mentre lavora e osserva l'utente che esegue le attività. Questa operazione può essere eseguita facilmente in una sala riunioni o in un ufficio. Per altre informazioni sui test tramite osservazione, vedere la voce Dumas e Redish in [Altre risorse](other-resources.md).

Quando i test di usabilità si sviluppano e diventano più coinvolti, è possibile aggiungere apparecchiature come una videocamera, un mirror unidiredireale o strumenti che consentono di visualizzare e registrare il monitoraggio di un utente in tempo reale.

In alternativa, i test possono essere affidati a consulenti per l'usabilità. La sezione seguente contiene suggerimenti per trovare i consulenti più esperti.

### <a name="how-do-i-get-started"></a>Come si Informazioni di base?

Dopo aver deciso di incorporare i principi di progettazione centrati sull'utente nel processo di sviluppo, è necessario decidere se assumere professionisti dell'usabilità o esternalizzare i test di usabilità a un fornitore.

Usability Professionals Association (UPA) include una guida ai fornitori che consente di trovare consulenti per l'usabilità.

Alcuni gruppi di consulenza possono anche aiutare a configurare lab di usabilità o sviluppare un programma di usabilità interno per incorporare i principi di usabilità nel processo di progettazione.

Se si assumono professionisti dell'usabilità, Human Factors and Ergonomics Society ha un servizio di posizionamento che può aiutare a trovare potenziali dipendenti. Molti professionisti dell'usabilità appartengono anche a ACM Special Interest Group on Computer-Human Interaction (SIGCHI) e UPA. Inserire annunci di impiego nelle pubblicazioni o nelle conferenze.

Indipendentemente dalla route, tenere presente che si tratta di servizi di test. Il principio secondo cui i progettisti non sono utenti tipici è vero anche per i professionisti dell'usabilità.

Per altre informazioni su queste aziende e organizzazioni e per altre informazioni sui test di usabilità e sulla progettazione centrata [sull'utente,](other-resources.md)vedere Altre risorse .

 

 




