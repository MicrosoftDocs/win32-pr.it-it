---
description: Questo esempio crea un grafo di anteprima video usando il metodo ICaptureGraphBuilder2::RenderStream in DirectShow.
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Anteprima di video (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92a6fd3f34a6b2678f41f95a80caca64e47adcc62cbeb6c37f2ed7b71f8d947
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748287"
---
# <a name="previewing-video-directshow"></a>Anteprima di video (DirectShow)

Per compilare un grafo di anteprima video, chiamare il [**metodo ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) come indicato di seguito:


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



In questo esempio si presuppone quanto segue:

-   *pBuild* è stato inizializzato, come descritto in [About the Capture Graph Builder](about-the-capture-graph-builder.md).
-   *pCap* è stato inizializzato creando un'istanza del filtro di acquisizione e aggiungendola al grafico dei filtri, come descritto in [Selezione di un dispositivo di acquisizione.](selecting-a-capture-device.md)

Il primo parametro per il [**metodo ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) specifica una categoria di puntine; Per un grafico di anteprima, usare **PIN \_ CATEGORY \_ PREVIEW**. Il secondo parametro specifica un tipo di supporto, come GUID di tipo principale. Per i video, usare **MEDIATYPE \_ Video.** I dispositivi DV forniscono audio e video interleaved, per i quali il tipo di supporto **è MEDIATYPE \_ Interleaved.** Per altre informazioni sull'acquisizione DV, vedere [Video digitale in DirectShow.](digital-video-in-directshow.md)

Il terzo parametro è un puntatore all'interfaccia [**IBaseFilter del filtro**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) di acquisizione. I due parametri successivi non sono necessari in questo esempio. Vengono usati per specificare filtri aggiuntivi che potrebbero essere necessari per eseguire il rendering del flusso. Se si imposta l'ultimo parametro su **NULL,** Capture Graph Builder seleziona un renderer predefinito per il flusso, in base al tipo di supporto. Per i video, Capture Graph Builder usa sempre il filtro [Renderer video](video-renderer-filter.md) come renderer predefinito.

> [!Note]  
> In Windows XP e versioni successive, anche se il renderer di combinazione video (VMR) è il renderer video predefinito per i metodi [**IGraphBuilder,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) non è il renderer predefinito per il metodo [**RenderStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) In qualsiasi piattaforma, Capture Graph Builder usa sempre il filtro del renderer video precedente, se non diversamente specificato.

 

Anche se la categoria pin viene specificata come **PIN \_ CATEGORY \_ PREVIEW**, non è importante se il filtro ha effettivamente un pin di anteprima, ma potrebbe avere un pin della porta video o solo un pin di acquisizione. In entrambi i casi, Capture Graph Builder compila automaticamente il grafico corretto.

Il diagramma seguente mostra il grafico più semplice possibile per la visualizzazione in anteprima dei video.

![Grafico dell'anteprima video](images/vidcap01.png)

In questo diagramma il filtro di acquisizione ha un pin di anteprima, che si connette direttamente al renderer video.

Se il filtro di acquisizione ha solo un pin di acquisizione, Capture Graph Builder inserisce un filtro [Smart Tee,](smart-tee-filter.md) che suddivide il flusso in un flusso di acquisizione e un flusso di anteprima. Questa operazione è descritta in modo più dettagliato in [Combinazione di Acquisizione video e Anteprima.](combining-video-capture-and-preview.md)

In alcuni casi, il flusso video deve passare attraverso il filtro di Mixer sovrimpressione. In tal caso, [**il metodo RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) lo aggiunge automaticamente al grafico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Combinazione di acquisizione video e anteprima](combining-video-capture-and-preview.md)
</dt> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



