---
title: Modifiche importanti da Direct3D 11 a Direct3D 12
description: Direct3D 12 rappresenta una differenza significativa rispetto al modello di programmazione Direct3D 11. Direct3D 12 consente alle app di essere più vicine all'hardware che mai.
ms.assetid: CE5066C9-7EA6-437D-9EB0-AACFB6CFAD9E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3afc5fe9a451addf1d1f7b9aeddf1f55ca40a22db99134ba71d8195c72ad2b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123834"
---
# <a name="important-changes-from-direct3d-11-to-direct3d-12"></a>Modifiche importanti da Direct3D 11 a Direct3D 12

Direct3D 12 rappresenta una differenza significativa rispetto al modello di programmazione Direct3D 11. Direct3D 12 consente alle app di essere più vicine all'hardware che mai. Essendo più vicino all'hardware, Direct3D 12 è più veloce ed efficiente. Tuttavia, il compromesso dell'app con maggiore velocità ed efficienza con Direct3D 12 è che si è responsabili di più attività rispetto a Direct3D 11.

-   [Sincronizzazione esplicita](#explicit-synchronization)
-   [Gestione della residenza della memoria fisica](#physical-memory-residency-management)
-   [Oggetti di stato della pipeline](#pipeline-state-objects)
-   [Elenchi di comandi e aggregazioni](#command-lists-and-bundles)
-   [Heap e tabelle dei descrittori](#descriptor-heaps-and-tables)
-   [Porting da Direct3D 11](#porting-from-direct3d-11)
-   [Argomenti correlati](#related-topics)

Direct3D 12 è un ritorno alla programmazione di basso livello; offre maggiore controllo sugli elementi grafici dei giochi e delle app introducendo queste nuove funzionalità: oggetti per rappresentare lo stato complessivo della pipeline, elenchi di comandi e aggregazioni per l'invio del lavoro e heap e tabelle descrittori per l'accesso alle risorse.

L'app ha aumentato la velocità e l'efficienza con Direct3D 12, ma si è responsabili di più attività rispetto a Direct3D 11.

## <a name="explicit-synchronization"></a>Sincronizzazione esplicita

-   In Direct3D 12 la sincronizzazione CPU-GPU è ora responsabilità esplicita dell'app e non viene più eseguita in modo implicito dal runtime, come in Direct3D 11. Questo significa anche che Direct3D 12 non verifica automaticamente i rischi della pipeline, quindi anche in questo caso questa è la responsabilità delle app.
-   In Direct3D 12 le app sono responsabili della pipelining degli aggiornamenti dei dati. Ciò significa che il modello "Map/Lock-DISCARD" in Direct3D 11 deve essere eseguito manualmente in Direct3D 12. In Direct3D 11, se la GPU usa ancora il buffer quando si chiama [**ID3D11DeviceContext::Map**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map) con [**D3D11 \_ MAP WRITE \_ \_ DISCARD,**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_map)il runtime restituisce un puntatore a una nuova area di memoria anziché ai dati del buffer precedente. Ciò consente alla GPU di continuare a usare i dati vecchi mentre l'app inserisce i dati nel nuovo buffer. Nell'app non è necessaria alcuna gestione della memoria aggiuntiva. il buffer precedente viene riutilizzato o eliminato automaticamente al termine della GPU.
-   In Direct3D 12 tutti gli aggiornamenti dinamici (inclusi i buffer costanti, i vertex buffer dinamici, le trame dinamiche e così via) vengono controllati in modo esplicito dall'app. Questi aggiornamenti dinamici includono eventuali recinti GPU necessari o memorizzazione nel buffer. L'app è responsabile di mantenere la memoria disponibile fino a quando non è più necessaria.
-   Direct3D 12 usa il conteggio dei riferimenti in stile COM solo per la durata delle interfacce (usando il modello di riferimento debole di Direct3D associato alla durata del dispositivo). Tutte le durate di memoria delle risorse e delle descrizioni sono l'unica responsabilità dell'app da mantenere per la durata corretta e non vengono conteggiati i riferimenti. Direct3D 11 usa il conteggio dei riferimenti per gestire anche le durate delle dipendenze dell'interfaccia.

## <a name="physical-memory-residency-management"></a>Gestione della residenza della memoria fisica

Un'applicazione Direct3D 12 deve impedire race-conditions tra più code, più schede e thread della CPU. D3D12 non sincronizza più CPU e GPU, né supporta meccanismi pratici per la ridenominazione delle risorse o il multi-buffering. I recinti devono essere usati per evitare che più unità di elaborazione eseere sovrascise la memoria prima che un'altra unità di elaborazione finisca di usarla.

L'applicazione Direct3D 12 deve garantire che i dati siano residenti in memoria durante la lettura della GPU. La memoria usata da ogni oggetto viene resa residente durante la creazione dell'oggetto. Le applicazioni che chiamano questi metodi devono usare recinti per garantire che la GPU non accerta gli oggetti che sono stati sfrattati.

Le barriere delle risorse sono un altro tipo di sincronizzazione necessario, usato per sincronizzare le transizioni di risorse e sottorisorse a un livello molto granulare.

Vedere [Gestione della memoria in Direct3D 12.](memory-management.md)

## <a name="pipeline-state-objects"></a>Oggetti di stato della pipeline

Direct3D 11 consente la manipolazione dello stato della pipeline tramite un ampio set di oggetti indipendenti. Ad esempio, lo stato dell'assembler di input, pixel shader, lo stato del rasterizzatore e lo stato di unione dell'output possono essere tutti modificati in modo indipendente. Questa progettazione offre una rappresentazione pratica e relativamente elevata della pipeline grafica, ma non usa le funzionalità dell'hardware moderno, principalmente perché i vari stati sono spesso interdipendenti. Ad esempio, molte GPU combinano pixel shader stato di unione e output in un'unica rappresentazione hardware. Tuttavia, poiché l'API Direct3D 11 consente l'impostazione separata di queste fasi della pipeline, il driver di visualizzazione non può risolvere i problemi di stato della pipeline fino a quando lo stato non viene finalizzato, che non è fino al tempo di disegno. Questo schema ritarda la configurazione dello stato dell'hardware, ovvero un sovraccarico aggiuntivo e un minor numero massimo di chiamate di disegno per frame.

Direct3D 12 risolve questo schema unificando gran parte dello stato della pipeline in oggetti di stato della pipeline (PSO) non modificabili, che vengono finalizzati al momento della creazione. L'hardware e i driver possono quindi convertire immediatamente il PSO in tutte le istruzioni e lo stato nativi dell'hardware necessari per eseguire il lavoro gpu. È comunque possibile modificare dinamicamente l'oggetto PSO in uso, ma a tale scopo, l'hardware deve solo copiare la quantità minima di stato pre-calcolato direttamente nei registri hardware, anziché calcolare lo stato hardware in tempo reale. L'uso di PSO riduce significativamente l'overhead delle chiamate di disegno e molte altre chiamate di disegno possono verificarsi per ogni frame. Per altre informazioni su PSO, vedere [Gestione dello stato della pipeline grafica in Direct3D 12.](managing-graphics-pipeline-state-in-direct3d-12.md)

## <a name="command-lists-and-bundles"></a>Elenchi di comandi e aggregazioni

In Direct3D 11 tutto l'invio di lavoro viene eseguito tramite il contesto immediato [,](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render)che rappresenta un singolo flusso di comandi che passano alla GPU. Per ottenere il ridimensionamento multithreading, i giochi hanno anche [contesti posticimanti](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render) disponibili. I contesti posticimentati in Direct3D 11 non sono perfettamente mappati all'hardware, quindi al loro interno è possibile eseguire relativamente poco lavoro.

Direct3D 12 introduce un nuovo modello per l'invio di lavoro in base agli elenchi di comandi che contengono l'intera totalità delle informazioni necessarie per eseguire un particolare carico di lavoro nella GPU. Ogni nuovo elenco di comandi contiene informazioni quali PSO usare, quali risorse di trama e buffer sono necessarie e gli argomenti per tutte le chiamate di disegno. Poiché ogni elenco di comandi è autonomo e non eredita alcuno stato, il driver può pre-calcolare tutti i comandi GPU necessari in anticipo e in modo a thread libero. L'unico processo seriale necessario è l'invio finale di elenchi di comandi alla GPU tramite la coda dei comandi.

Oltre agli elenchi di comandi, Direct3D 12 introduce anche un secondo livello di pre-calcolo del lavoro: *bundle .* A differenza degli elenchi di comandi, completamente indipendenti e in genere costruiti, inviati una sola volta e eliminati, i bundle forniscono una forma di ereditarietà dello stato che consente il riutilizzo. Ad esempio, se un gioco vuole disegnare due modelli di caratteri con trame diverse, un approccio consiste nel registrare un elenco di comandi con due set di chiamate di disegno identiche. Un altro approccio consiste nel "registrare" un bundle che disegna un modello a carattere singolo, quindi "riprodurre" il bundle due volte nell'elenco dei comandi usando risorse diverse. In quest'ultimo caso, il driver di visualizzazione deve solo calcolare le istruzioni appropriate una sola volta e la creazione dell'elenco di comandi è essenzialmente due chiamate di funzione a basso costo.

Per altre informazioni sugli elenchi di comandi e sui bundle, vedere [Invio di lavoro in Direct3D 12.](command-queues-and-command-lists.md)

## <a name="descriptor-heaps-and-tables"></a>Heap e tabelle dei descrittori

L'associazione di risorse in Direct3D 11 è altamente astratta e comoda, ma lascia sottoutilizzate molte funzionalità hardware moderne. In Direct3D 11  i giochi creano oggetti di visualizzazione delle risorse e quindi associano tali visualizzazioni a diversi *slot* in varie fasi dello shader nella pipeline. Gli shader, a loro volta, leggono i dati da questi slot di associazione espliciti, che sono fissi in fase di disegno. Questo modello significa che ogni volta che un gioco disegna usando risorse diverse, deve riassolare visualizzazioni diverse a slot diversi e chiamare di nuovo draw. Questo caso rappresenta anche il sovraccarico che può essere eliminato usando completamente le moderne funzionalità hardware.

Direct3D 12 modifica il modello di associazione in modo che corrisponda all'hardware moderno e migliora significativamente le prestazioni. Invece di richiedere visualizzazioni di risorse autonome e mapping esplicito agli slot, Direct3D 12 fornisce un heap descrittore in cui i giochi creano le diverse visualizzazioni delle risorse. Questo schema fornisce un meccanismo che consente alla GPU di scrivere direttamente la descrizione della risorsa nativa dell'hardware (descrittore) nella memoria in anticipo. Per dichiarare le risorse che devono essere usate dalla pipeline per una particolare chiamata di disegno, i giochi specificano una o più tabelle descrittori che rappresentano gli intervalli secondari dell'heap completo del descrittore. Poiché l'heap dei descrittori è già stato popolato con i dati del descrittore specifici dell'hardware appropriati, la modifica delle tabelle dei descrittori è un'operazione estremamente a basso costo.

Oltre alle prestazioni migliorate offerte dagli heap e dalle tabelle dei descrittori, Direct3D 12 consente anche l'indicizzazione dinamica delle risorse negli shader, che offre flessibilità senza precedenti e sblocca nuove tecniche di rendering. Ad esempio, i moderni motori di rendering posticipati codificano in genere un materiale o un identificatore di oggetto di qualche tipo nel buffer g intermedio. In Direct3D 11 questi motori devono prestare attenzione a evitare l'uso di troppi materiali, perché l'inclusione di troppi in un buffer g può rallentare significativamente il passaggio di rendering finale. Con le risorse indicizzabili in modo dinamico, una scena con un migliaio di materiali può essere finalizzata esattamente come una con solo dieci.

Per altre informazioni sugli heap e sulle tabelle dei descrittori, vedere [Associazione di](resource-binding.md)risorse e Differenze nel modello di associazione [da Direct3D 11.](binding-model.md)

## <a name="porting-from-direct3d-11"></a>Porting da Direct3D 11

Il porting da Direct3D 11 è un processo interessato, descritto in [Porting from Direct3D 11 to Direct3D 12 ( Porting from Direct3D 11 to Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md)). Vedere anche la gamma di opzioni disponibili in [Uso di Direct3D 11, Direct3D 10 e Direct2D.](direct3d-12-interop.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 