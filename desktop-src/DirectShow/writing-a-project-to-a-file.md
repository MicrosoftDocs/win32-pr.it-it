---
description: Scrittura di un progetto in un file
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: Scrittura di un progetto in un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f63ddbc6a021362134d420220f7e25c662553f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313391"
---
# <a name="writing-a-project-to-a-file"></a>Scrittura di un progetto in un file

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Questo articolo descrive come scrivere un progetto di [servizi di modifica DirectShow](directshow-editing-services.md) in un file. In primo luogo viene descritto come scrivere un file con il motore di rendering di base. Viene quindi descritta la ricompressione intelligente con il motore di rendering intelligente.

Per una panoramica su come i servizi di modifica DirectShow eseguono il rendering dei progetti, vedere [informazioni sui motori di rendering](about-the-render-engines.md).

**Uso del motore di rendering di base**

Iniziare compilando il front-end del grafo, come indicato di seguito:

1.  Creare il motore di rendering.
2.  Specificare la sequenza temporale.
3.  Impostare l'intervallo di rendering. Facoltativa
4.  Compilare il front-end del grafo.

Nell'esempio di codice seguente vengono illustrati questi passaggi.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



Aggiungere quindi i filtri multiplexer e di scrittura file al grafico filtro. Il modo più semplice per eseguire questa operazione è il [Generatore Graph di acquisizione](capture-graph-builder.md), un componente DirectShow per la creazione di grafici di acquisizione. Il generatore di grafici di acquisizione espone l'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . Eseguire la procedura seguente:

1.  Creare un'istanza del generatore di grafici di acquisizione.
2.  Ottenere un puntatore al grafo e passarlo al generatore di grafici.
3.  Specificare il nome e il tipo di supporto del file di output. Questo passaggio ottiene anche un puntatore al filtro Mux, che è necessario in un secondo momento.

Nell'esempio di codice seguente vengono illustrati questi passaggi.


```C++
CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, CLSCTX_INPROC, 
    IID_ICaptureGraphBuilder2, (void **)&pBuilder);

// Get a pointer to the graph front end.
IGraphBuilder *pGraph;
pRender->GetFilterGraph(&pGraph);
pBuilder->SetFiltergraph(pGraph);

// Create the file-writing section.
IBaseFilter *pMux;
pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("Output.avi"), &pMux, NULL);
```



Infine, connettere i pin di output sul front-end al filtro MUX.

1.  Recuperare il numero di gruppi.
2.  Per ogni pin, ottenere un puntatore al pin.
3.  Facoltativamente, creare un'istanza di un filtro di compressione per comprimere il flusso. Il tipo di compressore dipenderà dal tipo di supporto del gruppo. È possibile utilizzare l' [enumeratore System Device](system-device-enumerator.md) per enumerare i filtri di compressione disponibili. Per altre informazioni, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md).
4.  Facoltativamente, impostare parametri di compressione, ad esempio la frequenza dei fotogrammi chiave. Questo passaggio è descritto in dettaglio più avanti in questo articolo.
5.  Chiamare [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream). Questo metodo accetta puntatori al pin, al filtro di compressione (se presente) e al multiplexer.

Nell'esempio di codice seguente viene illustrato come connettere i pin di output.


```C++
long NumGroups;
pTimeline->GetGroupCount(&NumGroups);

// Loop through the groups and get the output pins.
for (i = 0; i < NumGroups; i++)
{
    IPin *pPin;
    if (pRender->GetGroupOutputPin(i, &pPin) == S_OK) 
    {
        IBaseFilter *pCompressor;
        // Create a compressor filter. (Not shown.)
        // Set compression parameters. (Not shown.)

        // Connect the pin.
        pBuilder->RenderStream(NULL, NULL, pPin, pCompressor, pMux);
        pCompressor->Release();
        pPin->Release();
    }
}
```



Per impostare i parametri di compressione (passaggio 4, in precedenza), usare l'interfaccia [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) . Questa interfaccia viene esposta nei pin di output dei filtri di compressione. Enumerare i pin del filtro di compressione ed eseguire una query su ogni pin di output per **IAMVideoCompression**. Per informazioni sull'enumerazione dei pin, vedere [enumerazione dei pin](enumerating-pins.md). Assicurarsi di rilasciare tutti i puntatori di interfaccia ottenuti durante questo passaggio.

Dopo aver compilato il grafico del filtro, chiamare il metodo [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) in gestione grafico dei filtri. Durante l'esecuzione del grafico di filtro, i dati vengono scritti in un file. Usare la notifica degli eventi per attendere il completamento della riproduzione. (Vedere [rispondere agli eventi](responding-to-events.md)). Al termine della riproduzione, è necessario chiamare in modo esplicito [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) per arrestare il grafico del filtro. In caso contrario, il file non viene scritto correttamente.

**Uso del motore di rendering intelligente**

Per ottenere i vantaggi della ricompressione intelligente, usare il motore di rendering intelligente al posto del motore di rendering di base. I passaggi per la compilazione del grafo sono quasi identici. La differenza principale consiste nel fatto che la compressione viene gestita nel front-end del grafo, non nella sezione relativa alla scrittura di file.

> [!IMPORTANT]
> Non usare il motore di rendering intelligente per leggere o scrivere file di Windows Media.

 

Ogni gruppo di video dispone di una proprietà che specifica il formato di compressione per il gruppo. Il formato di compressione deve corrispondere esattamente al formato non compresso del gruppo in altezza, larghezza, profondità dei bit e frequenza dei fotogrammi. Il motore di rendering intelligente utilizza il formato di compressione quando costruisce il grafo. Prima di impostare il formato di compressione, assicurarsi di impostare il formato non compresso per il gruppo chiamando [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md).

Per impostare il formato di compressione di un gruppo, chiamare il metodo [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) . Questo metodo accetta un puntatore a una struttura [**SCompFmt0**](scompfmt0.md) . La struttura **SCompFmt0** ha due membri: **nFormatId**, che deve essere zero e **mediaType**, ovvero una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Inizializzare la struttura del **\_ \_ tipo di supporto am** con le informazioni sul formato.

> [!Note]  
> Se si vuole che il progetto finale abbia lo stesso formato di uno dei file di origine, è possibile ottenere la \_ struttura del tipo di supporto am \_ direttamente dal file di origine, usando il rilevatore di contenuti multimediali. Vedere [**IMediaDet:: Get \_ StreamMediaType**](imediadet-get-streammediatype.md).

 

Eseguire il cast della variabile [**SCompFmt0**](scompfmt0.md) a un puntatore di tipo **Long**, come illustrato nell'esempio seguente.


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



Il motore di rendering intelligente cerca automaticamente un filtro di compressione compatibile. È anche possibile specificare un filtro di compressione per un gruppo chiamando [**ISmartRenderEngine:: SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).

Per compilare il grafo, usare la stessa procedura descritta per il motore di rendering di base nella sezione precedente. Le uniche differenze sono le seguenti:

-   Usare il motore di rendering intelligente, non il motore di rendering di base. L'identificatore di classe è CLSID \_ SmartRenderEngine.
-   Impostare i parametri di compressione dopo aver compilato il front-end, ma prima di eseguire il rendering dei pin di output. Chiamare il metodo [**ISmartRenderEngine:: GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) per ottenere un puntatore al filtro di compressione di un gruppo. Quindi eseguire una query per l'interfaccia [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , come descritto in precedenza.
-   Quando si esegue il rendering dei pin di output, non è necessario inserire un filtro di compressione. Il flusso è già compresso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un progetto](rendering-a-project.md)
</dt> </dl>

 

 



