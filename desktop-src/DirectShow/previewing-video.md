---
description: Questo esempio compila un grafico di anteprima video usando il metodo ICaptureGraphBuilder2::RenderStream in DirectShow.
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Anteprima di video (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482fed2e164bbe867d848b05d417c89d0790256f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406894"
---
# <a name="previewing-video-directshow"></a>Anteprima di video (DirectShow)

Per compilare un grafico di anteprima video, chiamare il [**metodo ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) come segue:


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



Questo esempio presuppone quanto segue:

-   *pBuild* è stato inizializzato, come descritto in [Informazioni su Capture Graph Builder](about-the-capture-graph-builder.md).
-   *pCap* è stato inizializzato creando un'istanza del filtro di acquisizione e aggiungendola al grafico dei filtri, come descritto in [Selezione di un dispositivo di acquisizione](selecting-a-capture-device.md).

Il primo parametro del [**metodo ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) specifica una categoria di pin. per un grafico di anteprima, usare **PIN \_ CATEGORY \_ PREVIEW**. Il secondo parametro specifica un tipo di supporto, come GUID di tipo principale. Per il video, usare **MEDIATYPE \_ Video**. I dispositivi DV offrono audio e video interleaved, per i quali il tipo di supporto **è MEDIATYPE \_ Interleaved.** Per altre informazioni sull'acquisizione DV, vedere [Video digitale in DirectShow.](digital-video-in-directshow.md)

Il terzo parametro è un puntatore all'interfaccia [**IBaseFilter del**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) filtro di acquisizione. I due parametri successivi non sono necessari in questo esempio. Vengono usati per specificare filtri aggiuntivi che potrebbero essere necessari per eseguire il rendering del flusso. Impostando l'ultimo parametro **su NULL,** Capture Graph Builder seleziona un renderer predefinito per il flusso, in base al tipo di supporto. Per i video, Capture Graph Builder usa sempre il filtro [Renderer video](video-renderer-filter.md) come renderer predefinito.

> [!Note]  
> In Windows XP e versioni successive, sebbene video mixing renderer (VMR) sia il renderer video predefinito per i metodi [**IGraphBuilder,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) non è il renderer predefinito per il [**metodo RenderStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) In qualsiasi piattaforma, Capture Graph Builder usa sempre il filtro renderer video precedente, a meno che non venga specificato diversamente.

 

Anche se la categoria pin viene specificata come **PIN \_ CATEGORY \_ PREVIEW,** non è importante se il filtro dispone effettivamente di un pin di anteprima; potrebbe avere un pin della porta video o solo un pin di acquisizione. In entrambi i casi, Capture Graph Builder compila automaticamente il grafico corretto.

Il diagramma seguente illustra il grafico più semplice possibile per l'anteprima del video.

![Grafico di anteprima video](images/vidcap01.png)

In questo diagramma il filtro di acquisizione ha un segnaposto di anteprima che si connette direttamente al renderer video.

Se il filtro di acquisizione ha solo un pin di acquisizione, Capture Graph Builder inserisce un filtro [Smart Tee,](smart-tee-filter.md) che suddivide il flusso in un flusso di acquisizione e in un flusso di anteprima. Questa operazione è descritta in modo più dettagliato in [Combinazione di acquisizione video e anteprima.](combining-video-capture-and-preview.md)

In alcuni casi, il flusso video deve passare attraverso il filtro Overlay Mixer. In tal caso, [**il metodo RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) lo aggiunge automaticamente al grafico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Combinazione di acquisizione video e anteprima](combining-video-capture-and-preview.md)
</dt> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



