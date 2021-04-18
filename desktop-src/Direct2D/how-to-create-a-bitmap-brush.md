---
title: Come creare un pennello bitmap
description: Viene illustrato come creare un pennello bitmap utilizzando Direct2D.
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8f28735368916d1abd0c1c9aa091dec4fd93f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300164"
---
# <a name="how-to-create-a-bitmap-brush"></a>Come creare un pennello bitmap

Per creare un pennello bitmap, usare il metodo [**ID2D1RenderTarget:: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) e specificare le proprietà del pennello bitmap. Alcuni overload consentono di specificare le proprietà del pennello. Il codice seguente illustra come creare un pennello bitmap per riempire un quadrato e un pennello nero a tinta unita per disegnare il contorno del quadrato. Il codice produce l'output mostrato nello screenshot seguente.

> [!Note]  
> A partire da Windows 8, è possibile usare il metodo [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) sull'interfaccia [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) per creare un [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) anziché un **ID2D1BitmapBrush**. **ID2D1BitmapBrush1** aggiunge modalità di ridimensionamento di alta qualità al pennello bitmap.

 

![Screenshot di un quadrato riempito con una bitmap della pianta](images/brushes-ovw-bitmap.png)

1.  Dichiarare una variabile di tipo [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  Caricare una bitmap da una risorsa. Per ulteriori informazioni, vedere [come caricare una bitmap da una risorsa](how-to-load-a-bitmap-from-a-resource.md).
    ```C++
    // Create the bitmap to be used by the bitmap brush.
    if (SUCCEEDED(hr))
    {
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"FERN",
            L"Image",
            &m_pBitmap
            );
    ```

    

3.  Scegliere le modalità Estendi ([**d2d1 \_ extend \_ mode**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) e la modalità di interpolazione (modalità di interpolazione [**\_ bitmap \_ \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) del pennello bitmap, quindi chiamare il metodo [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) per creare un pennello, come illustrato nel codice seguente.
    ```C++
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento Direct2D](reference.md)
</dt> </dl>

 

 