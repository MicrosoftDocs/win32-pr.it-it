---
title: Come ritagliare con un rettangolo Axis-Aligned clip
description: Illustra come ritagliare un'area con un rettangolo di ritaglio allineato all'asse.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f666bac88d93cb8ea0f27bfb9c2d5b14975e0dc8bb67aba4f0e767178f6ebddc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569316"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a>Come ritagliare con un rettangolo Axis-Aligned clip

Questo argomento descrive come ritagliare un'immagine con un rettangolo di ritaglio allineato all'asse. Questo approccio produce solo clip rettangolari, perché i limiti del contenuto sono allineati all'asse del rettangolo. Questo approccio è più efficiente rispetto all'uso dei livelli con i limiti del contenuto. Per altre informazioni, vedere[Panoramica dei livelli.](direct2d-layers-overview.md)

**Per ritagliare con un rettangolo di ritaglio allineato all'asse**

1.  Caricare l'immagine originale da una risorsa. Per informazioni su come caricare una bitmap, vedere [Come caricare una bitmap da una risorsa.](how-to-load-a-bitmap-from-a-resource.md)
2.  Chiamare [**ID2D1RenderTarget::P ushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) per specificare un rettangolo. I comandi di rendering vengono ritagliati in base al rettangolo.

3.  Paint'immagine originale.
4.  Chiamare [**ID2D1RenderTarget::P opAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) per rimuovere l'ultima clip allineata all'asse dalla destinazione di rendering.

Nella figura seguente, ad esempio, la bitmap originale a sinistra è 200 \* 130 pixel. La bitmap a destra è la bitmap originale ritagliata in base al rettangolo di ritaglio allineato all'asse. Le dimensioni sono da (20, 20) a (100, 100).

![illustrazione di una bitmap goldfish prima e dopo che la bitmap è stata ritagliata](images/cliparegion-axisalignedclip.png)

Per creare l'immagine ritagliata, creare una struttura rettangolare come area di ritaglio. Chiamare [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) con l'area di ritaglio e disegnare l'immagine originale. Chiama [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) per rimuovere il clip dalla destinazione di rendering. A tal fine, osservare il codice indicato di seguito.


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su Direct2D](reference.md)
</dt> </dl>

 

 