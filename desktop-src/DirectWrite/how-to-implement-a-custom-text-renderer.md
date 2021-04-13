---
title: Eseguire il rendering usando un renderer di testo personalizzato
description: Un DirectWrite \ 160; il layout del testo può essere disegnato da un renderer di testo personalizzato derivato da IDWriteTextRenderer.
ms.assetid: a5b09733-24b2-408e-a1f9-cf7ad20c5c63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cda56fc5cc38a62e48a2f62066edfec2327e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399309"
---
# <a name="render-using-a-custom-text-renderer"></a><span data-ttu-id="fdaf3-103">Eseguire il rendering usando un renderer di testo personalizzato</span><span class="sxs-lookup"><span data-stu-id="fdaf3-103">Render Using a Custom Text Renderer</span></span>

<span data-ttu-id="fdaf3-104">Un [](direct-write-portal.md) [**layout di testo**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) DirectWrite può essere disegnato da un renderer di testo personalizzato derivato da [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer).</span><span class="sxs-lookup"><span data-stu-id="fdaf3-104">A [DirectWrite](direct-write-portal.md) [**text layout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) can be drawn by a custom text renderer derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer).</span></span> <span data-ttu-id="fdaf3-105">È necessario un renderer personalizzato per sfruttare le funzionalità avanzate di DirectWrite, ad esempio il rendering in una bitmap o in una superficie GDI, oggetti inline ed effetti di disegno dei client.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-105">A custom renderer is required to take advantage of some advanced features of DirectWrite, such as rendering to a bitmap or GDI surface, inline objects, and client drawing effects.</span></span> <span data-ttu-id="fdaf3-106">In questa esercitazione vengono descritti i metodi di **IDWriteTextRenderer** e viene fornita un'implementazione di esempio che utilizza [Direct2D](../direct2d/direct2d-portal.md) per eseguire il rendering del testo con un riempimento bitmap.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-106">This tutorial describes the methods of **IDWriteTextRenderer**, and provides an example implementation that uses [Direct2D](../direct2d/direct2d-portal.md) to render text with a bitmap fill.</span></span>

<span data-ttu-id="fdaf3-107">Questa esercitazione contiene le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="fdaf3-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="fdaf3-108">Costruttore</span><span class="sxs-lookup"><span data-stu-id="fdaf3-108">The Constructor</span></span>](#the-constructor)
-   [<span data-ttu-id="fdaf3-109">DrawGlyphRun ()</span><span class="sxs-lookup"><span data-stu-id="fdaf3-109">DrawGlyphRun()</span></span>](#drawglyphrun)
-   [<span data-ttu-id="fdaf3-110">DrawUnderline () e DrawStrikethrough ()</span><span class="sxs-lookup"><span data-stu-id="fdaf3-110">DrawUnderline() and DrawStrikethrough()</span></span>](#drawunderline-and-drawstrikethrough)
-   [<span data-ttu-id="fdaf3-111">Allineamento pixel, pixel per DIP e trasformazione</span><span class="sxs-lookup"><span data-stu-id="fdaf3-111">Pixel Snapping, Pixels per DIP, and Transform</span></span>](#pixel-snapping-pixels-per-dip-and-transform)
    -   [<span data-ttu-id="fdaf3-112">IsPixelSnappingDisabled()</span><span class="sxs-lookup"><span data-stu-id="fdaf3-112">IsPixelSnappingDisabled()</span></span>](#ispixelsnappingdisabled)
    -   [<span data-ttu-id="fdaf3-113">GetCurrentTransform()</span><span class="sxs-lookup"><span data-stu-id="fdaf3-113">GetCurrentTransform()</span></span>](#getcurrenttransform)
    -   [<span data-ttu-id="fdaf3-114">GetPixelsPerDip()</span><span class="sxs-lookup"><span data-stu-id="fdaf3-114">GetPixelsPerDip()</span></span>](#getpixelsperdip)
-   [<span data-ttu-id="fdaf3-115">DrawInlineObject()</span><span class="sxs-lookup"><span data-stu-id="fdaf3-115">DrawInlineObject()</span></span>](#drawinlineobject)
-   [<span data-ttu-id="fdaf3-116">Distruttore</span><span class="sxs-lookup"><span data-stu-id="fdaf3-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="fdaf3-117">Uso del renderer di testo personalizzato</span><span class="sxs-lookup"><span data-stu-id="fdaf3-117">Using the Custom Text Renderer</span></span>](#using-the-custom-text-renderer)

<span data-ttu-id="fdaf3-118">Il renderer di testo personalizzato deve implementare i metodi ereditati da IUnknown oltre ai metodi elencati nella pagina di riferimento [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) e di seguito.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-118">Your custom text renderer must implement the methods inherited from IUnknown in addition to the methods listed on the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) reference page and below.</span></span>

<span data-ttu-id="fdaf3-119">Per il codice sorgente completo per il renderer di testo personalizzato, vedere i file CustomTextRenderer. cpp e CustomTextRenderer. h dell' [esempio DirectWrite Hello World](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="fdaf3-119">For the full source code for the custom text renderer, see the CustomTextRenderer.cpp and CustomTextRenderer.h files of the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="the-constructor"></a><span data-ttu-id="fdaf3-120">Costruttore</span><span class="sxs-lookup"><span data-stu-id="fdaf3-120">The Constructor</span></span>

<span data-ttu-id="fdaf3-121">Il renderer di testo personalizzato richiede un costruttore.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-121">Your custom text renderer will need a constructor.</span></span> <span data-ttu-id="fdaf3-122">In questo esempio vengono utilizzati pennelli [Direct2D](../direct2d/direct2d-portal.md) a tinta unita e bitmap per eseguire il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-122">This example uses both solid and bitmap [Direct2D](../direct2d/direct2d-portal.md) brushes to render the text.</span></span>

<span data-ttu-id="fdaf3-123">Per questo motivo, il costruttore accetta i parametri trovati nella tabella seguente con le descrizioni.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-123">Because of this, the constructor takes the parameters found in the table below with descriptions.</span></span>



| <span data-ttu-id="fdaf3-124">Parametro</span><span class="sxs-lookup"><span data-stu-id="fdaf3-124">Parameter</span></span>       | <span data-ttu-id="fdaf3-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdaf3-125">Description</span></span>                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdaf3-126">*pD2DFactory*</span><span class="sxs-lookup"><span data-stu-id="fdaf3-126">*pD2DFactory*</span></span>   | <span data-ttu-id="fdaf3-127">Puntatore a un oggetto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) che verrà usato per creare le risorse Direct2D necessarie.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-127">A pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create any Direct2D resources that are needed.</span></span>                                                                                                        |
| <span data-ttu-id="fdaf3-128">*pRT*</span><span class="sxs-lookup"><span data-stu-id="fdaf3-128">*pRT*</span></span>           | <span data-ttu-id="fdaf3-129">Puntatore all'oggetto [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) di cui verrà eseguito il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-129">A pointer to the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object that the text will be rendered to.</span></span> |
| <span data-ttu-id="fdaf3-130">*pOutlineBrush*</span><span class="sxs-lookup"><span data-stu-id="fdaf3-130">*pOutlineBrush*</span></span> | <span data-ttu-id="fdaf3-131">Puntatore a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) che verrà usato per disegnare il contorno del testo</span><span class="sxs-lookup"><span data-stu-id="fdaf3-131">A pointer to the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) that will be use to draw outline of the text</span></span>                                                                                                                     |
| <span data-ttu-id="fdaf3-132">*pFillBrush*</span><span class="sxs-lookup"><span data-stu-id="fdaf3-132">*pFillBrush*</span></span>    | <span data-ttu-id="fdaf3-133">Puntatore a [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) che verrà usato per riempire il testo.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-133">A pointer to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that will be used to fill the text.</span></span>                                                                                                                                      |



 

<span data-ttu-id="fdaf3-134">Questi verranno archiviati dal costruttore, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-134">These will be stored by the constructor as shown in the following code.</span></span>


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT, 
    ID2D1SolidColorBrush* pOutlineBrush, 
    ID2D1BitmapBrush* pFillBrush
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT), 
pOutlineBrush_(pOutlineBrush), 
pFillBrush_(pFillBrush)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
    pOutlineBrush_->AddRef();
    pFillBrush_->AddRef();
}
```



## <a name="drawglyphrun"></a><span data-ttu-id="fdaf3-135">DrawGlyphRun ()</span><span class="sxs-lookup"><span data-stu-id="fdaf3-135">DrawGlyphRun()</span></span>

<span data-ttu-id="fdaf3-136">Il metodo [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) è il metodo di callback principale del renderer di testo.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-136">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method is the main callback method of the text renderer.</span></span> <span data-ttu-id="fdaf3-137">Viene passata un'esecuzione di glifi da sottoposta a rendering, oltre a informazioni quali l'origine e la modalità di misurazione della linea di base.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-137">It is passed a run of glyphs to be rendered in addition to information such as the baseline origin and measuring mode.</span></span> <span data-ttu-id="fdaf3-138">Passa inoltre un oggetto effetto di disegno client da applicare all'esecuzione del glifo.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-138">It also passes a client drawing effect object to be applied to the glyph run.</span></span> <span data-ttu-id="fdaf3-139">Per ulteriori informazioni, vedere l'argomento [How to Add client Drawing Effects to a text layout](how-to-add-custom-drawing-efffects-to-a-text-layout.md) .</span><span class="sxs-lookup"><span data-stu-id="fdaf3-139">For more information, see the [How to Add Client Drawing Effects to a Text Layout](how-to-add-custom-drawing-efffects-to-a-text-layout.md) topic.</span></span>

<span data-ttu-id="fdaf3-140">Questa implementazione del renderer di testo esegue il rendering delle esecuzioni del glifo mediante la conversione in geometrie [Direct2D](rendering-by-using-direct2d.md) e quindi il disegno e il riempimento delle geometrie.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-140">This text renderer implementation renders glyph runs by converting them to [Direct2D](rendering-by-using-direct2d.md) geometries and then drawing and filling the geometries.</span></span> <span data-ttu-id="fdaf3-141">Questa operazione è costituita dai passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-141">This consists of the following steps.</span></span>

1.  <span data-ttu-id="fdaf3-142">Creare un oggetto [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e quindi recuperare l'oggetto [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) usando il metodo [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .</span><span class="sxs-lookup"><span data-stu-id="fdaf3-142">Create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object, and then retrieve the [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) object by using the [**ID2D1PathGeometry::Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method.</span></span>

    ```C++
    // Create the path geometry.
    ID2D1PathGeometry* pPathGeometry = NULL;
    hr = pD2DFactory_->CreatePathGeometry(
            &pPathGeometry
            );

    // Write to the path geometry using the geometry sink.
    ID2D1GeometrySink* pSink = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Open(
            &pSink
            );
    }
    ```

    

2.  <span data-ttu-id="fdaf3-143">L' [**\_ \_ esecuzione del glifo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) passata a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contiene un oggetto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) , denominato *fontFace*, che rappresenta il tipo di carattere per l'intera esecuzione del glifo.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-143">The [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) that is passed to [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contains a [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object, named *fontFace*, that represents the font face for the whole glyph run.</span></span> <span data-ttu-id="fdaf3-144">Inserire il contorno del glifo eseguito nel sink di geometria usando il metodo [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-144">Put the outline of the glyph run into the geometry sink by using the [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) method, as shown in the following code.</span></span>

    ```C++
    // Get the glyph run outline geometries back from DirectWrite and place them within the
    // geometry sink.
    if (SUCCEEDED(hr))
    {
        hr = glyphRun->fontFace->GetGlyphRunOutline(
            glyphRun->fontEmSize,
            glyphRun->glyphIndices,
            glyphRun->glyphAdvances,
            glyphRun->glyphOffsets,
            glyphRun->glyphCount,
            glyphRun->isSideways,
            glyphRun->bidiLevel%2,
            pSink
            );
    }
    ```

    

3.  <span data-ttu-id="fdaf3-145">Dopo aver compilato il sink di geometria, chiuderlo.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-145">After filling the geometry sink, close it.</span></span>

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  <span data-ttu-id="fdaf3-146">L'origine dell'esecuzione del glifo deve essere convertita in modo che venga sottoposta a rendering dall'origine di base corretta, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-146">The origin of the glyph run must be translated so that it is rendered from the correct baseline origin, as shown in the following code.</span></span>

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    <span data-ttu-id="fdaf3-147">*BaselineOriginX* e *baselineOriginY* vengono passati come parametri al metodo di callback [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="fdaf3-147">The *baselineOriginX* and *baselineOriginY* are passed as parameters to the [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback method.</span></span>

5.  <span data-ttu-id="fdaf3-148">Creare la geometria trasformata usando il metodo [**ID2D1Factory:: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) e passando la geometria del percorso e la matrice di traslazione.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-148">Create the transformed geometry by using the [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method and passing the path geometry and the translation matrix.</span></span>

    ```C++
    // Create the transformed geometry
    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pPathGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

6.  <span data-ttu-id="fdaf3-149">Infine, disegnare la struttura della geometria trasformata e riempirla usando i metodi [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) e i pennelli [Direct2D](../direct2d/direct2d-portal.md) archiviati come variabili membro.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-149">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

7.  <span data-ttu-id="fdaf3-150">Ora che è stata completata la creazione, non dimenticare di pulire gli oggetti creati in questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-150">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a><span data-ttu-id="fdaf3-151">DrawUnderline () e DrawStrikethrough ()</span><span class="sxs-lookup"><span data-stu-id="fdaf3-151">DrawUnderline() and DrawStrikethrough()</span></span>

<span data-ttu-id="fdaf3-152">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) dispone anche di callback per disegnare la sottolineatura e la barratura.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-152">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) also has callbacks for drawing the underline and strikethrough.</span></span> <span data-ttu-id="fdaf3-153">Questo esempio disegna un rettangolo semplice per una sottolineatura o una barratura, ma è possibile disegnare altre forme.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-153">This example draws a simple rectangle for an underline or strikethrough, but other shapes can be drawn.</span></span>

<span data-ttu-id="fdaf3-154">Il disegno di una sottolineatura tramite [Direct2D](../direct2d/direct2d-portal.md) è costituito dai passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-154">Drawing an underline by using [Direct2D](../direct2d/direct2d-portal.md) consists of the following steps.</span></span>

1.  <span data-ttu-id="fdaf3-155">Per prima cosa, creare una struttura [**d2d1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) con le dimensioni e la forma della sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-155">First, create a [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure of the size and shape of the underline.</span></span> <span data-ttu-id="fdaf3-156">La struttura di [**\_ sottolineatura DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) passata al metodo di callback [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) fornisce l'offset, la larghezza e lo spessore della sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-156">The [**DWRITE\_UNDERLINE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) structure that is passed to the [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) callback method provides the offset, width, and thickness of the underline.</span></span>

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  <span data-ttu-id="fdaf3-157">Successivamente, creare un oggetto [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) usando il metodo [**ID2D1Factory:: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) e la struttura di [**d2d1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) inizializzata.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-157">Next, create an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object by using the [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) method and the initialized [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure.</span></span>

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  <span data-ttu-id="fdaf3-158">Come per l'esecuzione del glifo, l'origine della geometria di sottolineatura deve essere convertita in base ai valori di origine della linea di base, usando il metodo [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) .</span><span class="sxs-lookup"><span data-stu-id="fdaf3-158">As with the glyph run, the origin of the underline geometry must be translated, based on the baseline origin values, by using the [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method.</span></span>

    ```C++
    // Initialize a matrix to translate the origin of the underline
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );

    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pRectangleGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

4.  <span data-ttu-id="fdaf3-159">Infine, disegnare la struttura della geometria trasformata e riempirla usando i metodi [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) e i pennelli [Direct2D](../direct2d/direct2d-portal.md) archiviati come variabili membro.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-159">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

5.  <span data-ttu-id="fdaf3-160">Ora che è stata completata la creazione, non dimenticare di pulire gli oggetti creati in questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-160">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

<span data-ttu-id="fdaf3-161">Il processo di disegno di un barrato è lo stesso.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-161">The process for drawing a strikethrough is the same.</span></span> <span data-ttu-id="fdaf3-162">Tuttavia, la barratura avrà un offset diverso e probabilmente una larghezza e uno spessore differenti.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-162">However, the strikethrough will have a different offset, and likely a different width and thickness.</span></span>

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a><span data-ttu-id="fdaf3-163">Allineamento pixel, pixel per DIP e trasformazione</span><span class="sxs-lookup"><span data-stu-id="fdaf3-163">Pixel Snapping, Pixels per DIP, and Transform</span></span>

### <a name="ispixelsnappingdisabled"></a><span data-ttu-id="fdaf3-164">IsPixelSnappingDisabled()</span><span class="sxs-lookup"><span data-stu-id="fdaf3-164">IsPixelSnappingDisabled()</span></span>

<span data-ttu-id="fdaf3-165">Questo metodo viene chiamato per determinare se il blocco del pixel è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-165">This method is called to determine whether pixel snapping is disabled.</span></span> <span data-ttu-id="fdaf3-166">Il valore predefinito consigliato è **false** ed è l'output di questo esempio.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-166">The recommended default is **FALSE**, and that is the output of this example.</span></span>


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a><span data-ttu-id="fdaf3-167">GetCurrentTransform()</span><span class="sxs-lookup"><span data-stu-id="fdaf3-167">GetCurrentTransform()</span></span>

<span data-ttu-id="fdaf3-168">In questo esempio viene eseguito il rendering in una destinazione di rendering Direct2D, quindi la trasformazione viene reindirizzata dalla destinazione di rendering utilizzando [**ID2D1RenderTarget:: GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).</span><span class="sxs-lookup"><span data-stu-id="fdaf3-168">This example renders to a Direct2D render target, so forward the transform from the render target using [**ID2D1RenderTarget::GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).</span></span>


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a><span data-ttu-id="fdaf3-169">GetPixelsPerDip()</span><span class="sxs-lookup"><span data-stu-id="fdaf3-169">GetPixelsPerDip()</span></span>

<span data-ttu-id="fdaf3-170">Questo metodo viene chiamato per ottenere il numero di pixel per ogni DIP (device independent pixel).</span><span class="sxs-lookup"><span data-stu-id="fdaf3-170">This method is called to get the number of pixels per Device Independent Pixel (DIP).</span></span>


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a><span data-ttu-id="fdaf3-171">DrawInlineObject()</span><span class="sxs-lookup"><span data-stu-id="fdaf3-171">DrawInlineObject()</span></span>

<span data-ttu-id="fdaf3-172">Un renderer di testo personalizzato dispone anche di un callback per disegnare oggetti inline.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-172">A custom text renderer also has a callback for drawing inline objects.</span></span> <span data-ttu-id="fdaf3-173">In questo esempio, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-173">In this example, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) returns E\_NOTIMPL.</span></span> <span data-ttu-id="fdaf3-174">Una spiegazione di come creare oggetti inline esula dall'ambito di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-174">An explanation of how to draw inline objects is beyond the scope of this tutorial.</span></span> <span data-ttu-id="fdaf3-175">Per ulteriori informazioni, vedere l'argomento [come aggiungere oggetti inline a un layout di testo](how-to-add-inline-objects-to-a-text-layout.md) .</span><span class="sxs-lookup"><span data-stu-id="fdaf3-175">For more information, see the [How to Add Inline Objects to a Text Layout](how-to-add-inline-objects-to-a-text-layout.md) topic.</span></span>

## <a name="the-destructor"></a><span data-ttu-id="fdaf3-176">Distruttore</span><span class="sxs-lookup"><span data-stu-id="fdaf3-176">The Destructor</span></span>

<span data-ttu-id="fdaf3-177">È importante rilasciare tutti i puntatori usati dalla classe renderer del testo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-177">It is important to release any pointers that were used by the custom text renderer class.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a><span data-ttu-id="fdaf3-178">Uso del renderer di testo personalizzato</span><span class="sxs-lookup"><span data-stu-id="fdaf3-178">Using the Custom Text Renderer</span></span>

<span data-ttu-id="fdaf3-179">Per eseguire il rendering con il renderer personalizzato, usare il metodo [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , che accetta un'interfaccia di callback derivata da [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) come argomento, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-179">You render with the custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="fdaf3-180">Il metodo [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) chiama i metodi del callback del renderer personalizzato fornito.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-180">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="fdaf3-181">I metodi [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)e [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) descritti in precedenza eseguono le funzioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="fdaf3-181">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods described above perform the drawing functions.</span></span>

 

 