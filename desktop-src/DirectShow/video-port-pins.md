---
description: PIN della porta video
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: PIN della porta video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d13ab4ad63995dd38460bf29064035c9c1802dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883078"
---
# <a name="video-port-pins"></a>PIN della porta video

Un dispositivo di acquisizione con una porta video hardware può usare VPE (video Port Extensions) in Microsoft® DirectX®. In tal caso, il filtro di acquisizione avrà un PIN della porta video (VP). Nessun dato video passa dal perno VP al grafico del filtro. Al contrario, i frame video vengono prodotti nell'hardware e inviati direttamente alla memoria del video. Il pin VP consente l'invio di messaggi di controllo all'hardware.

È importante connettere il pin VP, anche se l'applicazione esegue solo l'acquisizione di file senza anteprima. Se si lascia il PIN non connesso, il grafico non viene eseguito correttamente. Questo comportamento è diverso dai pin di anteprima, che non devono essere connessi.

I diversi renderer video DirectShow offrono un supporto variabile per i pin VP:

-   Renderer video: connettere il pin VP al pin 0 nel filtro [sovrimpressione](overlay-mixer-filter.md) e connettere il filtro del mixer sovrapposto al renderer video.
-   VMR-7: connettere il pin VP al filtro di [Gestione porte video](video-port-manager.md) e connettere Gestione porta video a VMR-7.
-   VMR-9: non è possibile usare VMR-9 se il dispositivo ha un pin VP, perché Direct3D 9 non supporta le porte video. Usare il renderer video o VMR-7.

Per gli scenari di porta video, il mixer overlay e il renderer video sono consigliati rispetto a gestione porta video e VMR-7, perché non tutti i driver supportano il gestore della porta video. In generale, il mixer overlay è l'opzione più affidabile per le porte video.

Il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserisce automaticamente il mixer della sovrimpressione se è presente un pin VP. Se si compila il grafico senza usare questo metodo, è necessario verificare la presenza di un PIN della porta video nel filtro di acquisizione e, se presente, connetterlo al filtro della sovrimpressione, come illustrato nella figura seguente.

![connessione di un PIN della porta video al filtro della sovrimpressione.](images/vidcap11.png)

È possibile usare il metodo [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) per cercare un pin VP sul filtro di acquisizione:


```C++
hr = pBuild->FindPin(
    pCap,                    // Pointer to the capture filter.
    PINDIR_OUTPUT,           // Look for an output pin.
    &PIN_CATEGORY_VIDEOPORT, // Look for a video port pin.
    NULL,                    // Any media type.
    FALSE,                   // Pin can be connected.
    0,                       // Retrieve the first matching pin.
    &pVPPin                  // Receives a pointer to the pin.
);
```



Dopo aver aggiunto il mixer della sovrimpressione al grafo, chiamare di nuovo **FindPin** per trovare il pin 0 nel mixer della sovrimpressione. Il pin 0 è sempre il primo pin di input sul filtro.


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



Connettere i due pin chiamando [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).


```C++
pGraph->Connect(pVPPin, pOvPin);
```



Quindi connettere il pin di output del mixer overlay al filtro renderer video. È possibile nascondere il video chiamando il [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) e [**IVideoWindow::p UT \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) methods on the Filter Graph Manager.

Per i sintonizzatori TV, il filtro di acquisizione potrebbe avere anche una porta video VBI pin (PIN \_ Category \_ VIDEOPORT \_ VBI). In tal caso, connettere il PIN al filtro [VBI Surface allocator](vbi-surface-allocator.md) . Per ulteriori informazioni, vedere [visualizzazione di didascalie chiuse](viewing-closed-captions.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti sull'acquisizione avanzata](advanced-capture-topics.md)
</dt> <dt>

[Uso del mixer overlay in acquisizione video](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



