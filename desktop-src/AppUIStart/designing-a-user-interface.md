---
title: Progettazione di un'interfaccia utente
description: In questa sezione vengono descritte in dettaglio alcune delle attività associate alla progettazione di un'interfaccia utente per un'applicazione Windows.
ms.assetid: 22deda0c-bf03-4fcd-9cc9-6381b601c152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97d5027baf7276b1353e03254478545e554daa5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473731"
---
# <a name="designing-a-user-interface"></a>Progettazione di un'interfaccia utente

In questa sezione vengono descritte in dettaglio alcune delle attività associate alla progettazione di un'interfaccia utente per un'applicazione Windows.

-   [Introduzione](#introduction)
-   [Requisiti funzionali](#functional-requirements)
-   [Analisi utente](#user-analysis)
    -   [Istruzioni problem](#problem-statements)
    -   [Priorità](#priorities)
-   [Progettazione concettuale](#conceptual-design)
-   [Progettazione logica](#logical-design)
-   [Progettazione fisica](#physical-design)

## <a name="introduction"></a>Introduzione

La progettazione dell'interfaccia utente può essere divisa in tre elementi essenziali: funzionalità, estetica e prestazioni.

Spesso, l'obiettivo principale durante lo sviluppo di applicazioni è la funzionalità. L'applicazione è utilizzabile? Consente agli utenti di completare le attività? Tuttavia, la funzionalità è solo una parte della storia.

Le estetiche descrivono come vengono visualizzati e presentati gli elementi, lo stile in cui gli elementi vengono comunicati all'utente. Le estetiche sono molto soggettive e molto più difficili da quantificare rispetto ai requisiti funzionali e alle metriche delle prestazioni. In genere, le estetiche si riferiscono a scelte semplici, come i colori sono complementari o il modo in cui gli elementi dell'interfaccia utente comportano il loro significato, che spesso influiscono sul modo in cui una persona prova a usare qualcosa e influisce sull'esito positivo

Le prestazioni vengono misurate solo in base alla velocità, ma anche all'affidabilità. Se un'applicazione ha un aspetto ottimale, è facile da utilizzare, ma si interrompe ripetutamente, probabilmente non avrà successo. L'applicazione deve fornire agli utenti una piena fiducia nell'affidabilità.

Di seguito sono riportate alcune attività della fase di progettazione che possono contribuire a una corretta interfaccia utente per un'applicazione Windows.

## <a name="functional-requirements"></a>Requisiti funzionali

Prendere in considerazione i suggerimenti seguenti all'inizio della fase di progettazione per ottimizzare l'esperienza utente nei più ampi destinatari possibili:

-   Seguire le linee guida di progettazione dell'interfaccia utente.

    Acquisire familiarità con le linee guida per l'interazione con l' [esperienza utente di Windows](../uxguide/guidelines.md) e farvi riferimento spesso come la progettazione, l'implementazione e il test dei progressi dell'interfaccia utente dell'applicazione.

-   Verificare che l'interfaccia utente sia accessibile.

    Assicurarsi di integrare l'accessibilità nella progettazione dell'interfaccia utente a partire dall'inizio del ciclo di vita del prodotto. Il retrofit dell'accessibilità può essere estremamente costoso perché parte dello sviluppo dell'accessibilità richiede attenzione a livello di architettura. Per ulteriori informazioni, scaricare il [software tecnico per l'eBook di accessibilità](https://www.microsoft.com/download/details.aspx?id=19262).

-   Supporto del Marketplace internazionale.

    Windows include tecnologie che consentono il supporto per molte impostazioni cultura e linguaggi scritti in un'applicazione Windows. Se l'applicazione è destinata al Marketplace internazionale, è importante includere il supporto per l'internazionalizzazione nella progettazione dell'interfaccia utente dall'inizio del progetto. Per ulteriori informazioni, vedere [internazionalizzazione per le applicazioni Windows](../intl/international-support.md).

## <a name="user-analysis"></a>Analisi utente

Un passaggio cruciale per la progettazione di un'interfaccia corretta è il raggiungimento di una conoscenza di base degli utenti necessari e desiderati da un'applicazione prima di scrivere codice. Tenere presente che i potenziali utenti di un'applicazione stanno già eseguendo il proprio lavoro in qualche modo e gli strumenti e i processi esistenti devono essere interpretati nel modo più completo possibile. Non progettare senza considerare completamente questi problemi.

L'approccio più semplice e informale consiste nel comunicare con gli utenti desiderati del prodotto. Ottenere informazioni direttamente dall'origine: evitare di usare Manager o dirigenti come proxy per i consumatori effettivi. Si consiglia di fare in modo che piccoli gruppi di sviluppatori e responsabili del programma paghino visite informali agli utenti nelle loro area di lavoro, in cui è possibile discutere il modo in cui funzionano e raccogliere i dettagli dei problemi che affrontano con gli strumenti attuali.

Tenere presente che non è necessario porre domande iniziali o parziali perché questo influirà direttamente sulla qualità e sulla validità dei commenti degli utenti. Quando si compongono le domande durante questa fase, tenere presente quanto segue:

-   Chi sono gli utenti? Quali competenze e conoscenze sono disponibili?
-   Quali origini dati possono essere usate per comprendere la loro esperienza?
-   Quali obiettivi e attività utilizzeranno il prodotto per il completamento?
-   Quali sono i presupposti e come è possibile verificarli?
-   Quali origini dei dati sono disponibili? (Gli studi di usabilità e le valutazioni euristiche sono ottimi da iniziare).

### <a name="problem-statements"></a>Istruzioni problem

Una volta raccolti tutti i commenti degli utenti, analizzarli e distillrli in problemi e requisiti correlati. A questo punto, provare a evitare di considerare le soluzioni. Assicurarsi che i problemi siano identificati completamente, non solo i sintomi.

Spesso è utile comporre un elenco di istruzioni di un problema di frase (dal punto di vista degli utenti) per ogni problema o requisito. Ad esempio, "Resize edit box width to 15 characters" non è un problema. Ma "è troppo difficile digitare i termini di ricerca lunghi" è un'istruzione di problema valida. La differenza è drammatica. Provare a non definire la soluzione e il problema nello stesso momento: spesso il problema reale viene perso. In questo esempio è possibile risolvere il problema dei termini di ricerca in molti altri modi, inclusa la modifica delle dimensioni della casella di modifica. Tenere sempre presenti le soluzioni alternative.

Di seguito sono riportati alcuni esempi aggiuntivi di istruzioni di problema:

-   È difficile spostarsi da una sezione del sito Web a un'altra.
-   Gli utenti devono attendere troppo tempo per il caricamento del software.
-   I messaggi di errore di sicurezza sono difficili da comprendere.
-   La pagina di registrazione contiene troppe domande e spesso gli utenti le abbandonano.
-   Il completamento della ricerca di un prodotto specifico nell'indice del sito è troppo complesso.

Se le istruzioni sul problema sono sufficientemente ampie, è probabile che siano disponibili molti metodi innovativi e creativi per risolverli.

### <a name="priorities"></a>Priorità

Il fatto di prendere un elenco di elementi e classificarli per priorità, definisce una versione. Senza chiare priorità, i team possono combattere e discutere sulle operazioni da eseguire e sulle operazioni da tagliare. Il lavoro necessario per impostare le priorità dovrebbe essere più semplice con la ricerca completata, ma è sempre una sfida.

Per impostare le priorità è necessario avere la possibilità di valutare almeno tre criteri: pianificazione, team e business. Potrebbe essere prevista una pianificazione predefinita per il progetto, che limita le dimensioni e la scalabilità delle operazioni che è possibile eseguire. Un problema che probabilmente richiede la riscrittura della metà della base del codice non deve essere eseguito durante un ciclo di rilascio ridotto.

Il trucco e la natura di un team definiscono i tipi di lavoro che è possibile eseguire. Quali sono gli altri impegni del team? Esiste una finestra di progettazione o un tecnico di usabilità del team? Quali sono le competenze della progettazione Web o dell'interfaccia utente? Gli ultimi e più importanti sono considerazioni aziendali. Quali sono gli obiettivi dei ricavi per questo progetto? Chi sono i concorrenti? Quali sono i vantaggi della risoluzione di determinati problemi? Quali partnership possono essere falsificate? Eventuali altre considerazioni dovrebbero essere identificate prima di definire la priorità dell'elenco.

Una volta classificate in ordine di priorità, l'elenco di istruzioni per il problema imposta la direzione del prodotto e garantisce che lo sviluppo sia destinato alle aree giuste.

## <a name="conceptual-design"></a>Progettazione concettuale

In genere, l'interfaccia utente non viene risolta nella fase di progettazione concettuale. Tuttavia, questa fase richiede un modello di business completo con profili utente e scenari di utilizzo completi che sono imperativi per un'esperienza utente corretta.

## <a name="logical-design"></a>Progettazione logica

La fase di progettazione logica si verifica quando vengono sviluppati i prototipi iniziali che supportano la progettazione concettuale.

In questa fase vengono anche identificate le tecnologie hardware e software specifiche da usare durante lo sviluppo, che possono determinare le funzionalità dell'interfaccia utente nel prodotto finale. Per ulteriori informazioni, vedere [tecnologie dell'interfaccia utente](user-interface-technologies-for-windows-applications.md).

Oltre agli strumenti di sviluppo, è necessario identificare i vari requisiti hardware e i fattori di forma che devono essere considerati come destinazione dell'applicazione.

## <a name="physical-design"></a>Progettazione fisica

La fase di progettazione fisica determina il modo in cui deve essere implementata una progettazione dell'interfaccia utente per i fattori hardware e form specifici identificati nella progettazione logica.

Durante questa fase, le limitazioni dell'hardware o del fattore di forma potrebbero introdurre vincoli imprevisti sull'interfaccia utente che richiedono miglioramenti significativi per la progettazione.

 

 