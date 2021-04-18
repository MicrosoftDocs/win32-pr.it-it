---
title: Come trasformare una geometria
description: Viene illustrato come trasformare una geometria tramite Direct2D.
ms.assetid: de434615-14b1-4b66-b09b-e90468e03d58
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: ae15d0b1da304f9dfe24ff5de33a9f1582e2ca05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300254"
---
# <a name="how-to-transform-a-geometry"></a>Come trasformare una geometria

Per trasformare una geometria, è possibile applicare la trasformazione alla destinazione di [**rendering chiamando la trasformazione o applicare**](id2d1rendertarget-settransform.md) la trasformazione alla geometria chiamando [**CreateTransformedGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)). Sebbene entrambi gli approcci trasformino una geometria, presentano alcune differenze fondamentali. **CreateTransformedGeometry** influisce sul riempimento, ma non influisce sulla larghezza del tratto. Inoltre, **CreateTransformedGeometry** trasforma la geometria da sola senza influito sulle altre forme sulla destinazione di rendering [**, mentre la trasformazione viene**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) applicata a tutte le forme nella destinazione di rendering.

Questo argomento illustra come trasformare una geometria chiamando [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)).

**Per trasformare una geometria**

1.  Dichiarare una variabile [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) .
2.  Chiamare il metodo [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) per creare una geometria trasformata.

Nel codice seguente viene illustrato come creare un'ora, trasformare il vetro dell'ora e creare gli occhiali per le ore originali e risultanti.


```C++
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

if (SUCCEEDED(hr))
{
    // Create a transformed geometry which is tilted at an angle to the previous geometry
    hr = m_pD2DFactory->CreateTransformedGeometry(
        m_pPathGeometry,
        D2D1::Matrix3x2F::Rotation(
            45.f,
            D2D1::Point2F(100, 100)),
        &m_pTransformedGeometry
        );
}
```



 

 