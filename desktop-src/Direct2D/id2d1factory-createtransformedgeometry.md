---
title: Metodi ID2D1Factory CreateTransformedGeometry (D2d1.h)
description: Trasforma la geometria specificata e archivia il risultato come oggetto ID2D1TransformedGeometry.
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- Metodi CreateTransformedGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 8216b5b63951e3f393dc1c8a204a4a4e38ee652d79eb795ba4f4e97041aff3f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832851"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a>Metodi ID2D1Factory::CreateTransformedGeometry

Trasforma la geometria specificata e archivia il risultato come [**oggetto ID2D1TransformedGeometry.**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                  | Descrizione                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTransformedGeometry(ID2D1Geometry,D2D \* \_ MATRIX \_ 3X2 \_ \* F,ID2D1TransformedGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) | Trasforma la geometria specificata e archivia il risultato come [**oggetto ID2D1TransformedGeometry.**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) <br/> |
| [**CreateTransformedGeometry(ID2D1Geometry,D2D \* \_ MATRIX \_ 3X2 \_ F&,ID2D1TransformedGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))  | Trasforma la geometria specificata e archivia il risultato come [**oggetto ID2D1TransformedGeometry.**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) <br/> |



## <a name="remarks"></a>Commenti

Analogamente ad altre risorse, una geometria trasformata eredita lo spazio delle risorse e i criteri di threading della factory che l'ha creata. Questo oggetto non è modificabile.

Quando si accarezza una geometria trasformata con il [**metodo DrawGeometry,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) la larghezza del tratto non viene influenzata dalla trasformazione applicata alla geometria. La larghezza del tratto è interessata solo dalla trasformazione del mondo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato [**un ID2D1RectangleGeometry,**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))quindi viene disezionato senza trasformarlo. Produce l'output illustrato nella figura seguente.

![illustrazione di un rettangolo](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



L'esempio successivo usa la destinazione di rendering per ridimensionare la geometria di un fattore di 3 e quindi la disegna. La figura seguente mostra il risultato del disegno del rettangolo senza la trasformazione e con la trasformazione . nota che il tratto è più spesso dopo la trasformazione, anche se lo spessore del tratto è 1.

![Illustrazione di un rettangolo più piccolo all'interno di un rettangolo più grande con un tratto più spesso](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



L'esempio successivo usa **il metodo CreateTransformedGeometry** per ridimensionare la geometria di un fattore di 3 e quindi la disegna. Produce l'output illustrato nella figura seguente. Si noti che, anche se il rettangolo è più grande, il tratto non è aumentato.

![illustrazione di un rettangolo più piccolo all'interno di un rettangolo più grande con lo stesso tratto](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );


// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
