---
title: Come ridimensionare un oggetto
description: Viene illustrato come ridimensionare un oggetto.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f46ae37197cb7cbfeb3f86588e1b5298cfc467
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473830"
---
# <a name="how-to-scale-an-object"></a>Come ridimensionare un oggetto

In questo argomento viene descritto come ridimensionare un oggetto utilizzando la classe [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) . Per ridimensionare un oggetto significa che l'oggetto è più grande o più piccolo. È possibile chiamare uno dei due metodi seguenti per ridimensionare un oggetto.

-   **Matrix3x2F:: scale (D2D1 \_ size \_ F SCALEFACTOR, d2d1 \_ Point \_ 2F Centerpoint)**
-   **Matrix3x2F:: scale (float scaleX, float scaleY, D2D1 \_ Point \_ 2F Centerpoint)**

Il primo metodo Archivia *ScaleX* e *ScaleY* come coppia ordinata di valori a virgola mobile nella struttura [**d2d1 \_ size \_ F**](/windows/desktop/Direct2D/d2d1-size-f) . Il secondo metodo definisce *ScaleX* e *ScaleY* come singoli parametri.

Indipendentemente dal metodo usato, è necessario specificare sia il metodo *ScaleX* che i fattori di *scalabilità* . Il valore *ScaleX* è il fattore di scala nella direzione x. Ad esempio, un valore *ScaleX* di 1,5 estende l'oggetto a 150% lungo l'asse x. Analogamente, il valore di *scalabilità* è il fattore di scala nella direzione y. Ad esempio, un valore di *scalabilità* di 0,5 compatta l'altezza dell'oggetto del 50% lungo l'asse y.

Per specificare un punto come centro dell'operazione di ridimensionamento, usare il parametro *Centerpoint* . Per impostazione predefinita, un oggetto viene centrato sulla relativa origine (0,0).

Nell'esempio di codice seguente viene creata una trasformazione di scala per aumentare le dimensioni di un quadrato al 130% delle dimensioni originali. *Centerpoint* è impostato in modo da essere l'angolo superiore sinistro del quadrato originale.


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



Nella figura seguente viene illustrato l'effetto dell'applicazione della trasformazione scala al quadrato. Il quadrato originale è un contorno tratteggiato e il quadrato ridimensionato è un contorno a tinta unita.

![illustrazione del quadrato ridimensionato al 130% delle dimensioni originali](images/scale-ovw.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sulle trasformazioni Direct2D](direct2d-transforms-overview.md)
</dt> <dt>

[Riferimento Direct2D](reference.md)
</dt> </dl>

 

 