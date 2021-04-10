---
title: Panoramica delle destinazioni di rendering a8 compatibili
description: Descrive le nozioni di base delle destinazioni di rendering a8 compatibili e fornisce esempi che illustrano come usarle.
ms.assetid: 218c0123-8da9-4d73-9882-cbf7f205001f
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 552577283adfa9a440e94b7e04f4056bd6c3ecda
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "103963623"
---
# <a name="compatible-a8-render-targets-overview"></a><span data-ttu-id="5bdcd-103">Panoramica delle destinazioni di rendering a8 compatibili</span><span class="sxs-lookup"><span data-stu-id="5bdcd-103">Compatible A8 render targets overview</span></span>

<span data-ttu-id="5bdcd-104">Questo argomento descrive le nozioni di base di una destinazione di rendering a8 compatibile e fornisce esempi su come usarla.</span><span class="sxs-lookup"><span data-stu-id="5bdcd-104">This topic describes the basics of a compatible A8 render target, and provides examples of how to use it.</span></span>

<span data-ttu-id="5bdcd-105">Una destinazione di rendering a8 compatibile è una destinazione di rendering compatibile ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)) che usa un formato pixel A8 ( \_ formato DXGI \_ a8 \_ UNORM).</span><span class="sxs-lookup"><span data-stu-id="5bdcd-105">A compatible A8 render target is a compatible render target ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)) that uses an A8 pixel format (DXGI\_FORMAT\_A8\_UNORM).</span></span> <span data-ttu-id="5bdcd-106">È possibile usare una destinazione di rendering a8 compatibile per migliorare le prestazioni dell'applicazione e fornire transizioni più fluide durante l'animazione del testo.</span><span class="sxs-lookup"><span data-stu-id="5bdcd-106">You can use a compatible A8 render target to improve the application's performance and provide smoother transitions during text animation.</span></span> <span data-ttu-id="5bdcd-107">Una destinazione di rendering a8 compatibile è particolarmente utile quando si tenta di migliorare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="5bdcd-107">A compatible A8 render target is particular useful when you try to improve the following:</span></span>

-   <span data-ttu-id="5bdcd-108">Frequenza dei fotogrammi dell'applicazione che esegue il rendering del testo o della geometria con aliasing che include solo animazioni semplici, ad esempio le modifiche alla conversione, alla rotazione, alla scala o al colore.</span><span class="sxs-lookup"><span data-stu-id="5bdcd-108">The frame rate of the application that renders text or anti-aliased geometry that includes only simple animations, such as translation, rotation, scale, or color changes.</span></span>

-   <span data-ttu-id="5bdcd-109">Continuità visiva dell'applicazione che estende e DIMINSHES il testo durante un'animazione.</span><span class="sxs-lookup"><span data-stu-id="5bdcd-109">The visual continuity of the application that stretches and diminshes text during an animation.</span></span>

<span data-ttu-id="5bdcd-110">Per creare una destinazione di rendering a8 compatibile, usare il metodo [**ID2D1RenderTarget:: CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) insieme al formato DXGI \_ formato \_ a8 \_ UNORM pixel e specificare una destinazione di rendering compatibile restituita.</span><span class="sxs-lookup"><span data-stu-id="5bdcd-110">To create a compatible A8 render target, use the [**ID2D1RenderTarget::CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) method together with the DXGI\_FORMAT\_A8\_UNORM pixel format, and specify a returned compatible render target.</span></span> <span data-ttu-id="5bdcd-111">Per ulteriori informazioni sui formati pixel, vedere [formati di pixel supportati e modalità Alpha](./supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="5bdcd-111">For more information about pixel formats, see [Supported pixel formats and alpha modes](./supported-pixel-formats-and-alpha-modes.md).</span></span>

<span data-ttu-id="5bdcd-112">Ad esempio, per animare in modo efficiente il testo illustrato nello screenshot seguente, usare una destinazione di rendering a8 compatibile per memorizzare nella cache il testo come maschera di opacità.</span><span class="sxs-lookup"><span data-stu-id="5bdcd-112">For example, to efficiently animate the text that is shown in the following screen shot, use a compatible A8 render target to cache the text as an opacity mask.</span></span> <span data-ttu-id="5bdcd-113">Applicare quindi le trasformazioni alla maschera di opacità per ottenere risultati di rendering veloci.</span><span class="sxs-lookup"><span data-stu-id="5bdcd-113">Then, apply transformations to the opacity mask to achieve fast rendering results.</span></span>

![screenshot del testo a cui aggiungere un'animazione](images/a8rendertarget.png)

<span data-ttu-id="5bdcd-115">A tal fine, osservare il codice indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="5bdcd-115">The following code shows how to do this.</span></span> <span data-ttu-id="5bdcd-116">Viene creata una destinazione di rendering a8 compatibile, viene recuperata la bitmap, quindi viene eseguito il rendering della bitmap utilizzando [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md).</span><span class="sxs-lookup"><span data-stu-id="5bdcd-116">It creates a compatible A8 render target, retrieves the bitmap from it, and then renders the bitmap by using [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md).</span></span>

```cpp
ID2D1BitmapRenderTarget *m_pOpacityRT;

// Create the compatible render target using desiredPixelSize to avoid
// blurriness issues caused by a fractional-pixel desiredSize.

D2D1_PIXEL_FORMAT alphaOnlyFormat = D2D1::PixelFormat(
    DXGI_FORMAT_A8_UNORM, 
    D2D1_ALPHA_MODE_PREMULTIPLIED);

hr = m_pRT->CreateCompatibleRenderTarget(
    NULL,
    &maskPixelSize,
    &alphaOnlyFormat,
    D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE,
    &m_pOpacityRT
    );

D2D1_RECT_F destinationRect = D2D1::RectF(
    roundedOffset.x,
    roundedOffset.y,
    roundedOffset.x + opacityRTSize.width,
    roundedOffset.y + opacityRTSize.height
    );

ID2D1Bitmap *pBitmap = NULL;
m_pOpacityRT->GetBitmap(&pBitmap);

pBitmap->GetDpi(&dpiX, &dpiY);

// The antialias mode must be set to D2D1_ANTIALIAS_MODE_ALIASED
// for this method to succeed. We've set this mode already though
// so no need to do it again.

m_pRT->FillOpacityMask(
    pBitmap,
    m_pBlackBrush,
    D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL,
    &destinationRect
    );

pBitmap->Release();
```

## <a name="related-topics"></a><span data-ttu-id="5bdcd-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5bdcd-117">Related topics</span></span>

[<span data-ttu-id="5bdcd-118">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="5bdcd-118">Direct2D Reference</span></span>](reference.md)