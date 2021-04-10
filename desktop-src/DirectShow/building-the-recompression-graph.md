---
description: Creazione del grafico di ricompressione
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Creazione del grafico di ricompressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8ea604bead34c22c123bbabe5d88e985006a9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876082"
---
# <a name="building-the-recompression-graph"></a>Creazione del grafico di ricompressione

Un tipico grafico di filtro per la ricompressione dei file AVI è simile al seguente:

![grafico di ricompressione AVI](images/avi2avi4.png)

Il [filtro Splitter AVI](avi-splitter-filter.md) estrae i dati dal [filtro di origine file (Async)](file-source--async--filter.md) e li analizza in flussi video e audio. Il video decompressore decodifica il video compresso, dove viene ricompresso dal compressore video. La scelta dei decompressori dipende dal file di origine. verrà gestito automaticamente da [Intelligent Connect](intelligent-connect.md). L'applicazione deve scegliere il compressore, in genere presentando un elenco all'utente. (Vedere [scelta di un filtro di compressione](choosing-a-compression-filter.md)).

Il video compresso passa quindi al [filtro Mux AVI](avi-mux-filter.md). Il flusso audio in questo esempio non è compresso, quindi passa direttamente dalla barra di divisione AVI alla Mux AVI. Il mux AVI interleaves The Two Streams e il [filtro del writer di file](file-writer-filter.md) scrive l'output su disco. Si noti che il mux AVI è necessario anche se il file originale non dispone di un flusso audio.

Il modo più semplice per creare questo grafico di filtro consiste nell'usare il [Generatore di grafici di acquisizione](capture-graph-builder.md), un componente DirectShow per la creazione di grafici di acquisizione e altri grafici di filtri personalizzati.

Per iniziare, chiamare CoCreateInstance per creare il generatore del grafico di acquisizione:


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



Usare quindi il generatore del grafico di acquisizione per compilare il grafico del filtro:

1.  Compilare la sezione rendering del grafo, che include il filtro Mux AVI e il [writer di file](file-writer-filter.md).
2.  Aggiungere il filtro di origine e il filtro di compressione al grafico.
3.  Connettere il filtro di origine al filtro MUX. Il generatore di grafici di acquisizione inserisce tutti i filtri splitter e decodificatore necessari per analizzare il file di origine. Può inoltre instradare i flussi video e audio attraverso i filtri di compressione.

Le sezioni seguenti illustrano ognuno di questi passaggi.

Compilare la sezione rendering

Per compilare la sezione rendering del grafo, chiamare il metodo [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) . Questo metodo accetta parametri di input che specificano il sottotipo di supporto per l'output e il nome del file di output. Restituisce i puntatori al filtro MUX e al writer di file. Il filtro MUX è necessario per la fase successiva della creazione di grafici. Il puntatore al writer di file non è necessario per questo esempio, in modo che il parametro possa essere **null**:


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



Quando il metodo restituisce, il filtro MUX ha un conteggio dei riferimenti in attesa, quindi assicurarsi di rilasciare il puntatore in un secondo momento.

Il diagramma seguente mostra il grafico di filtro in questo punto.

![sezione rendering del grafico del filtro](images/avi2avi1.png)

Il filtro MUX espone due interfacce per il controllo del formato AVI:

-   [**Interfaccia IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): imposta la modalità di interfoliazione.
-   [**Interfaccia IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): imposta il flusso master e l'indice di compatibilità AVI.

Aggiungere i filtri di origine e compressione

Il passaggio successivo consiste nell'aggiungere i filtri di origine e compressione al grafico dei filtri. Il generatore di grafici di acquisizione crea automaticamente un'istanza del gestore del grafico dei filtri quando si chiama SetOutputFileName. Ottenere un puntatore a esso chiamando il metodo [**ICaptureGraphBuilder2:: GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) :


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



A questo punto chiamare il metodo [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) per aggiungere il filtro di origine del file asincrono e il metodo [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il compressore video:


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



A questo punto, il filtro di origine e il filtro di compressione non sono connessi ad altri elementi nel grafico, come illustrato nella figura seguente:

![filtrare il grafico con filtri di origine e compressione](images/avi2avi2.png)

Connettere l'origine a Mux

Il passaggio finale consiste nel connettere il filtro di origine al filtro Mux AVI, tramite il compressore video. Usare il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , che connette un pin di output sul filtro di origine a un filtro di sink specificato, facoltativamente tramite un filtro di compressione.

I primi due parametri specificano quale dei pin del filtro di origine connettersi, designando una categoria pin e un tipo di supporto. Il filtro di origine del file asincrono ha un solo pin di output, quindi questi parametri devono essere **null**. I tre parametri successivi specificano il filtro di origine, il filtro di compressione (se presente) e il filtro MUX.

Nell'esempio di codice seguente viene eseguito il rendering del flusso video attraverso il compressore video:


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



Il diagramma seguente mostra il grafico di filtro fino a questo punto.

![flusso video sottoposto a rendering](images/avi2avi3.png)

Supponendo che il file di origine disponga di un flusso audio, il filtro [splitter AVI](avi-splitter-filter.md) ha creato un pin di output per l'audio. Per connettere questo pin, chiamare di nuovo RenderStream:


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



In questo caso non viene specificato alcun filtro di compressione. Il pin di output del filtro di origine è già connesso, quindi il metodo RenderStream Cerca un pin di output non connesso nel filtro della barra di divisione. Trova il pin audio e lo connette direttamente al filtro MUX. Se il file di origine non dispone di un flusso audio, la seconda chiamata a RenderStream avrà esito negativo. Si tratta di un comportamento previsto. Il grafo viene completato dopo la prima chiamata a RenderStream, quindi l'errore nella seconda chiamata è innocuo.

In questo esempio, l'ordine delle due chiamate RenderStream è importante. Poiché la seconda chiamata non specifica un compressore, verrà connesso qualsiasi PIN non connesso dal separatore AVI. Se si effettua questa chiamata prima dell'altra, è possibile connettere il flusso video al Mux di AVI, senza compressore video. Pertanto, la chiamata più specifica (con il filtro di compressione) deve essere eseguita per prima.

Nella discussione precedente si presuppone che il file di origine sia un file AVI. Tuttavia, questa tecnica funziona anche con altri tipi di file, ad esempio file MPEG. Il grafico di filtro risultante sarà leggermente diverso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricompressione di un file AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 



