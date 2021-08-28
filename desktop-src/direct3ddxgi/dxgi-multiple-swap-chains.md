---
description: Per migliorare le prestazioni, è possibile creare più catene di scambio per ogni dispositivo di rendering Direct3D.
ms.assetid: 29AB9799-9E4E-4A96-B4AB-F1B754794879
title: Miglioramento delle prestazioni con più catene di scambio per ogni dispositivo di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91445660bf9efc59e9e39c88819587dce3960325df0659487eaae67a845a7329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627505"
---
# <a name="improving-performance-with-multiple-swap-chains-per-rendering-device"></a>Miglioramento delle prestazioni con più catene di scambio per ogni dispositivo di rendering

Per migliorare le prestazioni, è possibile creare più catene di scambio per ogni dispositivo di rendering Direct3D. Usare questo approccio per risparmiare memoria necessaria per la creazione di dispositivi aggiuntivi o per ridurre la quantità di tempo di rendering per il rendering in singole catene di scambio per dispositivo separatamente o per risparmiare memoria e ridurre il tempo di rendering.

-   [Scenari di app con più catene di scambio per dispositivo](#app-scenarios-with-multiple-swap-chains-per-device)
-   [Gestione di più catene di scambio per dispositivo](#managing-multiple-swap-chains-per-device)
    -   [Impostazione della latenza massima dei frame](#setting-maximum-frame-latency)
    -   [Uso del modello flip con più catene di scambio per dispositivo](#using-flip-model-with-multiple-swap-chains-per-device)
-   [Argomenti correlati](#related-topics)

## <a name="app-scenarios-with-multiple-swap-chains-per-device"></a>Scenari di app con più catene di scambio per dispositivo

È consigliabile usare più catene quando la scena dell'app è costituita da oggetti di visualizzazione separati sottoposti a rendering e aggiornati in modo indipendente. Ad esempio, l'app ha un'animazione in continua evoluzione, ad esempio video su un lato e testo scorrevole su un altro lato. Per risparmiare memoria che in genere è necessario creare un dispositivo aggiuntivo e per semplificare la condivisione del contenuto tra le due catene di scambio, è possibile creare entrambe le catene di scambio collegate allo stesso dispositivo di rendering Direct3D. Usare una catena di scambio per l'animazione e una catena di scambio per il testo. Un esempio comune di questo scenario è un'app Direct3D che usa anche l'API [DirectComposition.](../directcomp/directcomposition-portal.md)

Un altro scenario è quando si vuole risparmiare tempo di rendering impostando più destinazioni di rendering in più catene di scambio contemporaneamente. Si supponga, ad esempio, di voler eseguire il rendering di una scena complessa con molte trame e geometrie, ad esempio automobili da corsa su un tracciato, e che la finestra dell'app mostri le visualizzazioni da entrambi gli mirror posteriore e laterale in due finestre di visualizzazione sottoposte a rendering da due catene di scambio. Se si impostano più catene di scambio come destinazioni di rendering, l'app non deve ripetere i tempi di rendering in ogni catena di scambio separatamente.

## <a name="managing-multiple-swap-chains-per-device"></a>Gestione di più catene di scambio per dispositivo

Usare le linee guida in questa sezione per gestire più catene di scambio create per un singolo dispositivo di rendering Direct3D.

### <a name="setting-maximum-frame-latency"></a>Impostazione della latenza massima dei frame

Usare il [**metodo IDXGIDevice1::SetMaximumFrameLatency**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) per impostare il numero massimo di operazioni presenti che il sistema operativo può accodare per il rendering alla visualizzazione. Questo numero massimo è per ogni dispositivo di rendering Direct3D anziché per ogni catena di scambio. Pertanto, per assicurarsi che il sistema operativo visualizzi le operazioni presenti all'intervallo vsync previsto, è consigliabile non impostare la latenza massima dei frame su 1 quando si creano più catene di scambio di modelli flip o bitblt per dispositivo e quando più di una di queste catene di scambio verrà visualizzata per ogni frame. Come regola generale, se si inviano in modo affidabile solo 2 operazioni presenti per frame tra tutte le catene di scambio dello stesso dispositivo, è possibile impostare la latenza massima dei frame su 2. Se non è possibile inviare e contare in modo affidabile [](dxgi-flip-model.md) le operazioni presenti per ogni frame, è possibile usare le statistiche presenti per tenere traccia quando il sistema operativo visualizza le operazioni presenti.

### <a name="using-flip-model-with-multiple-swap-chains-per-device"></a>Uso del modello flip con più catene di scambio per dispositivo

Usare queste linee guida quando si usa il modello [flip DXGI](dxgi-flip-model.md) con più catene di scambio create per un singolo dispositivo di rendering Direct3D.

### <a name="targeting-specific-vsync-intervals-with-each-swap-chains-present-operations"></a>Destinazione di intervalli vsync specifici con le operazioni presenti di ogni catena di scambio

Quando si creano due o più catene di scambio di modelli flip per dispositivo, prestare attenzione alle differenze di visualizzazione quando si gestisce la sequenza di stato del dispositivo e la sequenza di chiamate al metodo [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) di tutte le catene di scambio. Per assicurarsi che il sistema operativo visualizzi l'operazione corrente di ogni catena di scambio all'intervallo vsync previsto, è consigliabile assicurarsi che il numero di operazioni presenti in coda sia sempre almeno uno in meno del numero di buffer back per la catena di scambio con il numero minimo di buffer nascosto.

### <a name="flip-model-swap-chains-with-two-buffers"></a>Capovolgere le catene di scambio del modello con due buffer

L'app può avere come destinazione intervalli vsync specifici quando il numero di operazioni presenti in coda è minore o uguale al numero di buffer nascosto - 1. Inoltre, è necessario usare o eseguire il rendering in ogni catena di scambio separatamente e quindi terminare l'uso di ogni catena di scambio con un'operazione presente. Pertanto, quando si inviano tutte le operazioni presenti per una catena di scambio con flip-model a 2 buffer, si raggiunge la soglia per il numero di buffer back in cui è necessario prestare particolare attenzione se si vuole che l'app rivolgiti a intervalli vsync specifici.

Nel caso di catene di scambio a 2 buffer, per impostare come destinazione intervalli vsync specifici, è necessario assicurarsi che il sistema operativo completa la visualizzazione dell'operazione corrente di ogni catena di scambio prima di eseguire il rendering nel buffer successivo. È consigliabile completare l'impostazione della visualizzazione di destinazione di rendering e di un altro stato di rendering, eseguire il rendering successivo e quindi chiamare [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) per ognuno dei due buffer di una catena di scambio prima di eseguire la stessa operazione per un'altra catena di scambio. Quando si lavora con due o più catene di scambio, è necessario reimpostare la destinazione di rendering e lo stato di rendering nel dispositivo per ogni catena di scambio. Il vantaggio di questo approccio consiste nell'evitare il caso in cui una o più delle operazioni presenti della catena di scambio non rilassano l'intervallo vsync previsto. Per il primo esempio, l'app con animazione e testo che cambiano, come descritto in Scenari di app con più catene di scambio [per](#app-scenarios-with-multiple-swap-chains-per-device)dispositivo, selezionando specifici intervalli presenti, è garantito che quando l'animazione viene aggiornata in una finestra di visualizzazione, anche il testo corrispondente sottoposto a rendering da una catena di scambio separata viene visualizzato contemporaneamente in un'altra finestra di visualizzazione. Se l'app deve avere come destinazione intervalli vsync specifici, è necessario seguire queste indicazioni.

Questo diagramma mostra un esempio del flusso di codice del rendering e della presentazione della catena di scambio in un'app con due catene di scambio di modelli di flip ognuna con due buffer. In questo caso, è necessario impostare come destinazione un intervallo di presentazione specifico per ogni operazione presente.

![Illustrazione del modello flip con due buffer](images/flip-mode-2-buffers.png)

### <a name="reducing-rendering-time-by-simultaneously-setting-multiple-swap-chains-as-render-targets"></a>Riduzione del tempo di rendering impostando simultaneamente più catene di scambio come destinazioni di rendering

Per il secondo esempio, le automobili da corsa su un tracciato, come descritto in Scenari di app con più catene di [scambio per](#app-scenarios-with-multiple-swap-chains-per-device)dispositivo, è possibile scegliere di scegliere come destinazione specifici intervalli vsync presenti con il risparmio di tempo di rendering che si ottiene impostando più destinazioni di rendering in tutte le catene di scambio contemporaneamente. In questo caso, impostare più destinazioni di rendering contemporaneamente, eseguire il rendering della scena in ogni catena di scambio e quindi chiamare [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) in ogni catena di scambio usata nella scena. Il vantaggio di questo approccio consiste nel ridurre il tempo di rendering. La limitazione di questo approccio è che le operazioni simultanee presenti nella catena di scambio non possono avere come destinazione lo stesso vsync quando si usano catene di scambio a 2 buffer. Ad esempio, il sistema operativo non visualizza il contenuto degli mirror di visualizzazione laterale dell'auto da corsa fino a 1 vsync dopo che lo stesso contenuto è stato visualizzato dallo mirror della visualizzazione posteriore dell'auto da corsa.

Questo diagramma mostra un esempio del flusso di codice del rendering e della presentazione della catena di scambio in un'app con due catene di scambio di modelli flip ognuna con due buffer di lunghezza. In questo tipo di esempio si risparmiano i tempi di rendering per scambiare le catene 1 e 2 per i buffer A e C. Non è tuttavia possibile sincronizzare gli intervalli vsync in corrispondenza dei quali vengono visualizzate le operazioni presenti per i buffer A e C. Questo modello si ripete per il frame 2.

![Illustrazione dell'impostazione simultanea di più catene di scambio come destinazioni di rendering](images/multi-swap-chains-as-render-targets.png)

Per evitare di mancare l'intervallo vsync previsto a causa di molte operazioni presenti in coda, è possibile aumentare il numero di buffer nascosto in ogni catena di scambio. Questa tecnica usa tuttavia una maggiore quantità di memoria video. Per evitare intervalli vsync di destinazione mancanti, è consigliabile mantenere sempre il numero di operazioni presenti in coda inferiori al numero di buffer nascosto nella catena di scambio con il minor numero di buffer nascosto. Quando si impostano due catene di scambio come più destinazioni di rendering, poiché si accoda due operazioni presenti contemporaneamente su entrambe le catene di scambio, è consigliabile creare catene di scambio con almeno tre buffer di lunghezza.

Il diagramma successivo mostra un esempio del flusso di codice di rendering e presentazione della catena di scambio in un'app con due catene di scambio flip-model ognuna con tre buffer di lunghezza. In questo caso, poiché il numero di oggetti presenti in coda per un frame specifico è 2, ovvero minore del numero di buffer nascosto per ogni catena di scambio, l'app può impostare più destinazioni di rendering e ancora avere come destinazione gli stessi intervalli vsync per i buffer A e D nel frame 2 e per i buffer nei frame successivi.

![Illustrazione dell'impostazione simultanea di più catene di scambio come destinazioni di rendering che hanno come destinazione lo stesso vsync](images/multi-swap-chains-as-render-targets-same-vsync.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento della presentazione con il modello di capovolgimento, rettangoli dirty e aree di scorrimento](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
