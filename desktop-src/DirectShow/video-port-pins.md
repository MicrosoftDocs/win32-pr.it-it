---
description: Pin della porta video
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: Pin della porta video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94202e05cc467eabb77719a145a77310a62482e6f82772261b57e5ff544d2b63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696786"
---
# <a name="video-port-pins"></a>Pin della porta video

Un dispositivo di acquisizione con una porta video hardware potrebbe usare le estensioni della porta video (VPE) in Microsoft® DirectX®. In questo caso, il filtro di acquisizione avrà un pin di porta video (VP). Nessun dato video passa dal pin del VP attraverso il grafico del filtro. I fotogrammi video vengono invece prodotti nell'hardware e inviati direttamente alla memoria video. Il pin VP consente di inviare messaggi di controllo all'hardware.

È importante connettere il pin VP, anche se l'applicazione esegue solo l'acquisizione di file senza anteprima. Se si lascia la puntina non connessa, il grafico non verrà eseguito correttamente. Questo è diverso dai pin di anteprima, che non devono essere connessi.

I diversi DirectShow renderer video offrono un supporto variabile per i pin VP:

-   Renderer video: Connessione il pin VP per aggiungere 0 al filtro overlay Mixer e connettere il filtro overlay [Mixer](overlay-mixer-filter.md) al renderer video.
-   VMR-7: Connessione il pin VP al filtro [di Gestione](video-port-manager.md) porte video e connettere Video Port Manager a VMR-7.
-   VMR-9: non è possibile usare VMR-9 se il dispositivo ha un pin VP, perché Direct3D 9 non supporta le porte video. Usare il renderer video o VMR-7.

Per gli scenari con porte video, i renderer di overlay Mixer e video sono consigliati su Gestione porte video e VMR-7, perché non tutti i driver supportano Gestione porte video. In generale, la sovrapposizione Mixer è l'opzione più affidabile per le porte video.

Il [**metodo ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserisce automaticamente la sovrimpressione Mixer se è presente un pin VP. Se si compila il grafo senza usare questo metodo, è necessario verificare la presenza di un pin della porta video nel filtro di acquisizione e, se presente, connetterlo al filtro overlay Mixer, come illustrato nel diagramma seguente.

![connessione di un pin della porta video al filtro del mixer di sovrimpressione.](images/vidcap11.png)

È possibile usare il [**metodo ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) per cercare un pin VP nel filtro di acquisizione:


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



Dopo aver aggiunto la sovrimpressione Mixer al grafo, chiamare di nuovo **FindPin** per trovare il segnaposto 0 nella Mixer. Pin 0 è sempre il primo pin di input nel filtro.


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



Connessione i due segnaposto chiamando [**IGraphBuilder::Connessione**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).


```C++
pGraph->Connect(pVPPin, pOvPin);
```



Connettere quindi il pin Mixer di output della sovrimpressione al filtro Renderer video. È possibile nascondere il video chiamando i metodi [**IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) e [**IVideoWindow::p ut \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) in Filter Graph Manager.

Per gli ottimizzatori TV, il filtro di acquisizione potrebbe avere anche un pin VBI della porta video (PIN \_ CATEGORY \_ VIDEOPORT \_ VBI). In tal caso, connettere il segnaposto al filtro [VBI Surface Allocator.](vbi-surface-allocator.md) Per altre informazioni, vedere [Visualizzazione di sottotitoli codificati.](viewing-closed-captions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati sull'acquisizione](advanced-capture-topics.md)
</dt> <dt>

[Uso della sovrimpressione Mixer'acquisizione video](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



