---
title: Modifiche importanti da Direct3D 11 a Direct3D 12
description: Direct3D 12 rappresenta una partenza significativa dal modello di programmazione Direct3D 11. Direct3D 12 consente alle app di avvicinarsi a hardware che mai.
ms.assetid: CE5066C9-7EA6-437D-9EB0-AACFB6CFAD9E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be891d71d6c1f3a12d8d5aac3ec46785207ed31
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548794"
---
# <a name="important-changes-from-direct3d-11-to-direct3d-12"></a>Modifiche importanti da Direct3D 11 a Direct3D 12

Direct3D 12 rappresenta una partenza significativa dal modello di programmazione Direct3D 11. Direct3D 12 consente alle app di avvicinarsi a hardware che mai. Grazie alla vicinanza all'hardware, Direct3D 12 è più veloce ed efficiente. Tuttavia, il compromesso dell'app con una maggiore velocità ed efficienza con Direct3D 12 è che si è responsabili di più attività rispetto a Direct3D 11.

-   [Sincronizzazione esplicita](#explicit-synchronization)
-   [Gestione della residenza di memoria fisica](#physical-memory-residency-management)
-   [Oggetti stato della pipeline](#pipeline-state-objects)
-   [Elenchi di comandi e bundle](#command-lists-and-bundles)
-   [Heap e tabelle descrittore](#descriptor-heaps-and-tables)
-   [Porting da Direct3D 11](#porting-from-direct3d-11)
-   [Argomenti correlati](#related-topics)

Direct3D 12 è un ritorno alla programmazione di basso livello. offre un maggiore controllo sugli elementi grafici dei giochi e delle app introducendo queste nuove funzionalità: gli oggetti per rappresentare lo stato complessivo della pipeline, gli elenchi di comandi e le aggregazioni per l'invio del lavoro e gli heap e le tabelle dei descrittori per l'accesso alle risorse.

L'app ha aumentato la velocità e l'efficienza con Direct3D 12, ma è responsabile di più attività rispetto a Direct3D 11.

## <a name="explicit-synchronization"></a>Sincronizzazione esplicita

-   In Direct3D 12 la sincronizzazione della GPU CPU è ora la responsabilità esplicita dell'app e non viene più eseguita in modo implicito dal runtime, così come si trova in Direct3D 11. Questo fatto significa anche che nessun controllo automatico dei rischi per la pipeline viene eseguito da Direct3D 12, di conseguenza si tratta della responsabilità delle app.
-   In Direct3D 12, le app sono responsabili del pipelining degli aggiornamenti dei dati. Ovvero il modello "map/Lock-scarto" in Direct3D 11 deve essere eseguito manualmente in Direct3D 12. In Direct3D 11, se la GPU usa ancora il buffer quando si chiama [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map) con lo [**\_ scarto di \_ scrittura \_ della mappa d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_map), il runtime restituisce un puntatore a una nuova area di memoria anziché ai dati del buffer obsoleti. Questo consente alla GPU di continuare a usare i dati obsoleti mentre l'app inserisce i dati nel nuovo buffer. Nell'app non è necessaria alcuna gestione della memoria aggiuntiva. il buffer precedente viene riutilizzato o eliminato automaticamente al termine della GPU.
-   In Direct3D 12 tutti gli aggiornamenti dinamici, inclusi i buffer costanti, i buffer dei vertici dinamici, le trame dinamiche e così via, sono controllati in modo esplicito dall'app. Questi aggiornamenti dinamici includono eventuali barriere GPU o buffering necessari. L'app è responsabile della disponibilità della memoria fino a quando non è più necessaria.
-   Direct3D 12 USA il conteggio dei riferimenti di tipo COM solo per la durata delle interfacce, usando il modello di riferimento debole di Direct3D associato alla durata del dispositivo. Tutte le durate della memoria della risorsa e della descrizione sono l'unica responsabilità dell'app di mantenere la durata appropriata e non vengono conteggiati i riferimenti. Direct3D 11 utilizza il conteggio dei riferimenti per gestire anche la durata delle dipendenze di interfaccia.

## <a name="physical-memory-residency-management"></a>Gestione della residenza di memoria fisica

Un'applicazione Direct3D 12 deve impedire race condition tra più code, più adapter e i thread della CPU. D3D12 non Sincronizza più la CPU e la GPU, né supporta meccanismi pratici per la ridenominazione delle risorse o il multibuffering. È necessario usare i limiti per evitare che più unità di elaborazione sovrascrivano la memoria prima che un'altra unità di elaborazione lo usi.

L'applicazione Direct3D 12 deve garantire che i dati siano residenti in memoria mentre vengono letti dalla GPU. La memoria utilizzata da ogni oggetto viene resa residente durante la creazione dell'oggetto. Le applicazioni che chiamano questi metodi devono usare le schermate per assicurarsi che la GPU non acceda a oggetti rimossi.

Le barriere delle risorse sono un altro tipo di sincronizzazione necessario, usato per sincronizzare le transizioni di risorse e risorse a un livello estremamente granulare.

Vedere [gestione della memoria in Direct3D 12](memory-management.md).

## <a name="pipeline-state-objects"></a>Oggetti stato della pipeline

Direct3D 11 consente la manipolazione dello stato della pipeline tramite un ampio set di oggetti indipendenti. Ad esempio, lo stato dell'assembler di input, lo stato pixel shader, lo stato di rasterizzazione e lo stato di Unione di output possono essere tutti modificati in modo indipendente. Questa progettazione offre una rappresentazione comoda e relativamente generale della pipeline grafica, ma non usa le funzionalità dell'hardware moderno, principalmente perché i vari Stati sono spesso interdipendenti. Molte GPU, ad esempio, combinano pixel shader e lo stato di Unione dell'output in una singola rappresentazione hardware. Tuttavia, poiché l'API Direct3D 11 consente di impostare le fasi della pipeline separatamente, il driver di visualizzazione non riesce a risolvere i problemi di stato della pipeline fino a quando lo stato non viene finalizzato, che non è fino al momento dell'estrazione. Questo schema ritarda la configurazione dello stato dell'hardware, ovvero un sovraccarico aggiuntivo e un minor numero massimo di chiamate di disegno per fotogramma.

Direct3D 12 risolve questo schema unificando la maggior parte dello stato della pipeline in oggetti di stato della pipeline non modificabili (PSO), che vengono finalizzati al momento della creazione. L'hardware e i driver possono quindi convertire immediatamente il PSO in tutte le istruzioni native hardware e lo stato necessario per eseguire il lavoro della GPU. È comunque possibile modificare in modo dinamico quale PSO è in uso, ma a tale scopo, l'hardware deve solo copiare la quantità minima di stato pre-calcolato direttamente nei registri hardware, anziché calcolare lo stato dell'hardware in tempo reale. Usando PSO, il sovraccarico delle chiamate di progetto viene ridotto in modo significativo e molte altre chiamate di progetto possono verificarsi per ogni fotogramma. Per altre informazioni su PSO, vedere [gestione dello stato della pipeline grafica in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="command-lists-and-bundles"></a>Elenchi di comandi e bundle

In Direct3D 11 tutti gli invii di lavoro vengono eseguiti tramite il [contesto immediato](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render), che rappresenta un singolo flusso di comandi che passano alla GPU. Per ottenere il ridimensionamento multithreading, i giochi hanno anche [contesti posticipati](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render) disponibili. I contesti posticipati in Direct3D 11 non vengono mappati perfettamente all'hardware, quindi è possibile eseguire un lavoro relativamente ridotto.

Direct3D 12 introduce un nuovo modello per l'invio di lavoro in base agli elenchi di comandi che contengono tutte le informazioni necessarie per eseguire un determinato carico di lavoro sulla GPU. Ogni nuovo elenco di comandi contiene informazioni quali il PSO da usare, le risorse di trama e buffer necessarie e gli argomenti per tutte le chiamate di creazione. Poiché ogni elenco di comandi è autonomo e non eredita alcuno stato, il driver è in grado di pre-calcolare tutti i comandi GPU necessari in primo piano e in modalità a thread libero. L'unico processo seriale necessario è l'invio finale degli elenchi di comandi alla GPU tramite la coda dei comandi.

Oltre agli elenchi di comandi, Direct3D 12 introduce anche un secondo livello di pre-calcolo del lavoro: *bundle*. A differenza degli elenchi di comandi, che sono completamente autonomi e vengono in genere costruiti, inviati una sola volta ed eliminati, i bundle forniscono una forma di ereditarietà dello stato che consente il riutilizzo. Se, ad esempio, un gioco vuole creare due modelli di caratteri con diverse trame, un approccio consiste nel registrare un elenco di comandi con due set di chiamate di traccia identiche. Un altro approccio consiste nel "registrare" un bundle che disegna un singolo modello di caratteri, quindi "riprodurre" il bundle due volte nell'elenco dei comandi usando risorse diverse. Nel secondo caso, il driver di visualizzazione deve solo calcolare le istruzioni appropriate una sola volta e la creazione dell'elenco di comandi essenzialmente equivale a due chiamate di funzione a basso costo.

Per altre informazioni sugli elenchi di comandi e sui bundle, vedere [lavoro di invio in Direct3D 12](command-queues-and-command-lists.md).

## <a name="descriptor-heaps-and-tables"></a>Heap e tabelle descrittore

Il binding di risorse in Direct3D 11 è altamente astratto e pratico, ma lascia molte funzionalità hardware moderne sottoutilizzate. In Direct3D 11 i giochi creano oggetti *visualizzazione* delle risorse, quindi associano tali viste a diversi *slot* in varie fasi dello shader della pipeline. Gli shader, a loro volta, leggono i dati da tali slot di binding espliciti, che vengono corretti in fase di estrazione. Questo modello significa che ogni volta che un gioco viene disegnato usando risorse diverse, deve riassociare diverse visualizzazioni a slot diversi e chiamare di nuovo il metodo di creazione. Questo caso rappresenta anche un sovraccarico che può essere eliminato usando completamente le funzionalità hardware moderne.

Direct3D 12 modifica il modello di binding in modo che corrisponda all'hardware moderno e migliora significativamente le prestazioni. Anziché richiedere visualizzazioni di risorse autonome e mapping esplicito agli slot, Direct3D 12 fornisce un heap dei descrittori in cui i giochi creano le varie visualizzazioni di risorse. Questo schema fornisce un meccanismo che consente alla GPU di scrivere direttamente la descrizione della risorsa nativa hardware (descrittore) in memoria in primo piano. Per dichiarare quali risorse devono essere usate dalla pipeline per una determinata chiamata di progetto, i giochi specificano una o più tabelle descrittore che rappresentano intervalli secondari dell'heap completo del descrittore. Poiché l'heap del descrittore è già stato popolato con i dati appropriati del descrittore specifico dell'hardware, la modifica delle tabelle dei descrittori è un'operazione estremamente a basso costo.

Oltre alle prestazioni migliorate offerte dagli heap e dalle tabelle dei descrittori, Direct3D 12 consente anche di indicizzare dinamicamente le risorse in shader, che offrono una flessibilità senza precedenti e sbloccano nuove tecniche di rendering. Ad esempio, i motori di rendering posticipati moderni in genere codificano un identificatore di materiale o di oggetto di qualche tipo nel buffer g intermedio. In Direct3D 11, questi motori devono prestare attenzione a evitare di usare troppi materiali, in quanto l'inclusione di troppi in un g-buffer può rallentare significativamente il passaggio di rendering finale. Con le risorse indicizzabili in modo dinamico, una scena con migliaia di materiali può essere finalizzata con la stessa rapidità di una con soli dieci.

Per ulteriori informazioni sugli heap e le tabelle dei descrittori, vedere [associazione di risorse](resource-binding.md)e [differenze nel modello di associazione da Direct3D 11](binding-model.md).

## <a name="porting-from-direct3d-11"></a>Porting da Direct3D 11

Il porting da Direct3D 11 è un processo necessario, descritto in [porting da Direct3D 11 a Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md). Vedere anche l'intervallo di opzioni disponibili in [utilizzo di Direct3D 11, Direct3D 10 e Direct2D](direct3d-12-interop.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 