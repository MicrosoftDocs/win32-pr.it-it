---
title: Cenni preliminari sulle geometrie del percorso
description: Viene descritto come usare le geometrie di tracciato per definire forme complesse.
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0189c46f50e2ccc9ecc4523a4bb6f34006e59139
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104566295"
---
# <a name="path-geometries-overview"></a>Cenni preliminari sulle geometrie del percorso

Questo argomento descrive come usare le geometrie del percorso Direct2D per creare disegni complessi. Include le sezioni seguenti:

-   [Prerequisiti](#prerequisites)
-   [Geometrie di percorso in Direct2D](#path-geometries-in-direct2d)
-   [Uso di un ID2D1GeometrySink per popolare una geometria del percorso](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [Esempio: creare un disegno complesso](#example-create-a-complex-drawing)
    -   [Creare una geometria del percorso per la montagna sinistra](#create-a-path-geometry-for-the-left-mountain)
    -   [Creare una geometria del percorso per la montagna corretta](#create-a-path-geometry-for-the-right-mountain)
    -   [Creare una geometria del percorso per il sole](#create-a-path-geometry-for-the-sun)
    -   [Creare una geometria del percorso per il fiume](#create-a-path-geometry-for-the-river)
    -   [Eseguire il rendering delle geometrie di tracciato sullo schermo](#render-the-path-geometries-onto-the-display)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

In questa panoramica si presuppone che l'utente abbia familiarità con la creazione di applicazioni Direct2D di base, come descritto in [creazione di una semplice applicazione Direct2D](direct2d-quickstart.md). Si presuppone anche che l'utente abbia familiarità con le funzionalità di base delle geometrie Direct2D, come descritto in [Cenni preliminari sulle geometrie](direct2d-geometries-overview.md).

## <a name="path-geometries-in-direct2d"></a>Geometrie di percorso in Direct2D

Le geometrie del percorso sono rappresentate dall'interfaccia [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) . Per creare un'istanza di una geometria del percorso, chiamare il metodo [**ID2D1Factory:: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) . Questi oggetti possono essere usati per descrivere figure geometriche complesse costituite da segmenti come archi, curve e linee. Per popolare una geometria del percorso con figure e segmenti, chiamare il metodo [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) per recuperare un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) e usare i metodi del sink Geometry per aggiungere figure e segmenti alla geometria del percorso.

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a>Uso di un ID2D1GeometrySink per popolare una geometria del percorso

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) descrive un percorso geometrico che può contenere linee, archi, curve di Bézier cubiche e curve di Bézier quadratiche.

Un sink di geometria è costituito da una o più cifre. Ogni figura è costituita da uno o più segmenti di linea, curva o arco. Per creare una figura, chiamare il metodo [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) , passando il punto di partenza della figura, quindi usare i metodi Add, ad esempio [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) e [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per aggiungere segmenti. Al termine dell'aggiunta dei segmenti, chiamare il metodo [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) . È possibile ripetere questa sequenza per creare figure aggiuntive. Al termine della creazione delle figure, chiamare il metodo [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) .

## <a name="example-create-a-complex-drawing"></a>Esempio: creare un disegno complesso

Nella figura seguente viene illustrato un disegno complesso con linee, archi e curve di Bezier. Nell'esempio di codice seguente viene illustrato come creare il disegno usando quattro oggetti Geometry di percorso, uno per la montagna sinistra, uno per la montagna destra, uno per il fiume e uno per il sole con flare.

![illustrazione di un fiume, delle montagne e del sole, usando geometrie di percorso](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a>Creare una geometria del percorso per la montagna sinistra

Nell'esempio viene innanzitutto creata una geometria del percorso per la montagna sinistra, come illustrato nella figura seguente.

![Mostra un disegno complesso di un poligono che mostra una montagna.](images/path-geo-leftmnt.png)

Per creare la montagna sinistra, nell'esempio viene chiamato il metodo [**ID2D1Factory:: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) per creare un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



Nell'esempio viene quindi usato il metodo [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) per ottenere un sink di geometria da un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e archiviarlo nella variabile *pSink* .


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



Nell'esempio viene quindi chiamato [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), passando [**nella \_ Figura d2d1 \_ Begin \_ filled**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) che indica che questa figura è compilata, quindi chiama [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), passando una matrice di punti di [**d2d1 \_ punto \_ 2F**](d2d1-point-2f.md) , (267, 177), (236, 192), (212, 160), (156, 255) e (346, 255).

A tal fine, osservare il codice indicato di seguito.


```C++
pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

pSink->BeginFigure(
    D2D1::Point2F(346,255),
    D2D1_FIGURE_BEGIN_FILLED
    );
D2D1_POINT_2F points[5] = {
   D2D1::Point2F(267, 177),
   D2D1::Point2F(236, 192),
   D2D1::Point2F(212, 160),
   D2D1::Point2F(156, 255),
   D2D1::Point2F(346, 255), 
   };
pSink->AddLines(points, ARRAYSIZE(points));
pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
```



### <a name="create-a-path-geometry-for-the-right-mountain"></a>Creare una geometria del percorso per la montagna corretta

Nell'esempio viene quindi creata un'altra geometria del percorso per la montagna corretta con i punti (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263) e (575, 263). L'illustrazione seguente mostra come viene visualizzata la montagna corretta.

![illustrazione di un poligono che mostra una montagna](images/path-geo-rightmnt.png)

A tal fine, osservare il codice indicato di seguito.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRightMountainGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRightMountainGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

                pSink->BeginFigure(
                    D2D1::Point2F(575,263),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                D2D1_POINT_2F points[] = {
                   D2D1::Point2F(481, 146),
                   D2D1::Point2F(449, 181),
                   D2D1::Point2F(433, 159),
                   D2D1::Point2F(401, 214),
                   D2D1::Point2F(381, 199), 
                   D2D1::Point2F(323, 263), 
                   D2D1::Point2F(575, 263)
                   };
                pSink->AddLines(points, ARRAYSIZE(points));
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-sun"></a>Creare una geometria del percorso per il sole

Nell'esempio viene quindi popolata un'altra geometria del percorso per il Dom, come illustrato nella figura seguente.

![illustrazione di curve arco e Bezier che mostrano il sole](images/path-geo-sun.png)

A tale scopo, la geometria del percorso crea un sink e aggiunge una figura per l'arco e una figura per ogni bagliore al sink. Ripetendo la sequenza di [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), i metodi Add (ad esempio [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) e [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), vengono aggiunte più cifre al sink.

A tal fine, osservare il codice indicato di seguito.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pSunGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pSunGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
            
                pSink->BeginFigure(
                    D2D1::Point2F(270, 255),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddArc(
                    D2D1::ArcSegment(
                        D2D1::Point2F(440, 255), // end point
                        D2D1::SizeF(85, 85),
                        0.0f, // rotation angle
                        D2D1_SWEEP_DIRECTION_CLOCKWISE,
                        D2D1_ARC_SIZE_SMALL
                        ));            
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

                pSink->BeginFigure(
                    D2D1::Point2F(299, 182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(299, 182),
                       D2D1::Point2F(294, 176),
                       D2D1::Point2F(285, 178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(276, 179),
                       D2D1::Point2F(272, 173),
                       D2D1::Point2F(272, 173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(354, 156),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(354, 156),
                       D2D1::Point2F(358, 149),
                       D2D1::Point2F(354, 142)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(349, 134),
                       D2D1::Point2F(354, 127),
                       D2D1::Point2F(354, 127)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(322,164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(322, 164),
                       D2D1::Point2F(322, 156),
                       D2D1::Point2F(314, 152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(306, 149),
                       D2D1::Point2F(305, 141),
                       D2D1::Point2F(305, 141)
                       ));              
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(385, 164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(385,164),
                       D2D1::Point2F(392,161),
                       D2D1::Point2F(394,152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(395,144),
                       D2D1::Point2F(402,141),
                       D2D1::Point2F(402,142)
                       ));                
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(408,182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(408,182),
                       D2D1::Point2F(416,184),
                       D2D1::Point2F(422,178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(428,171),
                       D2D1::Point2F(435,173),
                       D2D1::Point2F(435,173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-river"></a>Creare una geometria del percorso per il fiume

Nell'esempio viene quindi creato un altro percorso geometrico per il fiume che contiene curve di Bezier. La figura seguente mostra come viene visualizzato il fiume.

![illustrazione delle curve di Bezier che mostrano un fiume](images/path-geo-river.png)

A tal fine, osservare il codice indicato di seguito.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRiverGeometry);
    
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRiverGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
                pSink->BeginFigure(
                    D2D1::Point2F(183, 392),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(238, 284),
                       D2D1::Point2F(472, 345),
                       D2D1::Point2F(356, 303)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(237, 261),
                       D2D1::Point2F(333, 256),
                       D2D1::Point2F(333, 256)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(335, 257),
                       D2D1::Point2F(241, 261),
                       D2D1::Point2F(411, 306)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(574, 350),
                       D2D1::Point2F(288, 324),
                       D2D1::Point2F(296, 392)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
```



### <a name="render-the-path-geometries-onto-the-display"></a>Eseguire il rendering delle geometrie di tracciato sullo schermo

Il codice seguente illustra come eseguire il rendering delle geometrie del percorso popolato sullo schermo. Disegna e disegna prima di tutto la geometria solare, successiva la geometria della montagna sinistra, quindi la geometria del fiume e infine la geometria della montagna corretta.


```C++
 m_pRenderTarget->BeginDraw();

 m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

 m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

 D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
 m_pRenderTarget->FillRectangle(
     D2D1::RectF(0, 0, rtSize.width, rtSize.height),
     m_pGridPatternBitmapBrush
     );

 m_pRenderTarget->FillGeometry(m_pSunGeometry, m_pRadialGradientBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pSunGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::OliveDrab, 1.f));
 m_pRenderTarget->FillGeometry(m_pLeftMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pLeftMountainGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::LightSkyBlue, 1.f));
 m_pRenderTarget->FillGeometry(m_pRiverGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRiverGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::YellowGreen, 1.f));
 m_pRenderTarget->FillGeometry(m_pRightMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRightMountainGeometry, m_pSceneBrush, 1.f);


 hr = m_pRenderTarget->EndDraw();
```



Nell'esempio completo viene restituita la figura seguente.

![illustrazione di un fiume, delle montagne e del sole, usando geometrie di percorso](images/path-geo-mnts.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'applicazione Direct2D semplice](direct2d-quickstart.md)
</dt> <dt>

[Panoramica delle geometrie](direct2d-geometries-overview.md)
</dt> </dl>

 

 