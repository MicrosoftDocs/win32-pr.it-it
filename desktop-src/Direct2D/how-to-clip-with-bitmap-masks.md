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
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a>Come usare una bitmap come maschera di opacità

Questo argomento descrive come usare una bitmap come maschera opacty chiamando il metodo [**ID2D1Factory:: FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) . La maschera di opacità è una bitmap che fornisce le informazioni di code coverage rappresentate dal canale alfa, che controlla la trasparenza del contenuto di cui viene eseguito il rendering. Questo approccio è più efficiente rispetto all'uso di livelli con una maschera di opacità. Per altre informazioni, vedere [Cenni preliminari sui livelli](direct2d-layers-overview.md).

**Per ritagliare un'area**

1.  Caricare la bitmap originale da una risorsa. Per informazioni su come caricare una bitmap, vedere [come caricare una bitmap da una risorsa](how-to-load-a-bitmap-from-a-resource.md).
2.  Caricare la bitmap mask da una risorsa.
3.  Creare un pennello bitmap con la bitmap originale. Per informazioni su come creare un pennello bitmap, vedere [How to create a bitmap Brush](how-to-create-a-bitmap-brush.md).
4.  Chiamare [**ID2D1Factory:: SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) per impostare la modalità antialias sulla destinazione di rendering su \_ d2d1 \_ antialias \_ con alias per [**ID2D1Factory:: FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) per funzionare.
5.  Chiamare [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) con la maschera di bitmap e il pennello bitmap sulla destinazione di rendering per riempire la clip.

Nella figura seguente viene mostrata la bitmap originale a sinistra, la maschera di bitmap al centro e la bitmap ritagliata alla maschera a destra.

![illustrazione di una bitmap Goldfish, una maschera a forma di pesce creata dalla bitmap e la bitmap a forma di pesce risultante dopo la maschera](images/cliparegion-opacitymask.png)

Il codice seguente illustra come ritagliare l'area con la maschera mostrata nell'illustrazione precedente. Carica innanzitutto la bitmap originale e la maschera bitmap. E quindi crea un pennello bitmap con la bitmap originale.


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



Chiama quindi [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) per impostare la modalità antialias. Chiamare [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) per usare una maschera di bitmap per ritagliare la bitmap originale.


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



Per ulteriori informazioni sulle maschere di opacità, vedere [Cenni preliminari sulle maschere di opacità](opacity-masks-overview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento Direct2D](reference.md)
</dt> </dl>

 

 