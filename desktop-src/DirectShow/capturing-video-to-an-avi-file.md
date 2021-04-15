---
description: Acquisizione di video in un file AVI
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Acquisizione di video in un file AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86504e9ce149f495e1ea31664f56382340d33887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569451"
---
# <a name="capturing-video-to-an-avi-file"></a>Acquisizione di video in un file AVI

La figura seguente mostra il grafico più semplice possibile per l'acquisizione di video in un file AVI.

![grafico di acquisizione video AVI](images/vidcap02.png)

Il filtro [Mux AVI](avi-mux-filter.md) accetta il flusso video dal pin di acquisizione e lo inserisce in un flusso AVI. Un flusso audio potrebbe anche essere connesso al filtro Mux AVI, nel qual caso il mux eseguirà l'interleave dei due flussi. Il filtro del [writer di file](file-writer-filter.md) scrive il flusso AVI su disco.

Per compilare il grafo, iniziare chiamando il metodo [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , come indicato di seguito:


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



Il primo parametro specifica il tipo di file, in questo caso AVI. Il secondo parametro assegna il nome del file. Per AVI, il metodo SetOutputFileName crea il filtro MUX per AVI e il filtro del writer di file e li aggiunge al grafico. Imposta anche il nome del file nel filtro del writer di file, chiamando il metodo [**IFileSinkFilter:: myFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) e connette i due filtri. Il metodo restituisce un puntatore al Mux AVI nel terzo parametro. Facoltativamente, restituisce un puntatore all'interfaccia [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) nel quarto parametro. Se questa interfaccia non è necessaria, è possibile impostare questo parametro su **null**, come illustrato nell'esempio precedente.

Chiamare quindi il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per connettere il filtro di acquisizione al Mux AVI, come indicato di seguito:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



Il primo parametro assegna la categoria pin, che è l' \_ acquisizione della categoria pin \_ per l'acquisizione. Il secondo parametro fornisce il tipo di supporto. Il terzo parametro è un puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro di acquisizione. Il quarto parametro è facoltativo. consente di instradare il flusso video tramite un filtro intermedio, ad esempio un codificatore, prima di passarlo al filtro MUX. In caso contrario, impostare questo parametro su **null**, come illustrato nell'esempio precedente. Il quinto parametro è il puntatore al filtro MUX. Questo puntatore viene ottenuto chiamando il metodo SetOutputFileName.

Per acquisire audio, chiamare RenderStream con il tipo di supporto MEDIATYPE \_ audio. Se si acquisisce audio e video da due dispositivi distinti, è consigliabile fare in modo che il flusso audio sia il flusso master. In questo modo è possibile evitare la deriva tra i due flussi, perché il filtro Mux AVI regola la velocità di riproduzione nel flusso video in modo che corrisponda al flusso audio. Per impostare il flusso Master, chiamare il metodo [**IConfigAviMux:: SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) sul filtro Mux AVI:


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



Il parametro per SetMasterStream è il numero del flusso, determinato dall'ordine in cui viene chiamato RenderStream. Ad esempio, se si chiama prima RenderStream per il video e quindi per l'audio, il video è Stream 0 e l'audio è Stream 1.

È anche possibile impostare il modo in cui il filtro Mux AVI interleaves i flussi audio e video chiamando il metodo [**IConfigInterleaving::p UT \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) .


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



Con il flag di acquisizione interleave \_ , il mux di AVI esegue l'interfoliazione a una velocità adatta per l'acquisizione video. È anche possibile usare l'interleave \_ None, che significa nessuna interfoliazione: il mux di AVI scriverà semplicemente i dati nell'ordine in cui arrivano. Il \_ flag di interfoliazione completo significa che il mux di AVI esegue l'interfoliazione completo. Tuttavia, questa modalità è meno adatta per l'acquisizione video perché richiede il più overheard.

Codifica del flusso video

È possibile codificare il flusso video inserendo un filtro del codificatore tra il filtro di acquisizione e il filtro Mux AVI. Usare l' [enumeratore del dispositivo di sistema](system-device-enumerator.md) o il [mapper del filtro](filter-mapper.md) per selezionare un filtro del codificatore. Per ulteriori informazioni, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md).

Specificare il filtro del codificatore come quarto parametro per RenderStream, illustrato in grassetto nell'esempio seguente:


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



Il filtro del codificatore potrebbe supportare [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) o altre interfacce per l'impostazione dei parametri di codifica. Per un elenco delle interfacce possibili, vedere [codifica e decodifica di file](file-encoding-and-decoding-interfaces.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di video in un file](capturing-video-to-a-file.md)
</dt> </dl>

 

 



