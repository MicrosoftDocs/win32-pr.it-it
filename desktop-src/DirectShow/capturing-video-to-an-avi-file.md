---
description: Acquisizione di video in un file AVI
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Acquisizione di video in un file AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5ec58c021c5f37fed992959b33965efddb5603798ff756909879d307bca1f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689037"
---
# <a name="capturing-video-to-an-avi-file"></a>Acquisizione di video in un file AVI

La figura seguente mostra il grafico più semplice possibile per l'acquisizione di video in un file AVI.

![Grafico di acquisizione video avi](images/vidcap02.png)

Il [filtro AVI Mux](avi-mux-filter.md) acquisisce il flusso video dal pin di acquisizione e lo insere in un flusso AVI. Un flusso audio potrebbe anche essere connesso al filtro Mux AVI, nel qual caso il mux interleaverebbe i due flussi. Il [filtro writer di](file-writer-filter.md) file scrive il flusso AVI su disco.

Per compilare il grafico, iniziare chiamando il [**metodo ICaptureGraphBuilder2::SetOutputFileName,**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) come indicato di seguito:


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



Il primo parametro specifica il tipo di file, in questo caso AVI. Il secondo parametro fornisce il nome del file. Per AVI, il metodo SetOutputFileName crea insieme il filtro Mux AVI e il filtro Writer file e li aggiunge al grafo. Imposta anche il nome del file nel filtro writer di file, chiamando il metodo [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) e connette i due filtri. Il metodo restituisce un puntatore al mux AVI nel terzo parametro. Facoltativamente, restituisce un puntatore [**all'interfaccia IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) nel quarto parametro. Se questa interfaccia non è necessaria, è possibile impostare questo parametro su **NULL,** come illustrato nell'esempio precedente.

Chiamare quindi il [**metodo ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per connettere il filtro di acquisizione al mux AVI, come indicato di seguito:


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



Il primo parametro fornisce la categoria pin, ovvero PIN \_ CATEGORY \_ CAPTURE per l'acquisizione. Il secondo parametro fornisce il tipo di supporto. Il terzo parametro è un puntatore all'interfaccia [**IBaseFilter del**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) filtro di acquisizione. Il quarto parametro è facoltativo. consente di instradare il flusso video tramite un filtro intermedio, ad esempio un codificatore, prima di passarlo al filtro mux. In caso contrario, impostare questo parametro **su NULL,** come illustrato nell'esempio precedente. Il quinto parametro è il puntatore al filtro mux. Questo puntatore viene ottenuto chiamando il metodo SetOutputFileName.

Per acquisire l'audio, chiamare RenderStream con il tipo di supporto MEDIATYPE \_ Audio. Se si acquisisce audio e video da due dispositivi separati, è buona idea impostare il flusso audio come flusso master. Ciò consente di evitare la deriva tra i due flussi, perché il filtro Mux AVI regola la velocità di riproduzione nel flusso video in modo che corrisponda al flusso audio. Per impostare il flusso master, chiamare il [**metodo IConfigAviMux::SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) sul filtro Mux AVI:


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



Il parametro per SetMasterStream è il numero di flusso, determinato dall'ordine in cui si chiama RenderStream. Ad esempio, se si chiama RenderStream prima per il video e quindi per l'audio, il video è il flusso 0 e l'audio è il flusso 1.

È anche possibile impostare il modo in cui il filtro Mux AVI interfolia i flussi audio e video chiamando il metodo [**IConfigInterleaving::p ut \_ Mode.**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode)


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



Con il flag INTERLEAVE CAPTURE, AVI Mux esegue l'interfoliazione a una velocità adatta \_ per l'acquisizione video. È anche possibile usare INTERLEAVE NONE, ovvero nessuna \_ interfoliazione. AVI Mux scriverà semplicemente i dati nell'ordine in cui arrivano. Il flag INTERLEAVE FULL indica che \_ AVI Mux esegue l'interfoliazione completa. Tuttavia, questa modalità è meno adatta per l'acquisizione video perché richiede il più sentito.

Codifica del flusso video

È possibile codificare il flusso video inserendo un filtro del codificatore tra il filtro di acquisizione e il filtro Mux AVI. Usare [l'enumeratore del dispositivo di sistema](system-device-enumerator.md) o filter [mapper](filter-mapper.md) per selezionare un filtro del codificatore. Per altre informazioni, vedere [Enumerazione di dispositivi e filtri.](enumerating-devices-and-filters.md)

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



Il filtro del codificatore potrebbe [**supportare IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) o altre interfacce per l'impostazione dei parametri di codifica. Per un elenco delle possibili interfacce, vedere [Codifica file e decodifica di interfacce](file-encoding-and-decoding-interfaces.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di video in un file](capturing-video-to-a-file.md)
</dt> </dl>

 

 



