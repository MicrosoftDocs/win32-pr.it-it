---
title: Come inclinare un oggetto
description: Viene illustrato come inclinare un oggetto.
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691062e64d4255b1e2f7711b5ff700d72fd90063
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872826"
---
# <a name="how-to-skew-an-object"></a>Come inclinare un oggetto

Per inclinare (o inclinare) un oggetto significa distorcere un oggetto in base a un angolo specificato dall'asse x, dall'asse y o da entrambi. Ad esempio, quando si inclina un quadrato, diventa un parallelogramma.

Il metodo [**Matrix3x2F:: asimmetria**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) accetta 3 parametri:

-   *AngleX*: angolo di inclinazione dell'asse x, misurato in gradi in senso antiorario rispetto all'asse y.
-   *AngleY*: angolo di inclinazione dell'asse y, misurato in gradi in senso orario dall'asse x.
-   *centerPoint*: punto in cui viene eseguita l'asimmetria.

Per stimare l'effetto di una trasformazione asimmetria, tenere presente che *AngleX* è l'angolo di inclinazione misurato in gradi in senso antiorario rispetto all'asse y. Se, ad esempio, *AngleX* è impostato su 30, l'oggetto inclina 30 gradi in senso antiorario lungo l'asse y relativo al *centerPoint*. Nella figura seguente viene mostrato un quadrato inclinato orizzontalmente di 30 gradi sull'angolo superiore sinistro del quadrato.

![illustrazione di un quadrato inclinato di 30 gradi in senso antiorario dall'asse y](images/skewx.png)

Analogamente, *AngleY* è un angolo di inclinazione misurato in gradi in senso orario dall'asse x. Se ad esempio *AngleY* è impostato su 30, l'oggetto inclina 30 gradi in senso orario lungo l'asse x relativo a *centerPoint*. Nella figura seguente viene mostrato un quadrato inclinato in verticale di 30 gradi sull'angolo superiore sinistro del quadrato.

![illustrazione di un quadrato inclinato di 30 gradi in senso orario dall'asse x](images/skewy.png)

Se si impostano sia *AngleX* che *AngleY* su 30 gradi e il *centerPoint* nell'angolo superiore sinistro del quadrato, viene visualizzato il quadrato inclinato seguente (con linee solide). Si noti che il quadrato inclinato è inclinato di 30 gradi in senso antiorario rispetto all'asse y e 30 gradi in senso orario dall'asse x.

![illustrazione di un quadrato inclinato di 30 gradi in senso antiorario dall'asse y e 30 gradi in senso orario dall'asse x](images/skewxy.png)

L'esempio di codice seguente inclina il quadrato di 45 gradi orizzontalmente rispetto all'angolo superiore sinistro del quadrato.


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



Nella figura seguente viene illustrato l'effetto dell'applicazione della trasformazione asimmetria al quadrato, in cui il quadrato originale è un contorno tratteggiato e l'oggetto inclinato (parallelogramma) è un contorno a tinta unita. Si noti che l'angolo di inclinazione è di 45 gradi in senso antiorario rispetto all'asse y.

![illustrazione di un quadrato inclinato di 45 gradi in senso antiorario dall'asse y](images/skew-ovw.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sulle trasformazioni Direct2D](direct2d-transforms-overview.md)
</dt> <dt>

[Riferimento Direct2D](reference.md)
</dt> </dl>

 

 