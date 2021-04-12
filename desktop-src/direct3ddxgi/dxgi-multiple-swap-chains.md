---
description: Per migliorare le prestazioni, è consigliabile creare più di una catena di scambio per ogni dispositivo di rendering Direct3D.
ms.assetid: 29AB9799-9E4E-4A96-B4AB-F1B754794879
title: Miglioramento delle prestazioni con più catene di scambio per ogni dispositivo di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e356434521054bc13b553c8ae3d6e43d8d98ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481957"
---
# <a name="improving-performance-with-multiple-swap-chains-per-rendering-device"></a>Miglioramento delle prestazioni con più catene di scambio per ogni dispositivo di rendering

Per migliorare le prestazioni, è consigliabile creare più di una catena di scambio per ogni dispositivo di rendering Direct3D. Usare questo approccio per risparmiare memoria necessaria per la creazione di dispositivi aggiuntivi o per ridurre la quantità di tempo di rendering per il rendering separatamente per singole catene di scambio per dispositivo o per risparmiare memoria e ridurre il tempo di rendering.

-   [Scenari di app con più catene di scambio per dispositivo](#app-scenarios-with-multiple-swap-chains-per-device)
-   [Gestione di più catene di scambio per dispositivo](#managing-multiple-swap-chains-per-device)
    -   [Impostazione della latenza massima del frame](#setting-maximum-frame-latency)
    -   [Uso di flip model con più catene di scambio per dispositivo](#using-flip-model-with-multiple-swap-chains-per-device)
-   [Argomenti correlati](#related-topics)

## <a name="app-scenarios-with-multiple-swap-chains-per-device"></a>Scenari di app con più catene di scambio per dispositivo

Si consiglia di usare più catene quando la scena dell'app è costituita da oggetti di visualizzazione separati che vengono sottoposti a rendering e aggiornati in modo indipendente. Ad esempio, l'app ha un'animazione costantemente modificata, ad esempio un video su un lato e un testo scorrevole su un altro lato. Per risparmiare memoria che in genere è necessario creare un dispositivo aggiuntivo e semplificare la condivisione del contenuto tra le due catene di scambio, è possibile creare entrambe le catene di scambio legate allo stesso dispositivo di rendering Direct3D. Usare una catena di scambio per l'animazione e una catena di scambio per il testo. Un esempio comune di questo scenario è costituito da un'app Direct3D che usa anche l'API [DirectComposition](../directcomp/directcomposition-portal.md) .

Un altro scenario è quello in cui si vuole risparmiare tempo di rendering impostando più destinazioni di rendering simultaneamente su più catene di scambio. Si supponga, ad esempio, di voler eseguire il rendering di una scena complessa con un numero elevato di trame e geometria, ad esempio le automobili da corsa in una traccia, e che la finestra dell'app visualizzi le visualizzazioni da entrambi i mirror posteriori e laterali in due finestre visualizzate di cui è stato eseguito il rendering da due catene di scambio. Se si impostano più catene di scambio come destinazioni di rendering, non è necessario che l'app ripeta separatamente i tempi di rendering in ogni catena di scambio.

## <a name="managing-multiple-swap-chains-per-device"></a>Gestione di più catene di scambio per dispositivo

Usare le linee guida in questa sezione per gestire più catene di scambio create per un singolo dispositivo di rendering Direct3D.

### <a name="setting-maximum-frame-latency"></a>Impostazione della latenza massima del frame

Usare il metodo [**IDXGIDevice1:: SetMaximumFrameLatency**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) per impostare il numero massimo di operazioni presenti che il sistema operativo è in grado di accodare per il rendering sullo schermo. Il numero massimo è per dispositivo di rendering Direct3D anziché per ogni catena di scambio. Pertanto, per assicurarsi che il sistema operativo visualizzi le operazioni presenti nell'intervallo di vsync previsto, è consigliabile non impostare la latenza massima del frame su 1 quando si creano più catene di scambio del modello Flip o BitBlt per ogni dispositivo e quando più di una di queste catene di scambio eseguirà il rendering per ogni fotogramma. Come regola generale, se si inviano in modo affidabile solo 2 operazioni presenti per fotogramma tra tutte le catene di scambio dello stesso dispositivo, è possibile impostare la latenza massima del frame su 2. Se non è possibile inviare e contare in modo affidabile le operazioni presenti per fotogramma, è possibile usare le [statistiche attuali](dxgi-flip-model.md) per tenere traccia del momento in cui il sistema operativo Visualizza le operazioni presenti.

### <a name="using-flip-model-with-multiple-swap-chains-per-device"></a>Uso di flip model con più catene di scambio per dispositivo

Usare queste linee guida quando si usa il [modello DXGI Flip](dxgi-flip-model.md) con più catene di scambio create per un singolo dispositivo di rendering Direct3D.

### <a name="targeting-specific-vsync-intervals-with-each-swap-chains-present-operations"></a>Definizione di intervalli di vsync specifici con le operazioni presenti di ogni catena di scambio

Quando si creano due o più catene di scambio del modello Flip per ogni dispositivo, prestare attenzione alle differenze di visualizzazione quando si gestisce la sequenza di stato del dispositivo e la sequenza di chiamate al metodo [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) di tutte le catene di scambio. Per assicurarsi che il sistema operativo visualizzi l'operazione attuale di ogni catena di scambio nell'intervallo di vsync previsto, è consigliabile assicurarsi che il numero di operazioni in coda presenti sia sempre almeno uno inferiore al numero di buffer indietro per la catena di scambio con il minor numero di buffer back.

### <a name="flip-model-swap-chains-with-two-buffers"></a>Invertire le catene di scambio del modello con due buffer

L'app può essere destinata a intervalli vsync specifici quando il numero di operazioni in coda presenti è minore o uguale al numero di buffer back-1. Inoltre, è necessario usare o eseguire il rendering separatamente per ogni catena di scambio e quindi terminare l'uso di ogni catena di scambio con un'operazione esistente. Quindi, quando si inviano tutte le operazioni presenti per una catena di scambio flip-model a 2 buffer, si raggiunge la soglia per il numero di buffer indietro in cui è necessario prestare particolare attenzione se si vuole che l'app sia destinata a intervalli di vsync specifici.

Nel caso di catene di scambio a 2 buffer, per individuare intervalli di vsync specifici, è necessario assicurarsi che il sistema operativo completi la visualizzazione di ogni operazione presente della catena di scambio prima di eseguire il rendering nel buffer successivo. Si consiglia di completare l'impostazione della visualizzazione destinazione rendering e di altro stato di rendering, quindi eseguire il rendering successivo, quindi chiamare [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) per ognuno dei due buffer di una catena di scambio prima di eseguire la stessa operazione per un'altra catena di scambio. Quando si lavora con due o più catene di scambio, è necessario reimpostare la destinazione di rendering e lo stato di rendering sul dispositivo per ogni catena di scambio. Il vantaggio di questo approccio consiste nell'evitare il caso in cui una o più delle operazioni presenti della catena di scambio perdano l'intervallo di vsync previsto. Per il primo esempio, app con animazione e testo modificabili, come descritto in [scenari di app con più catene di scambio per ogni dispositivo](#app-scenarios-with-multiple-swap-chains-per-device), impostando come destinazione determinati intervalli di tempo, si garantisce che, quando l'animazione viene aggiornata in un'unica finestra di visualizzazione, il testo corrispondente di cui viene eseguito il rendering da una catena di scambio separata viene visualizzato contemporaneamente in un'altra finestra di visualizzazione. Se l'app deve essere destinata a intervalli di vsync specifici, è necessario seguire queste istruzioni.

Questo diagramma mostra un esempio del flusso di codice del rendering e della presentazione della catena di scambio in un'app con due catene di scambio Flip-Model ognuna con due buffer. In questo caso, è necessario specificare come destinazione un intervallo presente specifico per ogni operazione presente.

![illustrazione del modello flip con due buffer](images/flip-mode-2-buffers.png)

### <a name="reducing-rendering-time-by-simultaneously-setting-multiple-swap-chains-as-render-targets"></a>Riduzione del tempo di rendering impostando contemporaneamente più catene di scambio come destinazioni di rendering

Per il secondo esempio, Racing Cars in una traccia, come descritto in [scenari di app con più catene di scambio per ogni dispositivo](#app-scenarios-with-multiple-swap-chains-per-device), è possibile che si desideri comportare un compromesso specificando gli intervalli di vsync presenti con il risparmio di tempo di rendering ottenuto impostando contemporaneamente più destinazioni di rendering su tutte le catene di scambio. In questo caso, impostare più destinazioni di rendering simultaneamente, eseguire il rendering della scena in ogni catena di scambio e quindi chiamare [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) in ogni catena di scambio usata nella scena. Il vantaggio di questo approccio è la riduzione del tempo di rendering. La limitazione di questo approccio è che le operazioni simultanee della catena di scambio non possono avere come destinazione lo stesso vsync quando si usano catene di scambio a 2 buffer. Il sistema operativo, ad esempio, non visualizzerà il contenuto dei mirror della vista laterale di una corsa fino a 1 vsync dopo che lo stesso contenuto è stato rilevato dal mirroring della parte finale della corsa.

Questo diagramma mostra un esempio del flusso di codice del rendering e della presentazione della catena di scambio in un'app con due catene di scambio Flip-Model ognuna con due buffer di lunghezza. In questo tipo di esempio si salvano i tempi di rendering per scambiare le catene 1 e 2 per i buffer A e C. Tuttavia, non è possibile sincronizzare gli intervalli di VSync in cui vengono visualizzate le operazioni presenti per i buffer A e C. Questo modello si ripete per il frame 2.

![illustrazione di impostazione simultanea di più catene di scambio come destinazioni di rendering](images/multi-swap-chains-as-render-targets.png)

Per evitare di perdere l'intervallo di vsync previsto a causa di molte operazioni presenti in coda, è possibile aumentare il numero di buffer indietro in ogni catena di scambio. Questa tecnica usa tuttavia una maggiore quantità di memoria video. Per evitare gli intervalli di vsync di destinazione mancanti, è consigliabile lasciare sempre il numero di operazioni presenti in coda inferiori al numero di buffer indietro nella catena di scambio con il minor numero di buffer back. Quando si impostano due catene di scambio come più destinazioni di rendering, perché si accodano due operazioni presenti simultaneamente su entrambe le catene di scambio, è consigliabile creare catene di scambio con almeno tre buffer di lunghezza.

Il diagramma seguente mostra un esempio del flusso di codice del rendering e della presentazione della catena di scambio in un'app con due catene di scambio Flip-Model ognuna con tre buffer di lunghezza. In questo caso, poiché il numero di present in coda per un particolare frame è 2, che è inferiore al numero di buffer indietro per ogni catena di scambio, l'app può impostare più destinazioni di rendering e avere comunque come destinazione gli stessi intervalli di vsync per i buffer A e D nel frame 2 e per i buffer nei frame successivi.

![illustrazione di impostazione simultanea di più catene di scambio come destinazioni di rendering destinazione lo stesso vsync](images/multi-swap-chains-as-render-targets-same-vsync.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento della presentazione con il modello Flip, i rettangoli Dirty e le aree a scorrimento](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
