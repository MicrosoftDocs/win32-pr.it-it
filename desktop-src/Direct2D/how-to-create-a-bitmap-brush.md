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
# <a name="how-to-create-a-bitmap-brush"></a><span data-ttu-id="1437b-103">Come creare un pennello bitmap</span><span class="sxs-lookup"><span data-stu-id="1437b-103">How to Create a Bitmap Brush</span></span>

<span data-ttu-id="1437b-104">Per creare un pennello bitmap, usare il metodo [**ID2D1RenderTarget:: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) e specificare le proprietà del pennello bitmap.</span><span class="sxs-lookup"><span data-stu-id="1437b-104">To create a bitmap brush, use the [**ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method and specify the bitmap brush properties.</span></span> <span data-ttu-id="1437b-105">Alcuni overload consentono di specificare le proprietà del pennello.</span><span class="sxs-lookup"><span data-stu-id="1437b-105">Some overloads enable you to specify the brush properties.</span></span> <span data-ttu-id="1437b-106">Il codice seguente illustra come creare un pennello bitmap per riempire un quadrato e un pennello nero a tinta unita per disegnare il contorno del quadrato.</span><span class="sxs-lookup"><span data-stu-id="1437b-106">The following code shows how to create a bitmap brush to fill a square, and a solid black brush to draw the outline of the square.</span></span> <span data-ttu-id="1437b-107">Il codice produce l'output mostrato nello screenshot seguente.</span><span class="sxs-lookup"><span data-stu-id="1437b-107">The code produces the output shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="1437b-108">A partire da Windows 8, è possibile usare il metodo [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) sull'interfaccia [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) per creare un [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) anziché un **ID2D1BitmapBrush**.</span><span class="sxs-lookup"><span data-stu-id="1437b-108">Starting with Windows 8, you can use the [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface to create a [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) instead of a **ID2D1BitmapBrush**.</span></span> <span data-ttu-id="1437b-109">**ID2D1BitmapBrush1** aggiunge modalità di ridimensionamento di alta qualità al pennello bitmap.</span><span class="sxs-lookup"><span data-stu-id="1437b-109">**ID2D1BitmapBrush1** adds high-quality scaling modes to the bitmap brush.</span></span>

 

![Screenshot di un quadrato riempito con una bitmap della pianta](images/brushes-ovw-bitmap.png)

1.  <span data-ttu-id="1437b-111">Dichiarare una variabile di tipo [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="1437b-111">Declare a variable of type [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  <span data-ttu-id="1437b-112">Caricare una bitmap da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="1437b-112">Load a bitmap from a resource.</span></span> <span data-ttu-id="1437b-113">Per ulteriori informazioni, vedere [come caricare una bitmap da una risorsa](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="1437b-113">For more information, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
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

    

3.  <span data-ttu-id="1437b-114">Scegliere le modalità Estendi ([**d2d1 \_ extend \_ mode**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) e la modalità di interpolazione (modalità di interpolazione [**\_ bitmap \_ \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) del pennello bitmap, quindi chiamare il metodo [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) per creare un pennello, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="1437b-114">Choose the extend modes ([**D2D1\_EXTEND\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) and interpolation mode ([**D2D1\_BITMAP\_INTERPOLATION\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) of the bitmap brush and then call the [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method to create a brush, as shown in the following code.</span></span>
    ```C++
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="1437b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1437b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1437b-116">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="1437b-116">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 