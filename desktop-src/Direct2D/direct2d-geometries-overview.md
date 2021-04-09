---
title: 'Panoramica delle geometrie '
description: Vengono descritte le nozioni di base delle geometrie Direct2D, ovvero gli oggetti che è possibile utilizzare per rappresentare, modificare e analizzare le forme.
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Direct2D, Cenni preliminari sulle geometrie
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cb97b0737bfad391fb9ba2501793a970fcbd9886
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734570"
---
# <a name="geometries-overview"></a><span data-ttu-id="7c9a1-104">Panoramica delle geometrie </span><span class="sxs-lookup"><span data-stu-id="7c9a1-104">Geometries overview</span></span>

<span data-ttu-id="7c9a1-105">In questa panoramica viene descritto come creare e utilizzare oggetti [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) per definire e modificare le cifre 2D.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-105">This overview describes how to create and use [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) objects to define and manipulate 2D figures.</span></span> <span data-ttu-id="7c9a1-106">Include le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c9a1-106">It contains the following sections.</span></span>

## <a name="what-is-a-direct2d-geometry"></a><span data-ttu-id="7c9a1-107">Che cos'è una geometria Direct2D?</span><span class="sxs-lookup"><span data-stu-id="7c9a1-107">What is a Direct2D geometry?</span></span>

<span data-ttu-id="7c9a1-108">Una geometria Direct2D è un oggetto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) .</span><span class="sxs-lookup"><span data-stu-id="7c9a1-108">A Direct2D geometry is an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object.</span></span> <span data-ttu-id="7c9a1-109">Questo oggetto può essere una geometria semplice ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)o [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), una geometria del percorso ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) o una geometria composita ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) e [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).</span><span class="sxs-lookup"><span data-stu-id="7c9a1-109">This object can be a simple geometry ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), or [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), a path geometry ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)), or a composite geometry ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) and [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).</span></span>

<span data-ttu-id="7c9a1-110">Le geometrie Direct2D consentono di descrivere le cifre bidimensionali e offrono molti utilizzi, ad esempio la definizione di aree di hit test, aree di ritaglio e persino percorsi di animazione.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-110">Direct2D geometries enable you to describe two-dimensional figures and offer many uses, such as defining hit-test regions, clip regions, and even animation paths.</span></span>

<span data-ttu-id="7c9a1-111">Le geometrie Direct2D sono risorse non modificabili e indipendenti dal dispositivo create da [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="7c9a1-111">Direct2D geometries are immutable and device-independent resources created by [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span> <span data-ttu-id="7c9a1-112">In genere, è necessario creare geometrie una volta e mantenerle per la durata dell'applicazione o fino a quando non è necessario modificarle.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-112">Generally, you should create geometries one time and keep them for the life of the application, or until they have to be changed.</span></span> <span data-ttu-id="7c9a1-113">Per altre informazioni sulle risorse indipendenti dal dispositivo e dipendenti dal dispositivo, vedere [Panoramica delle risorse](resources-and-resource-domains.md).</span><span class="sxs-lookup"><span data-stu-id="7c9a1-113">For more information about device-independent and device-dependent resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="7c9a1-114">Le sezioni seguenti descrivono i diversi tipi di geometrie.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-114">The following sections describe the different kinds of geometries.</span></span>

## <a name="simple-geometries"></a><span data-ttu-id="7c9a1-115">Geometrie semplici</span><span class="sxs-lookup"><span data-stu-id="7c9a1-115">Simple geometries</span></span>

<span data-ttu-id="7c9a1-116">Le geometrie semplici includono oggetti [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)e [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) e possono essere usati per creare figure geometriche di base, ad esempio rettangoli, rettangoli arrotondati, cerchi e ellissi.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-116">Simple geometries include [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), and [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects, and can be used to create basic geometric figures, such as rectangles, rounded rectangles, circles, and ellipses.</span></span>

<span data-ttu-id="7c9a1-117">Per creare una geometria semplice, usare uno dei metodi [**ID2D1Factory:: create<*GeometryType*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .</span><span class="sxs-lookup"><span data-stu-id="7c9a1-117">To create a simple geometry, use one of the [**ID2D1Factory::Create<*geometryType*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) methods.</span></span> <span data-ttu-id="7c9a1-118">Questi metodi creano un oggetto del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-118">These methods create an object of the specified type.</span></span> <span data-ttu-id="7c9a1-119">Per creare, ad esempio, un rettangolo, chiamare [**ID2D1Factory:: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), che restituisce un oggetto [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) ; per creare un rettangolo arrotondato, chiamare [**ID2D1Factory:: CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), che restituisce un oggetto [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) e così via.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-119">For example, to create a rectangle, call [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), which returns an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object; to create a rounded rectangle, call [**ID2D1Factory::CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), which returns an [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) object, and so on.</span></span>

<span data-ttu-id="7c9a1-120">Nell'esempio di codice seguente viene chiamato il metodo [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) , passando una struttura ellisse con il *centro* impostato su (100, 100), *x-RADIUS* a 100 e *y-RADIUS* a 50.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-120">The following code example calls the [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) method, passing in an ellipse structure with the *center* set to (100, 100), *x-radius* to 100, and *y-radius* to 50.</span></span> <span data-ttu-id="7c9a1-121">Chiama quindi [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), passando la geometria dei puntini di sospensione restituita, un puntatore a una [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)nera e una larghezza del tratto di 5.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-121">Then, it calls [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), passing in the returned ellipse geometry, a pointer to a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), and a stroke width of 5.</span></span> <span data-ttu-id="7c9a1-122">La figura seguente mostra l'output dell'esempio di codice.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-122">The following illustration shows the output from the code example.</span></span>

![illustrazione di un'ellisse](images/geometry-ovw-drawstep6.png)


```C++
ID2D1EllipseGeometry *m_pEllipseGeometry;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateEllipseGeometry(
        D2D1::Ellipse(D2D1::Point2F(100.f, 60.f), 100.f, 50.f),
        &m_pEllipseGeometry
        );
}
```




```C++
m_pRenderTarget->DrawGeometry(m_pEllipseGeometry, m_pBlackBrush, 5);
```



<span data-ttu-id="7c9a1-124">Per disegnare la struttura di qualsiasi geometria, usare il metodo [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) .</span><span class="sxs-lookup"><span data-stu-id="7c9a1-124">To draw the outline of any geometry, use the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method.</span></span> <span data-ttu-id="7c9a1-125">Per disegnare l'interno, usare il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="7c9a1-125">To paint its interior, use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

## <a name="path-geometries"></a><span data-ttu-id="7c9a1-126">Geometrie percorso</span><span class="sxs-lookup"><span data-stu-id="7c9a1-126">Path geometries</span></span>

<span data-ttu-id="7c9a1-127">Le geometrie del percorso sono rappresentate dall'interfaccia [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="7c9a1-127">Path geometries are represented by the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface.</span></span> <span data-ttu-id="7c9a1-128">Questi oggetti possono essere usati per descrivere figure geometriche complesse costituite da segmenti come archi, curve e linee.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-128">These objects can be used to describe complex geometric figures composed of segments such as arcs, curves, and lines.</span></span> <span data-ttu-id="7c9a1-129">Nella figura seguente viene illustrato un disegno creato utilizzando la geometria del percorso.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-129">The following illustration shows a drawing created by using path geometry.</span></span>

![illustrazione di un fiume, delle montagne e del sole](images/path-geo-mnts.png)

<span data-ttu-id="7c9a1-131">Per altre informazioni ed esempi, vedere [Cenni preliminari sulle geometrie del percorso](path-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7c9a1-131">For more information and examples, see the [Path Geometries Overview](path-geometries-overview.md).</span></span>

## <a name="composite-geometries"></a><span data-ttu-id="7c9a1-132">Geometrie composite</span><span class="sxs-lookup"><span data-stu-id="7c9a1-132">Composite geometries</span></span>

<span data-ttu-id="7c9a1-133">Una geometria composita è una geometria raggruppata o combinata con un altro oggetto Geometry o con una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-133">A composite geometry is a geometry grouped or combined with another geometry object, or with a transform.</span></span> <span data-ttu-id="7c9a1-134">Le geometrie composite includono oggetti [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) e [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) .</span><span class="sxs-lookup"><span data-stu-id="7c9a1-134">Composite geometries include [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) and [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) objects.</span></span>

### <a name="geometry-groups"></a><span data-ttu-id="7c9a1-135">Gruppi di geometria</span><span class="sxs-lookup"><span data-stu-id="7c9a1-135">Geometry groups</span></span>

<span data-ttu-id="7c9a1-136">I gruppi Geometry rappresentano un modo pratico per raggruppare contemporaneamente più geometrie, in modo che tutte le cifre di diverse geometrie vengano concatenate in una sola.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-136">Geometry groups are a convenient way to group several geometries at the same time so all figures of several distinct geometries are concatenated into one.</span></span> <span data-ttu-id="7c9a1-137">Per creare un oggetto [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) , chiamare il metodo [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) sull'oggetto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , passando il *FillMode* con i valori possibili della [**modalità di \_ riempimento \_ d2d1 \_ alternativa**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternativa) e **la \_ \_ modalità di \_ riempimento d2d1**, una matrice di oggetti Geometry da aggiungere al gruppo Geometry e il numero di elementi in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-137">To create a [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) object, call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) method on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in the *fillMode* with possible values of [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternate) and **D2D1\_FILL\_MODE\_WINDING**, an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>

<span data-ttu-id="7c9a1-138">Nell'esempio di codice riportato di seguito viene innanzitutto dichiarata una matrice di oggetti Geometry.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-138">The following code example first declares an array of geometry objects.</span></span> <span data-ttu-id="7c9a1-139">Questi oggetti sono quattro cerchi concentrici con i raggi seguenti: 25, 50, 75 e 100.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-139">These objects are four concentric circles that have the following radii: 25, 50, 75, and 100.</span></span> <span data-ttu-id="7c9a1-140">Chiamare quindi il metodo [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) sull'oggetto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , passando in [**\_ \_ modalità di riempimento \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), una matrice di oggetti Geometry da aggiungere al gruppo Geometry e il numero di elementi in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-140">Then call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>


```C++
ID2D1Geometry *ppGeometries[] =
{
    m_pEllipseGeometry1,
    m_pEllipseGeometry2,
    m_pEllipseGeometry3,
    m_pEllipseGeometry4
};

hr = m_pD2DFactory->CreateGeometryGroup(
    D2D1_FILL_MODE_ALTERNATE,
    ppGeometries,
    ARRAYSIZE(ppGeometries),
    &m_pGeoGroup_AlternateFill
    );

if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateGeometryGroup(
        D2D1_FILL_MODE_WINDING,
        ppGeometries,
        ARRAYSIZE(ppGeometries),
        &m_pGeoGroup_WindingFill
        );
}
```

<span data-ttu-id="7c9a1-141">Nella figura seguente sono illustrati i risultati del rendering delle due geometrie di gruppo dall'esempio.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-141">The following illustration shows the results of rendering the two group geometries from the example.</span></span>

![illustrazione di due set di quattro cerchi concentrici, uno con anelli alternati pieni e uno con tutti gli anelli riempiti](images/create-geometry-group.png)

### <a name="transformed-geometries"></a><span data-ttu-id="7c9a1-143">Geometrie trasformate</span><span class="sxs-lookup"><span data-stu-id="7c9a1-143">Transformed geometries</span></span>

<span data-ttu-id="7c9a1-144">Esistono diversi modi per trasformare una geometria.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-144">There are multiple ways to transform a geometry.</span></span> <span data-ttu-id="7c9a1-145">È possibile utilizzare il metodo [**setransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) di una destinazione di rendering per trasformare tutti gli elementi che la destinazione di rendering disegna oppure è possibile associare una trasformazione direttamente a una geometria utilizzando il metodo [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) per creare un [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7c9a1-145">You can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of a render target to transform everything that the render target draws, or you can associate a transform directly with a geometry by using the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) method to create an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).</span></span>

<span data-ttu-id="7c9a1-146">Il metodo da usare dipende dall'effetto desiderato.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-146">The method that you should use depends on the effect that you want.</span></span> <span data-ttu-id="7c9a1-147">Quando si usa la destinazione di rendering per trasformare ed eseguire il rendering di una geometria, la trasformazione influiscono su tutti gli elementi relativi alla geometria, inclusa la larghezza di qualsiasi tratto applicato.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-147">When you use the render target to transform and then render a geometry, the transform affects everything about the geometry, including the width of any stroke that you have applied.</span></span> <span data-ttu-id="7c9a1-148">D'altra parte, quando si usa un [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), la trasformazione influiscono solo sulle coordinate che descrivono la forma.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-148">On the other hand, when you use an [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), the transform affects only the coordinates that describe the shape.</span></span> <span data-ttu-id="7c9a1-149">La trasformazione non influirà sullo spessore del tratto quando viene disegnata la geometria.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-149">The transformation will not affect the stroke thickness when the geometry is drawn.</span></span>

> [!Note]  
> <span data-ttu-id="7c9a1-150">A partire da Windows 8, la trasformazione globale non influisce sullo spessore del tratto dei tratti con [**\_ tipo di trasformazione Stroke d2d1 di \_ \_ tipo \_ fixed**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)o [**d2d1 \_ Stroke \_ Transform \_ \_**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).</span><span class="sxs-lookup"><span data-stu-id="7c9a1-150">Starting with Windows 8 the world transform will not affect the stroke thickness of strokes with [**D2D1\_STROKE\_TRANSFORM\_TYPE\_FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)or [**D2D1\_STROKE\_TRANSFORM\_TYPE\_HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).</span></span> <span data-ttu-id="7c9a1-151">È consigliabile usare questi tipi di trasformazione per ottenere tratti di trasformazione indipendenti</span><span class="sxs-lookup"><span data-stu-id="7c9a1-151">You should use these transform types to achieve transform independent strokes</span></span>

 

<span data-ttu-id="7c9a1-152">Nell'esempio seguente viene creato un [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), quindi viene disegnato senza trasformarlo.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-152">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), then draws it without transforming it.</span></span> <span data-ttu-id="7c9a1-153">Produce l'output mostrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-153">It produces the output shown in the following illustration.</span></span>

![illustrazione di un rettangolo](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```




```C++
// Draw the untransformed rectangle geometry.
m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="7c9a1-155">Nell'esempio seguente viene usata la destinazione di rendering per ridimensionare la geometria in base a un fattore 3, quindi viene disegnata.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-155">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="7c9a1-156">Nella figura seguente viene illustrato il risultato della creazione del rettangolo senza la trasformazione e con la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-156">The following illustration shows the result of drawing the rectangle without the transform and with the transform.</span></span> <span data-ttu-id="7c9a1-157">Si noti che il tratto è più spessa dopo la trasformazione, anche se lo spessore del tratto è 1.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-157">Notice that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

![illustrazione di un rettangolo più piccolo all'interno di un rettangolo più grande con un tratto più spessa](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="7c9a1-159">Nell'esempio seguente viene usato il metodo [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) per ridimensionare la geometria per un fattore 3, quindi viene disegnata.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-159">The next example uses the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="7c9a1-160">Produce l'output mostrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-160">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="7c9a1-161">Si noti che, anche se il rettangolo è più grande, il relativo tratto non è aumentato.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-161">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

![illustrazione di un rettangolo più piccolo all'interno di un rettangolo più grande con lo stesso spessore del tratto](images/transformedgeometry2-step3.png)


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
```




```C++
// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```



## <a name="geometries-as-masks"></a><span data-ttu-id="7c9a1-163">Geometrie come maschere</span><span class="sxs-lookup"><span data-stu-id="7c9a1-163">Geometries as masks</span></span>

<span data-ttu-id="7c9a1-164">Quando si chiama il metodo [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) , è possibile usare un oggetto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) come maschera geometrica.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-164">You can use an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object as a geometric mask when you call the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="7c9a1-165">La maschera geometrica specifica l'area del livello composito nella destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-165">The geometric mask specifies the area of the layer that is composited into the render target.</span></span> <span data-ttu-id="7c9a1-166">Per altre informazioni, vedere la sezione maschere geometriche della [Panoramica dei livelli](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7c9a1-166">For more information, see the Geometric Masks section of the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="geometric-operations"></a><span data-ttu-id="7c9a1-167">Operazioni geometriche</span><span class="sxs-lookup"><span data-stu-id="7c9a1-167">Geometric operations</span></span>

<span data-ttu-id="7c9a1-168">L'interfaccia [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) fornisce diverse operazioni geometriche che è possibile usare per modificare e misurare le cifre geometriche.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-168">The [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) interface provides several geometric operations that you can use to manipulate and measure geometric figures.</span></span> <span data-ttu-id="7c9a1-169">Ad esempio, è possibile usarli per calcolare e restituire i limiti, confrontare per vedere in che modo una geometria è correlata a livello spaziale a un'altra (utile per l'hit test), calcolare le aree e le lunghezze e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-169">For example, you can use them to calculate and return their bounds, compare to see how one geometry is spatially related to another (useful for hit testing), calculate the areas and lengths, and more.</span></span> <span data-ttu-id="7c9a1-170">Nella tabella seguente vengono descritte le operazioni geometriche comuni.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-170">The following table describes the common geometric operations.</span></span>



| <span data-ttu-id="7c9a1-171">Operazione</span><span class="sxs-lookup"><span data-stu-id="7c9a1-171">Operation</span></span>                                                   | <span data-ttu-id="7c9a1-172">Metodo</span><span class="sxs-lookup"><span data-stu-id="7c9a1-172">Method</span></span>                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c9a1-173">Combina</span><span class="sxs-lookup"><span data-stu-id="7c9a1-173">Combine</span></span>                                                     | [<span data-ttu-id="7c9a1-174">**CombineWithGeometry**</span><span class="sxs-lookup"><span data-stu-id="7c9a1-174">**CombineWithGeometry**</span></span>](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| <span data-ttu-id="7c9a1-175">Limiti/limiti estesi/recupera limiti, aggiornamento area dirty</span><span class="sxs-lookup"><span data-stu-id="7c9a1-175">Bounds/ Widened Bounds/Retrieve Bounds, Dirty Region update</span></span> | <span data-ttu-id="7c9a1-176">[**Ampliamento**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)</span><span class="sxs-lookup"><span data-stu-id="7c9a1-176">[**Widen**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)</span></span>                             |
| <span data-ttu-id="7c9a1-177">Hit Testing</span><span class="sxs-lookup"><span data-stu-id="7c9a1-177">Hit Testing</span></span>                                                 | <span data-ttu-id="7c9a1-178">[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [ **StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)</span><span class="sxs-lookup"><span data-stu-id="7c9a1-178">[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)</span></span>                                             |
| <span data-ttu-id="7c9a1-179">Stroke</span><span class="sxs-lookup"><span data-stu-id="7c9a1-179">Stroke</span></span>                                                      | [<span data-ttu-id="7c9a1-180">**StrokeContainsPoint**</span><span class="sxs-lookup"><span data-stu-id="7c9a1-180">**StrokeContainsPoint**</span></span>](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| <span data-ttu-id="7c9a1-181">Confronto</span><span class="sxs-lookup"><span data-stu-id="7c9a1-181">Comparison</span></span>                                                  | [<span data-ttu-id="7c9a1-182">**CompareWithGeometry**</span><span class="sxs-lookup"><span data-stu-id="7c9a1-182">**CompareWithGeometry**</span></span>](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| <span data-ttu-id="7c9a1-183">Semplificazione (rimuove archi e curve di Bézier quadratiche)</span><span class="sxs-lookup"><span data-stu-id="7c9a1-183">Simplification (removes arcs and quadratic Bezier curves)</span></span>   | [<span data-ttu-id="7c9a1-184">**Semplificare**</span><span class="sxs-lookup"><span data-stu-id="7c9a1-184">**Simplify**</span></span>](id2d1geometry-simplify.md)                                                                                                                                 |
| <span data-ttu-id="7c9a1-185">Suddivisione a mosaico</span><span class="sxs-lookup"><span data-stu-id="7c9a1-185">Tessellation</span></span>                                                | [<span data-ttu-id="7c9a1-186">**Conteggiarla suddividerla**</span><span class="sxs-lookup"><span data-stu-id="7c9a1-186">**Tessellate**</span></span>](id2d1geometry-tessellate.md)                                                                                                                             |
| <span data-ttu-id="7c9a1-187">Struttura (Rimuovi intersezione)</span><span class="sxs-lookup"><span data-stu-id="7c9a1-187">Outline (remove intersection)</span></span>                               | [<span data-ttu-id="7c9a1-188">**Riquadro**</span><span class="sxs-lookup"><span data-stu-id="7c9a1-188">**Outline**</span></span>](id2d1geometry-outline.md)                                                                                                                                   |
| <span data-ttu-id="7c9a1-189">Calcolare l'area o la lunghezza di una geometria</span><span class="sxs-lookup"><span data-stu-id="7c9a1-189">Calculate the area or length of a geometry</span></span>                  | <span data-ttu-id="7c9a1-190">[**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md)</span><span class="sxs-lookup"><span data-stu-id="7c9a1-190">[**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md)</span></span> |



 

> [!Note]  
> <span data-ttu-id="7c9a1-191">A partire da Windows 8, è possibile usare il metodo [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) in [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) per calcolare l'area o la lunghezza di una geometria.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-191">Starting in Windows 8, you can use the [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) method on the [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) to calculate the area or length of a geometry.</span></span>

 

### <a name="combining-geometries"></a><span data-ttu-id="7c9a1-192">Combinazione di geometrie</span><span class="sxs-lookup"><span data-stu-id="7c9a1-192">Combining geometries</span></span>

<span data-ttu-id="7c9a1-193">Per combinare una geometria con un'altra, chiamare il metodo [**ID2D1Geometry:: CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) .</span><span class="sxs-lookup"><span data-stu-id="7c9a1-193">To combine one geometry with another, call the [**ID2D1Geometry::CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) method.</span></span> <span data-ttu-id="7c9a1-194">Quando si combinano le geometrie, è possibile specificare uno dei quattro modi per eseguire l'operazione di combinazione, ovvero Unione [**d2d1 \_ \_ modalità \_ combinata**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Unione), [**\_ modalità combinata d2d1 \_ \_ Intersect**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Intersect), [**d2d1 \_ Combine \_ mode \_ Xor**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (XOR) e [**d2d1 \_ Combine \_ mode \_ Escludi**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Escludi).</span><span class="sxs-lookup"><span data-stu-id="7c9a1-194">When you combine the geometries, you specify one of the four ways to perform the combine operation: [**D2D1\_COMBINE\_MODE\_UNION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (union), [**D2D1\_COMBINE\_MODE\_INTERSECT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (intersect), [**D2D1\_COMBINE\_MODE\_XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (xor), and [**D2D1\_COMBINE\_MODE\_EXCLUDE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (exclude).</span></span> <span data-ttu-id="7c9a1-195">Nell'esempio di codice seguente vengono illustrati due cerchi combinati tramite la modalità di Unione delle unioni, in cui il primo cerchio ha il punto centrale di (75, 75) e il raggio di 50 e il secondo cerchio ha il punto centrale di (125, 75) e il raggio di 50.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-195">The following code example shows two circles that are combined by using the union combine mode, where the first circle has the center point of (75, 75) and the radius of 50, and the second circle has the center point of (125, 75) and the radius of 50.</span></span>


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}


if (SUCCEEDED(hr))
{
    //
    // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
    //
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

    if (SUCCEEDED(hr))
    {
        hr = m_pPathGeometryUnion->Open(&pGeometrySink);

        if (SUCCEEDED(hr))
        {
            hr = m_pCircleGeometry1->CombineWithGeometry(
                m_pCircleGeometry2,
                D2D1_COMBINE_MODE_UNION,
                NULL,
                NULL,
                pGeometrySink
                );
        }

        if (SUCCEEDED(hr))
        {
            hr = pGeometrySink->Close();
        }

        SafeRelease(&pGeometrySink);
    }
}
```



<span data-ttu-id="7c9a1-196">Nella figura seguente vengono illustrati due cerchi combinati con una modalità di combinazione di Union.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-196">The following illustration shows two circles combined with a combine mode of union.</span></span>

![illustrazione di due cerchi sovrapposti combinati in un'Unione](images/combine-mode-union.png)

<span data-ttu-id="7c9a1-198">Per illustrazioni di tutte le modalità di combinazione, vedere [**l' \_ enumerazione della \_ modalità di combinazione d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).</span><span class="sxs-lookup"><span data-stu-id="7c9a1-198">For illustrations of all the combine modes, see the [**D2D1\_COMBINE\_MODE enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).</span></span>

### <a name="widen"></a><span data-ttu-id="7c9a1-199">Ampliare</span><span class="sxs-lookup"><span data-stu-id="7c9a1-199">Widen</span></span>

<span data-ttu-id="7c9a1-200">Il metodo [**Wide**](id2d1geometry-widen.md) genera una nuova geometria il cui riempimento equivale a tracciare la geometria esistente e quindi scrive il risultato nell'oggetto [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) specificato.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-200">The [**Widen**](id2d1geometry-widen.md) method generates a new geometry whose fill is equivalent to stroking the existing geometry, and then writes the result to the specified [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) object.</span></span> <span data-ttu-id="7c9a1-201">Nell'esempio di codice seguente viene chiamato [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) sull'oggetto [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="7c9a1-201">The following code example calls [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) on the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object.</span></span> <span data-ttu-id="7c9a1-202">Se l' **apertura** ha esito positivo, viene chiamato **Wide** nell'oggetto Geometry.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-202">If **Open** succeeds, it calls **Widen** on the geometry object.</span></span>


```C++
ID2D1GeometrySink *pGeometrySink = NULL;
hr = pPathGeometry->Open(&pGeometrySink);
if (SUCCEEDED(hr))
{
    hr = pGeometry->Widen(
            strokeWidth,
            pIStrokeStyle,
            pWorldTransform,
            pGeometrySink
            );
```



### <a name="tessellate"></a><span data-ttu-id="7c9a1-203">Conteggiarla suddividerla</span><span class="sxs-lookup"><span data-stu-id="7c9a1-203">Tessellate</span></span>

<span data-ttu-id="7c9a1-204">Il metodo [**conteggiarla suddividerla**](id2d1geometry-tessellate.md) crea un set di triangoli con ferita in senso orario che coprono la geometria dopo che è stata trasformata utilizzando la matrice specificata e appiattita utilizzando la tolleranza specificata.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-204">The [**Tessellate**](id2d1geometry-tessellate.md) method creates a set of clockwise-wound triangles that cover the geometry after it is transformed by using the specified matrix and flattened by using the specified tolerance.</span></span> <span data-ttu-id="7c9a1-205">Nell'esempio di codice seguente viene usato **conteggiarla suddividerla** per creare un elenco di triangoli che rappresentano *pPathGeometry*.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-205">The following code example uses **Tessellate** to create a list of triangles that represent *pPathGeometry*.</span></span> <span data-ttu-id="7c9a1-206">I triangoli vengono archiviati in un [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh*, quindi trasferiti a un membro di classe, *m \_ pStrokeMesh*, per un uso successivo durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-206">The triangles are stored in an [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh*, then transferred to a class member, *m\_pStrokeMesh*, for later use when rendering.</span></span>


```C++
ID2D1Mesh *pMesh = NULL;
hr = m_pRT->CreateMesh(&pMesh);
if (SUCCEEDED(hr))
{
    ID2D1TessellationSink *pSink = NULL;
    hr = pMesh->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Tessellate(
                NULL, // world transform (already handled in Widen)
                pSink
                );
        if (SUCCEEDED(hr))
        {
            hr = pSink->Close();
            if (SUCCEEDED(hr))
            {
                SafeReplace(&m_pStrokeMesh, pMesh);
            }
        }
        pSink->Release();
    }
    pMesh->Release();
}
```



### <a name="fillcontainspoint-and-strokecontainspoint"></a><span data-ttu-id="7c9a1-207">FillContainsPoint e StrokeContainsPoint</span><span class="sxs-lookup"><span data-stu-id="7c9a1-207">FillContainsPoint and StrokeContainsPoint</span></span>

<span data-ttu-id="7c9a1-208">Il metodo [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) indica se l'area riempita dalla geometria contiene il punto specificato.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-208">The [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) method indicates whether the area filled by the geometry contains the specified point.</span></span> <span data-ttu-id="7c9a1-209">È possibile utilizzare questo metodo per eseguire l'hit testing.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-209">You can use this method to do hit testing.</span></span> <span data-ttu-id="7c9a1-210">Nell'esempio di codice seguente viene chiamato **FillContainsPoint** su un oggetto [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , passando un punto in (0, 0) e una matrice di [**identità**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) .</span><span class="sxs-lookup"><span data-stu-id="7c9a1-210">The following code example calls **FillContainsPoint** on an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) object, passing in a point at (0,0) and an [**Identity**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) matrix.</span></span>


```C++
BOOL containsPoint1;
hr = m_pCircleGeometry1->FillContainsPoint(
    D2D1::Point2F(0,0),
    D2D1::Matrix3x2F::Identity(),
    &containsPoint1
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



<span data-ttu-id="7c9a1-211">Il metodo [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) determina se il tratto della geometria contiene il punto specificato.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-211">The [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) method determines whether the geometry's stroke contains the specified point.</span></span> <span data-ttu-id="7c9a1-212">È possibile utilizzare questo metodo per eseguire l'hit testing.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-212">You can use this method to do hit testing.</span></span> <span data-ttu-id="7c9a1-213">Nell'esempio di codice seguente viene usato **StrokeContainsPoint**.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-213">The following code example uses **StrokeContainsPoint**.</span></span>


```C++
BOOL containsPoint;

hr = m_pCircleGeometry1->StrokeContainsPoint(
    D2D1::Point2F(0,0),
    10,     // stroke width
    NULL,   // stroke style
    NULL,   // world transform
    &containsPoint
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



### <a name="simplify"></a><span data-ttu-id="7c9a1-214">Semplificare </span><span class="sxs-lookup"><span data-stu-id="7c9a1-214">Simplify</span></span>

<span data-ttu-id="7c9a1-215">Il metodo [**semplifica**](id2d1geometry-simplify.md) rimuove archi e curve di Bézier quadratiche da una geometria specificata.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-215">The [**Simplify**](id2d1geometry-simplify.md) method removes arcs and quadratic Bezier curves from a specified geometry.</span></span> <span data-ttu-id="7c9a1-216">La geometria risultante contiene quindi solo le linee e, facoltativamente, le curve di Bézier cubiche.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-216">So, the resulting geometry contains only lines and, optionally, cubic Bezier curves.</span></span> <span data-ttu-id="7c9a1-217">Nell'esempio di codice seguente viene usato il comando **semplificato** per trasformare una geometria con curve di Bezier in una geometria che contiene solo segmenti di linea.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-217">The following code example uses **Simplify** to transform a geometry with Bezier curves into a geometry that contains only line segments.</span></span>


```C++
HRESULT D2DFlatten(
    ID2D1Geometry *pGeometry,
    float flatteningTolerance,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES,
                    NULL, // world transform
                    flatteningTolerance,
                    pSink
                    );

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="computelength-and-computearea"></a><span data-ttu-id="7c9a1-218">ComputeLength e ComputeArea</span><span class="sxs-lookup"><span data-stu-id="7c9a1-218">ComputeLength and ComputeArea</span></span>

<span data-ttu-id="7c9a1-219">Il metodo [**ComputeLength**](id2d1geometry-computelength.md) calcola la lunghezza della geometria specificata se ogni segmento è stato registrato in una riga.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-219">The [**ComputeLength**](id2d1geometry-computelength.md) method calculates the length of the specified geometry if each segment were unrolled into a line.</span></span> <span data-ttu-id="7c9a1-220">Questo include il segmento di chiusura implicito se la geometria viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-220">This includes the implicit closing segment if the geometry is closed.</span></span> <span data-ttu-id="7c9a1-221">Nell'esempio di codice seguente viene usato **ComputeLength** per calcolare la lunghezza di un cerchio specificato (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="7c9a1-221">The following code example uses **ComputeLength** to compute the length of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float length;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeLength(
    D2D1::IdentityMatrix(),
    &length
    );

if (SUCCEEDED(hr))
{
    // Process the length of the geometry.
}
```



<span data-ttu-id="7c9a1-222">Il metodo [**ComputeArea**](id2d1geometry-computearea.md) calcola l'area della geometria specificata.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-222">The [**ComputeArea**](id2d1geometry-computearea.md) method calculates the area of the specified geometry.</span></span> <span data-ttu-id="7c9a1-223">Nell'esempio di codice seguente viene usato **ComputeArea** per calcolare l'area di un cerchio specificato (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="7c9a1-223">The following code example uses **ComputeArea** to compute the area of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a><span data-ttu-id="7c9a1-224">CompareWithGeometry</span><span class="sxs-lookup"><span data-stu-id="7c9a1-224">CompareWithGeometry</span></span>

<span data-ttu-id="7c9a1-225">Il metodo [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) descrive l'intersezione tra la geometria che chiama questo metodo e la geometria specificata.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-225">The [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) method describes the intersection between the geometry that calls this method and the specified geometry.</span></span> <span data-ttu-id="7c9a1-226">I valori possibili per l'intersezione includono la relazione di geometria d2d1 (disgiunta), la **\_ relazione di geometria d2d1 \_ \_ è \_ contenuta** (is contained), la relazione di geometria **d2d1 \_ \_ \_ contiene** (Contains) e **d2d1 \_ Geometry \_ Relation \_** (sovrapposizioni). [**\_ \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation)</span><span class="sxs-lookup"><span data-stu-id="7c9a1-226">The possible values for intersection include [**D2D1\_GEOMETRY\_RELATION\_DISJOINT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (disjoint), **D2D1\_GEOMETRY\_RELATION\_IS\_CONTAINED** (is contained), **D2D1\_GEOMETRY\_RELATION\_CONTAINS** (contains), and **D2D1\_GEOMETRY\_RELATION\_OVERLAP** (overlap).</span></span> <span data-ttu-id="7c9a1-227">"disgiunto" significa che due riempimenti di geometria non si intersecano affatto.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-227">"disjoint" means that two geometry fills do not intersect at all.</span></span> <span data-ttu-id="7c9a1-228">"è contenuto" significa che la geometria è completamente contenuta dalla geometria specificata.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-228">"is contained" means that the geometry is completely contained by the specified geometry.</span></span> <span data-ttu-id="7c9a1-229">"Contains" significa che la geometria contiene completamente la geometria specificata e "sovrapposizione" significa che le due geometrie si sovrappongono, ma nessuna delle due contiene completamente l'altra.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-229">"contains" means that the geometry completely contains the specified geometry, and "overlap" means the two geometries overlap but neither completely contains the other.</span></span>

<span data-ttu-id="7c9a1-230">Nell'esempio di codice riportato di seguito viene illustrato come confrontare due cerchi con lo stesso raggio di 50 ma con offset di 50.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-230">The following code example shows how to compare two circles that have the same radius of 50 but are offset by 50.</span></span>


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}

```




```C++
D2D1_GEOMETRY_RELATION result = D2D1_GEOMETRY_RELATION_UNKNOWN;

// Compare circle1 with circle2
hr = m_pCircleGeometry1->CompareWithGeometry(
    m_pCircleGeometry2,
    D2D1::IdentityMatrix(),
    0.1f,
    &result
    );

if (SUCCEEDED(hr))
{
    static const WCHAR szGeometryRelation[] = L"Two circles overlap.";
    m_pRenderTarget->SetTransform(D2D1::IdentityMatrix());
    if (result == D2D1_GEOMETRY_RELATION_OVERLAP)
    {
        m_pRenderTarget->DrawText(
            szGeometryRelation,
            ARRAYSIZE(szGeometryRelation) - 1,
            m_pTextFormat,
            D2D1::RectF(25.0f, 160.0f, 200.0f, 300.0f),
            m_pTextBrush
            );
    }
}
```



### <a name="outline"></a><span data-ttu-id="7c9a1-231">Riquadro</span><span class="sxs-lookup"><span data-stu-id="7c9a1-231">Outline</span></span>

<span data-ttu-id="7c9a1-232">Il metodo di [**struttura**](id2d1geometry-outline.md) calcola il contorno della geometria (una versione della geometria in cui nessuna figura si interseca se stessa o qualsiasi altra figura) e scrive il risultato in un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span><span class="sxs-lookup"><span data-stu-id="7c9a1-232">The [**Outline**](id2d1geometry-outline.md) method computes the outline of the geometry (a version of the geometry in which no figure crosses itself or any other figure) and writes the result to an [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span> <span data-ttu-id="7c9a1-233">Nell'esempio di codice seguente viene usato il **contorno** per costruire una geometria equivalente senza alcuna intersezione automatica.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-233">The following code example uses **Outline** to construct an equivalent geometry without any self-intersections.</span></span> <span data-ttu-id="7c9a1-234">Usa la tolleranza di Flat predefinita.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-234">It uses the default flattening tolerance.</span></span>


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="getbounds-and-getwidenedbounds"></a><span data-ttu-id="7c9a1-235">GetBounds e GetWidenedBounds</span><span class="sxs-lookup"><span data-stu-id="7c9a1-235">GetBounds and GetWidenedBounds</span></span>

<span data-ttu-id="7c9a1-236">Il metodo [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) recupera i limiti della geometria.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-236">The [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) method retrieves the bounds of the geometry.</span></span> <span data-ttu-id="7c9a1-237">Nell'esempio di codice seguente viene usato **GetBounds** per recuperare i limiti di un cerchio specificato **( \_ m pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="7c9a1-237">The following code example uses **GetBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
D2D1_RECT_F bounds;

hr = m_pCircleGeometry1->GetBounds(
      D2D1::IdentityMatrix(),
      &bounds
     );

if (SUCCEEDED(hr))
{
    // Retrieve the bounds.
}
```



<span data-ttu-id="7c9a1-238">Il metodo [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) recupera i limiti della geometria dopo che è stato ampliato dalla larghezza e dallo stile del tratto specificato e trasformato dalla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-238">The [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) method retrieves the bounds of the geometry after it is widened by the specified stroke width and style and transformed by the specified matrix.</span></span> <span data-ttu-id="7c9a1-239">Nell'esempio di codice seguente viene usato **GetWidenedBounds** per recuperare i limiti di un cerchio specificato (**m \_ pCircleGeometry1**) dopo che è stato ampliato in base alla larghezza del tratto specificata.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-239">The following code example uses **GetWidenedBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**) after it is widened by the specified stroke width.</span></span>


```C++
float dashes[] = {1.f, 1.f, 2.f, 3.f, 5.f};

m_pD2DFactory->CreateStrokeStyle(
    D2D1::StrokeStyleProperties(
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_ROUND,
        D2D1_LINE_JOIN_ROUND,   // lineJoin
        10.f,   //miterLimit
        D2D1_DASH_STYLE_CUSTOM,
        0.f     //dashOffset
        ),
     dashes,
     ARRAYSIZE(dashes)-1,
     &m_pStrokeStyle
     );
```




```C++
D2D1_RECT_F bounds1;
hr = m_pCircleGeometry1->GetWidenedBounds(
      5.0,
      m_pStrokeStyle,
      D2D1::IdentityMatrix(),
      &bounds1
     );
if (SUCCEEDED(hr))
{
    // Retrieve the widened bounds.
}
```



### <a name="computepointatlength"></a><span data-ttu-id="7c9a1-240">ComputePointAtLength</span><span class="sxs-lookup"><span data-stu-id="7c9a1-240">ComputePointAtLength</span></span>

<span data-ttu-id="7c9a1-241">Il metodo [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) calcola il vettore punto e tangente alla distanza specificata lungo la geometria.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-241">The [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) method calculates the point and tangent vector at the specified distance along the geometry.</span></span> <span data-ttu-id="7c9a1-242">Nell'esempio di codice seguente viene usato **ComputePointAtLength**.</span><span class="sxs-lookup"><span data-stu-id="7c9a1-242">The following code example uses **ComputePointAtLength**.</span></span>


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a><span data-ttu-id="7c9a1-243">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c9a1-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c9a1-244">Cenni preliminari sulle geometrie del percorso</span><span class="sxs-lookup"><span data-stu-id="7c9a1-244">Path Geometries Overview</span></span>](path-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="7c9a1-245">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="7c9a1-245">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 