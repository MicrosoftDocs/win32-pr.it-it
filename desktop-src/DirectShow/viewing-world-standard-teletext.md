---
description: Visualizzazione del televideo standard internazionale
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Visualizzazione del televideo standard internazionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b0885c08403de9578a8dee1eca6e000408ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344376"
---
# <a name="viewing-world-standard-teletext"></a>Visualizzazione del televideo standard internazionale

> [!Note]  
> Questa funzionalità è stata rimossa da Windows Vista e dai sistemi operativi successivi. È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.

 

Il televideo WST (World Standard Teletext) viene codificato nell'intervallo di spaziatura verticale (VBI) del segnale della televisione analogo. Il grafico filtro per la visualizzazione in anteprima del televideo è simile al grafico usato per visualizzare le didascalie chiuse. Il diagramma seguente illustra il grafico.

![grafico di anteprima WST](images/vidcap10.png)

Questo grafico usa i filtri seguenti per la visualizzazione WST:

-   [Convertitore da tee a sink a sink](tee-sink-to-sink-converter.md). Accetta le informazioni VBI dal filtro di acquisizione e le suddivide in flussi distinti per ognuno dei servizi dati presenti sul segnale.
-   [Codec WST](wst-codec-filter.md). Decodifica i dati del televideo dagli esempi di VBI.
-   [Decodificatore WST](wst-decoder-filter.md). Converte i dati del televideo e disegna il testo sulle bitmap. Il filtro downstream (in questo caso il mixer overlay) sovrappone le bitmap nel video.

Il metodo **RenderStream** del generatore di grafici di acquisizione non supporta direttamente i filtri WST, quindi l'applicazione deve eseguire alcune operazioni aggiuntive.

1.  Aggiungere il filtro del mixer sovrapposto al grafico del filtro. Il codice seguente usa la funzione AddFilterByCLSID descritta in [aggiungere un filtro in base a CLSID](add-a-filter-by-clsid.md). (AddFilterByCLSID non è un'API DirectShow).
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  Connettere il pin di anteprima al filtro renderer video tramite il mixer overlay. È possibile usare il metodo **RenderStream** , come indicato di seguito:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  Aggiungere il filtro del convertitore Tee/Sink-to-sink al grafico dei filtri. Il codice seguente usa la funzione CreateKernelFilter descritta in [creazione di filtri Kernel-Mode](creating-kernel-mode-filters.md). (CreateKernelFilter non è un'API DirectShow).
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  Aggiungere il filtro del codec WST al grafico del filtro:
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  Chiamare **RenderStream** per connettere il pin VBI del filtro di acquisizione al convertitore Tee/Sink-to-sink e il convertitore Tee/Sink-to-sink al filtro per il codec WST:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  Chiamare nuovamente **RenderStream** per connettere il filtro del codec WST al mixer della sovrimpressione. Il filtro del decodificatore WST viene automaticamente inserito nel grafico.
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  Ricordarsi di rilasciare tutte le interfacce del filtro.
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> Attualmente, il filtro decodificatore WST non supporta le connessioni al filtro VMR (video Mixing Renderer). Pertanto, è necessario utilizzare il filtro renderer video legacy per visualizzare il televideo.

 

Se il filtro di acquisizione ha una porta video VBI pin (PIN \_ CATEGPORY \_ VIDEOPORT \_ VBI), connetterlo al filtro [VBI Surface allocator](vbi-surface-allocator.md) . Il grafico non viene eseguito correttamente in caso contrario. Nell'esempio di codice seguente viene usata la funzione AddFilterByCLSID, descritta in [aggiungere un filtro in base al CLSID](add-a-filter-by-clsid.md)e la funzione FindPinByCategory, descritta in [uso delle categorie di pin](working-with-pin-categories.md). (Nessuna delle due funzioni è un'API DirectShow).


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Didascalie e televideo chiusi](closed-captions-and-teletext.md)
</dt> </dl>

 

 



