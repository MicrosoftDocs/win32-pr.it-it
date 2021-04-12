---
title: Come tradurre un oggetto
description: Viene illustrato come tradurre un oggetto.
ms.assetid: 0fc48801-de14-4398-816d-6e7ddf4ffdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab7921e6de3286f3e1b5cf7e3da8571815848d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338743"
---
# <a name="how-to-translate-an-object"></a>Come tradurre un oggetto

Per tradurre un oggetto 2D è necessario spostare l'oggetto lungo l'asse x, l'asse y o entrambi. È possibile chiamare uno dei due metodi seguenti per creare una trasformazione di conversione.

-   [**Translation (D2D1 \_ size \_ F size)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): accetta una coppia ordinata che definisce la distanza da tradurre lungo l'asse x e l'asse y.
-   [**Translation (float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): accetta la distanza da tradurre lungo l'asse x e la distanza per traslare lungo l'asse y.

Il codice seguente crea una matrice di trasformazione della traduzione che sposta le 20 unità quadrate a destra lungo l'asse x e le 10 unità verso il basso lungo l'asse y.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 80.5f, 186.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the translation transform to the render target.
    m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(20, 10));

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



Nella figura seguente viene illustrato l'effetto dell'applicazione della trasformazione traduzione al quadrato, in cui il quadrato originale è un contorno tratteggiato e il quadrato tradotto è un contorno a tinta unita.

![illustrazione di un quadrato spostato di 20 unità a destra lungo l'asse x e 10 unità verso il basso lungo l'asse y](images/translation-ovw.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento Direct2D](reference.md)
</dt> <dt>

[Cenni preliminari sulle trasformazioni Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 