---
title: Come ritagliare una maschera geometrica
description: Illustra come ritagliare un'area con livelli.
ms.assetid: eaeb6cfd-de62-46f1-972d-a11e0ccc11d9
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0c2258938020593014b5b6f5ea77516e7770f8589601cf4139971b3532b22fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569347"
---
# <a name="how-to-clip-to-a-geometric-mask"></a>Come ritagliare una maschera geometrica

Questo argomento descrive come usare una maschera geometrica per ritagliare un'area di un livello.

**Per ritagliare un'area con una maschera geometrica**

1.  Creare [**l'id2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) che verrà usato per ritagliare l'area.
2.  Chiamare [**ID2D1RenderTarget::CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) per creare un livello.
3.  Chiamare [**ID2D1RenderTarget::P ushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e passare la maschera geometrica definita nel passaggio 1.
4.  Disegnare il contenuto da ritagliare.
5.  Chiamare [**ID2D1RenderTarget::P opLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) per rimuovere il livello dalla destinazione di rendering.

L'esempio seguente usa una maschera geometrica per ritagliare un'immagine e diversi rettangoli. La figura seguente mostra la bitmap originale a sinistra e la bitmap ritagliata alla maschera geometrica a destra.

![Illustrazione di una bitmap goldfish prima e dopo che la bitmap viene ritagliata in una maschera a forma di stella](images/cliparegion-layers.png)

Per ritagliare il disegno come illustrato nella figura precedente, creare un [**id2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e usarlo per definire una stella. A tal fine, osservare il codice indicato di seguito.


```C++
// Create the path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
}

// Write to the path geometry using the geometry sink to create a star.
if (SUCCEEDED(hr))
{
    hr = m_pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
    pSink->BeginFigure(D2D1::Point2F(20, 50), D2D1_FIGURE_BEGIN_FILLED);
    pSink->AddLine(D2D1::Point2F(130, 50));
    pSink->AddLine(D2D1::Point2F(20, 130));
    pSink->AddLine(D2D1::Point2F(80, 0));
    pSink->AddLine(D2D1::Point2F(130, 130));
    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}

SafeRelease(&pSink);
```



Chiamare [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) per creare un livello.

> [!Note]  
> A partire Windows 8, non è necessario chiamare [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)). Nella maggior parte dei casi le prestazioni sono migliori se non si chiama questo metodo e Direct2D gestisce le risorse del livello.

 

Chiamare [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) con la maschera geometrica per eseguire il push del livello. Disegnare il contenuto da ritagliare, quindi chiamare [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) per visualizzare il livello. Questo produce il disegno a forma di stella. A tal fine, osservare il codice indicato di seguito.


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dei livelli](direct2d-layers-overview.md)
</dt> <dt>

[Informazioni di riferimento su Direct2D](reference.md)
</dt> </dl>

 

 