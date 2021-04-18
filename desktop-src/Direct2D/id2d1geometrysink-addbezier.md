---
title: Metodi AddBezier di ID2D1GeometrySink (D2d1. h)
description: Crea una curva di Bezier cubica tra il punto corrente e il punto finale specificato e la aggiunge al sink di geometria.
ms.assetid: d1e228eb-dac6-485d-b3c9-69b2bd45e531
keywords:
- Metodo AddBezier Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b470129350463920583c34bec5f886f60b16485e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330073"
---
# <a name="id2d1geometrysinkaddbezier-methods"></a>Metodi ID2D1GeometrySink:: AddBezier

Crea una curva di Bezier cubica tra il punto corrente e il punto finale specificato e la aggiunge al sink di geometria.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                            | Descrizione                                                                                    |
|:--------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**AddBezier ( \_ segmento Bezier D2D1 \_&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))  | Crea una curva di Bézier cubica tra il punto corrente e il punto finale specificato.<br/> |
| [**AddBezier ( \_ segmento Bezier \_ d2d1 \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment)) | Crea una curva di Bezier cubica tra il punto corrente e l'endpoint specificato.<br/>  |



## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), viene recuperato un sink e utilizzato per definire una forma di clessidra. Per l'esempio completo, vedere [How to disegnare and Fill an Complex Shape](how-to-draw-and-fill-a-complex-shape.md).


```C++
ID2D1GeometrySink *pSink = NULL;



// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            pSink->BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink->AddLine(D2D1::Point2F(200, 0));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink->AddLine(D2D1::Point2F(0, 200));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink->Close();
        }
        SafeRelease(&pSink);
    }
}
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)
</dt> </dl>

�

�
