---
title: Come creare e riempire una forma di base
description: In questo argomento viene descritto come creare una forma di base.
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6b6b5a6fb08ac962475c2f0aa2812b4c3ae5da03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104558238"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a><span data-ttu-id="6aa83-103">Come creare e riempire una forma di base</span><span class="sxs-lookup"><span data-stu-id="6aa83-103">How to Draw and Fill a Basic Shape</span></span>

<span data-ttu-id="6aa83-104">In questo argomento viene descritto come creare una forma di base.</span><span class="sxs-lookup"><span data-stu-id="6aa83-104">This topic describes how to draw a basic shape.</span></span> <span data-ttu-id="6aa83-105">L'interfaccia [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) fornisce metodi per la struttura e il riempimento di ellissi, rettangoli e linee.</span><span class="sxs-lookup"><span data-stu-id="6aa83-105">The [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface provides methods for outlining and filling ellipses, rectangles, and lines.</span></span> <span data-ttu-id="6aa83-106">Negli esempi seguenti viene illustrato come creare e creare un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="6aa83-106">The following examples show how to create and draw an ellipse.</span></span>

<span data-ttu-id="6aa83-107">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6aa83-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="6aa83-108">Disegnare il contorno di un'ellisse con un tratto a tinta unita</span><span class="sxs-lookup"><span data-stu-id="6aa83-108">Draw the Outline of an Ellipse with a Solid Stroke</span></span>](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [<span data-ttu-id="6aa83-109">Disegnare un'ellisse con un tratto tratteggiato</span><span class="sxs-lookup"><span data-stu-id="6aa83-109">Draw an Ellipse with a Dashed Stroke</span></span>](#draw-an-ellipse-with-a-dashed-stroke)
-   [<span data-ttu-id="6aa83-110">Creare e riempire un'ellisse</span><span class="sxs-lookup"><span data-stu-id="6aa83-110">Draw and Fill an Ellipse</span></span>](#draw-and-fill-an-ellipse)
-   [<span data-ttu-id="6aa83-111">Disegno di forme più complesse</span><span class="sxs-lookup"><span data-stu-id="6aa83-111">Drawing More Complex Shapes</span></span>](#drawing-more-complex-shapes)
-   [<span data-ttu-id="6aa83-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6aa83-112">Related topics</span></span>](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a><span data-ttu-id="6aa83-113">Disegnare il contorno di un'ellisse con un tratto a tinta unita</span><span class="sxs-lookup"><span data-stu-id="6aa83-113">Draw the Outline of an Ellipse with a Solid Stroke</span></span>

<span data-ttu-id="6aa83-114">Per disegnare la struttura di un'ellisse, è necessario definire un pennello, ad esempio [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) o [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), per disegnare il contorno e un' [**\_ ellisse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) per descrivere la posizione e le dimensioni dell'ellisse, quindi passare questi oggetti al metodo [**ID2D1RenderTarget::D rawellipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) .</span><span class="sxs-lookup"><span data-stu-id="6aa83-114">To draw the outline of an ellipse, you define a brush (such as a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) for painting the outline and a [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) for describing the ellipse's position and dimensions, then pass these objects to the [**ID2D1RenderTarget::DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="6aa83-115">L'esempio seguente crea un pennello tinta unita nero e lo archivia nel \_ membro della classe m spBlackBrush.</span><span class="sxs-lookup"><span data-stu-id="6aa83-115">The following example creates a black solid color brush and stores it in the m\_spBlackBrush class member.</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



<span data-ttu-id="6aa83-116">L'esempio seguente definisce un' [**\_ ellisse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) e la USA con il pennello definito nell'esempio precedente per disegnare il contorno di un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="6aa83-116">The next example defines an [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) and uses it with the brush defined in the previous example to draw the outline of an ellipse.</span></span> <span data-ttu-id="6aa83-117">Questo esempio produce l'output illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="6aa83-117">This example produces the output shown in the following illustration.</span></span>

![illustrazione di un'ellisse con un tratto a tinta unita](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a><span data-ttu-id="6aa83-119">Disegnare un'ellisse con un tratto tratteggiato</span><span class="sxs-lookup"><span data-stu-id="6aa83-119">Draw an Ellipse with a Dashed Stroke</span></span>

<span data-ttu-id="6aa83-120">Nell'esempio precedente è stato usato un tratto normale.</span><span class="sxs-lookup"><span data-stu-id="6aa83-120">The preceding example used a plain stroke.</span></span> <span data-ttu-id="6aa83-121">È possibile modificare l'aspetto di un tratto in diversi modi creando un [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle).</span><span class="sxs-lookup"><span data-stu-id="6aa83-121">You can modify the look of a stroke in several ways by creating an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle).</span></span> <span data-ttu-id="6aa83-122">**ID2D1StrokeStyle** consente di specificare la forma all'inizio e alla fine di un tratto, se dispone di uno schema di tratteggio e così via.</span><span class="sxs-lookup"><span data-stu-id="6aa83-122">The **ID2D1StrokeStyle** lets you specify the shape at the beginning and end of a stroke, whether it has a dash pattern, and so on.</span></span> <span data-ttu-id="6aa83-123">Nell'esempio seguente viene creato un **ID2D1StrokeStyle** che descrive un tratto tratteggiato.</span><span class="sxs-lookup"><span data-stu-id="6aa83-123">The following example creates an **ID2D1StrokeStyle** that describes a dashed stroke.</span></span> <span data-ttu-id="6aa83-124">Questo esempio usa un modello Dash predefinito, [**d2d1 Dash \_ \_ Style \_ Dash \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), ma è anche possibile specificarne uno personalizzato.</span><span class="sxs-lookup"><span data-stu-id="6aa83-124">This example uses a predefined dash pattern, [**D2D1\_DASH\_STYLE\_DASH\_DOT\_DOT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), but you can also specify your own.</span></span>


```C++
D2D1_STROKE_STYLE_PROPERTIES strokeStyleProperties = D2D1::StrokeStyleProperties(
    D2D1_CAP_STYLE_FLAT,  // The start cap.
    D2D1_CAP_STYLE_FLAT,  // The end cap.
    D2D1_CAP_STYLE_TRIANGLE, // The dash cap.
    D2D1_LINE_JOIN_MITER, // The line join.
    10.0f, // The miter limit.
    D2D1_DASH_STYLE_DASH_DOT_DOT, // The dash style.
    0.0f // The dash offset.
    );

hr = m_pDirect2dFactory->CreateStrokeStyle(strokeStyleProperties, NULL, 0, &m_pStrokeStyle);

```



<span data-ttu-id="6aa83-125">Nell'esempio seguente viene usato lo stile del tratto con il metodo [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) .</span><span class="sxs-lookup"><span data-stu-id="6aa83-125">The next example uses the stroke style with the [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="6aa83-126">Questo esempio produce l'output illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="6aa83-126">This example produces the output shown in the following illustration.</span></span>

![illustrazione di un'ellisse con tratto tratteggiato](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a><span data-ttu-id="6aa83-128">Creare e riempire un'ellisse</span><span class="sxs-lookup"><span data-stu-id="6aa83-128">Draw and Fill an Ellipse</span></span>

<span data-ttu-id="6aa83-129">Per disegnare l'area interna di un'ellisse, usare il metodo [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) .</span><span class="sxs-lookup"><span data-stu-id="6aa83-129">To paint the interior of an ellipse, you use the [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method.</span></span> <span data-ttu-id="6aa83-130">Nell'esempio seguente viene usato il metodo [**DrawEllipse**]/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse (constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) per delineare l'ellisse, quindi viene usato il metodo **FillEllipse** per disegnare l'interno.</span><span class="sxs-lookup"><span data-stu-id="6aa83-130">The following example uses the [**DrawEllipse**]/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method to outline the ellipse, then uses the **FillEllipse** method to paint its interior.</span></span> <span data-ttu-id="6aa83-131">Questo esempio produce l'output illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="6aa83-131">This example produces the output shown in the following illustration.</span></span>

![illustrazione di un'ellisse con un tratto tratteggiato e quindi riempito con un colore grigio a tinta unita](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



<span data-ttu-id="6aa83-133">Nell'esempio successivo viene prima riempito l'ellisse, quindi ne viene disegnato il contorno.</span><span class="sxs-lookup"><span data-stu-id="6aa83-133">The next example fills the ellipse first, then draws its outline.</span></span> <span data-ttu-id="6aa83-134">Questo esempio produce l'output illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="6aa83-134">This example produces the output shown in the following illustration.</span></span>

![illustrazione di un'ellisse riempita con un colore grigio a tinta unita e quindi delineata con un tratto tratteggiato](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



<span data-ttu-id="6aa83-136">Il codice è stato omesso da questi esempi.</span><span class="sxs-lookup"><span data-stu-id="6aa83-136">Code has been omitted from these examples.</span></span>

## <a name="drawing-more-complex-shapes"></a><span data-ttu-id="6aa83-137">Disegno di forme più complesse</span><span class="sxs-lookup"><span data-stu-id="6aa83-137">Drawing More Complex Shapes</span></span>

<span data-ttu-id="6aa83-138">Per creare forme più complesse, è necessario definire gli oggetti ID2D1Geometry e usarli con i metodi [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="6aa83-138">To draw more complex shapes, you define ID2D1Geometry objects and use them with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods.</span></span> <span data-ttu-id="6aa83-139">Per altre informazioni, vedere [Cenni preliminari sulle geometrie](direct2d-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6aa83-139">For more information, see the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6aa83-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6aa83-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6aa83-141">Panoramica delle geometrie</span><span class="sxs-lookup"><span data-stu-id="6aa83-141">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="6aa83-142">Panoramica dei pennelli</span><span class="sxs-lookup"><span data-stu-id="6aa83-142">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

 

 