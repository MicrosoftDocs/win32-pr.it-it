---
title: Come applicare più trasformazioni a un oggetto
description: Illustra come applicare più trasformazioni a un oggetto .
ms.assetid: a3875072-bb73-4698-944e-102ab5539d80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d63db7899b79dd07a6a4a14a4efbbfaeefc5723ad09c71a3462ba5d2fd0c042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259687"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a>Come applicare più trasformazioni a un oggetto

Per eseguire più trasformazioni su un oggetto, è necessario combinare più trasformazioni in una sola. In altri termini, prendere l'output di ogni matrice di trasformazione e usarlo come input per la successiva, ottenendo in tal modo gli effetti cumulativi di tutte le trasformazioni di matrice.

Si supponga che due matrici di trasformazione, rotazione e traslazione, siano moltiplicate insieme. Il risultato è una nuova matrice che esegue le funzioni di rotazione e traslazione. Poiché la moltiplicazione di matrici non è commutativa, una trasformazione di rotazione moltiplicata per una trasformazione di traslazione è diversa dalla trasformazione di traslazione moltiplicata per la trasformazione di rotazione.

Gli esempi di codice seguenti illustrano come applicare la rotazione seguita dalla traslazione e quindi dalla traslazione seguita dalla rotazione. Si noti che i risultati del rendering sono diversi.


```C++
D2D1_RECT_F rectangle = D2D1::RectF(300.0f, 40.0f, 360.0f, 100.0f);

// Draw the rectangle before transforming the render target.

m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(330.0f, 70.0f)
    );


D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

// First rotate about the center of the square and then move
// 20 pixels to the right along the x-axis
// and 10 pixels downward along the y-axis.
m_pRenderTarget->SetTransform(rotation* translation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush, 1.0f);
```




```C++
D2D1_RECT_F rectangle = D2D1::Rect(40.0f, 40.0f, 100.0f, 100.0f);

// Draw a rectangle without transforming it.
m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

m_pRenderTarget->SetTransform(translation);

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(70.0f, 70.0f)
    );

// First move 20 pixels to the right along the x-axis and
// 10 pixels downward along the y-axis,
// and then rotate about the center of the original square.
m_pRenderTarget->SetTransform(translation * rotation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



Il codice produce l'output illustrato nella figura seguente.

![illustrazione di un rettangolo che è stato traslato e quindi ruotato e di un rettangolo che è stato ruotato e quindi convertito](images/multipletransforms.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su Direct2D](reference.md)
</dt> <dt>

[Cenni preliminari sulle trasformazioni Direct2D](direct2d-transforms-overview.md)
</dt> </dl>

 

 




