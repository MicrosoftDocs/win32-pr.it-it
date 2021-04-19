---
title: D2D1_MATRIX_3X2_F (D2d1. h)
description: Rappresenta una matrice 3 per 2.
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb252e35508c48570c96f251205fc8a54755687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301272"
---
# <a name="d2d1_matrix_3x2_f"></a>\_Matrice d2d1 \_ 3x2 \_ F

Rappresenta una matrice 3 per 2.


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a>Commenti

**D2d1 \_ MATRIX \_ 3x2** è un nuovo nome per la struttura [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) . Per un elenco dei campi forniti dalla matrice, vedere [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).

Per semplificare le operazioni comuni della matrice, Direct2D fornisce la classe [**D2D1:: Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) , derivata dalla struttura [**d2d1 \_ Matrix \_ 3x2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) . La classe **Matrix3x2F** fornisce un set di metodi helper per l'esecuzione di attività comuni, ad esempio la creazione di una matrice di traslazione o di inclinazione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato il metodo [**D2D1:: Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) per creare una matrice di rotazione che ruota un quadrato di 45 gradi in senso orario sul centro del quadrato e passa la matrice al metodo [**setransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) della destinazione di rendering (*m \_ pRenderTarget*).

Nella figura seguente viene illustrato l'effetto dell'applicazione della trasformazione di rotazione precedente al quadrato. Il quadrato originale è un contorno tratteggiato e il quadrato ruotato è un contorno a tinta unita.

![illustrazione di un quadrato ruotato di 45 gradi in senso orario rispetto al centro del quadrato originale](images/rotate-ovw.png)


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



Il codice è stato omesso da questo esempio. Per ulteriori informazioni sulle trasformazioni, vedere [Cenni preliminari sulle trasformazioni](direct2d-transforms-overview.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D2D1:: Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
</dt> <dt>

[Cenni preliminari sulle trasformazioni](direct2d-transforms-overview.md)
</dt> <dt>

[Come ruotare un oggetto](how-to-rotate.md)
</dt> <dt>

[Come ridimensionare un oggetto](how-to-scale.md)
</dt> <dt>

[Come inclinare un oggetto](how-to-skew.md)
</dt> <dt>

[Come tradurre un oggetto](how-to-translate.md)
</dt> <dt>

[**\_Matrice D2D \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

