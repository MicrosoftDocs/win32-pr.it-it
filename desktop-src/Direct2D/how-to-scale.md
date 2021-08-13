---
title: Come ridimensionare un oggetto
description: Illustra come ridimensionare un oggetto.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d833ea44e4a38672729dd7647063e8ed9f8de3574d820a3db40d5a848064ef15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259147"
---
# <a name="how-to-scale-an-object"></a>Come ridimensionare un oggetto

Questo argomento descrive come ridimensionare un oggetto usando la [**classe Matrix3x2F.**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) Ridimensionare un oggetto significa rendere l'oggetto più grande o più piccolo. È possibile chiamare uno dei due metodi seguenti per ridimensionare un oggetto.

-   **Matrix3x2F::Scale(D2D1 \_ SIZE \_ F scalefactor, D2D1 \_ POINT \_ 2F centerpoint)**
-   **Matrix3x2F::Scale(float scalex, float scaley, D2D1 \_ POINT \_ 2F centerpoint)**

Il primo metodo archivia *scalex* e *scaley* come coppia ordinata di valori a virgola mobile nella struttura [**D2D1 \_ SIZE \_ F.**](/windows/desktop/Direct2D/d2d1-size-f) Il secondo metodo definisce *scalex* e *scaley* come singoli parametri.

Indipendentemente dal metodo utilizzato, è necessario specificare sia *i fattori scalex* che *scaley.* Il *valore scalex* è il fattore di scala nella direzione x. Ad esempio, un *valore scalex* di 1,5 estende l'oggetto al 150% lungo l'asse x. Analogamente, il *valore scaley* è il fattore di scala nella direzione y. Ad esempio, un *valore scaley* pari a 0,5 riduce l'altezza dell'oggetto del 50% lungo l'asse y.

Per specificare un punto come centro dell'operazione di ridimensionamento, usare il *parametro centerpoint.* Per impostazione predefinita, un oggetto è centrato sull'origine (0,0).

Il codice di esempio seguente crea una trasformazione di scala per aumentare le dimensioni di un quadrato fino al 130% delle dimensioni originali. Il *punto centrale* è impostato sull'angolo superiore sinistro del quadrato originale.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 80.5f, 498.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the scale transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Scale(
            D2D1::Size(1.3f, 1.3f),
            D2D1::Point2F(438.0f, 80.5f))
        );

    // Paint the rectangle's interior.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



Nella figura seguente viene illustrato l'effetto dell'applicazione della trasformazione scala al quadrato. Il quadrato originale è un contorno punteggiato e il quadrato ridimensionato è un contorno a tinta unita.

![Illustrazione del quadrato ridimensionato al 130% delle dimensioni originali](images/scale-ovw.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica delle trasformazioni Direct2D](direct2d-transforms-overview.md)
</dt> <dt>

[Informazioni di riferimento su Direct2D](reference.md)
</dt> </dl>

 

 