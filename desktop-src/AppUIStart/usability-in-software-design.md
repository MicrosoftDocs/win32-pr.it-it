---
title: Usabilità nella progettazione del software
description: In questo argomento viene introdotto il concetto di usabilità e il motivo per cui deve essere una parte importante di qualsiasi progetto di progettazione software.
ms.assetid: 912b3224-e36d-44d6-98fa-a7f28e68a2d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b302e63a475d060748e896440b28915816d910e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044260"
---
# <a name="usability-in-software-design"></a>Usabilità nella progettazione del software

In questo argomento viene introdotto il concetto di usabilità e il motivo per cui deve essere una parte importante di qualsiasi progetto di progettazione software.

-   [Introduzione](#introduction)
-   [Definizione dell'usabilità](#defining-usability)
    -   [Semplicità d'uso](#ease-of-use)
    -   [Usabilità e utilità](#usability-vs-utility)
    -   [Gradimento rispetto al suo utilizzo](#liking-it-vs-using-it)
    -   [Confronto tra individuazione e apprendimento e efficienza](#discovery-vs-learning-vs-efficiency)
    -   [Gli sloganti non funzionano](#slogans-do-not-work)
-   [Perché l'usabilità è importante?](#why-is-usability-important)
    -   [Perché è necessario prestare attenzione?](#why-should-you-care)
    -   [Qual è il costo?](#what-does-it-cost)
    -   [Come è possibile aumentare l'usabilità?](#how-do-i-increase-usability)
    -   [Perché è necessario coinvolgere gli utenti?](#why-should-i-involve-users)
    -   [Non è possibile seguire solo le linee guida?](#cant-i-just-follow-guidelines)
    -   [È necessario creare un Lab di usabilità?](#do-i-need-to-build-a-usability-lab)
    -   [Come iniziare?](#how-do-i-get-started)

## <a name="introduction"></a>Introduzione

Il termine "usabilità" nel contesto della creazione di software rappresenta un approccio che inserisce l'utente, invece del sistema, al centro del processo. Questa filosofia, nota come progettazione incentrata sull'utente, incorpora le preoccupazioni degli utenti e il patrocinio fin dall'inizio del processo di progettazione e impone che le esigenze dell'utente siano quelle più importanti di tutte le decisioni di progettazione.

L'aspetto più visibile di questo approccio è il test di usabilità, in cui gli utenti lavorano e interagiscono con l'interfaccia del prodotto e condividono le proprie opinioni e le proprie preoccupazioni con i progettisti e gli sviluppatori.

## <a name="defining-usability"></a>Definizione dell'usabilità

La sezione definisce il significato dell'usabilità nel contesto dello sviluppo del software e il modo in cui si riferisce ad altri aspetti del processo di sviluppo.

### <a name="ease-of-use"></a>Semplicità d'uso

L'usabilità è una misura della semplicità con cui è possibile utilizzare un prodotto per eseguire le attività prescritte. Si tratta di un'operazione distinta rispetto ai concetti correlati di utilità e affinità.

### <a name="usability-vs-utility"></a>Usabilità e utilità

Un attributo centrale che determina la qualità di un prodotto è utile. Questo consente di determinare se gli utilizzi effettivi di un prodotto possono raggiungere gli obiettivi che i progettisti desiderano ottenere. Il concetto di utilità si ramifica ulteriormente nell'utilità e nell'usabilità. Sebbene questi termini siano correlati, non sono intercambiabili.

L'utilità si riferisce alla capacità del prodotto di eseguire un'attività o un'attività. Maggiore è il numero di attività che il prodotto è progettato per eseguire, maggiore è l'utilità.

Prendere in considerazione i tipici processori Microsoft MS-DOS a partire dal tardo 1980. Tali programmi forniscono molte potenti funzionalità di modifica e manipolazione del testo, ma gli utenti devono apprendere e ricordare decine di sequenze di tasti Arcane per eseguirle. Per le applicazioni come queste si può affermare che l'utilità è elevata (forniscono agli utenti la funzionalità necessaria) ma con una bassa usabilità (gli utenti devono dedicare molto tempo e lavoro per apprendere e usare). Al contrario, un'applicazione semplice e ben progettata, ad esempio una calcolatrice, può essere molto facile da utilizzare, ma non offre molta utilità.

Entrambe le qualità sono necessarie per l'accettazione del mercato ed entrambe fanno parte del concetto generale di utilità. Ovviamente, se un programma è altamente utilizzabile ma non esegue alcuna operazione di valore, nessuno lo utilizzerà. E gli utenti che presentano un potente programma che è difficile da usare probabilmente resisteranno o cercheranno alternative.

Il test di usabilità consente di determinare la semplicità con cui gli utenti possono eseguire determinate attività. Tuttavia, non consente di determinare direttamente se il prodotto stesso ha valore o utilità. (Gli utenti possono fare volontariamente commenti relativi all'utilità durante i test di usabilità, ma i commenti devono essere verificati con altri metodi di ricerca più affidabili).

### <a name="liking-it-vs-using-it"></a>Gradimento rispetto al suo utilizzo

La somiglianza è sempre un tratto auspicabile in un prodotto. Se persone come il prodotto, è più probabile utilizzarlo e consigliarlo ad altri utenti. Tuttavia, come per l'utilità, è necessario prestare attenzione a non confondere la somiglianza con l'usabilità.

Spesso, come un prodotto, per i motivi non correlati all'utilità e all'usabilità. Possono essere attratti dallo stile o dallo stato in cui ritengono che il prodotto conferisca loro. Si tratta in genere di prodotti altamente utilizzabili, ma è preferibile non presupporre che un prodotto ben apprezzato sia utilizzabile.

L'usabilità indica se un utente può utilizzare il prodotto per eseguire le attività che devono eseguire. Il test di usabilità misura principalmente le prestazioni, non le preferenze. Tuttavia, i questionari standardizzati possono essere usati per misurare le preferenze tra i prodotti.

### <a name="discovery-vs-learning-vs-efficiency"></a>Confronto tra individuazione e apprendimento e efficienza

Esistono molti aspetti dell'usabilità, ma tradizionalmente il termine si riferisce in modo specifico agli attributi di individuazione, apprendimento ed efficienza.

-   L'individuazione implica la ricerca e la ricerca della funzionalità di un prodotto in risposta a una particolare esigenza. I test di usabilità possono determinare il tempo impiegato da un utente per trovare una funzionalità e il numero di errori (scelte errate relative al percorso) che l'utente esegue lungo il percorso.
-   L'apprendimento si riferisce al processo in base al quale l'utente comprende come utilizzare una funzionalità individuata per completare un'attività. I test di usabilità possono determinare il tempo impiegato da questo processo e anche il numero di errori che l'utente effettua durante l'apprendimento della funzionalità.
-   L'efficienza indica il punto in cui l'utente ha "padroneggiato" la funzionalità e la utilizza senza richiedere ulteriore apprendimento. I test di usabilità possono determinare il tempo impiegato dall'utente esperto per eseguire i passaggi necessari per l'uso della funzionalità.

Questi tre aspetti di base dell'usabilità sono fortemente influenzati dalla natura dell'attività e dalla frequenza con cui l'utente lo esegue. Alcune funzionalità vengono usate raramente o sono così complesse che l'utente li riapprende ogni volta; per queste funzionalità, Microsoft sviluppa spesso procedure guidate per guidare l'utente durante il processo.

### <a name="slogans-do-not-work"></a>Gli sloganti non funzionano

Gli sviluppatori di software a volte pensano che semplici sloganti come "rendere più usabile il prodotto" contribuiscano a risolvere i problemi di usabilità. Anche se un atteggiamento positivo verso l'usabilità è importante, solo i test di usabilità appropriati con utenti normali, nel contesto del prodotto specifico creato, possono fornire agli sviluppatori le informazioni necessarie per creare un prodotto che soddisfi le esigenze degli utenti. "Rendere il prodotto più utilizzabile" deve essere lo slogante di ogni sviluppatore di software, ma ha senso solo se lo sviluppatore conosce il significato dell'usabilità. Il test con utenti normali è il modo più affidabile per scoprirlo.

## <a name="why-is-usability-important"></a>Perché l'usabilità è importante?

La sezione risponde ad alcune domande comuni sul motivo per cui l'usabilità è importante e su come incorporare i principi di progettazione centrati sull'utente nel processo di sviluppo.

### <a name="why-should-you-care"></a>Perché è necessario prestare attenzione?

Se le considerazioni sull'usabilità non sono già state incorporate nel processo di progettazione del prodotto, è possibile chiedersi perché sia necessario o auspicabile. Dopo tutto, è certamente possibile rilasciare un prodotto funzionante, privo di bug senza eseguire alcuna operazione di usabilità. Tuttavia, l'integrazione di principi di progettazione centrati sugli utenti può causare un prodotto molto migliorato in diverse aree.

Il motivo migliore per eseguire i test di usabilità consiste nel ridurre il numero di chiamate di supporto da parte degli utenti. Una cattiva usabilità è il motivo principale per cui gli utenti chiamano le linee di supporto tecnico software e ogni responsabile aziendale e Information Services Manager sa quanto può essere il supporto del prodotto costoso. Inoltre, l'addebito degli utenti per il supporto aumenta la potenziale insoddisfazione del prodotto. Se gli utenti trovano un prodotto facile da usare, non dovranno chiamare il supporto tecnico come spesso.

Per il software prodotto per uso interno, il prossimo motivo migliore per rendere l'usabilità una parte importante del processo di sviluppo consiste nel ridurre i costi di training. Un prodotto altamente utilizzabile è molto più semplice per gli utenti che ne apprendano una per cui l'usabilità non è una priorità elevata. Gli utenti apprenderanno più rapidamente le funzionalità e manterranno più a lungo le proprie conoscenze, correlate direttamente a costi e tempi di formazione ridotti.

Il test di usabilità aiuta a migliorare l'accettazione dell'utente. Risultati dell'accettazione da diversi fattori, tra cui usabilità, utilità e somiglianza. Per i prodotti per la vendita al dettaglio, l'accettazione da parte degli utenti spesso è direttamente correlata all'acquisto ripetuto o alla fedeltà, il che significa che l'utente può consigliare il prodotto ad altri utenti. Per le applicazioni interne, l'accettazione dell'utente è correlata alla volontà di utilizzare il software per eseguire le attività per le quali è stato progettato, consentendo di aumentare la produttività. L'aumento dell'usabilità è uno dei fattori che possono contribuire a una maggiore accettazione dell'utente.

L'usabilità può contribuire a distinguere i prodotti da quelli dei concorrenti. Se due prodotti sono sostanzialmente uguali in utilità, il prodotto con una migliore usabilità sarà probabilmente considerato superiore. Inoltre, le linee guida per la programmazione e l'aspetto di Windows hanno livellato il campo di gioco per l'interfaccia utente di base, in modo che molti programmi che svolgono funzioni simili abbiano un aspetto analogo. Queste analogie significano che le piccole differenze nell'usabilità possono avere un effetto significativo sulle preferenze dell'utente.

Infine, ogni prodotto viene testato per la loro usabilità alla fine. Gli utenti eseguono test di usabilità sul prodotto ogni volta che lo usano e rendono il loro verdetto attraverso l'uso continuato o la loro mancanza. Testare il prodotto prima di rilasciarlo sul mercato può contribuire a garantire che le esperienze degli utenti con il prodotto siano positive.

### <a name="what-does-it-cost"></a>Qual è il costo?

Gli sviluppatori di software e i Project Manager temono spesso che l'avvio di un processo di progettazione centrato dall'utente e l'esecuzione di test di usabilità appropriati richiedano quantità inaccettabili di tempo e denaro. La realtà è che il costo nel tempo e il denaro impiegato per concentrarsi sull'utente sono spesso relativamente ridotti e, di conseguenza, rispetto al costo di non farlo.

Si consideri, ad esempio, il costo nel tempo e il denaro necessario per apportare le revisioni di progettazione in ritardo nel ciclo di sviluppo rispetto a quello precedente, quando il prodotto si trova ancora nella lavagna. L'attesa fino al periodo beta per esporre gli utenti al prodotto per scopi di test di usabilità può comportare lo smantellamento di parti del programma che hanno richiesto molto tempo per lo sviluppo. E in attesa fino a quando il prodotto non viene rilasciata e quindi apportando modifiche in base a commenti negativi o al supporto di un progetto di scarsa qualità potrebbe rendere il costo incommensurabilmente più elevato a causa di costi elevati di supporto del prodotto o di una ricezione scadente

Uno studio di usabilità ragionevole può essere in genere eseguito in circa due settimane o meno e può ridurre notevolmente il tempo e il costo di apportare modifiche in ritardo nel ciclo di sviluppo. Il costo dell'esecuzione dei test varia a seconda della natura del prodotto e delle parti dell'interfaccia sottoposte a test.

Il test di usabilità può essere considerato analogo al test del codice. Account Project Manager riusciti per il test del codice durante la pianificazione di un progetto di sviluppo. Non vengono visualizzati come elementi aggiuntivi che devono essere apportati alla pianificazione del progetto e al budget. I Project Manager accettano i test di codice come costo per l'attività aziendale perché l'alternativa è molto più costosa. Lo stesso vale per i test di usabilità.

### <a name="how-do-i-increase-usability"></a>Come è possibile aumentare l'usabilità?

Durante la lettura e la comprensione dell'importanza dell'usabilità, gli sviluppatori di software sono talvolta tentati di aggiungere usabilità, come se si trattasse di un ingrediente che può essere semplicemente aggiunto a un prodotto per renderlo più utilizzabile. L'usabilità, invece, deve far parte del processo di progettazione, anziché di una "cosa" aggiunta al processo qui o. Il motivo per cui gli esperti di usabilità fanno riferimento a "Focus utente" e "progettazione centrata sull'utente" è che l'usabilità dipende dal modo in cui le esigenze degli utenti sono fondamentali per il processo di progettazione. La progettazione incentrata sull'utente per necessità comporta più di quanto segue un set di regole che controllano la posizione di pulsanti e menu in un'interfaccia. Il test di usabilità è un'opportunità per verificare il lavoro di progettazione. Non è possibile aggiungere l'usabilità a un prodotto.

Gould, Boies e Lewis (1991) identificano quattro principi importanti della progettazione centrata sull'utente:

-   Primo interesse per gli utenti.

    Gli sviluppatori devono concentrarsi sulla comprensione delle esigenze degli utenti nelle fasi iniziali del processo di progettazione.

-   Progettazione integrata.

    Tutti gli aspetti della progettazione dovrebbero evolversi in parallelo, anziché in sequenza. Mantiene la struttura interna del prodotto coerente con le esigenze dell'interfaccia utente.

-   Test tempestivi e continui.

    L'unico approccio attualmente praticabile alla progettazione del software è uno empirico: il progetto funziona se gli utenti reali decidono che funziona. L'incorporamento dei test di usabilità durante il processo di sviluppo offre agli utenti la possibilità di fornire commenti e suggerimenti sulla progettazione prima del rilascio del prodotto.

-   Progettazione iterativa.

    I problemi principali spesso mascherano piccoli problemi. I progettisti e gli sviluppatori devono modificare il progetto in modo iterativo tramite cicli di test.

### <a name="why-should-i-involve-users"></a>Perché è necessario coinvolgere gli utenti?

Gli sviluppatori dovrebbero riconoscere che non sono utenti tipici. Hanno una conoscenza più approfondita e una migliore comprensione del sistema che stanno sviluppando rispetto alla media dell'utente. Gli aspetti dell'interfaccia che risultano poco chiari o confusi per la maggior parte degli utenti possono quindi essere perfettamente chiari per qualcuno che ha lavorato al progetto. Alcuni sviluppatori di software sono in grado di entrare in empatia con l'utente medio a un certo livello, ma non vi è alcun sostituto per le interazioni reali degli utenti effettivi con il prodotto.

Di conseguenza, concentrandosi sulle esigenze tipiche degli utenti in modo tempestivo e rivedendo la progettazione in base ai test degli utenti, gli sviluppatori di software incentrati sugli utenti producono soluzioni migliori e, di conseguenza, migliori prodotti.

Con una progettazione migliore, l'accettazione degli utenti è migliore. Il vantaggio del software per la vendita al dettaglio è evidente: aumento delle vendite. L'accettazione è importante anche per quanto riguarda il software sviluppato per l'uso interno: il miglioramento della progettazione centrata sugli utenti comporta un aumento della produttività e una riduzione della necessità di supporto. Il coinvolgimento evidente degli utenti dall'inizio dello sviluppo Mostra anche un interesse per le proprie esigenze e le loro esigenze, che aumentano la loro volontà di aiutare nel lavoro di sviluppo.

### <a name="cant-i-just-follow-guidelines"></a>Non è possibile seguire solo le linee guida?

Microsoft ha sviluppato un set di linee guida per l'interfaccia per la piattaforma Windows computing per garantire che i programmi Windows abbiano un aspetto coerente. Altre aziende hanno sviluppato linee guida simili per altre piattaforme di elaborazione e gli esperti di usabilità come Jakob Nielsen hanno scritto ampiamente sulla progettazione di pagine Web utilizzabili. Con la grande quantità di informazioni disponibili in questi argomenti, i progettisti a volte ritengono che la rigorosa aderenza a linee guida e standard sia sufficiente per produrre prodotti utilizzabili.

Il problema di questo approccio è che le linee guida sono intrinsecamente generali. Le linee guida devono essere valide per un'ampia gamma di casi e pertanto non sempre prevedono la migliore linea di azione per la particolare applicazione in fase di sviluppo. L'adesione a un set di linee guida ben scritto può risultare utile nella progettazione di un'interfaccia coerente, ma non può garantire la usablility, a meno che non venga testato con utenti reali. Quando si usano le linee guida, non usarle come un Cookbook, in cui le linee guida indicano il modo migliore di tutti i risultati. Due sviluppatori possono implementare le stesse linee guida in due modi diversi ed entrambe le implementazioni potrebbero non essere ugualmente appropriate per la situazione. Occasionalmente, una rigorosa aderenza alle linee guida può causare scarsi risultati o conflitti tra le linee guida. Solo la progettazione centrata sull'utente può contribuire a scaricare questi problemi prima che diventino problemi.

Un altro modo per considerare questo problema è: lasciare che la progettazione incentrata sull'utente sia l'arbitro delle decisioni di progettazione, non le linee guida dell'interfaccia utente.

### <a name="do-i-need-to-build-a-usability-lab"></a>È necessario creare un Lab di usabilità?

Non presupporre che i test di usabilità significhino eseguire il commit in un Lab costoso, con fotocamere montate a soffitto, Mirror unidirezionali e altre intercettazioni di gruppi di interesse. Per essere certi, le aziende che eseguono molti test spesso risultano utili per creare laboratori dedicati e i consulenti di usabilità spesso hanno un'ampia gamma di strutture e attrezzature per offrire i loro clienti. Tuttavia, un test di usabilità valido può essere eseguito in un'ampia gamma di impostazioni e circostanze.

Un approccio consiste nel disporre semplicemente di un tester? un utente che ha effettuato ricerche e la raccolta di dati da parte di un utente, si trova dietro un utente mentre lavora e osserva le attività eseguite dall'utente. Questa operazione può essere eseguita facilmente in una sala riunioni o in un ufficio. Per altre informazioni sui test per osservazione, vedere la voce relativa a Dumas e redish in [altre risorse](other-resources.md).

Poiché i test di usabilità si sviluppano e diventano più necessari, è possibile aggiungere apparecchiature quali una videocamera, un mirror unidirezionale o strumenti che consentono di visualizzare e registrare il monitoraggio di un utente in tempo reale.

In alternativa, è possibile esternalizzare i test ai consulenti di usabilità. La sezione seguente contiene suggerimenti su come trovare i consulenti appropriati.

### <a name="how-do-i-get-started"></a>Come iniziare?

Una volta deciso di incorporare i principi di progettazione centrati sull'utente nel processo di sviluppo, sarà necessario decidere se assumere i professionisti dell'usabilità o esternalizzare i test di usabilità a un fornitore.

L'associazione di usabilità Professionals (UPA) offre una guida per i fornitori che può aiutare a trovare i consulenti di usabilità.

Alcuni gruppi di consulenza possono anche configurare i laboratori di usabilità o sviluppare un programma di usabilità interna per incorporare i principi di usabilità nel processo di progettazione.

Se assumono i professionisti dell'usabilità, i fattori umani e la società ergonomica hanno un servizio di posizionamento che può aiutare a trovare i potenziali dipendenti. Molti professionisti dell'usabilità appartengono anche al gruppo di interesse speciale ACM per l'interazione Computer-Human (SIGCHI) e UPA. Inserire annunci per l'occupazione nelle pubblicazioni o nelle conferenze.

Indipendentemente dalla Route, tenere presente che si tratta di servizi di test. Il principio che i progettisti non sono utenti tipici è anche vero per i professionisti dell'usabilità.

Per ulteriori informazioni su queste società e organizzazioni e per altre informazioni sui test di usabilità e sulla progettazione centrata sull'utente, vedere [altre risorse](other-resources.md).

 

 




