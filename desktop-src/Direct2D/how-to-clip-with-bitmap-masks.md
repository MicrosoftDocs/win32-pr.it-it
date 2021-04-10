---
title: Come usare una bitmap come maschera di opacità
description: Mostra come ritagliare un'area con le maschere bitmap.
ms.assetid: d6ad53a6-5e84-49d0-ab2c-5d6ad9428f9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2106f43a6845cd724204fbf3e5aa1ec2b866bf46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963327"
---
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a><span data-ttu-id="1d6ae-103">Come usare una bitmap come maschera di opacità</span><span class="sxs-lookup"><span data-stu-id="1d6ae-103">How to Use a Bitmap as an Opacity Mask</span></span>

<span data-ttu-id="1d6ae-104">Questo argomento descrive come usare una bitmap come maschera opacty chiamando il metodo [**ID2D1Factory:: FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) .</span><span class="sxs-lookup"><span data-stu-id="1d6ae-104">This topic describes how to use a bitmap as an opacty mask by calling the [**ID2D1Factory::FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) method.</span></span> <span data-ttu-id="1d6ae-105">La maschera di opacità è una bitmap che fornisce le informazioni di code coverage rappresentate dal canale alfa, che controlla la trasparenza del contenuto di cui viene eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-105">The opacity mask is a bitmap that supplies the coverage information that is represented by the alpha channel, which controls the transparency of the content that is rendered.</span></span> <span data-ttu-id="1d6ae-106">Questo approccio è più efficiente rispetto all'uso di livelli con una maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-106">This approach is more efficient than using layers with an opacity mask.</span></span> <span data-ttu-id="1d6ae-107">Per altre informazioni, vedere [Cenni preliminari sui livelli](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1d6ae-107">For more information, see [Layers Overview](direct2d-layers-overview.md).</span></span>

<span data-ttu-id="1d6ae-108">**Per ritagliare un'area**</span><span class="sxs-lookup"><span data-stu-id="1d6ae-108">**To clip a region**</span></span>

1.  <span data-ttu-id="1d6ae-109">Caricare la bitmap originale da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-109">Load the original bitmap from a resource.</span></span> <span data-ttu-id="1d6ae-110">Per informazioni su come caricare una bitmap, vedere [come caricare una bitmap da una risorsa](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="1d6ae-110">For information on how to load a bitmap, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
2.  <span data-ttu-id="1d6ae-111">Caricare la bitmap mask da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-111">Load the bitmap mask from a resource.</span></span>
3.  <span data-ttu-id="1d6ae-112">Creare un pennello bitmap con la bitmap originale.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-112">Create a bitmap brush with the original bitmap.</span></span> <span data-ttu-id="1d6ae-113">Per informazioni su come creare un pennello bitmap, vedere [How to create a bitmap Brush](how-to-create-a-bitmap-brush.md).</span><span class="sxs-lookup"><span data-stu-id="1d6ae-113">For information on how to create a bitmap brush, see [How to Create a Bitmap Brush](how-to-create-a-bitmap-brush.md).</span></span>
4.  <span data-ttu-id="1d6ae-114">Chiamare [**ID2D1Factory:: SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) per impostare la modalità antialias sulla destinazione di rendering su \_ d2d1 \_ antialias \_ con alias per [**ID2D1Factory:: FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) per funzionare.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-114">Call [**ID2D1Factory::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set antialias mode on the render target to D2D1\_ANTIALIAS\_MODE\_ALIASED for [**ID2D1Factory::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) to work.</span></span>
5.  <span data-ttu-id="1d6ae-115">Chiamare [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) con la maschera di bitmap e il pennello bitmap sulla destinazione di rendering per riempire la clip.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-115">Call [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) with the bitmap mask and the bitmap brush on the render target to fill the clip.</span></span>

<span data-ttu-id="1d6ae-116">Nella figura seguente viene mostrata la bitmap originale a sinistra, la maschera di bitmap al centro e la bitmap ritagliata alla maschera a destra.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-116">The following illustration shows the original bitmap on the left, the bitmap mask in the center, and the bitmap clipped to the mask on the right.</span></span>

![illustrazione di una bitmap Goldfish, una maschera a forma di pesce creata dalla bitmap e la bitmap a forma di pesce risultante dopo la maschera](images/cliparegion-opacitymask.png)

<span data-ttu-id="1d6ae-118">Il codice seguente illustra come ritagliare l'area con la maschera mostrata nell'illustrazione precedente.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-118">The following code shows how to clip the region with the mask shown in the preceding illustration.</span></span> <span data-ttu-id="1d6ae-119">Carica innanzitutto la bitmap originale e la maschera bitmap.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-119">It first loads the original bitmap and the bitmap mask.</span></span> <span data-ttu-id="1d6ae-120">E quindi crea un pennello bitmap con la bitmap originale.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-120">And then creates a bitmap brush with the original bitmap.</span></span>


```C++
// Create the bitmap to be used by the bitmap brush
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFish",
        L"Image",
        &m_pOrigBitmap
        );
}

if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFishMask",
        L"Image",
        &m_pBitmapMask
        );
}

if (SUCCEEDED(hr))
{
    D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = D2D1::BitmapBrushProperties(
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
        );

    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pOrigBitmap,
        propertiesXClampYClamp,
        &m_pOriginalBitmapBrush
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateBitmapBrush(
            m_pBitmapMask,
            propertiesXClampYClamp,
            &m_pBitmapMaskBrush
            );
    }
}
```



<span data-ttu-id="1d6ae-121">Chiama quindi [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) per impostare la modalità antialias.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-121">It then calls [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set the antialias mode.</span></span> <span data-ttu-id="1d6ae-122">Chiamare [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) per usare una maschera di bitmap per ritagliare la bitmap originale.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-122">Call [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) to use a bitmap mask to clip the original bitmap.</span></span>


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



<span data-ttu-id="1d6ae-123">Per ulteriori informazioni sulle maschere di opacità, vedere [Cenni preliminari sulle maschere di opacità](opacity-masks-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1d6ae-123">For more information about opacity masks, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d6ae-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d6ae-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d6ae-125">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="1d6ae-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 