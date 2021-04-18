---
description: Questo argomento descrive come usare tipi diversi di pennelli in un OM XPS.
ms.assetid: 392ca1d5-283e-4eed-ae21-6477c469014d
title: Pennelli OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0557757bfaf81156b2015525d35897cfb042e44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310150"
---
# <a name="xps-om-brushes"></a><span data-ttu-id="61c3f-103">Pennelli OM XPS</span><span class="sxs-lookup"><span data-stu-id="61c3f-103">XPS OM Brushes</span></span>

<span data-ttu-id="61c3f-104">Questo argomento descrive come usare tipi diversi di pennelli in un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="61c3f-104">This topic describes how to use different types of brushes in an XPS OM.</span></span>

<span data-ttu-id="61c3f-105">I pennelli in XPS OM sono basati sull' [**interfaccia IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) e includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="61c3f-105">The brushes in the XPS OM are based on the [**IXpsOMBrush Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) and include the following:</span></span>

<dl> <span data-ttu-id="61c3f-106">Pennelli affiancati</span><span class="sxs-lookup"><span data-stu-id="61c3f-106">Tile Brushes</span></span>

-   [<span data-ttu-id="61c3f-107">**Interfaccia IXpsOMTileBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-107">**IXpsOMTileBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
-   [<span data-ttu-id="61c3f-108">**Interfaccia IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-108">**IXpsOMSolidColorBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
-   [<span data-ttu-id="61c3f-109">**Interfaccia IXpsOMVisualBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-109">**IXpsOMVisualBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
-   [<span data-ttu-id="61c3f-110">**Interfaccia IXpsOMImageBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-110">**IXpsOMImageBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)

  
<span data-ttu-id="61c3f-111">Pennelli sfumatura</span><span class="sxs-lookup"><span data-stu-id="61c3f-111">Gradient Brushes</span></span>

-   [<span data-ttu-id="61c3f-112">**Interfaccia IXpsOMGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-112">**IXpsOMGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
-   [<span data-ttu-id="61c3f-113">**Interfaccia IXpsOMLinearGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-113">**IXpsOMLinearGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
-   [<span data-ttu-id="61c3f-114">**Interfaccia IXpsOMRadialGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-114">**IXpsOMRadialGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)

  
</dl>

## <a name="code-examples"></a><span data-ttu-id="61c3f-115">Esempi di codice</span><span class="sxs-lookup"><span data-stu-id="61c3f-115">Code Examples</span></span>

### <a name="create-a-solid-color-brush"></a><span data-ttu-id="61c3f-116">Creare un pennello a tinta unita</span><span class="sxs-lookup"><span data-stu-id="61c3f-116">Create a solid-color brush</span></span>

<span data-ttu-id="61c3f-117">Nell'esempio di codice seguente viene creato un pennello a tinta unita da un valore di colore definito nel codice.</span><span class="sxs-lookup"><span data-stu-id="61c3f-117">The following code example creates a solid-color brush from a color value that is defined in the code.</span></span>


```C++
    HRESULT                hr = S_OK;

    XPS_COLOR              xpsColor;
    IXpsOMSolidColorBrush  *brush;

    // creates a solid red brush
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush(
       &xpsColor, 
       NULL, 
       reinterpret_cast<IXpsOMSolidColorBrush**>(&brush));
    
    // use brush

    // when finished with brush, release pointer
    brush->Release();
```



### <a name="create-a-visual-brush"></a><span data-ttu-id="61c3f-118">Creazione di un pennello visivo</span><span class="sxs-lookup"><span data-stu-id="61c3f-118">Create a visual brush</span></span>

<span data-ttu-id="61c3f-119">Nell'esempio di codice seguente viene creato un pennello da un oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="61c3f-119">The following code example creates a brush from a visual object.</span></span>


```C++
    HRESULT                       hr = S_OK;
    IXpsOMVisualBrush             *brush;

    XPS_RECT viewBoxRect = {0,0,0,0};
    XPS_RECT viewPortRect = {0,0,0,0};

    // set viewBoxRect to define the portion of the visual to use
    // as the brush.
    //
    // set viewPortRect to define the location and size of the 
    // the brush in the destination 
    //
    // create the brush
    hr = xpsFactory->CreateVisualBrush (
        &viewBoxRect,
        &viewPortRect,
        reinterpret_cast<IXpsOMVisualBrush**>(&brush));

    // assign the visual object
    //   brushVisual points to a visual
    //   that is defined outside of this example

    hr = brush->SetVisualLocal (brushVisual);
    
    // use brush
    
    // when finished with brush, release pointer
    brush->Release();
    
```



### <a name="create-an-image-brush"></a><span data-ttu-id="61c3f-120">Creare un pennello immagine</span><span class="sxs-lookup"><span data-stu-id="61c3f-120">Create an image brush</span></span>

<span data-ttu-id="61c3f-121">Vedere l'esempio di codice sulle [Immagini del posto in un OM XPS](place-images-in-an-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="61c3f-121">Refer to the code example in [Place Images in an XPS OM](place-images-in-an-xps-om.md).</span></span>

### <a name="create-a-linear-gradient-brush"></a><span data-ttu-id="61c3f-122">Creare un pennello a sfumatura lineare</span><span class="sxs-lookup"><span data-stu-id="61c3f-122">Create a linear-gradient brush</span></span>

<span data-ttu-id="61c3f-123">Nell'esempio di codice seguente viene creato un pennello a sfumatura lineare.</span><span class="sxs-lookup"><span data-stu-id="61c3f-123">The following code example creates a linear-gradient brush.</span></span> <span data-ttu-id="61c3f-124">La sfumatura presenta due cursori sfumatura.</span><span class="sxs-lookup"><span data-stu-id="61c3f-124">The gradient has two gradient stops.</span></span>


```C++
    HRESULT                       hr = S_OK;
    XPS_COLOR                     xpsColorStop;
    IXpsOMGradientStop            *xpsGradientStop1, *xpsGradientStop2;
    IXpsOMLinearGradientBrush     *brush;
    XPS_POINT                     startPoint, endPoint;

    // define the start color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xE4;
    xpsColorStop.value.sRGB.green = 0x3B;
    xpsColorStop.value.sRGB.blue  = 0x2F;
    
    // create a gradient stop by setting the color and location 
    // for the beginning of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop, 
        NULL, 
        0.0f,
        &xpsGradientStop1);
    startPoint.x = 375.75f;
    startPoint.y = 18.0f;

    // define the end color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xEF;
    xpsColorStop.value.sRGB.green = 0x79;
    xpsColorStop.value.sRGB.blue  = 0x2F;

    // create a gradient stop by setting the color and  location
    //  for the end of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop,
        NULL, 
        1.0f, 
        &xpsGradientStop2);
    endPoint.x   = 375.75f;
    endPoint.y   = 134.6f;

    // create the brush
    hr = xpsFactory->CreateLinearGradientBrush(
        xpsGradientStop1, 
        xpsGradientStop2, 
        &startPoint, 
        &endPoint, 
        &brush);
    // release gradient stops after creating brush
    xpsGradientStop1->Release();
    xpsGradientStop2->Release();

    // when finished with brush, release pointer to brush
    brush->Release();
```



## <a name="related-topics"></a><span data-ttu-id="61c3f-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61c3f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61c3f-126">**Interfaccia IXpsOMGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-126">**IXpsOMGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
</dt> <dt>

[<span data-ttu-id="61c3f-127">**Interfaccia IXpsOMImageBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-127">**IXpsOMImageBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)
</dt> <dt>

[<span data-ttu-id="61c3f-128">**Interfaccia IXpsOMLinearGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-128">**IXpsOMLinearGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
</dt> <dt>

[<span data-ttu-id="61c3f-129">**Interfaccia IXpsOMRadialGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-129">**IXpsOMRadialGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)
</dt> <dt>

[<span data-ttu-id="61c3f-130">**Interfaccia IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-130">**IXpsOMSolidColorBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="61c3f-131">**Interfaccia IXpsOMTileBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-131">**IXpsOMTileBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
</dt> <dt>

[<span data-ttu-id="61c3f-132">**Interfaccia IXpsOMVisualBrush**</span><span class="sxs-lookup"><span data-stu-id="61c3f-132">**IXpsOMVisualBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
</dt> <dt>

[<span data-ttu-id="61c3f-133">**\_colore XPS**</span><span class="sxs-lookup"><span data-stu-id="61c3f-133">**XPS\_COLOR**</span></span>](xps-color.md)
</dt> <dt>

[<span data-ttu-id="61c3f-134">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="61c3f-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



