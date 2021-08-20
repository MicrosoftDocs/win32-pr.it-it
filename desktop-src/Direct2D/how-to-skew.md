---
title: Come inclinare un oggetto
description: Viene illustrato come inclinare un oggetto.
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 849c292221a8b4503cdfd122e08b6f1b2521043b44732c33d851a86693853f2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003498"
---
# <a name="how-to-skew-an-object"></a>Come inclinare un oggetto

Per inclinare (o inclinare) un oggetto significa distorcere un oggetto in base a un angolo specificato rispetto all'asse x, all'asse y o a entrambi. Ad esempio, quando si inclina un quadrato, diventa un parallelogramma.

Il [**metodo Matrix3x2F::Skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) accetta 3 parametri:

-   *angleX:* angolo di inclinazione dell'asse x, misurato in gradi in senso antiorario rispetto all'asse y.
-   *angleY:* angolo di inclinazione dell'asse y, misurato in gradi in senso orario rispetto all'asse x.
-   *centerPoint:* punto su cui viene eseguita l'ancoraggio.

Per stimare l'effetto di una trasformazione dell'affondo, si consideri che *angleX* è l'angolo di affondo misurato in gradi in senso antiorario rispetto all'asse y. Ad esempio, se *angleX* è impostato su 30, l'oggetto inclina di 30 gradi in senso antiorario lungo l'asse y rispetto al *centerPoint*. La figura seguente mostra un quadrato a inclinazione orizzontale di 30 gradi rispetto all'angolo superiore sinistro del quadrato.

![Illustrazione di un quadrato a 30 gradi in senso antiorario rispetto all'asse y](images/skewx.png)

Analogamente, *angleY* è un angolo di inclinazione misurato in gradi in senso orario rispetto all'asse x. Ad esempio, se *angleY* è impostato su 30, l'oggetto inclina di 30 gradi in senso orario lungo l'asse x rispetto al *centerPoint*. La figura seguente mostra un quadrato a inclinazione verticale di 30 gradi rispetto all'angolo superiore sinistro del quadrato.

![Illustrazione di un quadrato a 30 gradi in senso orario rispetto all'asse x](images/skewy.png)

Se si *impostano sia angleX* che *angleY* su 30 gradi e *centerPoint* sull'angolo superiore sinistro del quadrato, verrà visualizzato il quadrato a sfalsato seguente (con contorno a tinta unita). Si noti che il quadrato affogato viene affogato di 30 gradi in senso antiorario rispetto all'asse y e di 30 gradi in senso orario rispetto all'asse x.

![Illustrazione di un quadrato di 30 gradi in senso antiorario rispetto all'asse y e di 30 gradi in senso orario rispetto all'asse x](images/skewxy.png)

L'esempio di codice seguente inclina orizzontalmente il quadrato di 45 gradi rispetto all'angolo superiore sinistro del quadrato.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 301.5f, 186.0f, 361.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the skew transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Skew(
            45.0f,
            0.0f,
            D2D1::Point2F(126.0f, 301.5f))
        );

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



Nella figura seguente viene illustrato l'effetto dell'applicazione della trasformazione a inclinazione al quadrato, in cui il quadrato originale è un contorno punteggiato e l'oggetto a inclinazione (parallelogramma) è un contorno a tinta unita. Si noti che l'angolo di inclinazione è di 45 gradi in senso antiorario rispetto all'asse y.

![Illustrazione di un quadrato a 45 gradi in senso antiorario rispetto all'asse y](images/skew-ovw.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica delle trasformazioni Direct2D](direct2d-transforms-overview.md)
</dt> <dt>

[Informazioni di riferimento su Direct2D](reference.md)
</dt> </dl>

 

 