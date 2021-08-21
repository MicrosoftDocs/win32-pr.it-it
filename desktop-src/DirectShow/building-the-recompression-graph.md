---
description: Compilazione del Graph
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Compilazione del Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0432f51e5309a308b32535993fef04da1762d45f179e1ab3a6826d4c5432b02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159118"
---
# <a name="building-the-recompression-graph"></a>Compilazione del Graph

Un grafico di filtro tipico per la ricompressione di file AVI è simile al seguente:

![avi recompression graph](images/avi2avi4.png)

Il [filtro AVI Splitter esegue](avi-splitter-filter.md) il pull dei dati dal filtro di origine file [(Async)](file-source--async--filter.md) e analizza i dati in flussi video e audio. Il decompressore video decodifica il video compresso, in cui viene compresso nuovamente dal video. La scelta dei decompressori dipende dal file di origine. verrà gestito automaticamente da [Intelligent Connessione](intelligent-connect.md). L'applicazione deve scegliere il tutto, in genere presentando un elenco all'utente. Vedere [Scelta di un filtro di compressione.](choosing-a-compression-filter.md)

Il video compresso passa quindi al filtro [Mux AVI.](avi-mux-filter.md) Il flusso audio in questo esempio non è compresso, quindi passa direttamente dallo splitter AVI al mux AVI. Il mux AVI interfolia i due flussi e il filtro writer di [file](file-writer-filter.md) scrive l'output su disco. Si noti che il mux AVI è necessario anche se il file originale non ha un flusso audio.

Il modo più semplice per creare questo grafo dei filtri è usare [Capture Graph Builder,](capture-graph-builder.md)un componente di DirectShow per la creazione di grafici di acquisizione e altri grafici di filtro personalizzati.

Per iniziare, chiamare CoCreateInstance per creare il generatore di Graph capture:


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



Usare quindi Capture Graph Builder per compilare il grafico dei filtri:

1.  Compilare la sezione di rendering del grafo, che include il filtro Mux AVI e il [writer di file](file-writer-filter.md).
2.  Aggiungere il filtro di origine e il filtro di compressione al grafico.
3.  Connessione filtro di origine al filtro MUX. Il generatore di grafi di acquisizione inserisce i filtri della barra di divisione e del decodificatore necessari per analizzare il file di origine. Può anche instradare i flussi video e audio tramite filtri di compressione.

Le sezioni seguenti illustrano ognuno di questi passaggi.

Compilare la sezione rendering

Per compilare la sezione di rendering del grafo, chiamare il [**metodo ICaptureGraphBuilder2::SetOutputFileName.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) Questo metodo accetta parametri di input che specificano il sottotipo multimediale per l'output e il nome del file di output. Restituisce puntatori al filtro MUX e al writer di file. Il filtro MUX è necessario per la fase successiva della creazione del grafo. Il puntatore al writer di file non è necessario per questo esempio, quindi il parametro può essere **NULL:**


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



Quando il metodo viene restituito, il filtro MUX ha un conteggio dei riferimenti in sospeso, quindi assicurarsi di rilasciare il puntatore in un secondo momento.

Il diagramma seguente mostra il grafico dei filtri a questo punto.

![sezione di rendering del grafico dei filtri](images/avi2avi1.png)

Il filtro MUX espone due interfacce per il controllo del formato AVI:

-   [**Interfaccia IConfigInterleaving:**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)imposta la modalità di interfoliazione.
-   [**Interfaccia IConfigAviMux:**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)imposta il flusso master e l'indice di compatibilità AVI.

Aggiungere i filtri di origine e di compressione

Il passaggio successivo consiste nell'aggiungere i filtri di origine e di compressione al grafico dei filtri. Capture Graph Builder crea automaticamente un'istanza di Filter Graph Manager quando si chiama SetOutputFileName. Ottenere un puntatore chiamando il [**metodo ICaptureGraphBuilder2::GetFiltergraph:**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph)


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



Chiamare ora [**il metodo IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) per aggiungere il filtro Origine file asincrona e il metodo [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il video:


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



A questo punto, il filtro di origine e il filtro di compressione non sono connessi ad altri elementi del grafico, come illustrato nella figura seguente:

![Grafico dei filtri con filtri di origine e compressione](images/avi2avi2.png)

Connessione l'origine al mux

Il passaggio finale consiste nel connettere il filtro di origine al filtro Mux AVI, tramite il video. Usare il [**metodo ICaptureGraphBuilder2::RenderStream,**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) che connette un pin di output nel filtro di origine a un filtro sink specificato, facoltativamente tramite un filtro di compressione.

I primi due parametri specificano quali pin del filtro di origine connettere, designando una categoria di pin e un tipo di supporto. Il filtro Origine file asincrona ha un solo pin di output, quindi questi parametri devono essere **NULL.** I tre parametri successivi specificano il filtro di origine, il filtro di compressione (se presente) e il filtro Mux.

L'esempio di codice seguente esegue il rendering del flusso video attraverso il video:


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



Il diagramma seguente illustra il grafico dei filtri fino a questo momento.

![flusso video di cui è stato eseguito il rendering](images/avi2avi3.png)

Supponendo che il file di origine abbia un flusso audio, il filtro [AVI Splitter](avi-splitter-filter.md) ha creato un pin di output per l'audio. Per connettere questo pin, chiamare di nuovo RenderStream:


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



In questo caso, non viene specificato alcun filtro di compressione. Il pin di output del filtro di origine è già connesso, quindi il metodo RenderStream cerca un pin di output non connesso nel filtro della barra di divisione. Trova il pin audio e lo connette direttamente al filtro MUX. Se il file di origine non ha un flusso audio, la seconda chiamata a RenderStream avrà esito negativo. Si tratta di un comportamento previsto. Il grafico viene completato dopo la prima chiamata a RenderStream, quindi l'errore nella seconda chiamata è innocuo.

In questo esempio, l'ordine delle due chiamate RenderStream è importante. Poiché la seconda chiamata non specifica un oggetto , connetterà qualsiasi pin non connesso dalla barra di divisione AVI. Se si effettua questa chiamata prima dell'altra, il flusso video potrebbe connettersi al mux AVI, senza il video. Pertanto, la chiamata più specifica (con il filtro di compressione) deve avvenire per prima.

Nella discussione precedente si presuppone che il file di origine sia un file AVI. Tuttavia, questa tecnica funziona anche con altri tipi di file, ad esempio i file MPEG. Il grafico dei filtri risultante sarà leggermente diverso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricompressione di un file AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 



