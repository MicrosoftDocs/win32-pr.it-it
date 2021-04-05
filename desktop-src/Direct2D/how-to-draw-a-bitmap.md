---
title: Come creare una bitmap
description: Viene illustrato come eseguire il rendering di bitmap con Direct2D.
ms.assetid: 9c6fc8b1-47ba-46fa-b812-2636cd8ff2b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfa13b75b4fe34ce6ff2b80598fac35f8483a2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872609"
---
# <a name="how-to-draw-a-bitmap"></a><span data-ttu-id="aa52e-103">Come creare una bitmap</span><span class="sxs-lookup"><span data-stu-id="aa52e-103">How to Draw a Bitmap</span></span>

<span data-ttu-id="aa52e-104">Per eseguire il rendering di una bitmap, usare il metodo [**ID2D1RenderTarget::D rawbitmap**](id2d1rendertarget-drawbitmap.md) .</span><span class="sxs-lookup"><span data-stu-id="aa52e-104">To render a bitmap, use the [**ID2D1RenderTarget::DrawBitmap**](id2d1rendertarget-drawbitmap.md) method.</span></span> <span data-ttu-id="aa52e-105">Nell'esempio seguente viene illustrato come utilizzare il metodo **DrawBitmap** per creare un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="aa52e-105">The following example shows how to use the **DrawBitmap** method to draw an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="aa52e-106">Viene creato l'output illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="aa52e-106">It creates the output shown in the following illustration.</span></span>

![illustrazione di una bitmap originale con le bitmap risultanti con diverse impostazioni di opacità e trasformazioni](images/drawbitmapexample.png)

<span data-ttu-id="aa52e-108">Per prima cosa, creare un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="aa52e-108">First, create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="aa52e-109">L'esempio seguente carica una bitmap dal file di risorse dell'applicazione e la archivia come *m \_ pBitmap*.</span><span class="sxs-lookup"><span data-stu-id="aa52e-109">The following example loads a bitmap from the application's resource file and stores it as *m\_pBitmap*.</span></span> <span data-ttu-id="aa52e-110">Per informazioni sul modo in cui `LoadResourceBitmap` viene implementato il metodo, vedere [come caricare una bitmap da una risorsa](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="aa52e-110">(To see how the `LoadResourceBitmap` method is implemented, refer to [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).)</span></span>


```C++
// Create a bitmap from an application resource.
hr = LoadResourceBitmap(
    m_pRenderTarget,
    m_pWICFactory,
    L"SampleImage",
    L"Image",
    200,
    0,
    &m_pBitmap
    );
```



<span data-ttu-id="aa52e-111">Creare [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) nello stesso metodo in cui è stata creata la destinazione di rendering che verrà utilizzata per disegnare la bitmap e rilasciare la bitmap quando la destinazione di rendering viene rilasciata.</span><span class="sxs-lookup"><span data-stu-id="aa52e-111">Create the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) in the same method where you created the render target that you will use to draw the bitmap, and release the bitmap when the render target is released.</span></span>

<span data-ttu-id="aa52e-112">Al termine della creazione della bitmap, eseguirne il rendering.</span><span class="sxs-lookup"><span data-stu-id="aa52e-112">Once the bitmap is created, render it.</span></span> <span data-ttu-id="aa52e-113">Nell'esempio seguente viene usato il metodo [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) per eseguire il rendering di una bitmap più volte usando impostazioni di dimensioni e opacità diverse.</span><span class="sxs-lookup"><span data-stu-id="aa52e-113">The following example uses the [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) method to render a bitmap several times using different size and opacity settings.</span></span>


```C++
HRESULT DrawBitmapExample::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        // Paint a grid background.
        m_pRenderTarget->FillRectangle(
            D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
            m_pGridPatternBitmapBrush
            );

        // Retrieve the size of the bitmap.
        D2D1_SIZE_F size = m_pBitmap->GetSize();

        D2D1_POINT_2F upperLeftCorner = D2D1::Point2F(100.f, 10.f);

        // Draw a bitmap.
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + size.width,
                upperLeftCorner.y + size.height)
            );

        // Draw the next bitmap below the first one.
        upperLeftCorner.y = upperLeftCorner.y + size.height + 10.f;

        // Scale the bitmap to half its size using the linear
        // interoplation mode and draw it.
        float scaledWidth = size.width / 2.f;
        float scaledHeight = size.height / 2.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            1.0,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        // Draw the bitmap at half its size and half its opacity.
        upperLeftCorner.y = upperLeftCorner.y + size.height / 2.f + 10.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.5,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        // Draw a series of bitmaps with different opacity and
        // rotation angles.
        upperLeftCorner.y = upperLeftCorner.y + scaledHeight + 20.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.5,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        D2D1_POINT_2F lowerLeftCorner = D2D1::Point2F(upperLeftCorner.x, upperLeftCorner.y + scaledHeight);
        D2D1_POINT_2F imageCenter = D2D1::Point2F(
            upperLeftCorner.x + scaledWidth / 2,
            upperLeftCorner.y + scaledHeight / 2
            );

        // Rotate the next bitmap by -20 degrees.
        m_pRenderTarget->SetTransform(
            D2D1::Matrix3x2F::Rotation(-20, imageCenter)
            );

        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.75,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        m_pRenderTarget->SetTransform(
            D2D1::Matrix3x2F::Rotation(-45, imageCenter)
            );

        // Make the last bitmap fully opaque.
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            1.0,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



<span data-ttu-id="aa52e-114">Se ha esito negativo, il metodo [**DrawBitmap**](id2d1rendertarget-drawbitmap.md) non restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="aa52e-114">The [**DrawBitmap**](id2d1rendertarget-drawbitmap.md) method does not return an error code if it fails.</span></span> <span data-ttu-id="aa52e-115">Per determinare se un'operazione di disegno (ad esempio **DrawBitmap**) non è riuscita, controllare il risultato restituito dal metodo [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="aa52e-115">To determine whether a drawing operation (such as **DrawBitmap**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method, as shown in the following example.</span></span>


```C++
hr = m_pRenderTarget->EndDraw();
```



<span data-ttu-id="aa52e-116">Il codice è stato omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="aa52e-116">Code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa52e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa52e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa52e-118">**DrawBitmap**</span><span class="sxs-lookup"><span data-stu-id="aa52e-118">**DrawBitmap**</span></span>](id2d1rendertarget-drawbitmap.md)
</dt> <dt>

[<span data-ttu-id="aa52e-119">**ID2D1Bitmap**</span><span class="sxs-lookup"><span data-stu-id="aa52e-119">**ID2D1Bitmap**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[<span data-ttu-id="aa52e-120">Come caricare una bitmap da una risorsa</span><span class="sxs-lookup"><span data-stu-id="aa52e-120">How to Load a Bitmap from a Resource</span></span>](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 