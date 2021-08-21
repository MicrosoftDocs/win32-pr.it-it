---
description: Visualizzazione del teletesto standard mondiale
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Visualizzazione del teletesto standard mondiale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2129538d91a7ac48fea26fd5f1987473896760c164fb3e2b1d4a2b1d142a1f04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078547"
---
# <a name="viewing-world-standard-teletext"></a>Visualizzazione del teletesto standard mondiale

> [!Note]  
> Questa funzionalità è stata rimossa da Windows Vista e sistemi operativi successivi. È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.

 

La codifica WST (World Standard Teletext) viene codificata nell'intervallo di blanking verticale (VBI) del segnale tv analogico. Il grafico dei filtri per l'anteprima del teletesto è simile al grafico usato per visualizzare i sottotitoli codificati. Il diagramma seguente illustra questo grafico.

![wst preview graph](images/vidcap10.png)

Questo grafico usa i filtri seguenti per la visualizzazione WST:

-   [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md). Accetta le informazioni VBI dal filtro di acquisizione e le suddivide in flussi separati per ognuno dei servizi dati presenti nel segnale.
-   [Codec WST](wst-codec-filter.md). Decodifica i dati Teletext degli esempi VBI.
-   [Decodificatore WST.](wst-decoder-filter.md) Converte i dati teletext e disegna il testo su bitmap. Il filtro downstream (in questo caso il filtro Overlay Mixer) sovrappone le bitmap al video.

Il metodo **RenderStream** di Capture Graph Builder non supporta direttamente i filtri WST, quindi l'applicazione deve eseguire alcune operazioni aggiuntive.

1.  Aggiungere il filtro Mixer sovrimpressione al grafico dei filtri. Il codice seguente usa la funzione AddFilterByCLSID descritta in [Aggiungere un filtro in base a CLSID.](add-a-filter-by-clsid.md) AddFilterByCLSID non è un'API DirectShow personalizzata.
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  Connessione il segnaposto dell'anteprima al filtro Renderer video tramite il filtro Overlay Mixer. È possibile usare il **metodo RenderStream,** come indicato di seguito:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  Aggiungere il filtro Tee/Sink-to-Sink Converter al grafico dei filtri. Il codice seguente usa la funzione CreateKernelFilter descritta in [Creazione di Kernel-Mode filtri .](creating-kernel-mode-filters.md) CreateKernelFilter non è un'API DirectShow.
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  Aggiungere il filtro codec WST al grafico dei filtri:
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  Chiamare **RenderStream** per connettere il pin VBI del filtro di acquisizione al convertitore Tee/Sink-to-Sink e il convertitore Tee/Sink-to-Sink al filtro codec WST:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  Chiamare **di nuovo RenderStream** per connettere il filtro codec WST al filtro overlay Mixer. Il filtro WST Decoder viene inserito automaticamente nel grafico.
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  Ricordarsi di rilasciare tutte le interfacce di filtro.
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> Attualmente, il filtro WST Decoder non supporta le connessioni al filtro VMR (Video Mixing Renderer). Pertanto, è necessario usare il filtro del renderer video legacy per visualizzare il teletesto.

 

Se il filtro di acquisizione ha un pin VBI della porta video (PIN \_ CATEGPORY \_ VIDEOPORT VBI), connetterlo al filtro \_ [VBI Surface Allocator.](vbi-surface-allocator.md) In caso contrario, il grafico non verrà eseguito correttamente. L'esempio di codice seguente usa la funzione AddFilterByCLSID, descritta in Aggiungere un filtro in base [a CLSID,](add-a-filter-by-clsid.md)e la funzione FindPinByCategory, descritta [in](working-with-pin-categories.md)Utilizzo delle categorie di pin. Nessuna delle due funzioni è un DirectShow API.


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

[Sottotitoli codificati e teletesto](closed-captions-and-teletext.md)
</dt> </dl>

 

 



