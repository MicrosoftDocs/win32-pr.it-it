---
description: Anteprima del video
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Anteprima video (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0a8f0d0a422794c4e887693e80391a99bd8d70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559856"
---
# <a name="previewing-video-directshow"></a>Anteprima video (DirectShow)

Per creare un grafico di anteprima video, chiamare il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) come indicato di seguito:


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



In questo esempio si presuppone quanto segue:

-   *pBuild* è stato inizializzato, come descritto in [informazioni sul generatore di grafici di acquisizione](about-the-capture-graph-builder.md).
-   *pCap* è stato inizializzato creando un'istanza del filtro di acquisizione e aggiungendola al grafico di filtro, come descritto in [selezione di un dispositivo di acquisizione](selecting-a-capture-device.md).

Il primo parametro del metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) specifica una categoria pin. per un grafico di anteprima, usare l' **\_ \_ anteprima della categoria pin**. Il secondo parametro specifica un tipo di supporto, come un GUID di tipo principale. Per video, usare **il \_ video di MEDIATYPE**. I dispositivi DV forniscono audio e video con interfoliazione, per i quali il tipo di supporto è **\_ Interleaved MEDIATYPE**. Per ulteriori informazioni sull'acquisizione DV, vedere la pagina relativa ai [video digitali in DirectShow](digital-video-in-directshow.md).

Il terzo parametro è un puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro di acquisizione. In questo esempio i due parametri successivi non sono necessari. Vengono usati per specificare filtri aggiuntivi che potrebbero essere necessari per eseguire il rendering del flusso. Impostando l'ultimo parametro su **null** , il generatore del grafico di acquisizione seleziona un renderer predefinito per il flusso, in base al tipo di supporto. Per i video, il generatore di grafici di acquisizione usa sempre il filtro [renderer video](video-renderer-filter.md) come renderer predefinito.

> [!Note]  
> In Windows XP e versioni successive, anche se il renderer video mixing (VMR) è il renderer video predefinito per i metodi [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , non è il renderer predefinito per il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) . In qualsiasi piattaforma, il generatore di grafici di acquisizione usa sempre il vecchio filtro renderer video, a meno che non venga specificato diversamente.

 

Sebbene la categoria PIN venga fornita come **\_ \_ anteprima della categoria pin**, non è importante se il filtro ha effettivamente un pin di anteprima, ma potrebbe avere un PIN della porta video o semplicemente un pin di acquisizione. In entrambi i casi, il generatore di grafici di acquisizione compila automaticamente il grafo corretto.

Il diagramma seguente mostra il grafico più semplice possibile per la visualizzazione in anteprima dei video.

![grafico di anteprima video](images/vidcap01.png)

In questo diagramma, il filtro di acquisizione include un pin di anteprima, che si connette direttamente al renderer video.

Se il filtro di acquisizione include solo un pin di acquisizione, il generatore del grafico di acquisizione inserisce un filtro di [Smart Tee](smart-tee-filter.md) , che suddivide il flusso in un flusso di acquisizione e in un flusso di anteprima. Questa operazione viene descritta in modo più dettagliato nella [combinazione di acquisizione video e anteprima](combining-video-capture-and-preview.md).

In alcuni casi, il flusso video deve passare attraverso il filtro del mixer sovrapposto. In tal caso, il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) lo aggiunge automaticamente al grafico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Combinazione di acquisizione video e anteprima](combining-video-capture-and-preview.md)
</dt> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



