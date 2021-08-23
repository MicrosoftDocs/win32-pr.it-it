---
title: Come disegnare e riempire una forma complessa
description: Direct2D fornisce l'interfaccia ID2D1PathGeometry per descrivere forme complesse che possono contenere curve, archi e linee. Questo argomento descrive come definire ed eseguire il rendering di una geometria di percorso.
ms.assetid: d7aad487-04e0-448d-bedf-b8dfadc7bbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222d3d94eb1f9e944a1c5113baf938a7c3da6e86751a7be748798ace12a9611
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569207"
---
# <a name="how-to-draw-and-fill-a-complex-shape"></a>Come disegnare e riempire una forma complessa

Direct2D fornisce [**l'interfaccia ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) per descrivere forme complesse che possono contenere curve, archi e linee. Questo argomento descrive come definire ed eseguire il rendering di una geometria di percorso.

Per definire una geometria del percorso, usare innanzitutto il metodo [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) per creare la geometria del percorso, quindi usare il metodo [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) della geometria del percorso per recuperare un [**ID2D1GeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) È quindi possibile aggiungere linee, curve e archi chiamando i vari metodi Add del sink.

L'esempio seguente crea [**un id2D1PathGeometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)recupera un sink e lo usa per definire una forma a forma di clessidra.


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

Si noti che [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) è una risorsa indipendente dal dispositivo e può quindi essere creata una sola volta e conservata per tutta la durata dell'applicazione. Per altre informazioni sui diversi tipi di risorse, vedere Panoramica [delle risorse.](resources-and-resource-domains.md)

L'esempio successivo crea due pennelli che verranno usati per disegnare il contorno e il riempimento della geometria del tracciato.


```C++
if (SUCCEEDED(hr))
{
    // Create a black brush.
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &m_pBlackBrush
        );
}

if (SUCCEEDED(hr))
{
    // Create a linear gradient.
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 0.25f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = m_pRenderTarget->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(100, 0),
                D2D1::Point2F(100, 200)),
            D2D1::BrushProperties(),
            pGradientStops,
            &m_pLGBrush
            );
    }

    SafeRelease(&pGradientStops);
}
```



L'esempio finale usa [**i metodi DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) per disegnare il contorno e l'interno della geometria. Questo esempio produce l'output illustrato nella figura seguente.

![Illustrazione di una geometria a forma di clessidra](images/transformgeometryexample-1.png)


```C++
void DemoApp::RenderGeometryExample()
{
    // Translate subsequent drawings by 20 device-independent pixels.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Translation(20.f, 20.f)
        );

    // Draw the hour glass geometry at the upper left corner of the client area.
    m_pRenderTarget->DrawGeometry(m_pPathGeometry, m_pBlackBrush, 10.f);
    m_pRenderTarget->FillGeometry(m_pPathGeometry, m_pLGBrush);
}
```

Il codice è stato omesso da questo esempio. Per altre informazioni sulle geometrie, vedere [Cenni preliminari sulle geometrie](direct2d-geometries-overview.md).
