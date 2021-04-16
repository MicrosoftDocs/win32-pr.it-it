---
title: Come ritagliare con un rettangolo di ritaglio Axis-Aligned
description: Mostra come ritagliare un'area con un rettangolo di ritaglio allineato all'asse.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9fea904f9df396918d2cdfdb5205f6dd0197d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104551595"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a>Come ritagliare con un rettangolo di ritaglio Axis-Aligned

In questo argomento viene descritto come ritagliare un'immagine con un rettangolo di ritaglio allineato all'asse. Questo approccio produce solo clip rettangolari, perché i limiti del contenuto sono allineati all'asse del rettangolo. Questo approccio è più efficiente rispetto all'uso di livelli con i limiti di contenuto. Per altre informazioni, vedere[Cenni preliminari sui livelli](direct2d-layers-overview.md).

**Per ritagliare un rettangolo di ritaglio allineato all'asse**

1.  Caricare l'immagine originale da una risorsa. Per informazioni su come caricare una bitmap, vedere [come caricare una bitmap da una risorsa](how-to-load-a-bitmap-from-a-resource.md).
2.  Chiamare [**ID2D1RenderTarget::P ushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) per specificare un rettangolo. I comandi di rendering vengono ritagliati nel rettangolo.

3.  Disegnare l'immagine originale.
4.  Chiamare [**ID2D1RenderTarget::P opaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) per rimuovere l'ultimo clip allineato all'asse dalla destinazione di rendering.

Nella figura seguente, ad esempio, la bitmap originale a sinistra è 200 \* 130 pixel. La bitmap a destra è la bitmap originale ritagliata nel rettangolo di ritaglio allineato all'asse. Le dimensioni sono (20, 20) in (100, 100).

![illustrazione di una bitmap Goldfish prima e dopo il ritaglio della bitmap](images/cliparegion-axisalignedclip.png)

Per creare l'immagine ritagliata, creare una struttura Rectangle come area di ridimensionamento. Chiamare [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) con l'area di ridimensionamento e disegnare l'immagine originale. Chiamare [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) per rimuovere il clip dalla destinazione di rendering. A tal fine, osservare il codice indicato di seguito.


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

[Riferimento Direct2D](reference.md)
</dt> </dl>

 

 