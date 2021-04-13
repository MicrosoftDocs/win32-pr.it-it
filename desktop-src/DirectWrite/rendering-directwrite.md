---
title: Rendering DirectWrite
description: Rendering DirectWrite
ms.assetid: e8099fac-b5d7-4fb1-b06d-a6e85da0d1dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7012bc4861a8befc9beb97c945dc0b03b4e761
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399334"
---
# <a name="rendering-directwrite"></a><span data-ttu-id="a982e-103">Rendering DirectWrite</span><span class="sxs-lookup"><span data-stu-id="a982e-103">Rendering DirectWrite</span></span>

## <a name="rendering-options"></a><span data-ttu-id="a982e-104">Opzioni di rendering</span><span class="sxs-lookup"><span data-stu-id="a982e-104">Rendering Options</span></span>

<span data-ttu-id="a982e-105">Il rendering del testo con la formattazione descritta solo da un oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) può essere eseguito con [Direct2D](../direct2d/direct2d-portal.md), tuttavia sono disponibili altre opzioni per il rendering di un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="a982e-105">Text with formatting described by only an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="a982e-106">La stringa descritta da un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) può essere sottoposta a rendering usando i metodi riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="a982e-106">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

## <a name="1-render-using-direct2d"></a><span data-ttu-id="a982e-107">1. rendering tramite Direct2D</span><span class="sxs-lookup"><span data-stu-id="a982e-107">1. Render using Direct2D</span></span>

<span data-ttu-id="a982e-108">Per eseguire il rendering di un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) tramite Direct2D, usare il metodo [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="a982e-108">To render an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using Direct2D, use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method, as shown in the following code.</span></span>


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



<span data-ttu-id="a982e-109">Per un'analisi più approfondita del disegno di un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) tramite [Direct2D](../direct2d/direct2d-portal.md), vedere [Introduzione con DirectWrite](getting-started-with-directwrite.md).</span><span class="sxs-lookup"><span data-stu-id="a982e-109">For a more in depth look at drawing an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using [Direct2D](../direct2d/direct2d-portal.md), see [Getting Started with DirectWrite](getting-started-with-directwrite.md).</span></span>

## <a name="2-render-using-a-custom-text-renderer"></a><span data-ttu-id="a982e-110">2. eseguire il rendering utilizzando un renderer di testo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a982e-110">2. Render using a custom text renderer.</span></span>

<span data-ttu-id="a982e-111">Per eseguire il rendering con un renderer personalizzato, usare il metodo [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , che accetta un'interfaccia di callback derivata da [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) come argomento, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="a982e-111">You render with a custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="a982e-112">Il metodo [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) chiama i metodi del callback del renderer personalizzato fornito.</span><span class="sxs-lookup"><span data-stu-id="a982e-112">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="a982e-113">I metodi [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)e [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) eseguono le funzioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="a982e-113">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods perform the drawing functions.</span></span>

<span data-ttu-id="a982e-114">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) dichiara i metodi per disegnare un'esecuzione del glifo, una sottolineatura, una barratura e oggetti inline.</span><span class="sxs-lookup"><span data-stu-id="a982e-114">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) declares methods for drawing a glyph run, underline, strikethrough, and inline objects.</span></span> <span data-ttu-id="a982e-115">È necessario che l'applicazione implementi questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a982e-115">It is up to the application to implement these methods.</span></span> <span data-ttu-id="a982e-116">La creazione di un renderer di testo personalizzato consente all'applicazione di applicare effetti aggiuntivi durante il rendering del testo, ad esempio un riempimento o un contorno personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a982e-116">Creating a custom text renderer allows the application to apply additional effects when rendering text, such as a custom fill or outline.</span></span> <span data-ttu-id="a982e-117">Un renderer di testo personalizzato di esempio è incluso nell' [esempio di Hello World DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="a982e-117">A sample custom text renderer is included in the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="3-render-cleartype-to-a-gdi-surface"></a><span data-ttu-id="a982e-118">3. eseguire il rendering di ClearType in una superficie GDI.</span><span class="sxs-lookup"><span data-stu-id="a982e-118">3. Render ClearType to a GDI surface.</span></span>

<span data-ttu-id="a982e-119">Il rendering in una superficie GDI è in realtà un esempio di utilizzo di un renderer di testo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a982e-119">Rendering to a GDI surface is actually an example of using a custom text renderer.</span></span> <span data-ttu-id="a982e-120">Tuttavia, parte del lavoro viene eseguita per l'utente sotto forma di interfaccia [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="a982e-120">However, some of the work is done for you in the form of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface.</span></span>

<span data-ttu-id="a982e-121">Per creare questa interfaccia, usare il metodo [**IDWriteGdiInterop:: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="a982e-121">To create this interface, use the [**IDWriteGdiInterop::CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) method.</span></span>

<span data-ttu-id="a982e-122">Il metodo [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) del renderer di testo personalizzato chiama il metodo [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) per creare i glifi.</span><span class="sxs-lookup"><span data-stu-id="a982e-122">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of your custom text renderer calls the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to draw the glyphs.</span></span> <span data-ttu-id="a982e-123">Il rendering degli oggetti Underline, barrato e inline deve essere eseguito dal renderer personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a982e-123">The rendering of the underline, strikethrough, and inline objects must be done by your custom renderer.</span></span>

<span data-ttu-id="a982e-124">L'interfaccia [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) esegue il rendering in un contesto di dispositivo (DC) in memoria.</span><span class="sxs-lookup"><span data-stu-id="a982e-124">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface renders to a device context (DC) in memory.</span></span> <span data-ttu-id="a982e-125">Si ottiene un handle per il controller di dominio usando il metodo [**IDWriteBitmapRenderTarget:: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) .</span><span class="sxs-lookup"><span data-stu-id="a982e-125">You get a handle to this DC by using the [**IDWriteBitmapRenderTarget::GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) method.</span></span>


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



<span data-ttu-id="a982e-126">Una volta eseguito il disegno, il controller di dominio della memoria dell'oggetto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) deve essere copiato nella superficie GDI di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a982e-126">Once the drawing has been performed, the memory DC of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object must be copied to the destination GDI surface.</span></span>

> [!Note]  
> <span data-ttu-id="a982e-127">È inoltre possibile trasferire la bitmap a un altro tipo di superficie, ad esempio una superficie GDI+.</span><span class="sxs-lookup"><span data-stu-id="a982e-127">You also have the option of transferring the bitmap to another type of surface, such as a GDI+ surface.</span></span>

 


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



> [!Note]  
> <span data-ttu-id="a982e-128">L'app ha la responsabilità di eseguire il rendering di tutti gli elementi nella finestra alla fine.</span><span class="sxs-lookup"><span data-stu-id="a982e-128">Your app has the responsibility to render everything to the window in the end.</span></span> <span data-ttu-id="a982e-129">Sono inclusi testo e grafica.</span><span class="sxs-lookup"><span data-stu-id="a982e-129">This includes text and graphics.</span></span> <span data-ttu-id="a982e-130">Si verifica una riduzione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a982e-130">There is a performance penalty to this.</span></span> <span data-ttu-id="a982e-131">Inoltre, il rendering in un controller di dominio di memoria non è un'accelerazione hardware GDI.</span><span class="sxs-lookup"><span data-stu-id="a982e-131">Additionally, rendering to a memory DC is not GDI hardware accelerated.</span></span>

 

<span data-ttu-id="a982e-132">Per una panoramica più dettagliata dell'interoperabilità con GDI, vedere [interoperabilità con GDI](interoperating-with-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="a982e-132">For a more detailed overview of interoperating with GDI see [Interoperating with GDI](interoperating-with-gdi.md).</span></span>

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a><span data-ttu-id="a982e-133">4. eseguire il rendering trasparente del testo in scala di grigi in una superficie GDI.</span><span class="sxs-lookup"><span data-stu-id="a982e-133">4. Render Grayscale Text Transparently to a GDI Surface.</span></span> <span data-ttu-id="a982e-134">(Windows 8 e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="a982e-134">(Windows 8 and later)</span></span>

<span data-ttu-id="a982e-135">A partire da Windows 8, è possibile eseguire il rendering trasparente del testo in scala di grigi in una superficie GDI per ottenere prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="a982e-135">Starting in Windows 8, you can render grayscale text transparently to a GDI surface for better performance.</span></span> <span data-ttu-id="a982e-136">A tale scopo è necessario:</span><span class="sxs-lookup"><span data-stu-id="a982e-136">To do this you need to:</span></span>

1.  <span data-ttu-id="a982e-137">Cancellare il controller di dominio della memoria per trasparenti.</span><span class="sxs-lookup"><span data-stu-id="a982e-137">Clear the memory DC to transparent.</span></span>
2.  <span data-ttu-id="a982e-138">Esegue il rendering del testo nell'HDC di memoria usando l'anti-aliasing in scala di grigi (DWRITE \_ Text \_ antialias \_ mode \_ ).</span><span class="sxs-lookup"><span data-stu-id="a982e-138">Render text to the memory HDC using grayscale antialiasing (DWRITE\_TEXT\_ANTIALIAS\_MODE\_GRAYSCALE).</span></span>
3.  <span data-ttu-id="a982e-139">Usare la funzione [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) per eseguire il rendering della memoria HDC in modo trasparente sopra l'HDC di destinazione finale.</span><span class="sxs-lookup"><span data-stu-id="a982e-139">Use the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function to render the memory HDC transparently on top of the final target HDC.</span></span>
4.  <span data-ttu-id="a982e-140">Ripetere il numero di volte necessario (ad esempio, una volta per ogni esecuzione del glifo) e tra altri elementi grafici può essere sottoposto a rendering direttamente nell'HDC di destinazione finale senza essere sovrascritto dalla funzione [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .</span><span class="sxs-lookup"><span data-stu-id="a982e-140">Repeat as many times as necessary (say, once per glyph run) and in between other graphics may be rendered directly to the final target HDC without being overwritten by the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>


```C++
pRT_->SetTextAntialiasMode(DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE);

pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

BLENDFUNCTION blendFunction = { 0 };  
blendFunction.BlendOp = AC_SRC_OVER;  
blendFunction.SourceConstantAlpha = 255;  
blendFunction.AlphaFormat = AC_SRC_ALPHA;

AlphaBlend(  
        hdc,  
        0, 0,  
        width, height,  
        pRT_->GetMemoryDC(),  
        0, 0,  
        width, height,  
        blendFunction  
        );

```



## <a name="related-topics"></a><span data-ttu-id="a982e-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a982e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a982e-142">Rendering tramite Direct2D</span><span class="sxs-lookup"><span data-stu-id="a982e-142">Render Using Direct2D</span></span>](rendering-by-using-direct2d.md)
</dt> <dt>

[<span data-ttu-id="a982e-143">Eseguire il rendering usando un renderer di testo personalizzato</span><span class="sxs-lookup"><span data-stu-id="a982e-143">Render Using a Custom Text Renderer</span></span>](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[<span data-ttu-id="a982e-144">Rendering in una superficie GDI</span><span class="sxs-lookup"><span data-stu-id="a982e-144">Render to a GDI surface</span></span>](render-to-a-gdi-surface.md)
</dt> <dt>

[<span data-ttu-id="a982e-145">Interoperabilità con GDI</span><span class="sxs-lookup"><span data-stu-id="a982e-145">Interoperating with GDI</span></span>](interoperating-with-gdi.md)
</dt> </dl>

 

 