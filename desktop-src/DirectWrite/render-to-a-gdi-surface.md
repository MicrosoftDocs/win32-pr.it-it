---
title: Rendering in una superficie GDI
description: Rendering in una superficie GDI
ms.assetid: a6096ff5-1e6e-4edb-b455-ea5d205072ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff292feb2250a4dd81abeb62d8ee48ebfb4488b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399640"
---
# <a name="render-to-a-gdi-surface"></a><span data-ttu-id="98ef4-103">Rendering in una superficie GDI</span><span class="sxs-lookup"><span data-stu-id="98ef4-103">Render to a GDI Surface</span></span>

<span data-ttu-id="98ef4-104">In alcuni casi, potrebbe essere necessario poter visualizzare il testo [DirectWrite](direct-write-portal.md) su una superficie GDI.</span><span class="sxs-lookup"><span data-stu-id="98ef4-104">In some cases, you may want to be able to display [DirectWrite](direct-write-portal.md) text on a GDI surface.</span></span> <span data-ttu-id="98ef4-105">L'interfaccia [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) incapsula una bitmap e un contesto di dispositivo su cui eseguire il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="98ef4-105">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface encapsulates a bitmap and device context to render text onto.</span></span> <span data-ttu-id="98ef4-106">Per creare un **IDWriteBitmapRenderTarget** , usare il metodo [**IDWriteGdiInterop:: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="98ef4-106">You create an **IDWriteBitmapRenderTarget** by using the [**IDWriteGdiInterop::CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) method, as shown in the following code.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



<span data-ttu-id="98ef4-107">Per eseguire il rendering con un [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget), è necessario implementare un'interfaccia di callback del renderer di testo personalizzata derivata dall'interfaccia [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) .</span><span class="sxs-lookup"><span data-stu-id="98ef4-107">To render with an [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget), you must implement a custom text renderer callback interface derived from the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) interface.</span></span> <span data-ttu-id="98ef4-108">È necessario implementare metodi per disegnare un'esecuzione del glifo, una sottolineatura, una barratura, oggetti inline e così via.</span><span class="sxs-lookup"><span data-stu-id="98ef4-108">You must implement methods for drawing a glyph run, underline, strikethrough, inline objects, and so on.</span></span> <span data-ttu-id="98ef4-109">Per un elenco completo dei metodi, vedere la pagina di riferimento di [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) .</span><span class="sxs-lookup"><span data-stu-id="98ef4-109">For a complete list of the methods, see the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) reference page.</span></span> <span data-ttu-id="98ef4-110">Non tutti i metodi devono essere implementati, possono solo restituire **e \_ NOTIMPL** e il disegno continuerà.</span><span class="sxs-lookup"><span data-stu-id="98ef4-110">Not every method must be implemented, they can just return **E\_NOTIMPL**, and drawing will continue.</span></span>

<span data-ttu-id="98ef4-111">È quindi possibile creare il testo usando il metodo [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) e passando l'interfaccia di callback implementata come parametro.</span><span class="sxs-lookup"><span data-stu-id="98ef4-111">You can then draw the text by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method and passing the callback interface that you implemented as a parameter.</span></span> <span data-ttu-id="98ef4-112">Il metodo **IDWriteTextLayout::D RAW** chiama i metodi del callback del renderer personalizzato fornito.</span><span class="sxs-lookup"><span data-stu-id="98ef4-112">The **IDWriteTextLayout::Draw** method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="98ef4-113">I metodi [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)e [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) eseguono le funzioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="98ef4-113">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods perform the drawing functions.</span></span>

<span data-ttu-id="98ef4-114">Nell'implementazione di [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)chiamare il metodo [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) per creare i glifi.</span><span class="sxs-lookup"><span data-stu-id="98ef4-114">In your implementation of [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), call the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to draw the glyphs.</span></span> <span data-ttu-id="98ef4-115">Il rendering degli oggetti Underline, barrato e inline deve essere eseguito dal renderer personalizzato.</span><span class="sxs-lookup"><span data-stu-id="98ef4-115">The rendering of the underline, strikethrough and inline objects must be done by your custom renderer.</span></span>

<span data-ttu-id="98ef4-116">[**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) ha un parametro di uscita Rect facoltativo che contiene i limiti dell'area in cui è stato disegnato il testo.</span><span class="sxs-lookup"><span data-stu-id="98ef4-116">[**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) has an optional RECT out parameter that contains the bounds of the area where the text was drawn.</span></span> <span data-ttu-id="98ef4-117">È possibile usare queste informazioni per impostare il rettangolo di delimitazione per il contesto di dispositivo con la funzione [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) fornita da GDI.</span><span class="sxs-lookup"><span data-stu-id="98ef4-117">You can use this information to set the bounding rectangle for the device context with the [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) function that is provided by GDI.</span></span> <span data-ttu-id="98ef4-118">Il codice seguente è un'implementazione di esempio del metodo [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) di un renderer personalizzato.</span><span class="sxs-lookup"><span data-stu-id="98ef4-118">The following code is an example implementation of the [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of a custom renderer.</span></span>


```C++
STDMETHODIMP GdiTextRenderer::DrawGlyphRun(
    __maybenull void* clientDrawingContext,
    FLOAT baselineOriginX,
    FLOAT baselineOriginY,
    DWRITE_MEASURING_MODE measuringMode,
    __in DWRITE_GLYPH_RUN const* glyphRun,
    __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
    IUnknown* clientDrawingEffect
    )
{
    HRESULT hr = S_OK;

    // Pass on the drawing call to the render target to do the real work.
    RECT dirtyRect = {0};

    hr = pRenderTarget_->DrawGlyphRun(
        baselineOriginX,
        baselineOriginY,
        measuringMode,
        glyphRun,
        pRenderingParams_,
        RGB(0,200,255),
        &dirtyRect
        );
    

    return hr;
}
```



<span data-ttu-id="98ef4-119">L'interfaccia [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) esegue il rendering in un contesto di dispositivo (DC) in memoria.</span><span class="sxs-lookup"><span data-stu-id="98ef4-119">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface renders to a device context (DC) in memory.</span></span> <span data-ttu-id="98ef4-120">Si ottiene un handle per il controller di dominio usando il metodo [**IDWriteBitmapRenderTarget:: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) .</span><span class="sxs-lookup"><span data-stu-id="98ef4-120">You get a handle to this DC by using the [**IDWriteBitmapRenderTarget::GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) method.</span></span> <span data-ttu-id="98ef4-121">Non appena il disegno è stato eseguito, il controller di dominio della memoria dell'oggetto **IDWriteBitmapRenderTarget** deve essere copiato nella superficie GDI di destinazione.</span><span class="sxs-lookup"><span data-stu-id="98ef4-121">As soon as the drawing has been performed, the memory DC of the **IDWriteBitmapRenderTarget** object must be copied to the destination GDI surface.</span></span>

<span data-ttu-id="98ef4-122">È possibile recuperare il rettangolo di delimitazione utilizzando la funzione [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) , quindi utilizzare il rettangolo di delimitazione con la funzione [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) per copiare il testo [DirectWrite](direct-write-portal.md) sottoposto a rendering dal controller di dominio della memoria alla superficie GDI, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="98ef4-122">You can retrieve the bounding rectangle by using the [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) function, then use the bounding rectangle with the [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) function to copy the rendered [DirectWrite](direct-write-portal.md) text from the memory DC to the GDI surface as shown in the following code.</span></span>


```C++
// Transfer from DWrite's rendering target to the window.
BitBlt(
    hdc,
    0, 0,
    size.cx, size.cy,
    memoryHdc,
    0, 0, 
    SRCCOPY | NOMIRRORBITMAP
    );
```



 

 