---
description: Scrittura di Project in un file
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: Scrittura di Project in un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efea1d0949c419ba6f595e7a381b689d8a8ce69836609d328b555ee695743b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051371"
---
# <a name="writing-a-project-to-a-file"></a>Scrittura di Project in un file

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Questo articolo descrive come scrivere un progetto DirectShow [di Servizi di modifica](directshow-editing-services.md) in un file. Prima di tutto descrive come scrivere un file con il motore di rendering di base. Descrive quindi la ricompressione intelligente con il motore di rendering intelligente.

Per una panoramica del rendering DirectShow Servizi di modifica, vedere [Informazioni sui motori di rendering](about-the-render-engines.md).

**Uso del motore di rendering di base**

Per iniziare, compilare il front-end del grafo, come indicato di seguito:

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



Aggiungere quindi filtri multiplexer e di scrittura di file al grafico dei filtri. Il modo più semplice per eseguire questa operazione è con [Capture Graph Builder,](capture-graph-builder.md)un componente DirectShow per la compilazione di grafici di acquisizione. Il generatore di grafi di acquisizione espone [**l'interfaccia ICaptureGraphBuilder2.**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) Eseguire la procedura seguente:

1.  Creare un'istanza del generatore di grafi di acquisizione.
2.  Ottenere un puntatore al grafo e passarlo al generatore di grafi.
3.  Specificare il nome e il tipo di supporto del file di output. Questo passaggio ottiene anche un puntatore al filtro mux, che sarà necessario in un secondo momento.

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



Infine, connettere i pin di output sul front-end al filtro mux.

1.  Recuperare il numero di gruppi.
2.  Per ogni pin, ottenere un puntatore al pin.
3.  Facoltativamente, creare un'istanza di un filtro di compressione per comprimere il flusso. Il tipo di compressione dipende dal tipo di supporto del gruppo. È possibile usare [l'enumeratore del dispositivo di sistema](system-device-enumerator.md) per enumerare i filtri di compressione disponibili. Per altre informazioni, vedere [Enumerazione di dispositivi e filtri.](enumerating-devices-and-filters.md)
4.  Facoltativamente, impostare i parametri di compressione, ad esempio la frequenza dei fotogrammi chiave. Questo passaggio viene descritto in dettaglio più avanti nell'articolo.
5.  Chiamare [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream). Questo metodo accetta puntatori al pin, al filtro di compressione (se presente) e al multiplexer.

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



Per impostare i parametri di compressione (passaggio 4, in precedenza), usare [**l'interfaccia IAMVideoCompression.**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) Questa interfaccia viene esposta sui pin di output dei filtri di compressione. Enumerare i pin del filtro di compressione ed eseguire una query su ogni pin di output **per IAMVideoCompression**. Per informazioni sull'enumerazione dei pin, vedere [Enumerazione dei pin.](enumerating-pins.md) Assicurarsi di rilasciare tutti i puntatori a interfaccia ottenuti durante questo passaggio.

Dopo aver compilato il grafico dei filtri, chiamare il [**metodo IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) nel gestore del grafico filtri. Durante l'esecuzione del grafico dei filtri, i dati vengono scritti in un file. Usare la notifica degli eventi per attendere il completamento della riproduzione. Vedere [Risposta agli eventi](responding-to-events.md). Al termine della riproduzione, è necessario chiamare in modo [**esplicito IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) per arrestare il grafico dei filtri. In caso contrario, il file non viene scritto correttamente.

**Uso del motore di rendering intelligente**

Per ottenere i vantaggi della ricompressione intelligente, usare il motore di rendering intelligente al posto del motore di rendering di base. I passaggi per la compilazione del grafo sono quasi gli stessi. La differenza principale è che la compressione viene gestita nel front-end del grafico, non nella sezione di scrittura di file.

> [!IMPORTANT]
> Non usare il motore di rendering intelligente per leggere o scrivere Windows file multimediali.

 

Ogni gruppo di video ha una proprietà che specifica il formato di compressione per tale gruppo. Il formato di compressione deve corrispondere esattamente al formato non compresso del gruppo in altezza, larghezza, profondità in bit e frequenza dei fotogrammi. Il motore di rendering intelligente usa il formato di compressione quando costruisce il grafico. Prima di impostare il formato di compressione, assicurarsi di impostare il formato non compresso per il gruppo chiamando [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md).

Per impostare il formato di compressione di un gruppo, chiamare il [**metodo IAMTimelineGroup::SetSmartRecompressFormat.**](iamtimelinegroup-setsmartrecompressformat.md) Questo metodo accetta un puntatore a una [**struttura SCompFmt0.**](scompfmt0.md) La **struttura SCompFmt0** ha due membri: **nFormatId**, che deve essere zero, e **MediaType**, che è una [**struttura AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Inizializzare la **struttura AM \_ MEDIA \_ TYPE** con le informazioni sul formato.

> [!Note]  
> Se si vuole che il progetto finale abbia lo stesso formato di uno dei file di origine, è possibile ottenere la struttura AM MEDIA TYPE direttamente dal file di origine, usando il rilevatore \_ \_ multimediale. Vedere [**IMediaDet::get \_ StreamMediaType**](imediadet-get-streammediatype.md).

 

Eseguire il [**cast della variabile SCompFmt0**](scompfmt0.md) a un puntatore di tipo **long**, come illustrato nell'esempio seguente.


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



Il motore di rendering intelligente cerca automaticamente un filtro di compressione compatibile. È anche possibile specificare un filtro di compressione per un gruppo chiamando [**ISmartRenderEngine::SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).

Per compilare il grafico, usare gli stessi passaggi descritti per il motore di rendering di base nella sezione precedente. Le uniche differenze sono le seguenti:

-   Usare il motore di rendering intelligente, non il motore di rendering di base. L'identificatore di classe è CLSID \_ SmartRenderEngine.
-   Impostare i parametri di compressione dopo aver compilato il front-end, ma prima di eseguire il rendering dei pin di output. Chiamare il [**metodo ISmartRenderEngine::GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) per ottenere un puntatore al filtro di compressione di un gruppo. Eseguire quindi una query per [**l'interfaccia IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) come descritto in precedenza.
-   Quando si esegue il rendering dei pin di output, non è necessario inserire un filtro di compressione. Il flusso è già compresso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un Project](rendering-a-project.md)
</dt> </dl>

 

 



