---
title: Panoramica delle destinazioni di rendering
description: Vengono descritti i diversi tipi di destinazioni di rendering Direct2D e il modo in cui utilizzarli.
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D, destinazioni di rendering
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963210"
---
# <a name="render-targets-overview"></a><span data-ttu-id="f8029-104">Panoramica delle destinazioni di rendering</span><span class="sxs-lookup"><span data-stu-id="f8029-104">Render Targets Overview</span></span>

<span data-ttu-id="f8029-105">Una destinazione di rendering è una risorsa che eredita dall'interfaccia [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="f8029-105">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="f8029-106">Una destinazione di rendering crea risorse per il disegno e l'esecuzione di operazioni di disegno effettive.</span><span class="sxs-lookup"><span data-stu-id="f8029-106">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="f8029-107">Questo argomento descrive i diversi tipi di destinazioni di rendering Direct2D e come usarli.</span><span class="sxs-lookup"><span data-stu-id="f8029-107">This topic describes the different types of Direct2D render targets and how to use them.</span></span>

-   [<span data-ttu-id="f8029-108">Destinazioni di rendering</span><span class="sxs-lookup"><span data-stu-id="f8029-108">Render Targets</span></span>](#render-targets-overview)
    -   [<span data-ttu-id="f8029-109">Funzionalità di destinazione di rendering</span><span class="sxs-lookup"><span data-stu-id="f8029-109">Render Target Features</span></span>](#render-target-features)
    -   [<span data-ttu-id="f8029-110">Risorse di destinazione di rendering</span><span class="sxs-lookup"><span data-stu-id="f8029-110">Render Target Resources</span></span>](#render-target-resources)
    -   [<span data-ttu-id="f8029-111">Disegno di comandi</span><span class="sxs-lookup"><span data-stu-id="f8029-111">Drawing Commands</span></span>](#drawing-commands)
    -   [<span data-ttu-id="f8029-112">Gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="f8029-112">Error Handling</span></span>](#error-handling)
-   [<span data-ttu-id="f8029-113">Esempio: rendering del contenuto in una finestra</span><span class="sxs-lookup"><span data-stu-id="f8029-113">Example: Render Content to a Window</span></span>](#example-render-content-to-a-window)

## <a name="render-targets"></a><span data-ttu-id="f8029-114">Destinazioni di rendering</span><span class="sxs-lookup"><span data-stu-id="f8029-114">Render Targets</span></span>

<span data-ttu-id="f8029-115">Una destinazione di rendering è una risorsa che eredita dall'interfaccia [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="f8029-115">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="f8029-116">Una destinazione di rendering crea risorse per il disegno e l'esecuzione di operazioni di disegno effettive.</span><span class="sxs-lookup"><span data-stu-id="f8029-116">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="f8029-117">Esistono diversi tipi di destinazioni di rendering che è possibile utilizzare per eseguire il rendering della grafica nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f8029-117">There are several kinds of render targets that can be used to render graphics in the following ways:</span></span>

-   <span data-ttu-id="f8029-118">Gli oggetti [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) eseguono il rendering del contenuto in una finestra.</span><span class="sxs-lookup"><span data-stu-id="f8029-118">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) objects render content to a window.</span></span>
-   <span data-ttu-id="f8029-119">Gli oggetti [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) eseguono il rendering in un contesto di dispositivo GDI.</span><span class="sxs-lookup"><span data-stu-id="f8029-119">[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) objects render to a GDI device context.</span></span>
-   <span data-ttu-id="f8029-120">Gli oggetti di destinazione di rendering bitmap eseguono il rendering del contenuto in una bitmap fuori schermo.</span><span class="sxs-lookup"><span data-stu-id="f8029-120">Bitmap render target objects render content to an off-screen bitmap.</span></span>
-   <span data-ttu-id="f8029-121">DXGI rendering degli oggetti di destinazione rendering in una superficie DXGI per l'uso con Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f8029-121">DXGI render target objects render to a DXGI surface for use with Direct3D.</span></span>

<span data-ttu-id="f8029-122">Poiché una destinazione di rendering è associata a un particolare dispositivo di rendering, si tratta di una risorsa dipendente dal dispositivo e smette di funzionare se il dispositivo viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="f8029-122">Because a render target is associated with a particular rendering device, it is a device-dependent resource and ceases to function if the device is removed.</span></span>

### <a name="render-target-features"></a><span data-ttu-id="f8029-123">Funzionalità di destinazione di rendering</span><span class="sxs-lookup"><span data-stu-id="f8029-123">Render Target Features</span></span>

<span data-ttu-id="f8029-124">È possibile specificare se una destinazione di rendering utilizza l'accelerazione hardware e se viene eseguito il rendering di una visualizzazione remota da un computer locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="f8029-124">You can specify whether a render target uses hardware acceleration and whether remote display is rendered by a local or a remote computer.</span></span> <span data-ttu-id="f8029-125">Le destinazioni di rendering possono essere impostate per il rendering con alias o con alias.</span><span class="sxs-lookup"><span data-stu-id="f8029-125">Render targets can be set up for aliased or antialiased rendering.</span></span> <span data-ttu-id="f8029-126">Per il rendering di scene con un numero elevato di primitive, uno sviluppatore può anche eseguire il rendering di grafica 2D in modalità con alias e utilizzare l'anti-aliasing di D3D multisample per ottenere una maggiore scalabilità.</span><span class="sxs-lookup"><span data-stu-id="f8029-126">For rendering scenes with a large number of primitives, a developer can also render 2-D graphics in aliased mode and use D3D multisample antialiasing to achieve greater scalability.</span></span>

<span data-ttu-id="f8029-127">Le destinazioni di rendering possono inoltre raggruppare le operazioni di disegno in livelli rappresentati dall'interfaccia [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) .</span><span class="sxs-lookup"><span data-stu-id="f8029-127">Render targets can also group drawing operations into layers represented by the [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) interface.</span></span> <span data-ttu-id="f8029-128">I livelli sono utili per raccogliere le operazioni di disegno da comporre insieme durante il rendering di un frame.</span><span class="sxs-lookup"><span data-stu-id="f8029-128">Layers are useful for collecting drawing operations to be composited together when rendering a frame.</span></span> <span data-ttu-id="f8029-129">Per alcuni scenari, può trattarsi di un'alternativa utile per eseguire il rendering in una destinazione di rendering bitmap e quindi riutilizzare il contenuto della bitmap, perché i costi di allocazione per i livelli sono inferiori rispetto a quelli di un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="f8029-129">For some scenarios, this can be a useful alternative to rendering to a bitmap render target, and then reusing the bitmap contents, as allocation costs for layering are lower than for an [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).</span></span>

<span data-ttu-id="f8029-130">Le destinazioni di rendering possono creare nuove destinazioni di rendering compatibili con se stesse, che risulta utile per il rendering intermedio all'esterno dello schermo, mantenendo al tempo stesso le varie proprietà di destinazione di rendering impostate nell'oggetto originale.</span><span class="sxs-lookup"><span data-stu-id="f8029-130">Render targets can create new render targets that are compatible with themselves, which is useful for intermediate off-screen rendering while retaining the various render-target properties that were set on the original.</span></span>

<span data-ttu-id="f8029-131">È anche possibile eseguire il rendering usando GDI in una destinazione di rendering Direct2D chiamando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) in una destinazione di rendering per [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), che contiene metodi [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) e [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) che possono essere usati per recuperare un contesto di dispositivo GDI.</span><span class="sxs-lookup"><span data-stu-id="f8029-131">It is also possible to render using GDI on a Direct2D render target by calling [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a render target for [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which has [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) and [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) methods on it that can be used to retrieve a GDI device context.</span></span> <span data-ttu-id="f8029-132">Il rendering tramite GDI è possibile solo se la destinazione di rendering è stata creata con il flag di [**utilizzo della destinazione di rendering d2d1 impostato su \_ \_ \_ \_ GDI \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) .</span><span class="sxs-lookup"><span data-stu-id="f8029-132">Rendering via GDI is possible only if the render target was created with the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag set.</span></span> <span data-ttu-id="f8029-133">Questa operazione è utile per le applicazioni che eseguono principalmente il rendering con Direct2D ma hanno un modello di estendibilità o altri contenuti legacy che richiedono la possibilità di eseguire il rendering con GDI.</span><span class="sxs-lookup"><span data-stu-id="f8029-133">This is useful for applications that are primarily rendering with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span> <span data-ttu-id="f8029-134">Per ulteriori informazioni, vedere [Cenni preliminari sull'interoperatività Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f8029-134">For more information, see the [Direct2D and GDI Interoperation Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

### <a name="render-target-resources"></a><span data-ttu-id="f8029-135">Risorse di destinazione di rendering</span><span class="sxs-lookup"><span data-stu-id="f8029-135">Render Target Resources</span></span>

<span data-ttu-id="f8029-136">Analogamente a una factory, una destinazione di rendering può creare risorse di disegno.</span><span class="sxs-lookup"><span data-stu-id="f8029-136">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="f8029-137">Tutte le risorse create da una destinazione di rendering sono risorse dipendenti dal dispositivo, proprio come la destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="f8029-137">Any resources created by a render target are device-dependent resources (just like the render target).</span></span> <span data-ttu-id="f8029-138">Una destinazione di rendering può creare i tipi di risorse seguenti:</span><span class="sxs-lookup"><span data-stu-id="f8029-138">A render target can create the following types of resources:</span></span>

-   <span data-ttu-id="f8029-139">Bitmap</span><span class="sxs-lookup"><span data-stu-id="f8029-139">Bitmaps</span></span>
-   <span data-ttu-id="f8029-140">Pennelli</span><span class="sxs-lookup"><span data-stu-id="f8029-140">Brushes</span></span>
-   <span data-ttu-id="f8029-141">Livelli</span><span class="sxs-lookup"><span data-stu-id="f8029-141">Layers</span></span>
-   <span data-ttu-id="f8029-142">Mesh</span><span class="sxs-lookup"><span data-stu-id="f8029-142">Meshes</span></span>

### <a name="drawing-commands"></a><span data-ttu-id="f8029-143">Disegno di comandi</span><span class="sxs-lookup"><span data-stu-id="f8029-143">Drawing Commands</span></span>

<span data-ttu-id="f8029-144">Per eseguire il rendering del contenuto, usare i metodi di disegno della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="f8029-144">To render content, you use the render target drawing methods.</span></span> <span data-ttu-id="f8029-145">Prima di iniziare a disegnare, chiamare il metodo [**ID2D1RenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) .</span><span class="sxs-lookup"><span data-stu-id="f8029-145">Before you begin drawing, you call the [**ID2D1RenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method.</span></span> <span data-ttu-id="f8029-146">Al termine del disegno, chiamare il metodo [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="f8029-146">After you finished drawing, you call the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="f8029-147">Tra queste chiamate, si usano i metodi Draw e Fill per eseguire il rendering delle risorse di disegno.</span><span class="sxs-lookup"><span data-stu-id="f8029-147">Between these calls, you use Draw and Fill methods to render drawing resources.</span></span> <span data-ttu-id="f8029-148">La maggior parte dei metodi di disegno e riempimento accetta una forma, ovvero una primitiva o una geometria, e un pennello per riempire o delineare la forma.</span><span class="sxs-lookup"><span data-stu-id="f8029-148">Most Draw and Fill methods take a shape (either a primitive or a geometry) and a brush for filling or outlining the shape.</span></span>

<span data-ttu-id="f8029-149">Le destinazioni di rendering forniscono metodi per il ritaglio, l'applicazione di maschere di opacità e la trasformazione dello spazio delle coordinate.</span><span class="sxs-lookup"><span data-stu-id="f8029-149">Render targets provide methods for clipping, applying opacity masks, and transforming the coordinate space.</span></span>

<span data-ttu-id="f8029-150">Direct2D usa un sistema di coordinate a sinistra: i valori positivi dell'asse x procedono verso destra e i valori positivi dell'asse y procedono verso il basso.</span><span class="sxs-lookup"><span data-stu-id="f8029-150">Direct2D uses a left-handed coordinate system: positive x-axis values proceed to the right and positive y-axis values proceed downward.</span></span>

### <a name="error-handling"></a><span data-ttu-id="f8029-151">Gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="f8029-151">Error Handling</span></span>

<span data-ttu-id="f8029-152">I comandi di disegno della destinazione di rendering non indicano se l'operazione richiesta è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="f8029-152">Render target drawing commands do not indicate whether the requested operation was successful.</span></span> <span data-ttu-id="f8029-153">Per determinare se sono presenti errori di disegno, chiamare il metodo [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) della destinazione di rendering o il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) per ottenere un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f8029-153">To find out whether there are drawing errors, call the render target [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) method or [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method to obtain an **HRESULT**.</span></span>

## <a name="example-render-content-to-a-window"></a><span data-ttu-id="f8029-154">Esempio: rendering del contenuto in una finestra</span><span class="sxs-lookup"><span data-stu-id="f8029-154">Example: Render Content to a Window</span></span>

<span data-ttu-id="f8029-155">Nell'esempio seguente viene usato il metodo [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) per creare un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span><span class="sxs-lookup"><span data-stu-id="f8029-155">The following example uses the [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) method to create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



<span data-ttu-id="f8029-156">Nell'esempio seguente viene usato [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) per creare testo nella finestra.</span><span class="sxs-lookup"><span data-stu-id="f8029-156">The next example uses the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) to draw text to the window.</span></span>


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
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



<span data-ttu-id="f8029-157">Il codice è stato omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="f8029-157">Code has been omitted from this example.</span></span>

 

 