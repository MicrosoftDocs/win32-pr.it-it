---
title: Cenni preliminari sull'interoperabilità
description: Riepiloga le diverse tecnologie che è possibile usare con Direct2D.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Direct2D, interoperatività GDI
- Direct2D, interoperatività GDI+
- Direct2D, interoperabilità
- Direct2D, interoperabilità DirectWrite
- interoperabilità, Direct2D
- interoperabilità, Direct3D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilità, Graphics Device Interface (GDI)
- interoperabilità, GDI+
- Interoperabilità DirectWrite
- interoperabilità, DirectWrite
- Windows Imaging Component (WIC)
- WIC (componente Windows Imaging)
- interoperabilità, componente imaging Windows (WIC)
- Direct2D, interoperatività WIC
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6f56c570a837a541bac9467477d4f6009bda019e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399198"
---
# <a name="interoperability-overview"></a><span data-ttu-id="b29ef-119">Cenni preliminari sull'interoperabilità</span><span class="sxs-lookup"><span data-stu-id="b29ef-119">Interoperability Overview</span></span>

<span data-ttu-id="b29ef-120">Una delle funzionalità chiave di le convenzioni è l'abilitazione dell'interoperabilità tra Direct2D e altre piattaforme di rendering, in modo che gli sviluppatori possano usare i punti di forza specifici di ogni piattaforma senza essere costretti a compromettere la scelta di una piattaforma per tutte le esigenze.</span><span class="sxs-lookup"><span data-stu-id="b29ef-120">One of Direct2D's key features is enabling interoperability between Direct2D and other rendering platforms so that developers can use the specific strengths of each platform without being forced into compromises by choosing one platform for all needs.</span></span> <span data-ttu-id="b29ef-121">In questo argomento vengono riepilogate le diverse piattaforme con cui Direct2D è interoperativo.</span><span class="sxs-lookup"><span data-stu-id="b29ef-121">This topic summarizes the different platforms with which Direct2D is interoperable.</span></span> <span data-ttu-id="b29ef-122">Include le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b29ef-122">It contains the following sections.</span></span>

-   [<span data-ttu-id="b29ef-123">Interoperabilità GDI</span><span class="sxs-lookup"><span data-stu-id="b29ef-123">GDI Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="b29ef-124">Interoperabilità GDI+</span><span class="sxs-lookup"><span data-stu-id="b29ef-124">GDI+ Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="b29ef-125">Interoperabilità Direct3D</span><span class="sxs-lookup"><span data-stu-id="b29ef-125">Direct3D Interoperability</span></span>](#direct3d-interoperability)
-   [<span data-ttu-id="b29ef-126">Interoperabilità DirectWrite</span><span class="sxs-lookup"><span data-stu-id="b29ef-126">DirectWrite Interoperability</span></span>](#directwrite-interoperability)
-   [<span data-ttu-id="b29ef-127">Interoperabilità di Windows Imaging Component (WIC)</span><span class="sxs-lookup"><span data-stu-id="b29ef-127">Windows Imaging Component (WIC) Interoperability</span></span>](#windows-imaging-component-wic-interoperability)
-   [<span data-ttu-id="b29ef-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b29ef-128">Related topics</span></span>](#related-topics)

<span data-ttu-id="b29ef-129">Il diagramma seguente riepiloga le diverse piattaforme con cui Direct2D è interoperativo e elenca alcuni metodi e interfacce che forniscono l'interoperabilità.</span><span class="sxs-lookup"><span data-stu-id="b29ef-129">The following diagram summarizes the different platforms with which Direct2D is interoperable and lists some methods and interfaces that provide interoperability.</span></span>

![diagramma delle piattaforme con cui è interopera Direct2D, tra cui Direct3D 10,1, DirectWrite, WIC, GDI+ e GDI](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a><span data-ttu-id="b29ef-131">Interoperabilità GDI</span><span class="sxs-lookup"><span data-stu-id="b29ef-131">GDI Interoperability</span></span>

<span data-ttu-id="b29ef-132">Direct2D consente l'interoperabilità bidirezionale con GDI.</span><span class="sxs-lookup"><span data-stu-id="b29ef-132">Direct2D enables two-way interoperability with GDI.</span></span> <span data-ttu-id="b29ef-133">È possibile utilizzare un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) per scrivere contenuto Direct2D in un [contesto di dispositivo](/windows/desktop/gdi/device-contexts) GDI (DC) oppure è possibile utilizzare [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) per ottenere una rappresentazione del controller di dominio di una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="b29ef-133">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to a GDI [device context](/windows/desktop/gdi/device-contexts) (DC), or you can use [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to obtain a DC representation of a render target.</span></span>

<span data-ttu-id="b29ef-134">Per ulteriori informazioni ed esempi, vedere [Cenni preliminari sull'interoperabilità Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b29ef-134">For more information and examples, see the [Direct2D and GDI Interoperability Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="b29ef-135">Interoperabilità GDI+</span><span class="sxs-lookup"><span data-stu-id="b29ef-135">GDI+ Interoperability</span></span>

<span data-ttu-id="b29ef-136">È possibile utilizzare GDI+ con Direct2D in modo analogo a GDI.</span><span class="sxs-lookup"><span data-stu-id="b29ef-136">You can use GDI+ with Direct2D in the same manner as GDI.</span></span> <span data-ttu-id="b29ef-137">È possibile usare un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) per scrivere contenuto Direct2D nello stesso controller di dominio del contenuto GDI+.</span><span class="sxs-lookup"><span data-stu-id="b29ef-137">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to the same DC as your GDI+ content.</span></span> <span data-ttu-id="b29ef-138">Questo approccio consente di iniziare ad aggiungere contenuto Direct2D alle applicazioni che vengono principalmente sottoposte a rendering tramite GDI+.</span><span class="sxs-lookup"><span data-stu-id="b29ef-138">This approach enables you to start adding Direct2D content to applications that primarily render by using GDI+.</span></span>

<span data-ttu-id="b29ef-139">È inoltre possibile utilizzare un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) per fornire l'accesso a un controller di dominio GDI che scrive tramite Direct2D, quindi utilizzare il metodo [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) per creare un oggetto.</span><span class="sxs-lookup"><span data-stu-id="b29ef-139">You can also use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to provide access to a GDI DC that writes by using Direct2D, and then use the [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) method to create a object.</span></span> <span data-ttu-id="b29ef-140">Questo approccio è utile per le applicazioni che eseguono principalmente il rendering con Direct2D, ma hanno un modello di estendibilità o altri contenuti legacy che richiedono la possibilità di eseguire il rendering con GDI+.</span><span class="sxs-lookup"><span data-stu-id="b29ef-140">This approach is useful for applications that primarily render with Direct2D, but have an extensibility model or other legacy content that requires the ability to render with GDI+.</span></span>

## <a name="direct3d-interoperability"></a><span data-ttu-id="b29ef-141">Interoperabilità Direct3D</span><span class="sxs-lookup"><span data-stu-id="b29ef-141">Direct3D Interoperability</span></span>

<span data-ttu-id="b29ef-142">Direct2D può usare una destinazione di rendering della superficie DXGI (creata dal metodo [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ) per scrivere in un [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface).</span><span class="sxs-lookup"><span data-stu-id="b29ef-142">Direct2D can use a DXGI surface render target (created by the [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method) to write to an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface).</span></span> <span data-ttu-id="b29ef-143">Questa azione consente di aggiungere sfondi e interfacce 2D a scene 3D e di usare il contenuto Direct2D come trama per un modello 3D.</span><span class="sxs-lookup"><span data-stu-id="b29ef-143">This action enables you to add 2-D backgrounds and interfaces to 3-D scenes and use Direct2D content as a texture for a 3-D model.</span></span> <span data-ttu-id="b29ef-144">Direct2D può inoltre assumere un [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) e utilizzare il metodo [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) per creare una rappresentazione bitmap.</span><span class="sxs-lookup"><span data-stu-id="b29ef-144">Direct2D can also take an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) and use the [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) method to create a bitmap representation.</span></span>

<span data-ttu-id="b29ef-145">Per ulteriori informazioni ed esempi, vedere [Cenni preliminari sull'interoperabilità di Direct2D e Direct3D](direct2d-and-direct3d-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b29ef-145">For more information and examples, see the [Direct2D and Direct3D Interoperability Overview](direct2d-and-direct3d-interoperation-overview.md).</span></span>

## <a name="directwrite-interoperability"></a><span data-ttu-id="b29ef-146">Interoperabilità DirectWrite</span><span class="sxs-lookup"><span data-stu-id="b29ef-146">DirectWrite Interoperability</span></span>

<span data-ttu-id="b29ef-147">Direct2D è strettamente integrato con DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="b29ef-147">Direct2D is tightly integrated with DirectWrite.</span></span> <span data-ttu-id="b29ef-148">Direct2D rende più semplice il rendering del contenuto DirectWrite fornendo i metodi [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)e [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="b29ef-148">Direct2D makes it easy to render DirectWrite content by providing the [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), and [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) methods.</span></span>

## <a name="windows-imaging-component-wic-interoperability"></a><span data-ttu-id="b29ef-149">Interoperabilità di Windows Imaging Component (WIC)</span><span class="sxs-lookup"><span data-stu-id="b29ef-149">Windows Imaging Component (WIC) Interoperability</span></span>

<span data-ttu-id="b29ef-150">Direct2D fornisce i metodi [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)e [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) per la modifica delle bitmap di WIC.</span><span class="sxs-lookup"><span data-stu-id="b29ef-150">Direct2D provides the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap), and [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) methods for manipulating WIC bitmaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b29ef-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b29ef-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b29ef-152">Panoramica dell'interoperabilità di Direct2D e GDI</span><span class="sxs-lookup"><span data-stu-id="b29ef-152">Direct2D and GDI Interoperability Overview</span></span>](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[<span data-ttu-id="b29ef-153">Panoramica sull'interoperabilità tra Direct2D e Direct3D</span><span class="sxs-lookup"><span data-stu-id="b29ef-153">Direct2D and Direct3D Interoperability Overview</span></span>](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 