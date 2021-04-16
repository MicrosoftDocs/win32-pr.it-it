---
title: Cenni preliminari sulle maschere di opacità
description: 'Questo argomento descrive come usare bitmap e pennelli per definire le maschere di opacità. Include le sezioni seguenti:'
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a4757a30247da465e0ae5226bd923219e3e665
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104564290"
---
# <a name="opacity-masks-overview"></a><span data-ttu-id="22bb9-104">Cenni preliminari sulle maschere di opacità</span><span class="sxs-lookup"><span data-stu-id="22bb9-104">Opacity Masks Overview</span></span>

<span data-ttu-id="22bb9-105">Questo argomento descrive come usare bitmap e pennelli per definire le maschere di opacità.</span><span class="sxs-lookup"><span data-stu-id="22bb9-105">This topic describes how to use bitmaps and brushes to define opacity masks.</span></span> <span data-ttu-id="22bb9-106">Include le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="22bb9-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="22bb9-107">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="22bb9-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="22bb9-108">Che cos'è una maschera di opacità?</span><span class="sxs-lookup"><span data-stu-id="22bb9-108">What Is an Opacity Mask?</span></span>](#what-is-an-opacity-mask)
-   [<span data-ttu-id="22bb9-109">Usare una bitmap come maschera di opacità con il metodo FillOpacityMask</span><span class="sxs-lookup"><span data-stu-id="22bb9-109">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [<span data-ttu-id="22bb9-110">Usare un pennello come maschera di opacità con il metodo FillGeometry</span><span class="sxs-lookup"><span data-stu-id="22bb9-110">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [<span data-ttu-id="22bb9-111">Usare un pennello sfumato lineare come maschera di opacità</span><span class="sxs-lookup"><span data-stu-id="22bb9-111">Use an Linear Gradient Brush as an Opacity Mask</span></span>](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [<span data-ttu-id="22bb9-112">Usare un pennello a sfumatura radiale come maschera di opacità</span><span class="sxs-lookup"><span data-stu-id="22bb9-112">Use a Radial Gradient Brush as an Opacity Mask</span></span>](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [<span data-ttu-id="22bb9-113">Applicare una maschera di opacità a un livello</span><span class="sxs-lookup"><span data-stu-id="22bb9-113">Apply an Opacity Mask to a Layer</span></span>](#apply-an-opacity-mask-to-a-layer)
-   [<span data-ttu-id="22bb9-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22bb9-114">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="22bb9-115">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="22bb9-115">Prerequisites</span></span>

<span data-ttu-id="22bb9-116">In questa panoramica si presuppone che l'utente abbia familiarità con le operazioni di disegno Direct2D di base, come descritto nella procedura dettagliata relativa alla [creazione di un'applicazione Direct2d semplice](direct2d-quickstart.md) .</span><span class="sxs-lookup"><span data-stu-id="22bb9-116">This overview assumes that you are familiar with basic Direct2D drawing operations, as described in the [Creating a Simple Direct2D Application](direct2d-quickstart.md) walkthrough.</span></span> <span data-ttu-id="22bb9-117">È anche necessario conoscere i diversi tipi di pennelli, come descritto nella panoramica dei [pennelli](direct2d-brushes-overview.md).</span><span class="sxs-lookup"><span data-stu-id="22bb9-117">You should also be familiar with the different types of brushes, as described in the [Brushes Overview](direct2d-brushes-overview.md).</span></span>

## <a name="what-is-an-opacity-mask"></a><span data-ttu-id="22bb9-118">Che cos'è una maschera di opacità?</span><span class="sxs-lookup"><span data-stu-id="22bb9-118">What Is an Opacity Mask?</span></span>

<span data-ttu-id="22bb9-119">Una maschera di opacità è una maschera, descritta da un pennello o una bitmap, applicata a un altro oggetto per rendere tale oggetto parzialmente o completamente trasparente.</span><span class="sxs-lookup"><span data-stu-id="22bb9-119">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="22bb9-120">Una maschera di opacità usa le informazioni sul canale alfa per specificare la modalità di fusione dei pixel di origine dell'oggetto nella destinazione finale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="22bb9-120">An opacity mask uses alpha channel information to specify how the source pixels of the object are blended into the final destination target.</span></span> <span data-ttu-id="22bb9-121">Le parti trasparenti della maschera indicano le aree in cui l'immagine sottostante è nascosta, mentre le parti opache della maschera indicano dove è visibile l'oggetto mascherato.</span><span class="sxs-lookup"><span data-stu-id="22bb9-121">The transparent portions of the mask indicate the areas where the underlying image is hidden, whereas the opaque portions of the mask indicate where the masked object is visible.</span></span>

<span data-ttu-id="22bb9-122">Esistono diversi modi per applicare una maschera di opacità:</span><span class="sxs-lookup"><span data-stu-id="22bb9-122">There are several ways to apply an opacity mask:</span></span>

-   <span data-ttu-id="22bb9-123">Usare il metodo [**ID2D1RenderTarget:: FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) .</span><span class="sxs-lookup"><span data-stu-id="22bb9-123">Use the [**ID2D1RenderTarget::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method.</span></span> <span data-ttu-id="22bb9-124">Il metodo **FillOpacityMask** disegna un'area rettangolare di una destinazione di rendering e quindi applica una maschera di opacità, definita da una bitmap.</span><span class="sxs-lookup"><span data-stu-id="22bb9-124">The **FillOpacityMask** method paints a rectangular region of a render target and then applies an opacity mask, defined by a bitmap.</span></span> <span data-ttu-id="22bb9-125">Utilizzare questo metodo quando la maschera di opacità è una bitmap e si desidera riempire un'area rettangolare.</span><span class="sxs-lookup"><span data-stu-id="22bb9-125">Use this method when your opacity mask is a bitmap and you want to fill a rectangular region.</span></span>
-   <span data-ttu-id="22bb9-126">Usare il metodo [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="22bb9-126">Use the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="22bb9-127">Il metodo **FillGeometry** disegna l'interno della geometria con il [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)specificato, quindi applica una maschera di opacità, definita da un pennello.</span><span class="sxs-lookup"><span data-stu-id="22bb9-127">The **FillGeometry** method paints the interior of geometry with the specified [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), then applies an opacity mask, defined by a brush.</span></span> <span data-ttu-id="22bb9-128">Utilizzare questo metodo quando si desidera applicare una maschera di opacità a una geometria o si desidera utilizzare un pennello come maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="22bb9-128">Use this method when you want to apply an opacity mask to a geometry or you want to use a brush as an opacity mask.</span></span>
-   <span data-ttu-id="22bb9-129">Usare un [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) per applicare una maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="22bb9-129">Use an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) to apply an opacity mask.</span></span> <span data-ttu-id="22bb9-130">Utilizzare questo approccio quando si desidera applicare una maschera di opacità a un gruppo di contenuto del disegno, non solo a una singola forma o immagine.</span><span class="sxs-lookup"><span data-stu-id="22bb9-130">Use this approach when you want to apply an opacity mask to a group of drawing content, not just a single shape or image.</span></span> <span data-ttu-id="22bb9-131">Per informazioni dettagliate, vedere [Cenni preliminari sui livelli](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="22bb9-131">For details, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a><span data-ttu-id="22bb9-132">Usare una bitmap come maschera di opacità con il metodo FillOpacityMask</span><span class="sxs-lookup"><span data-stu-id="22bb9-132">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>

<span data-ttu-id="22bb9-133">Il metodo [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) disegna un'area rettangolare di una destinazione di rendering e quindi applica una maschera di opacità, definita da un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="22bb9-133">The [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method paints a rectangular region of a render target and then applies an opacity mask, defined by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="22bb9-134">Utilizzare questo metodo quando si dispone di una bitmap che si desidera utilizzare come maschera di opacità per un'area rettangolare.</span><span class="sxs-lookup"><span data-stu-id="22bb9-134">Use this method when you have a bitmap that you want to use as an opacity mask for a rectangular region.</span></span>

<span data-ttu-id="22bb9-135">Il diagramma seguente mostra l'effetto dell'applicazione della maschera di opacità (un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) con un'immagine di un fiore) a un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con un'immagine di una pianta felce.</span><span class="sxs-lookup"><span data-stu-id="22bb9-135">The following diagram shows an effect of applying the opacity mask (an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with an image of a flower) to an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with an image of a fern plant.</span></span> <span data-ttu-id="22bb9-136">L'immagine risultante è una mappa di bit di un impianto ritagliata in forma floreale.</span><span class="sxs-lookup"><span data-stu-id="22bb9-136">The resulting image is a bitmap of a plant clipped to the flower shape.</span></span>

![diagramma di una bitmap floreale usata come maschera di opacità su un'immagine di una pianta di felce](images/brushes-ovw-bitmapopacity.png)

<span data-ttu-id="22bb9-138">Negli esempi di codice seguenti viene illustrato il modo in cui questa operazione viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="22bb9-138">The following code examples shows how this is accomplished.</span></span>

<span data-ttu-id="22bb9-139">Il primo esempio carica la bitmap seguente, *m \_ pBitmapMask*, da usare come maschera di bitmap.</span><span class="sxs-lookup"><span data-stu-id="22bb9-139">The first example loads the following bitmap, *m\_pBitmapMask*, for use as a bitmap mask.</span></span> <span data-ttu-id="22bb9-140">Nella figura seguente viene illustrato l'output generato.</span><span class="sxs-lookup"><span data-stu-id="22bb9-140">The following illustration shows the output that is produced.</span></span> <span data-ttu-id="22bb9-141">Si noti che, sebbene la parte opaca della bitmap appaia nera, le informazioni sul colore nella bitmap non hanno effetto sulla maschera di opacità. vengono utilizzate solo le informazioni di opacità di ogni pixel della bitmap.</span><span class="sxs-lookup"><span data-stu-id="22bb9-141">Note that, although the opaque portion of the bitmap appears black, the color information in the bitmap has no effect on the opacity mask; only the opacity information of each pixel in the bitmap is used.</span></span> <span data-ttu-id="22bb9-142">I pixel completamente opachi in questa bitmap sono stati colorati a scopo puramente illustrativo.</span><span class="sxs-lookup"><span data-stu-id="22bb9-142">The fully opaque pixels in this bitmap have been colored black for illustrative purposes only.</span></span>

![illustrazione della maschera di bit per i fiori](images/bitmapmask.png)

<span data-ttu-id="22bb9-144">In questo esempio, [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) viene caricato da un metodo helper, LoadResourceBitmap, definito altrove nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="22bb9-144">In this example, the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is loaded by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"BitmapMask",
                    L"Image",
                    &m_pBitmapMask
                    );
            }
```



<span data-ttu-id="22bb9-145">Nell'esempio successivo viene definito il pennello, *m \_ pFernBitmapBrush*, a cui viene applicata la maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="22bb9-145">The next example defines the brush, *m\_pFernBitmapBrush*, to which the opacity mask is applied.</span></span> <span data-ttu-id="22bb9-146">In questo esempio viene usato un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) che contiene un'immagine di una felce, ma è invece possibile usare [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)o [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="22bb9-146">This example uses an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that contains an image of a fern, but you could use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) instead.</span></span> <span data-ttu-id="22bb9-147">Nella figura seguente viene illustrato l'output generato.</span><span class="sxs-lookup"><span data-stu-id="22bb9-147">The following illustration shows the output that is produced.</span></span>

![illustrazione della bitmap utilizzata dal pennello bitmap](images/fern.png)


```C++
            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
                hr = m_pRenderTarget->CreateBitmapBrush(
                    m_pFernBitmap,
                    propertiesXClampYClamp,
                    &m_pFernBitmapBrush
                    );


            }
```





<span data-ttu-id="22bb9-149">Ora che la maschera di opacità e il pennello sono definiti, è possibile usare il metodo [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) nel metodo di rendering dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="22bb9-149">Now that opacity mask and the brush are defined, you can use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method in your application's rendering method.</span></span> <span data-ttu-id="22bb9-150">Quando si chiama il metodo **FillOpacityMask** , è necessario specificare il tipo di maschera di opacità che si sta usando: d2d1 maschera di opacità **\_ \_ \_ contenuto \_ grafica**, **d2d1 \_ opacità \_ \_ contenuto \_ testo \_ naturale** e **d2d1 \_ Opacity \_ maschera \_ contenuto \_ testo \_ GDI \_ compatibile**.</span><span class="sxs-lookup"><span data-stu-id="22bb9-150">When you call the **FillOpacityMask** method, you must specify the type of opacity mask you are using: **D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**, **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_NATURAL**, and **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_GDI\_COMPATIBLE**.</span></span> <span data-ttu-id="22bb9-151">Per i significati di questi tre tipi, vedere [**\_ contenuto della \_ maschera \_ di opacità di d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).</span><span class="sxs-lookup"><span data-stu-id="22bb9-151">For the meanings of these three types, see [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).</span></span>

> [!Note]  
> <span data-ttu-id="22bb9-152">A partire da Windows 8, [**il \_ \_ \_ contenuto della maschera di opacità d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="22bb9-152">Starting with Windows 8, the [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) is not required.</span></span> <span data-ttu-id="22bb9-153">Vedere il metodo [**ID2D1DeviceContext:: FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) , che non ha un parametro di **contenuto della \_ \_ maschera \_ di opacità d2d1** .</span><span class="sxs-lookup"><span data-stu-id="22bb9-153">See the [**ID2D1DeviceContext::FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) method, which has no **D2D1\_OPACITY\_MASK\_CONTENT** parameter.</span></span>

 

<span data-ttu-id="22bb9-154">Nell'esempio seguente la modalità di anti-aliasing della destinazione di rendering viene impostata su [**d2d1 \_ antialias \_ mode con \_ alias**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) in modo che la maschera di opacità funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="22bb9-154">The next example sets the render target's antialiasing mode to [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) so that the opacity mask will work properly.</span></span> <span data-ttu-id="22bb9-155">Chiama quindi il metodo [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) e lo passa alla maschera di opacità (*m \_ pBitmapMask*), al pennello a cui viene applicata la maschera di opacità (*m \_ pFernBitmapBrush*), al tipo di contenuto all'interno della maschera di opacità (immagine del [**contenuto della \_ maschera di opacità \_ \_ \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)) e all'area da disegnare.</span><span class="sxs-lookup"><span data-stu-id="22bb9-155">It then calls the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method and passes it the opacity mask (*m\_pBitmapMask*), the brush to which the opacity mask is applied (*m\_pFernBitmapBrush*), the type of content inside the opacity mask ([**D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)), and the area to paint.</span></span> <span data-ttu-id="22bb9-156">Nella figura seguente viene illustrato l'output generato.</span><span class="sxs-lookup"><span data-stu-id="22bb9-156">The following illustration shows the output that is produced.</span></span>

![illustrazione dell'immagine di Fern Plant con una maschera di opacità applicata](images/opacitymaskoutput.png)


```C++
        D2D1_RECT_F rcBrushRect = D2D1::RectF(5, 5, 155, 155);


        // D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask to function properly
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);
        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);
```





<span data-ttu-id="22bb9-158">Il codice è stato omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="22bb9-158">Code has been omitted from this example.</span></span>

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a><span data-ttu-id="22bb9-159">Usare un pennello come maschera di opacità con il metodo FillGeometry</span><span class="sxs-lookup"><span data-stu-id="22bb9-159">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>

<span data-ttu-id="22bb9-160">La sezione precedente descrive come usare un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) come maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="22bb9-160">The preceding section described how to use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) as an opacity mask.</span></span> <span data-ttu-id="22bb9-161">Direct2D fornisce anche il metodo [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , che consente di specificare facoltativamente il pennello come maschera di opacità quando si compila un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry).</span><span class="sxs-lookup"><span data-stu-id="22bb9-161">Direct2D also provides the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, which enables you to optionally specify brush as an opacity mask when you fill an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry).</span></span> <span data-ttu-id="22bb9-162">In questo modo è possibile creare maschere di opacità da sfumature (usando [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) o [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) e bitmap (usando **ID2D1Bitmap**).</span><span class="sxs-lookup"><span data-stu-id="22bb9-162">This enables you to create opacity masks from gradients (using [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) and bitmaps (using **ID2D1Bitmap**).</span></span>

<span data-ttu-id="22bb9-163">Il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) accetta tre parametri:</span><span class="sxs-lookup"><span data-stu-id="22bb9-163">The [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method takes three parameters:</span></span>

-   <span data-ttu-id="22bb9-164">Il primo parametro, [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), definisce la forma da disegnare.</span><span class="sxs-lookup"><span data-stu-id="22bb9-164">The first parameter, an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), defines the shape to paint.</span></span>
-   <span data-ttu-id="22bb9-165">Il secondo parametro, [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifica il pennello utilizzato per disegnare la geometria.</span><span class="sxs-lookup"><span data-stu-id="22bb9-165">The second parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies the brush used to paint the geometry.</span></span> <span data-ttu-id="22bb9-166">Questo parametro deve essere un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con le modalità di estensione x e y impostate su [**d2d1 \_ extend \_ mode \_ Clamp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="22bb9-166">This parameter must be an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that has its x- and y-extend modes set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>
-   <span data-ttu-id="22bb9-167">Il terzo parametro, [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifica un pennello da utilizzare come maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="22bb9-167">The third parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies a brush to use as the opacity mask.</span></span> <span data-ttu-id="22bb9-168">Questo pennello può essere [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)o [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="22bb9-168">This brush may be an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), or an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span> <span data-ttu-id="22bb9-169">Tecnicamente, è possibile usare un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), ma l'uso di un pennello tinta unita come maschera di opacità non produce risultati interessanti.</span><span class="sxs-lookup"><span data-stu-id="22bb9-169">(Technically, you may use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), but using a solid color brush as an opacity mask doesn't produce interesting results.)</span></span>

<span data-ttu-id="22bb9-170">Le sezioni seguenti descrivono come usare gli oggetti [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) e [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) come maschere di opacità.</span><span class="sxs-lookup"><span data-stu-id="22bb9-170">The following sections describe how to use [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) and [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) objects as opacity masks.</span></span>

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="22bb9-171">Usare un pennello sfumato lineare come maschera di opacità</span><span class="sxs-lookup"><span data-stu-id="22bb9-171">Use an Linear Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="22bb9-172">Il diagramma seguente mostra l'effetto dell'applicazione di un pennello sfumato lineare a un rettangolo riempito con una bitmap di fiori.</span><span class="sxs-lookup"><span data-stu-id="22bb9-172">The following diagram shows the effect of applying a linear gradient brush to a rectangle that is filled with a bitmap of flowers.</span></span>

![diagramma di una bitmap floreale con un pennello sfumato lineare applicato](images/brushes-ovw-lineargradient-opacitymask.png)

<span data-ttu-id="22bb9-174">I passaggi seguenti descrivono come ricreare questo effetto.</span><span class="sxs-lookup"><span data-stu-id="22bb9-174">The steps that follow describe how to re-create this effect.</span></span>

1.  <span data-ttu-id="22bb9-175">Definire il contenuto da mascherare.</span><span class="sxs-lookup"><span data-stu-id="22bb9-175">Define the content to be masked.</span></span> <span data-ttu-id="22bb9-176">Nell'esempio seguente viene creato un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pLinearFadeFlowersBitmap*.</span><span class="sxs-lookup"><span data-stu-id="22bb9-176">The following example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pLinearFadeFlowersBitmap*.</span></span> <span data-ttu-id="22bb9-177">La modalità di estensione x e y per *m \_ pLinearFadeFlowersBitmap* sono impostate su [**d2d1 \_ extend \_ mode \_ Clamp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) , in modo che possa essere usato con una maschera di opacità dal metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="22bb9-177">The extend mode x- and y- for *m\_pLinearFadeFlowersBitmap* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) so that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

    ```cpp
    if (SUCCEEDED(hr))
    {
        // Create the bitmap to be used by the bitmap brush.
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"LinearFadeFlowers",
            L"Image",
            &m_pLinearFadeFlowersBitmap
            );
    }
 
    if (SUCCEEDED(hr))
        {
            D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                D2D1::BitmapBrushProperties(
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                );
    ```

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="22bb9-178">C++</span><span class="sxs-lookup"><span data-stu-id="22bb9-178">C++</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>                if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateBitmapBrush(
                            m_pLinearFadeFlowersBitmap,
                            propertiesXClampYClamp,
                            &m_pLinearFadeFlowersBitmapBrush
                            );
                    }</code></pre></td>
    </tr>
    </tbody>
    </table>

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="22bb9-179">C++</span><span class="sxs-lookup"><span data-stu-id="22bb9-179">C++</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  <span data-ttu-id="22bb9-180">Definire la maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="22bb9-180">Define the opacity mask.</span></span> <span data-ttu-id="22bb9-181">Nell'esempio di codice successivo viene creato un pennello sfumato lineare diagonale (*m \_ pLinearGradientBrush*) che si dissolve dal nero completamente opaco nella posizione 0 al bianco completamente trasparente nella posizione 1.</span><span class="sxs-lookup"><span data-stu-id="22bb9-181">The next code example creates a diagonal linear gradient brush (*m\_pLinearGradientBrush*) that fades from fully opaque black at position 0 to completely transparent white at position 1.</span></span>
```C++
                if (SUCCEEDED(hr))
                {
                    ID2D1GradientStopCollection *pGradientStops = NULL;

                    static const D2D1_GRADIENT_STOP gradientStops[] =
                    {
                        {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                        {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                    };

                    hr = m_pRenderTarget->CreateGradientStopCollection(
                        gradientStops,
                        2,
                        &pGradientStops);


                    if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateLinearGradientBrush(
                            D2D1::LinearGradientBrushProperties(
                                D2D1::Point2F(0, 0),
                                D2D1::Point2F(150, 150)),
                            pGradientStops,
                            &m_pLinearGradientBrush);
                    }

    
                pGradientStops->Release();
                }
```



    

3.  <span data-ttu-id="22bb9-182">Usare il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="22bb9-182">Use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="22bb9-183">L'esempio finale usa il metodo **FillGeometry** per il pennello del contenuto per riempire [**un ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) con un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pLinearFadeFlowersBitmap*) e applica una maschera di opacità (*m \_ pLinearGradientBrush*).</span><span class="sxs-lookup"><span data-stu-id="22bb9-183">The final example uses the **FillGeometry** method to the content brush to fill a [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*) with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pLinearFadeFlowersBitmap*) and applies an opacity mask (*m\_pLinearGradientBrush*).</span></span>
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

<span data-ttu-id="22bb9-184">Il codice è stato omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="22bb9-184">Code has been omitted from this example.</span></span>

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="22bb9-185">Usare un pennello a sfumatura radiale come maschera di opacità</span><span class="sxs-lookup"><span data-stu-id="22bb9-185">Use a Radial Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="22bb9-186">Il diagramma seguente illustra l'effetto visivo dell'applicazione di un pennello a sfumatura radiale a un rettangolo riempito con una bitmap di fogliame.</span><span class="sxs-lookup"><span data-stu-id="22bb9-186">The following diagram shows the visual effect of applying a radial gradient brush to a rectangle that is filled with a bitmap of foliage.</span></span>

![diagramma di una bitmap fogliame con un pennello a sfumatura radiale applicato](images/brushes-ovw-radialgradient-opacitymask.png)

<span data-ttu-id="22bb9-188">Nel primo esempio viene creato un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pRadialFadeFlowersBitmapBrush*.</span><span class="sxs-lookup"><span data-stu-id="22bb9-188">The first example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pRadialFadeFlowersBitmapBrush*.</span></span> <span data-ttu-id="22bb9-189">In modo che possa essere usato con una maschera di opacità dal metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , la modalità di estensione x e y per *m \_ PRadialFadeFlowersBitmapBrush* sono impostate su [**d2d1 \_ extend \_ mode \_ Clamp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="22bb9-189">So that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, the extend mode x- and y- for *m\_pRadialFadeFlowersBitmapBrush* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                // Create the bitmap to be used by the bitmap brush.
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"RadialFadeFlowers",
                    L"Image",
                    &m_pRadialFadeFlowersBitmap
                    );
            }


            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22bb9-190">C++</span><span class="sxs-lookup"><span data-stu-id="22bb9-190">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateBitmapBrush(
                        m_pLinearFadeFlowersBitmap,
                        propertiesXClampYClamp,
                        &m_pLinearFadeFlowersBitmapBrush
                        );
                }</code></pre></td>
</tr>
</tbody>
</table>

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22bb9-191">C++</span><span class="sxs-lookup"><span data-stu-id="22bb9-191">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="22bb9-192">Nell'esempio successivo viene definito il pennello a sfumatura radiale che verrà utilizzato come maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="22bb9-192">The next example defines the radial gradient brush that will be used as the opacity mask.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                ID2D1GradientStopCollection *pGradientStops = NULL;

                static const D2D1_GRADIENT_STOP gradientStops[] =
                {
                    {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                    {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                };

                hr = m_pRenderTarget->CreateGradientStopCollection(
                    gradientStops,
                    2,
                    &pGradientStops);




                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateRadialGradientBrush(
                        D2D1::RadialGradientBrushProperties(
                            D2D1::Point2F(75, 75),
                            D2D1::Point2F(0, 0),
                            75,
                            75),
                        pGradientStops,
                        &m_pRadialGradientBrush);
                }
                pGradientStops->Release();
            }
```





<span data-ttu-id="22bb9-193">L'esempio di codice finale USA [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pRadialFadeFlowersBitmapBrush*) e la maschera di opacità (*m \_ pRadialGradientBrush*) per riempire un [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*).</span><span class="sxs-lookup"><span data-stu-id="22bb9-193">The final code example uses the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pRadialFadeFlowersBitmapBrush*) and the opacity mask (*m\_pRadialGradientBrush*) to fill an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*).</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



<span data-ttu-id="22bb9-194">Il codice è stato omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="22bb9-194">Code has been omitted from this example.</span></span>

## <a name="apply-an-opacity-mask-to-a-layer"></a><span data-ttu-id="22bb9-195">Applicare una maschera di opacità a un livello</span><span class="sxs-lookup"><span data-stu-id="22bb9-195">Apply an Opacity Mask to a Layer</span></span>

<span data-ttu-id="22bb9-196">Quando si chiama [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) per eseguire il push di un [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) su una destinazione di rendering, è possibile usare la struttura dei [**\_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) per applicare un pennello come maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="22bb9-196">When you call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) to push an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) onto an render target, you can use the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to apply a brush as an opacity mask.</span></span> <span data-ttu-id="22bb9-197">Nell'esempio di codice seguente viene usato un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) come maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="22bb9-197">The following code example uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) as an opacity mask.</span></span>


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



<span data-ttu-id="22bb9-198">Per ulteriori informazioni sull'utilizzo dei livelli, vedere [Cenni preliminari sui livelli](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="22bb9-198">For more information about using layers, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="22bb9-199">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22bb9-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22bb9-200">Panoramica dei pennelli</span><span class="sxs-lookup"><span data-stu-id="22bb9-200">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="22bb9-201">Panoramica sui livelli</span><span class="sxs-lookup"><span data-stu-id="22bb9-201">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

 

 