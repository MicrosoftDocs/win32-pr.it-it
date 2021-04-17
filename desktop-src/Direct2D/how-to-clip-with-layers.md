---
title: Come ritagliare una maschera geometrica
description: Viene illustrato come ritagliare un'area con livelli.
ms.assetid: eaeb6cfd-de62-46f1-972d-a11e0ccc11d9
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 979281fb7fa6e034894bffaecbd6246fe8a9aa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473726"
---
# <a name="how-to-clip-to-a-geometric-mask"></a><span data-ttu-id="657d5-103">Come ritagliare una maschera geometrica</span><span class="sxs-lookup"><span data-stu-id="657d5-103">How to Clip to a Geometric Mask</span></span>

<span data-ttu-id="657d5-104">Questo argomento descrive come usare una maschera geometrica per ritagliare un'area di un livello.</span><span class="sxs-lookup"><span data-stu-id="657d5-104">This topic describes how to use a geometric mask to clip a region of a layer.</span></span>

<span data-ttu-id="657d5-105">**Per ritagliare un'area con una maschera geometrica**</span><span class="sxs-lookup"><span data-stu-id="657d5-105">**To clip a region with a geometric mask**</span></span>

1.  <span data-ttu-id="657d5-106">Creare il [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) che verrà usato per ritagliare l'area.</span><span class="sxs-lookup"><span data-stu-id="657d5-106">Create the [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) that will be used to clip the region.</span></span>
2.  <span data-ttu-id="657d5-107">Chiamare [**ID2D1RenderTarget:: CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) per creare un livello.</span><span class="sxs-lookup"><span data-stu-id="657d5-107">Call [**ID2D1RenderTarget::CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>
3.  <span data-ttu-id="657d5-108">Chiamare [**ID2D1RenderTarget::P ushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e passare la maschera geometrica definita nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="657d5-108">Call [**ID2D1RenderTarget::PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and pass the geometric mask you defined in step 1.</span></span>
4.  <span data-ttu-id="657d5-109">Consente di creare il contenuto da ritagliare.</span><span class="sxs-lookup"><span data-stu-id="657d5-109">Draw the content to clip.</span></span>
5.  <span data-ttu-id="657d5-110">Chiamare [**ID2D1RenderTarget::P OPlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) per rimuovere il livello dalla destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="657d5-110">Call [**ID2D1RenderTarget::PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to remove the layer from the render target.</span></span>

<span data-ttu-id="657d5-111">Nell'esempio seguente viene usata una maschera geometrica per ritagliare un'immagine e diversi rettangoli.</span><span class="sxs-lookup"><span data-stu-id="657d5-111">The example that follows uses a geometric mask to clip an image and several rectangles.</span></span> <span data-ttu-id="657d5-112">Nella figura seguente viene mostrata la bitmap originale a sinistra e la bitmap ritagliata sulla maschera geometrica a destra.</span><span class="sxs-lookup"><span data-stu-id="657d5-112">The following illustration shows the original bitmap on the left, and the bitmap clipped to the geometric mask on the right.</span></span>

![illustrazione di una bitmap Goldfish prima e dopo che la bitmap viene ritagliata in una maschera a forma di stella](images/cliparegion-layers.png)

<span data-ttu-id="657d5-114">Per ritagliare il disegno come illustrato nella figura precedente, creare un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e usarlo per definire una stella.</span><span class="sxs-lookup"><span data-stu-id="657d5-114">To clip the drawing as shown in the preceding illustration, you create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and use it to define a star.</span></span> <span data-ttu-id="657d5-115">A tal fine, osservare il codice indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="657d5-115">The following code shows how to do this.</span></span>


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



<span data-ttu-id="657d5-116">Chiamare [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) per creare un livello.</span><span class="sxs-lookup"><span data-stu-id="657d5-116">Call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>

> [!Note]  
> <span data-ttu-id="657d5-117">A partire da Windows 8, non è necessario chiamare [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)).</span><span class="sxs-lookup"><span data-stu-id="657d5-117">Starting with Windows 8, you don't need to call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)).</span></span> <span data-ttu-id="657d5-118">Nella maggior parte dei casi le prestazioni sono migliori se non si chiama questo metodo e Direct2D gestisce le risorse del livello.</span><span class="sxs-lookup"><span data-stu-id="657d5-118">In most situations performance is better if you don't call this method and Direct2D manages the layer resources.</span></span>

 

<span data-ttu-id="657d5-119">Chiamare [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) con la maschera di geometria per eseguire il push del livello.</span><span class="sxs-lookup"><span data-stu-id="657d5-119">Call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) with the geometry mask to push the layer.</span></span> <span data-ttu-id="657d5-120">Creare il contenuto da ritagliare, quindi chiamare [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) per estrarre il livello.</span><span class="sxs-lookup"><span data-stu-id="657d5-120">Draw the content to clip, then call [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to pop the layer.</span></span> <span data-ttu-id="657d5-121">Viene generato il disegno a forma di stella.</span><span class="sxs-lookup"><span data-stu-id="657d5-121">This produces the star-shaped drawing.</span></span> <span data-ttu-id="657d5-122">A tal fine, osservare il codice indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="657d5-122">The following code shows how to do this.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="657d5-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="657d5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="657d5-124">Panoramica sui livelli</span><span class="sxs-lookup"><span data-stu-id="657d5-124">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> <dt>

[<span data-ttu-id="657d5-125">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="657d5-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 