---
title: Come disegnare e riempire una forma complessa
description: Direct2D fornisce l'interfaccia ID2D1PathGeometry per la descrizione di forme complesse che possono contenere curve, archi e linee. In questo argomento viene descritto come definire ed eseguire il rendering di una geometria del percorso.
ms.assetid: d7aad487-04e0-448d-bedf-b8dfadc7bbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a163e85d76a65f6b807ad1e4a9c9f740a32bf1
ms.sourcegitcommit: 4859402a45b9928c3e1354ded06b1d6a682a0be9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/30/2021
ms.locfileid: "106334291"
---
# <a name="how-to-draw-and-fill-a-complex-shape"></a><span data-ttu-id="93293-104">Come disegnare e riempire una forma complessa</span><span class="sxs-lookup"><span data-stu-id="93293-104">How to Draw and Fill a Complex Shape</span></span>

<span data-ttu-id="93293-105">Direct2D fornisce l'interfaccia [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) per la descrizione di forme complesse che possono contenere curve, archi e linee.</span><span class="sxs-lookup"><span data-stu-id="93293-105">Direct2D provides the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface for describing complex shapes that can contain curves, arcs, and lines.</span></span> <span data-ttu-id="93293-106">In questo argomento viene descritto come definire ed eseguire il rendering di una geometria del percorso.</span><span class="sxs-lookup"><span data-stu-id="93293-106">This topic describes how to define and render a path geometry.</span></span>

<span data-ttu-id="93293-107">Per definire una geometria del percorso, usare prima il metodo [**ID2D1Factory:: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) per creare la geometria del percorso, quindi usare il metodo [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) della geometria del percorso per recuperare un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span><span class="sxs-lookup"><span data-stu-id="93293-107">To define a path geometry, first use the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method to create the path geometry, then use the path geometry's [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to retrieve an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span></span> <span data-ttu-id="93293-108">È quindi possibile aggiungere linee, curve e archi chiamando i vari metodi di aggiunta del sink.</span><span class="sxs-lookup"><span data-stu-id="93293-108">You can then add lines, curves, and arcs by calling the sink's various Add methods.</span></span>

<span data-ttu-id="93293-109">Nell'esempio seguente viene creato un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), viene recuperato un sink e utilizzato per definire una forma di clessidra.</span><span class="sxs-lookup"><span data-stu-id="93293-109">The following example creates an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), retrieves a sink, and uses it to define an hourglass shape.</span></span>


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

<span data-ttu-id="93293-110">Si noti che un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) è una risorsa indipendente dal dispositivo e può, pertanto, essere creata una volta e conservata per la durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="93293-110">Note that an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) is a device-independent resource and can, therefore, be created once and retained for the life of the application.</span></span> <span data-ttu-id="93293-111">Per ulteriori informazioni sui diversi tipi di risorse, vedere [Cenni preliminari sulle risorse](resources-and-resource-domains.md).</span><span class="sxs-lookup"><span data-stu-id="93293-111">(For more information about different types of resources, see the [Resources Overview](resources-and-resource-domains.md).)</span></span>

<span data-ttu-id="93293-112">Nell'esempio seguente vengono creati due pennelli che verranno usati per disegnare il contorno e il riempimento della geometria del percorso.</span><span class="sxs-lookup"><span data-stu-id="93293-112">The next example creates two brushes that will be used to paint the path geometry's outline and fill.</span></span>


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



<span data-ttu-id="93293-113">L'esempio finale usa i metodi [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) per disegnare il contorno e l'interno della geometria.</span><span class="sxs-lookup"><span data-stu-id="93293-113">The final example uses the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods to paint the geometry's outline and interior.</span></span> <span data-ttu-id="93293-114">Questo esempio produce l'output illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="93293-114">This example produces the output shown in the following illustration.</span></span>

![illustrazione di una geometria a forma di clessidra](images/transformgeometryexample-1.png)


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

<span data-ttu-id="93293-116">Il codice è stato omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="93293-116">Code has been omitted from this example.</span></span> <span data-ttu-id="93293-117">Per altre informazioni sulle geometrie, vedere [Cenni preliminari sulle geometrie](direct2d-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="93293-117">For more information about geometries, see the [Geometries Overview](direct2d-geometries-overview.md).</span></span>
