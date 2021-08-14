---
title: Come ruotare un oggetto
description: Illustra come ruotare un oggetto.
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babc84c08af759d8484c8ba85db40780f68570d93a0a8b9442e93b960ecac39c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003533"
---
# <a name="how-to-rotate-an-object"></a>Come ruotare un oggetto

Questo argomento descrive come ruotare un oggetto intorno a un punto specificato. Per ruotare un oggetto, chiamare [**il metodo Matrix3x2F::Rotation.**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) Questo metodo accetta due parametri, l'angolo specificato e il punto centrale. L'angolo è un angolo di rotazione in senso orario in gradi e il punto centrale è il punto su cui ruota l'oggetto. Il punto centrale viene espresso nel sistema di coordinate dell'oggetto trasformato.

Ad esempio, il codice seguente ruota un quadrato in senso orario di 45 gradi intorno al centro del quadrato.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



Nella figura seguente viene illustrato l'effetto dell'applicazione della trasformazione di rotazione precedente al quadrato. Il quadrato originale è un contorno punteggiato e il quadrato ruotato è un contorno a tinta unita.

![illustrazione di un quadrato ruotato in senso orario di 45 gradi al centro del quadrato originale](images/rotate-ovw.png)

La figura seguente mostra l'effetto della rotazione dello stesso angolo rispetto a un punto centrale diverso. Si noti che gli oggetti ruotati sono in posizioni diverse rispetto all'originale. Il quadrato con contorni a sinistra è il risultato della rotazione attorno al centro del quadrato originale e il quadrato con contorno destro è il risultato della rotazione attorno all'angolo superiore sinistro del quadrato originale.

![illustrazione di un quadrato ruotato in senso orario di 45 gradi su un punto centrale diverso](images/translate-rotationcompare.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su Direct2D](reference.md)
</dt> <dt>

[Panoramica delle trasformazioni Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 