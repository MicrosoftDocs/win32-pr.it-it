---
description: Viene descritto come posizionare le immagini in un OM XPS.
ms.assetid: 4c7e3630-7331-47d7-91cc-da3cc2b7f8c9
title: Inserire immagini in un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f72b5d1b1380cd870f9ff6b7a1cd15763e5b46c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317294"
---
# <a name="place-images-in-an-xps-om"></a><span data-ttu-id="d7fd6-103">Inserire immagini in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="d7fd6-103">Place Images in an XPS OM</span></span>

<span data-ttu-id="d7fd6-104">Viene descritto come posizionare le immagini in un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="d7fd6-104">Describes how to place images in an XPS OM.</span></span>

<span data-ttu-id="d7fd6-105">Per inserire le immagini in un OM XPS, creare un oggetto Path che definisca il percorso e il contorno di un'immagine, quindi usare un pennello immagine per riempire il percorso.</span><span class="sxs-lookup"><span data-stu-id="d7fd6-105">To place images in an XPS OM, create a path object that defines the location and outline of an image, then use an image brush to fill the path.</span></span> <span data-ttu-id="d7fd6-106">Aggiungere l'oggetto Path creato all'elenco di oggetti visivi della pagina o dell'area di disegno, in modo che sia possibile eseguirne il rendering con l'altro contenuto visivo.</span><span class="sxs-lookup"><span data-stu-id="d7fd6-106">Add the created path object to the page's or canvas' list of visual objects, so that it can be rendered with the other visual content.</span></span>

<span data-ttu-id="d7fd6-107">Prima di usare questi esempi di codice nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="d7fd6-107">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="d7fd6-108">Esempio di codice</span><span class="sxs-lookup"><span data-stu-id="d7fd6-108">Code Example</span></span>

### <a name="create-image-resource"></a><span data-ttu-id="d7fd6-109">Crea risorsa immagine</span><span class="sxs-lookup"><span data-stu-id="d7fd6-109">Create image resource</span></span>

<span data-ttu-id="d7fd6-110">Se l'immagine di origine non è disponibile in XPS OM come risorsa immagine, creare prima di tutto la risorsa immagine:</span><span class="sxs-lookup"><span data-stu-id="d7fd6-110">If the source image is not available in the XPS OM as an image resource, first create the image resource:</span></span>


```C++
    HRESULT                hr = S_OK;
    IStreamPtr             imageStream; // the resulting image stream
    IOpcPartUri            *imagePartUri;
    IXpsOMImageResource    *imageResource;

     XPS_RECT    rect = {0.0f, 0.0f, 0.0f, 0.0f}; // set to image size

    hr = xpsFactory->CreateReadOnlyStreamOnFile ( 
            imageFileName, &imageStream );

    hr = xpsFactory->CreatePartUri( imagePartName, &imagePartUri );

    imageType; // set to type of image being read in
    hr = xpsFactory->CreateImageResource ( 
        imageStream,
        imageType,
        imagePartUri,
        &imageResource);
    imagePartUri->Release();
    imageStream->Release();

    // imageResource can now be used by other parts in the XPS OM.
```



### <a name="place-image-into-visual-collection"></a><span data-ttu-id="d7fd6-111">Inserisci immagine nella raccolta visuale</span><span class="sxs-lookup"><span data-stu-id="d7fd6-111">Place image into visual collection</span></span>

<span data-ttu-id="d7fd6-112">Se l'immagine di origine è disponibile in XPS OM come risorsa immagine, può essere usata per creare un oggetto pennello immagine e aggiungerlo come pennello di riempimento al percorso che descrive la posizione e le dimensioni dell'immagine nella pagina.</span><span class="sxs-lookup"><span data-stu-id="d7fd6-112">If the source image is available in the XPS OM as an image resource, it can be used to create an image brush object and added as the fill brush to the path that describes the image location and size in the page.</span></span>


```C++
    // These variables are initialized outside of this code example,
    //  for example, as the parameters of a method or from some 
    //  preceding program code.

    // dimensions of the image in pixels
    XPS_SIZE    bmpDim = {0,0} ; 

    // DPI resolution values obtained from image
    FLOAT        dpiX = 96.0f;
    FLOAT        dpiY = 96.0f;
    
    // initialize viewport values 
    XPS_RECT    viewPort = {0.0,0.0,0.0,0.0};

    // initialize viewbox values
    XPS_RECT    viewBox = {0.0,0.0,0.0,0.0}; 

    // These are part of this code example.
    IXpsOMPath *imageRectPath;
    IXpsOMImageBrush *imageBrush;
    IXpsOMVisualCollection *pageVisuals;

    // Describe image source dimensions and set viewbox to be the 
    // entire image DIP width of image. 
    //  Example: 
    //    600 image pixels, 300 dpi -> 2 inches -> 2 * 96 = 192 DIP width
    viewBox.width = FLOAT((double)bmpDim.width * 96.0 / dpiX); 
    viewBox.height = FLOAT((double)bmpDim.height * 96.0 / dpiY);

    // Describe the size and position of the image destination.
    //  rect is an XPS_RECT structure that is initialized outside
    //  of this sample for example, it might be passed in as a parameter.

    // destination rectangle
    viewPort.x = rect.x;
    viewPort.y = rect.y;
    viewPort.width = rect.width;
    viewPort.height = rect.height;

    // Create the image brush.
    hr = xpsFactory->CreateImageBrush(imageResource, &viewBox, &viewPort, 
        reinterpret_cast<IXpsOMImageBrush**>(&imageBrush));

    // Create the path that describes the outline of the image on the page.
    //  This step uses the function described in the next code example.
    hr = CreateRectanglePath(xpsFactory, &rect,
        reinterpret_cast<IXpsOMPath**>(&imageRectPath));

    // Set the accessibility description for the path object as required.
    hr = imageRectPath->SetAccessibilityShortDescription( shortDescText );

    // Set the image brush to be the fill brush for this path.
    hr = imageRectPath->SetFillBrushLocal( imageBrush );

    // Get the list of visuals for this page...
    hr = xpsPage->GetVisuals( &pageVisuals );

    // ...and add the completed path to the list.
    hr = pageVisuals->Append( imageRectPath );

    // Release locally created interfaces.
    if (NULL != pageVisuals) pageVisuals->Release();
    if (NULL != imageRectPath) imageRectPath->Release();
    if (NULL != imageBrush) imageBrush->Release();

```



### <a name="create-path-object-for-image"></a><span data-ttu-id="d7fd6-113">Crea oggetto percorso per l'immagine</span><span class="sxs-lookup"><span data-stu-id="d7fd6-113">Create path object for image</span></span>

<span data-ttu-id="d7fd6-114">Il metodo seguente accetta una struttura di **\_ Rect XPS** e crea un percorso rettangolare.</span><span class="sxs-lookup"><span data-stu-id="d7fd6-114">The following method accepts an **XPS\_RECT** structure and creates a rectangular path.</span></span>


```C++
HRESULT 
CreateRectanglePath(
    __in  IXpsOMObjectFactory   *xpsFactory,
    __in  const XPS_RECT        *rect,
    __out IXpsOMPath            **rectPath
)
{
   
    HRESULT hr = S_OK;

    IXpsOMGeometryFigure           *rectFigure;
    IXpsOMGeometry                 *imageRectGeometry;
    IXpsOMGeometryFigureCollection *geomFigureCollection;

    // Define start point and three of the four sides of the rectangle.
    //  The fourth side is implied by setting the path type to CLOSED.
    XPS_POINT            startPoint = {rect->x, rect->y};
    XPS_SEGMENT_TYPE     segmentTypes[3] = {
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE
    };
    FLOAT segmentData[6] = {
        rect->x,              rect->y+rect->height, 
        rect->x+rect->width,  rect->y+rect->height, 
        rect->x+rect->width,  rect->y 
    };
    BOOL segmentStrokes[3] = {
        TRUE, TRUE, TRUE
    };

    // Create a closed geometry figure using the three 
    //  segments defined above.

    hr = xpsFactory->CreateGeometryFigure( &startPoint, &rectFigure );
    hr = rectFigure->SetIsClosed( TRUE );
    hr = rectFigure->SetIsFilled( TRUE );
    hr = rectFigure->SetSegments( 3, 6, 
            segmentTypes, segmentData, segmentStrokes );

    // Create a geometry that consists of the figure created above.
    hr = xpsFactory->CreateGeometry( &imageRectGeometry );
    hr = imageRectGeometry->GetFigures( &geomFigureCollection );
    hr = geomFigureCollection->Append( rectFigure );

    // Create the path that consists of the geometry created above
    //  and return the pointer in the parameter passed in to the function.
    hr = xpsFactory->CreatePath( reinterpret_cast<IXpsOMPath**>(rectPath) );
    hr = (*rectPath)->SetGeometryLocal( imageRectGeometry );

    // The calling method will release these interfaces when 
    //  it is done with them.

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d7fd6-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7fd6-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d7fd6-116">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="d7fd6-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="d7fd6-117">Esplorare XPS OM</span><span class="sxs-lookup"><span data-stu-id="d7fd6-117">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="d7fd6-118">Scrivere testo in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="d7fd6-118">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="d7fd6-119">Creare grafica in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="d7fd6-119">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="d7fd6-120">Scrivere un OM XPS in un documento XPS</span><span class="sxs-lookup"><span data-stu-id="d7fd6-120">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="d7fd6-121">Stampare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="d7fd6-121">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="d7fd6-122">**Usato in questa pagina**</span><span class="sxs-lookup"><span data-stu-id="d7fd6-122">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="d7fd6-123">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="d7fd6-123">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="d7fd6-124">**IXpsOMImageBrush**</span><span class="sxs-lookup"><span data-stu-id="d7fd6-124">**IXpsOMImageBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)
</dt> <dt>

[<span data-ttu-id="d7fd6-125">**IXpsOMImageResource**</span><span class="sxs-lookup"><span data-stu-id="d7fd6-125">**IXpsOMImageResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)
</dt> <dt>

[<span data-ttu-id="d7fd6-126">**IXpsOMGeometry**</span><span class="sxs-lookup"><span data-stu-id="d7fd6-126">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[<span data-ttu-id="d7fd6-127">**IXpsOMGeometryFigure**</span><span class="sxs-lookup"><span data-stu-id="d7fd6-127">**IXpsOMGeometryFigure**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[<span data-ttu-id="d7fd6-128">**IXpsOMGeometryFigureCollection**</span><span class="sxs-lookup"><span data-stu-id="d7fd6-128">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[<span data-ttu-id="d7fd6-129">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="d7fd6-129">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="d7fd6-130">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="d7fd6-130">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="d7fd6-131">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="d7fd6-131">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[<span data-ttu-id="d7fd6-132">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="d7fd6-132">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="d7fd6-133">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="d7fd6-133">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="d7fd6-134">Inizializzare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="d7fd6-134">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="d7fd6-135">Informazioni di riferimento sulle API documento XPS</span><span class="sxs-lookup"><span data-stu-id="d7fd6-135">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="d7fd6-136">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="d7fd6-136">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
