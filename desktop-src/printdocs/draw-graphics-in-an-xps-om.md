---
description: Questa pagina descrive come creare elementi grafici in un OM XPS.
ms.assetid: 2384b522-208a-48db-ae0d-f82fa0214d09
title: Creare grafica in un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabbf8cfb821c80dfff43e2e7844331c8920f726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311540"
---
# <a name="draw-graphics-in-an-xps-om"></a><span data-ttu-id="e6f80-103">Creare grafica in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="e6f80-103">Draw Graphics in an XPS OM</span></span>

<span data-ttu-id="e6f80-104">Questa pagina descrive come creare elementi grafici in un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="e6f80-104">This page describes how to draw graphics in an XPS OM.</span></span>

<span data-ttu-id="e6f80-105">Per creare grafica basata su vettori in una pagina, creare un'istanza di un'interfaccia [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) , popolarla con il contenuto desiderato e aggiungerla all'elenco di oggetti visivi della pagina o dell'area di disegno.</span><span class="sxs-lookup"><span data-stu-id="e6f80-105">To draw vector-based graphics in a page, instantiate an [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface, populate it with the desired content, and add it to the page's or canvas' list of visual objects.</span></span> <span data-ttu-id="e6f80-106">Un'interfaccia **IXpsOMPath** contiene le proprietà di una forma basata su vettori come contorno, colore di riempimento, stile della linea e colore della linea.</span><span class="sxs-lookup"><span data-stu-id="e6f80-106">An **IXpsOMPath** interface contains such properties of a vector-based shape as the outline, fill color, line style, and line color.</span></span> <span data-ttu-id="e6f80-107">La forma del percorso è specificata da un'interfaccia [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) , che contiene una raccolta di interfacce [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) e, facoltativamente, un'interfaccia [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) .</span><span class="sxs-lookup"><span data-stu-id="e6f80-107">The path's shape is specified by an [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface, which contains a collection of [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interfaces and, optionally, an [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) interface.</span></span> <span data-ttu-id="e6f80-108">È possibile usare qualsiasi interfaccia che eredita dall'interfaccia [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) per riempire il perimetro del tracciato e l'interno della forma descritta dal percorso.</span><span class="sxs-lookup"><span data-stu-id="e6f80-108">You can use any interface that inherits from the [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) interface to fill the perimeter of the path and the interior of the shape that is described by the path.</span></span>

<span data-ttu-id="e6f80-109">Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="e6f80-109">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="e6f80-110">Esempio di codice</span><span class="sxs-lookup"><span data-stu-id="e6f80-110">Code Example</span></span>

<span data-ttu-id="e6f80-111">Nell'esempio di codice seguente viene creato un percorso semplice che descrive un rettangolo riempito con un solo colore.</span><span class="sxs-lookup"><span data-stu-id="e6f80-111">The following code example creates a simple path that describes a rectangle that is filled with a single color.</span></span>

### <a name="create-the-stroke-and-the-fill-brushes"></a><span data-ttu-id="e6f80-112">Creare il tratto e i pennelli di riempimento</span><span class="sxs-lookup"><span data-stu-id="e6f80-112">Create the stroke and the fill brushes</span></span>

<span data-ttu-id="e6f80-113">Nella prima sezione dell'esempio di codice viene creato il [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) che verrà usato per riempire l'oggetto Path.</span><span class="sxs-lookup"><span data-stu-id="e6f80-113">The first section of the code example creates the [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) that will be used to fill the path object.</span></span>


```C++
    HRESULT               hr = S_OK;

    XPS_COLOR             xpsColor;
    IXpsOMSolidColorBrush *xpsFillBrush = NULL;
    IXpsOMSolidColorBrush *xpsStrokeBrush = NULL;

    // Set the fill brush color to RED.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColor,
        NULL,          // color profile resource
        &xpsFillBrush);
    // The color profile resource parameter is NULL because
    //  this color type does not use a color profile resource.

    // Set the stroke brush color to BLACK.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0x00;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
            &xpsColor,
            NULL, // This color type does not use a color profile resource.
            &xpsStrokeBrush);

    // The brushes are released below after they have been used.
```



### <a name="define-the-shape"></a><span data-ttu-id="e6f80-114">Definire la forma</span><span class="sxs-lookup"><span data-stu-id="e6f80-114">Define the shape</span></span>

<span data-ttu-id="e6f80-115">La seconda sezione dell'esempio di codice crea l'interfaccia [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) .</span><span class="sxs-lookup"><span data-stu-id="e6f80-115">The second section of the code example creates the [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface.</span></span> <span data-ttu-id="e6f80-116">Viene quindi creata l'interfaccia [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) che specifica la forma della figura e viene aggiunta la figura all'interfaccia **IXpsOMGeometry** .</span><span class="sxs-lookup"><span data-stu-id="e6f80-116">It then creates the [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interface that specifies the figure's shape, and adds the figure to the **IXpsOMGeometry** interface.</span></span> <span data-ttu-id="e6f80-117">Nell'esempio viene creato un rettangolo specificato da *Rect*.</span><span class="sxs-lookup"><span data-stu-id="e6f80-117">The example creates a rectangle that is specified by *rect*.</span></span> <span data-ttu-id="e6f80-118">È necessario definire i segmenti solo per tre dei quattro lati del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="e6f80-118">Segments must be defined for only three of the four sides of the rectangle.</span></span> <span data-ttu-id="e6f80-119">Il perimetro della forma, in questo caso il rettangolo, inizia dal punto iniziale ed estende come definito dai segmenti della figura Geometry.</span><span class="sxs-lookup"><span data-stu-id="e6f80-119">The perimeter of the shape, the rectangle in this case, starts from the start point and extends as defined by the segments of the geometry figure.</span></span> <span data-ttu-id="e6f80-120">Se si imposta la proprietà di **chiusura** su **true** , il rettangolo viene chiuso aggiungendo un segmento aggiuntivo che connette la fine dell'ultimo segmento al punto iniziale.</span><span class="sxs-lookup"><span data-stu-id="e6f80-120">Setting the **IsClosed** property to **TRUE** indicates that the rectangle is closed by adding one additional segment that connects the end of the last segment to the start point.</span></span>


```C++
    // rect is initialized outside of the sample and 
    //  contains the coordinates of the rectangular geometry to create.
    XPS_RECT                            rect = {0,0,100,100};       

    HRESULT                             hr = S_OK;
    IXpsOMGeometryFigure                *rectFigure;
    IXpsOMGeometry                      *imageRectGeometry;
    IXpsOMGeometryFigureCollection      *geomFigureCollection;

    // Define the start point and create an empty figure.
    XPS_POINT                           startPoint = {rect.x, rect.y};
    hr = xpsFactory->CreateGeometryFigure( &startPoint, &rectFigure );
    // Define the segments of the geometry figure.
    //  First, define the type of each segment.
    XPS_SEGMENT_TYPE segmentTypes[3] = {
        XPS_SEGMENT_TYPE_LINE,  // each segment is a straight line
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE
    };

    // Define the x and y coordinates of each corner of the figure
    //  the start point has already been defined so only the 
    //  remaining three corners need to be defined.
    FLOAT segmentData[6] = {
        rect.x,                (rect.y + rect.height),
        (rect.x + rect.width), (rect.y + rect.height), 
        (rect.x + rect.width), rect.y 
    };

    // Describe if the segments are stroked (that is if the segment lines
    //  should be drawn as a line).
    BOOL segmentStrokes[3] = {
        TRUE, TRUE, TRUE // Yes, draw each of the segment lines.
    };

    // Add the segment data to the figure.
    hr = rectFigure->SetSegments(
                        3, 
                        6, 
                        segmentTypes, 
                        segmentData, 
                        segmentStrokes);

    // Set the closed and filled properties of the figure.
    hr = rectFigure->SetIsClosed( TRUE );
    hr = rectFigure->SetIsFilled( TRUE );
 
    // Create the geometry object.
    hr = xpsFactory->CreateGeometry( &imageRectGeometry );
    
    // Get a pointer to the figure collection interface of the geometry...
    hr = imageRectGeometry->GetFigures( &geomFigureCollection );

    // ...and then add the figure created above to this geometry.
    hr = geomFigureCollection->Append( rectFigure );
    // If not needed for anything else, release the rectangle figure.
    rectFigure->Release();

    // when done adding figures, release the figure collection. 
    geomFigureCollection->Release();

    //  When done with the geometry object, release the object.
    // imageRectGeometry->Release();
    //  In this case, imageRectGeometry is used in the next sample
    //  so the geometry object is not released, yet.
    
```



### <a name="create-the-path-and-add-it-to-the-visual-collection"></a><span data-ttu-id="e6f80-121">Creare il percorso e aggiungerlo alla raccolta di oggetti visivi</span><span class="sxs-lookup"><span data-stu-id="e6f80-121">Create the path and add it to the visual collection</span></span>

<span data-ttu-id="e6f80-122">Nella sezione finale di questo esempio di codice viene creato e configurato l'oggetto Path, che viene quindi aggiunto all'elenco di oggetti visivi della pagina.</span><span class="sxs-lookup"><span data-stu-id="e6f80-122">The final section of this code example creates and configures the path object, then adds it to the page's list of visual objects.</span></span>


```C++
    HRESULT                    hr = S_OK;
    // The page interface pointer is initialized outside of this sample.
    IXpsOMPath                *rectPath = NULL;
    IXpsOMVisualCollection    *pageVisuals = NULL;

    // Create the new path object.
    hr = xpsFactory->CreatePath( &rectPath );

    // Add the geometry to the path.
    //  imageRectGeometry is initialized outside of this example.
    hr = rectPath->SetGeometryLocal( imageRectGeometry );

    // Set the short description of the path to provide
    //  a textual description of the object for accessibility.
    hr = rectPath->SetAccessibilityShortDescription( L"Red Rectangle" );
    
    // Set the fill and stroke brushes to use the brushes 
    //  created in the first section.
    hr = rectPath->SetFillBrushLocal( xpsFillBrush );
    hr = rectPath->SetStrokeBrushLocal( xpsStrokeBrush);

    // Get the visual collection of this page and add this path to it.
    hr = xpsPage->GetVisuals( &pageVisuals );
    hr = pageVisuals->Append( rectPath );
    // If not needed for anything else, release the rectangle path.
    rectPath->Release();
    
    // When done with the visual collection, release it.
    pageVisuals->Release();

    // When finished with the brushes, release the interface pointers.
    if (NULL != xpsFillBrush) xpsFillBrush->Release();
    if (NULL != xpsStrokeBrush) xpsStrokeBrush->Release();

    // When done with the geometry interface, release it.
    imageRectGeometry->Release();

    // When done with the path interface, release it.
    rectPath->Release();

```



## <a name="best-practices"></a><span data-ttu-id="e6f80-123">Procedure consigliate</span><span class="sxs-lookup"><span data-stu-id="e6f80-123">Best Practices</span></span>

<span data-ttu-id="e6f80-124">Aggiungere una descrizione testuale della forma specificata dall'interfaccia [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) .</span><span class="sxs-lookup"><span data-stu-id="e6f80-124">Add a textual description of the shape that is specified by the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface.</span></span> <span data-ttu-id="e6f80-125">Per il vantaggio di utenti con problemi visivi, usare i metodi [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) e [**SetAccessibilityLongDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) per fornire contenuti testuali per le funzionalità di supporto dell'accessibilità, ad esempio le utilità per la lettura dello schermo.</span><span class="sxs-lookup"><span data-stu-id="e6f80-125">For the benefit of visually impaired users, use the [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) and [**SetAccessibilityLongDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) methods to provide textual content for accessibility support features, such as screen readers.</span></span>

## <a name="additional-information"></a><span data-ttu-id="e6f80-126">Informazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="e6f80-126">Additional Information</span></span>

<span data-ttu-id="e6f80-127">L'esempio di codice in questa pagina usa un'interfaccia [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) come pennello di riempimento e pennello per il tratto per il percorso.</span><span class="sxs-lookup"><span data-stu-id="e6f80-127">The code example on this page uses an [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) interface as the fill brush and stroke brush for the path.</span></span> <span data-ttu-id="e6f80-128">Oltre all'interfaccia **IXpsOMSolidColorBrush** , è possibile usare un'interfaccia [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush), [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)o [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) .</span><span class="sxs-lookup"><span data-stu-id="e6f80-128">In addition to the **IXpsOMSolidColorBrush** interface, you can use an [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush), [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush), or [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) interface.</span></span>

<span data-ttu-id="e6f80-129">Il tratto è la linea che può essere disegnata intorno al perimetro della figura.</span><span class="sxs-lookup"><span data-stu-id="e6f80-129">The stroke is the line that can be drawn around the perimeter of the figure.</span></span> <span data-ttu-id="e6f80-130">La [specifica di XML Paper](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) supporta diversi stili di linee di tratto.</span><span class="sxs-lookup"><span data-stu-id="e6f80-130">The [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) supports many different stroke line styles.</span></span> <span data-ttu-id="e6f80-131">Per specificare lo stile della linea del tratto, impostare le proprietà del tratto con i seguenti metodi dell'interfaccia [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) :</span><span class="sxs-lookup"><span data-stu-id="e6f80-131">To specify the stroke line style, set the stroke properties with the following methods of the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface:</span></span>

-   <span data-ttu-id="e6f80-132">[**SetStrokeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) o [**SetStrokeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) per impostare il pennello del tratto</span><span class="sxs-lookup"><span data-stu-id="e6f80-132">[**SetStrokeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) or [**SetStrokeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) to set the stroke brush</span></span>
-   <span data-ttu-id="e6f80-133">[**GetStrokeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) per ottenere la raccolta Dash del tratto che descrive i tratti</span><span class="sxs-lookup"><span data-stu-id="e6f80-133">[**GetStrokeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) to get the stroke dash collection that describes the strokes</span></span>
-   <span data-ttu-id="e6f80-134">[**SetStrokeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) a e [**SetStrokeDashOffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) per descrivere l'aspetto di un tratto tratteggiato</span><span class="sxs-lookup"><span data-stu-id="e6f80-134">[**SetStrokeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) to and [**SetStrokeDashOffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) to describe the appearance of a dashed stroke</span></span>
-   <span data-ttu-id="e6f80-135">[**SetStrokeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) e [**SetStrokeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) per definire lo stile di terminazione della riga</span><span class="sxs-lookup"><span data-stu-id="e6f80-135">[**SetStrokeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) and [**SetStrokeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) to define the line termination style</span></span>
-   <span data-ttu-id="e6f80-136">[**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) e [**SetStrokeMiterLimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) per descrivere la modalità di Unione dei segmenti</span><span class="sxs-lookup"><span data-stu-id="e6f80-136">[**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) and [**SetStrokeMiterLimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) to describe how the segments are joined</span></span>
-   <span data-ttu-id="e6f80-137">[**SetStrokeThickness**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) per impostare lo spessore del tratto</span><span class="sxs-lookup"><span data-stu-id="e6f80-137">[**SetStrokeThickness**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) to set the stroke thickness</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6f80-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e6f80-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e6f80-139">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="e6f80-139">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="e6f80-140">Esplorare XPS OM</span><span class="sxs-lookup"><span data-stu-id="e6f80-140">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="e6f80-141">Scrivere testo in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="e6f80-141">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="e6f80-142">Inserire immagini in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="e6f80-142">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="e6f80-143">Scrivere un OM XPS in un documento XPS</span><span class="sxs-lookup"><span data-stu-id="e6f80-143">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="e6f80-144">Stampare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="e6f80-144">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="e6f80-145">**Usato in questa pagina**</span><span class="sxs-lookup"><span data-stu-id="e6f80-145">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="e6f80-146">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="e6f80-146">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="e6f80-147">**IXpsOMGeometry**</span><span class="sxs-lookup"><span data-stu-id="e6f80-147">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[<span data-ttu-id="e6f80-148">**IXpsOMGeometryFigure**</span><span class="sxs-lookup"><span data-stu-id="e6f80-148">**IXpsOMGeometryFigure**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[<span data-ttu-id="e6f80-149">**IXpsOMGeometryFigureCollection**</span><span class="sxs-lookup"><span data-stu-id="e6f80-149">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[<span data-ttu-id="e6f80-150">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="e6f80-150">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="e6f80-151">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="e6f80-151">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="e6f80-152">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="e6f80-152">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[<span data-ttu-id="e6f80-153">**IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="e6f80-153">**IXpsOMSolidColorBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="e6f80-154">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="e6f80-154">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="e6f80-155">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="e6f80-155">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="e6f80-156">Inizializzare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="e6f80-156">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="e6f80-157">Informazioni di riferimento sulle API documento XPS</span><span class="sxs-lookup"><span data-stu-id="e6f80-157">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="e6f80-158">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="e6f80-158">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
