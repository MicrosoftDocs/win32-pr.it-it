---
title: Progettazione di un Interfaccia utente
description: Questa sezione descrive in dettaglio alcune delle attività associate alla progettazione di un'interfaccia utente per un Windows applizione.
ms.assetid: 22deda0c-bf03-4fcd-9cc9-6381b601c152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914f8a2bf2afb532e3deed8876ce0ddea0fe71a0e8ad5457e5967e5f48eeb2c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440311"
---
# <a name="designing-a-user-interface"></a>Progettazione di un Interfaccia utente

Questa sezione descrive in dettaglio alcune delle attività associate alla progettazione di un'interfaccia utente per un Windows applizione.

-   [Introduzione](#introduction)
-   [Requisiti funzionali](#functional-requirements)
-   [Analisi utente](#user-analysis)
    -   [Istruzioni di problema](#problem-statements)
    -   [Priorità](#priorities)
-   [Progettazione concettuale](#conceptual-design)
-   [Progettazione logica](#logical-design)
-   [Progettazione fisica](#physical-design)

## <a name="introduction"></a>Introduzione

La progettazione dell'interfaccia utente può essere suddivisa in tre elementi essenziali: funzionalità, aspetto estetico e prestazioni.

Più spesso, lo stato attivo principale durante lo sviluppo di applicazioni è la funzionalità. L'applicazione è utilizzabile? Consente agli utenti di completare le attività? Tuttavia, la funzionalità è solo una parte della storia.

L'aspetto estetico descrive il modo in cui le cose vengono visualizzate e presentate, lo stile in cui le cose vengono comunicate all'utente. L'aspetto estetico è molto soggettivo e molto più difficile da quantificare rispetto ai requisiti funzionali e alle metriche delle prestazioni. L'aspetto estetico è in genere una scelta semplice, ovvero il modo in cui i colori si integrano tra loro o il modo in cui gli elementi dell'interfaccia utente trasmettono il loro significato, che spesso influiscono sul modo in cui una persona prova qualcosa e influenzano il successo dell'uso.

Le prestazioni vengono misurate non solo in base alla velocità, ma anche all'affidabilità. Se un'applicazione ha un aspetto eccezionale, è facile da usare, ma si arresta ripetutamente in modo anomalo, probabilmente non sarà molto efficace. L'applicazione deve fornire all'utente la piena attendibilità della propria affidabilità.

Di seguito sono riportate alcune attività della fase di progettazione che possono contribuire a un'interfaccia utente corretta per un'Windows applicazione.

## <a name="functional-requirements"></a>Requisiti funzionali

Prendere in considerazione i suggerimenti seguenti all'inizio della fase di progettazione per ottimizzare l'esperienza utente tra i destinatari più ampi possibili:

-   Seguire le linee guida per la progettazione dell'interfaccia utente.

    Acquisire familiarità con le linee [guida](../uxguide/guidelines.md) Windows per l'interazione con l'esperienza utente e fare spesso riferimento a tali linee guida con l'avanzamento della progettazione, dell'implementazione e del test dell'interfaccia utente dell'applicazione.

-   Assicurarsi che l'interfaccia utente sia accessibile.

    Assicurarsi di integrare l'accessibilità nella progettazione dell'interfaccia utente dall'inizio del ciclo di vita del prodotto. L'adattamento dell'accessibilità può essere estremamente diss costose perché parte dello sviluppo dell'accessibilità richiede attenzione a livello di architettura. Per altre informazioni, scaricare [l'eBook Engineering Software for Accessibility](https://www.microsoft.com/download/details.aspx?id=19262).

-   Supportare il marketplace internazionale.

    Windows include tecnologie che consentono il supporto per molte impostazioni cultura e lingue scritte in un Windows applizione. Se l'applicazione è mirata al marketplace internazionale, è importante includere il supporto per l'internazionalizzazione nella progettazione dell'interfaccia utente dall'inizio del progetto. Per altre informazioni, vedere [Internazionalizzazione per Windows applicazioni](../intl/international-support.md).

## <a name="user-analysis"></a>Analisi utente

Un passaggio fondamentale per la progettazione di un'interfaccia efficace consiste nel ottenere una conoscenza di base di ciò che gli utenti hanno bisogno e vogliono da un'applicazione prima di scrivere codice. Tenere presente che i potenziali utenti di un'applicazione stanno già eseguendo il proprio lavoro in qualche modo e che gli strumenti e i processi esistenti devono essere compresi nel modo più completo possibile. Non progettare senza considerare completamente questi problemi.

L'approccio più semplice e informale consiste nel parlare con gli utenti del prodotto. Ottenere informazioni direttamente dall'origine: evitare di usare manager o dirigenti come proxy per i consumer effettivi. È consigliabile fare in modo che piccoli gruppi di sviluppatori e responsabili di programma visitino gli utenti nelle loro postazioni di lavoro, in cui è possibile discutere il loro funzionamento e raccogliere dettagli sui problemi che devono affrontare con gli strumenti attuali.

Tenere presente che non porre domande iniziali o parziali, in quanto ciò influirà direttamente sulla qualità e sulla validità dei commenti e suggerimenti degli utenti. Quando si compongono domande durante questa fase, tenere presente quanto segue:

-   Who sono gli utenti? Quali competenze e conoscenze hanno?
-   Quali diverse origini dati è possibile usare per comprenderne l'esperienza?
-   Quali obiettivi e attività useranno il prodotto per il completamento?
-   Quali presupposti vengono assunti e come è possibile verificarli?
-   Quali origini dati sono disponibili? Gli studi di usabilità e le valutazioni euristiche sono buoni punti di partenza.

### <a name="problem-statements"></a>Istruzioni di problema

Dopo aver raccolto tutti i commenti e suggerimenti degli utenti, analizzarli e distillarli in problemi e requisiti correlati. A questo punto, provare a evitare di pensare alle soluzioni. Assicurarsi che i problemi siano completamente identificati, non solo i sintomi.

Spesso è utile comporre un elenco di istruzioni relative a un problema di una frase (dal punto di vista degli utenti) per ogni problema o requisito. Ad esempio, "Ridimensionare la larghezza della casella di modifica a 15 caratteri" non è un problema. Ma "È troppo difficile digitare in termini di ricerca lunga" è un'istruzione di problema valida. La differenza è notevole. Provare a non definire contemporaneamente la soluzione e il problema: spesso il problema reale viene perso. In questo esempio possono essere disponibili molti altri modi per risolvere il problema dei termini di ricerca, inclusa la modifica delle dimensioni della casella di modifica. Tenere sempre presenti soluzioni alternative.

Di seguito sono riportati altri esempi di istruzioni di problema:

-   È difficile passare da una sezione del sito Web a un'altra.
-   Gli utenti devono attendere troppo a lungo il caricamento del software.
-   I messaggi di errore di sicurezza sono difficili da comprendere.
-   La pagina di registrazione presenta troppe domande e gli utenti spesso la abbandonano.
-   La ricerca di un prodotto specifico nell'indice del sito è troppo difficile da completare.

Se le affermazioni del problema sono sufficientemente ampie, è probabile che siano disponibili molti modi innovativi e creativi per risolverle.

### <a name="priorities"></a>Priorità

L'azione di prendere un elenco di elementi e classificarli in base alla priorità definisce una versione. Senza priorità chiare, i team possono affrontare e discutere su quali operazioni devono essere eseguite e quali operazioni devono essere tagliate. Il lavoro necessario per definire le priorità dovrebbe essere più semplice con il completamento della ricerca, ma è sempre una sfida.

L'impostazione delle priorità richiede la possibilità di valutare almeno tre criteri: pianificazione, team e business. Potrebbe essere presente un set di pianificazione predefinito per il progetto, che limita le dimensioni e la scalabilità del lavoro che è possibile eseguire. Un problema che potrebbe richiedere la riscrittura di metà della codebase non deve essere tentato durante un ciclo di rilascio di piccole dimensioni.

La composizione e la natura di un team definiscono i tipi di lavoro che è possibile eseguire. Quali altri impegni ha il team? Nel team è presente un progettista o un tecnico dell'usabilità? Quali competenze ha il team con la progettazione web o dell'interfaccia utente? Infine, e più importante, sono considerazioni aziendali. Quali sono gli obiettivi di ricavi per questo progetto? Who i concorrenti? Quali sono i vantaggi della risoluzione di determinati problemi? Quali partnership possono essere contraffatte? Eventuali altre considerazioni devono essere identificate anche prima di classificare l'elenco in ordine di priorità.

Dopo aver impostato la priorità, l'elenco di istruzioni relative ai problemi imposta la direzione per il prodotto e garantisce che lo sviluppo sia mirato nelle aree giuste.

## <a name="conceptual-design"></a>Progettazione concettuale

In genere, l'interfaccia utente non viene affrontata nella fase di progettazione concettuale. Tuttavia, questa fase richiede un modello aziendale completo con profili utente completi e scenari di utilizzo che sono imperativi per una corretta esperienza utente.

## <a name="logical-design"></a>Progettazione logica

La fase di progettazione logica si verifica quando vengono sviluppati i prototipi iniziali che supportano la progettazione concettuale.

In questa fase vengono identificate anche le tecnologie hardware e software specifiche da usare durante lo sviluppo, che possono determinare le funzionalità dell'interfaccia utente nel prodotto finale. Per altre informazioni, vedere Interfaccia utente [Technologies](user-interface-technologies-for-windows-applications.md).

Oltre agli strumenti di sviluppo, devono essere identificati i vari requisiti hardware e i fattori di forma che devono essere destinati all'applicazione.

## <a name="physical-design"></a>Progettazione fisica

La fase di progettazione fisica determina come deve essere implementata una progettazione dell'interfaccia utente per l'hardware specifico e i fattori di forma identificati nella progettazione logica.

È durante questa fase che le limitazioni dell'hardware o del fattore di forma potrebbero introdurre vincoli imprevisti sull'interfaccia utente che richiedono miglioramenti significativi alla progettazione.

 

 