---
title: Panoramica dell'interoperabilità di Direct2D e GDI
description: Viene descritto come usare Direct2D e GDI insieme.
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Direct2D, interoperatività GDI
- Direct2D, interoperabilità
- interoperabilità, Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilità, Graphics Device Interface (GDI)
- Direct3D, interoperabilità
- Direct3D, interoperatività Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991d94b4460e9130b3353be38d5f749511434eb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729663"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a><span data-ttu-id="04fe5-111">Panoramica dell'interoperabilità di Direct2D e GDI</span><span class="sxs-lookup"><span data-stu-id="04fe5-111">Direct2D and GDI Interoperability Overview</span></span>

<span data-ttu-id="04fe5-112">In questo argomento viene descritto come utilizzare contemporaneamente Direct2D e [GDI](/windows/desktop/gdi/windows-gdi) .</span><span class="sxs-lookup"><span data-stu-id="04fe5-112">This topic describes how to use Direct2D and [GDI](/windows/desktop/gdi/windows-gdi) together.</span></span> <span data-ttu-id="04fe5-113">Esistono due modi per combinare Direct2D con GDI: è possibile scrivere contenuto GDI in una destinazione di rendering compatibile con GDI Direct2D oppure scrivere contenuto Direct2D in un [contesto di dispositivo GDI (DC)](/windows/desktop/gdi/device-contexts).</span><span class="sxs-lookup"><span data-stu-id="04fe5-113">There are two ways to combine Direct2D with GDI: you can write GDI content to a Direct2D GDI-compatible render target, or you can write Direct2D content to a [GDI Device Context (DC)](/windows/desktop/gdi/device-contexts).</span></span>

<span data-ttu-id="04fe5-114">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="04fe5-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="04fe5-115">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="04fe5-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="04fe5-116">Creare contenuto Direct2D in un contesto di dispositivo GDI</span><span class="sxs-lookup"><span data-stu-id="04fe5-116">Draw Direct2D Content to a GDI Device Context</span></span>](#draw-direct2d-content-to-a-gdi-device-context)
-   [<span data-ttu-id="04fe5-117">ID2D1DCRenderTargets, le trasformazioni GDI e le compilazioni del linguaggio da destra a sinistra di Windows</span><span class="sxs-lookup"><span data-stu-id="04fe5-117">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [<span data-ttu-id="04fe5-118">Disegnare contenuto GDI in una destinazione di rendering GDI-Compatible Direct2D</span><span class="sxs-lookup"><span data-stu-id="04fe5-118">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [<span data-ttu-id="04fe5-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04fe5-119">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="04fe5-120">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="04fe5-120">Prerequisites</span></span>

<span data-ttu-id="04fe5-121">In questa panoramica si presuppone che l'utente abbia familiarità con le operazioni di disegno Direct2D di base.</span><span class="sxs-lookup"><span data-stu-id="04fe5-121">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="04fe5-122">Per un'esercitazione, vedere la [Guida introduttiva di Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="04fe5-122">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="04fe5-123">Si presuppone inoltre che l'utente abbia familiarità con le operazioni di disegno GDI.</span><span class="sxs-lookup"><span data-stu-id="04fe5-123">It also assumes that you are familiar with GDI drawing operations.</span></span>

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a><span data-ttu-id="04fe5-124">Creare contenuto Direct2D in un contesto di dispositivo GDI</span><span class="sxs-lookup"><span data-stu-id="04fe5-124">Draw Direct2D Content to a GDI Device Context</span></span>

<span data-ttu-id="04fe5-125">Per creare contenuto Direct2D in un controller di dominio GDI, usare un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span><span class="sxs-lookup"><span data-stu-id="04fe5-125">To draw Direct2D content to a GDI DC, you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span> <span data-ttu-id="04fe5-126">Per creare una destinazione di rendering del controller di dominio, usare il metodo [**ID2D1Factory:: CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="04fe5-126">To create a DC render target, you use the [**ID2D1Factory::CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) method.</span></span> <span data-ttu-id="04fe5-127">Questo metodo accetta due parametri.</span><span class="sxs-lookup"><span data-stu-id="04fe5-127">This method takes two parameters.</span></span>

<span data-ttu-id="04fe5-128">Il primo parametro, una struttura delle [**\_ proprietà della \_ destinazione \_ di rendering d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , specifica il rendering, la comunicazione remota, il formato dpi, il formato pixel e le informazioni sull'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="04fe5-128">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) structure, specifies rendering, remoting, DPI, pixel format, and usage information.</span></span> <span data-ttu-id="04fe5-129">Per abilitare la destinazione di rendering del controller di dominio per l'utilizzo con GDI, impostare il formato DXGI su [DXGI \_ Format \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) e la modalità Alpha su [**d2d1 \_ Alpha Mode \_ \_ premoltiplicated**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) o **d2d1 \_ Alpha \_ mode \_ Ignore**.</span><span class="sxs-lookup"><span data-stu-id="04fe5-129">To enable the DC render target to work with GDI, set the DXGI format to [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) and the alpha mode to [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="04fe5-130">Il secondo parametro è l'indirizzo del puntatore che riceve il riferimento alla destinazione di rendering del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="04fe5-130">The second parameter is the address of the pointer that receive the DC render target reference.</span></span>

<span data-ttu-id="04fe5-131">Il codice seguente crea una destinazione di rendering del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="04fe5-131">The following code creates a DC render target.</span></span>


```C++
// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory->CreateDCRenderTarget(&props, &m_pDCRT);
```



<span data-ttu-id="04fe5-132">Nel codice precedente, *m \_ pD2DFactory* è un puntatore a un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)e *m \_ pDCRT* è un puntatore a un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span><span class="sxs-lookup"><span data-stu-id="04fe5-132">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pDCRT* is a pointer to an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span>

<span data-ttu-id="04fe5-133">Prima di poter eseguire il rendering con la destinazione di rendering del controller di dominio, è necessario utilizzare il relativo metodo [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) per associarlo a un controller di dominio GDI.</span><span class="sxs-lookup"><span data-stu-id="04fe5-133">Before you can render with the DC render target, you must use its [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method to associate it with a GDI DC.</span></span> <span data-ttu-id="04fe5-134">Questa operazione viene eseguita ogni volta che si utilizza un controller di dominio diverso o la dimensione dell'area che si desidera creare per le modifiche.</span><span class="sxs-lookup"><span data-stu-id="04fe5-134">You do this each time you use a different DC, or the size of the area you want to draw to changes.</span></span>

<span data-ttu-id="04fe5-135">Il metodo [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) accetta due parametri, *HDC* e *pSubRect*.</span><span class="sxs-lookup"><span data-stu-id="04fe5-135">The [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method takes two parameters, *hDC* and *pSubRect*.</span></span> <span data-ttu-id="04fe5-136">Il parametro *HDC* fornisce un handle per il contesto di dispositivo che riceve l'output della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="04fe5-136">The *hDC* parameter provides a handle to the device context that receives the output of the render target.</span></span> <span data-ttu-id="04fe5-137">Il parametro *pSubRect* è un rettangolo che descrive la parte del contesto di dispositivo in cui viene eseguito il rendering del contenuto.</span><span class="sxs-lookup"><span data-stu-id="04fe5-137">The *pSubRect* parameter is a rectangle that describes the portion of the device context to which content is rendered.</span></span> <span data-ttu-id="04fe5-138">La destinazione del rendering del controller di dominio aggiorna le dimensioni in modo che corrispondano all'area del contesto del dispositivo descritta da *pSubRect*, qualora cambi la dimensione.</span><span class="sxs-lookup"><span data-stu-id="04fe5-138">The DC render target updates its size to match the device context area described by *pSubRect*, should it change size.</span></span>

<span data-ttu-id="04fe5-139">Il codice seguente associa un controller di dominio a una destinazione di rendering del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="04fe5-139">The following code binds a DC to a DC render target.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{


// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04fe5-140">C++</span><span class="sxs-lookup"><span data-stu-id="04fe5-140">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="04fe5-141">Dopo aver associato la destinazione di rendering del controller di dominio a un controller di dominio, è possibile usarla per disegnare.</span><span class="sxs-lookup"><span data-stu-id="04fe5-141">After you associate the DC render target with a DC, you can use it to draw.</span></span> <span data-ttu-id="04fe5-142">Il codice seguente disegna il contenuto Direct2D e GDI utilizzando un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="04fe5-142">The following code draws Direct2D and GDI content using a DC.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

    HRESULT hr;
    RECT rc;

    // Get the dimensions of the client drawing area.
    GetClientRect(m_hwnd, &rc);

    //
    // Draw the pie chart with Direct2D.
    //

    // Create the DC render target.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Bind the DC to the DC render target.
        hr = m_pDCRT->BindDC(ps.hdc, &rc);

        m_pDCRT->BeginDraw();

        m_pDCRT->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pDCRT->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pDCRT->DrawEllipse(
            D2D1::Ellipse(
                D2D1::Point2F(150.0f, 150.0f),
                100.0f,
                100.0f),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.15425f),
                (150.0f - 100.0f * 0.988f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.525f),
                (150.0f + 100.0f * 0.8509f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f - 100.0f * 0.988f),
                (150.0f - 100.0f * 0.15425f)),
            m_pBlackBrush,
            3.0
            );

        hr = m_pDCRT->EndDraw();
        if (SUCCEEDED(hr))
        {
            //
            // Draw the pie chart with GDI.
            //

            // Save the original object.
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(ps.hdc, blackPen);

            Ellipse(ps.hdc, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);


            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(ps.hdc, pntArray1, 2);
            Polyline(ps.hdc, pntArray2, 2);
            Polyline(ps.hdc, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(ps.hdc, original);
        }
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



<span data-ttu-id="04fe5-143">Questo codice produce output come illustrato nella figura seguente (sono stati aggiunti callout per evidenziare la differenza tra il rendering di Direct2D e GDI).</span><span class="sxs-lookup"><span data-stu-id="04fe5-143">This code produces outputs as shown in the following illustration (callouts have been added to highlight the difference between Direct2D and GDI rendering.)</span></span>

![illustrazione di due grafici circolari sottoposti a rendering con Direct2D e GDI](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a><span data-ttu-id="04fe5-145">ID2D1DCRenderTargets, le trasformazioni GDI e le compilazioni del linguaggio da destra a sinistra di Windows</span><span class="sxs-lookup"><span data-stu-id="04fe5-145">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>

<span data-ttu-id="04fe5-146">Quando si usa un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), viene eseguito il rendering del contenuto Direct2D in una bitmap interna, quindi il rendering della bitmap viene eseguito nel controller di dominio con GDI.</span><span class="sxs-lookup"><span data-stu-id="04fe5-146">When you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), it renders Direct2D content to an internal bitmap, and then renders the bitmap to the DC with GDI.</span></span>

<span data-ttu-id="04fe5-147">GDI può applicare una trasformazione GDI (tramite il metodo [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) ) o un altro effetto allo stesso DC usato dalla destinazione di rendering, nel qual caso GDI trasforma la bitmap prodotta da Direct2D.</span><span class="sxs-lookup"><span data-stu-id="04fe5-147">It's possible for GDI to apply a GDI transform (through the [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) method) or other effect to the same DC used by the render target, in which case GDI transforms the bitmap produced by Direct2D.</span></span> <span data-ttu-id="04fe5-148">L'uso di una trasformazione GDI per trasformare il contenuto Direct2D può compromettere la qualità visiva dell'output, perché si sta trasformando una bitmap per cui è già stato calcolato l'anti-aliasing e il posizionamento dei subpixel.</span><span class="sxs-lookup"><span data-stu-id="04fe5-148">Using a GDI transform to transform the Direct2D content has the potential to degrade the visual quality of the output, because you're transforming a bitmap for which antialiasing and subpixel positioning have already been calculated.</span></span>

<span data-ttu-id="04fe5-149">Si supponga, ad esempio, di usare la destinazione di rendering per disegnare una scena che contiene geometrie e testo con anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="04fe5-149">For example, suppose you use the render target to draw a scene that contains antialiased geometries and text.</span></span> <span data-ttu-id="04fe5-150">Se si usa una trasformazione GDI per applicare una trasformazione di ridimensionamento al controller di dominio e si ridimensiona la scena in modo che sia 10 volte più grande, verranno visualizzati i bordi di pixelzzazione e frastagliati.</span><span class="sxs-lookup"><span data-stu-id="04fe5-150">If you use a GDI transform to apply a scale transform to the DC and scale the scene so that it's 10 times larger, you'll see pixelization and jagged edges.</span></span> <span data-ttu-id="04fe5-151">Se, tuttavia, è stata applicata una trasformazione simile mediante Direct2D, la qualità visiva della scena non sarebbe peggiorata.</span><span class="sxs-lookup"><span data-stu-id="04fe5-151">(If, however, you applied a similar transform using Direct2D, the visual quality of the scene would not be degraded.)</span></span>

<span data-ttu-id="04fe5-152">In alcuni casi, potrebbe non essere evidente che GDI sta eseguendo un'elaborazione aggiuntiva che potrebbe peggiorare la qualità del contenuto Direct2D.</span><span class="sxs-lookup"><span data-stu-id="04fe5-152">In some cases, it might not be obvious that GDI is performing additional processing that might degrade the quality of the Direct2D content.</span></span> <span data-ttu-id="04fe5-153">Ad esempio, in una build di Windows da destra a sinistra (RTL), il contenuto di cui è stato eseguito il rendering da un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) potrebbe essere invertito orizzontalmente quando GDI lo copia nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="04fe5-153">For example, on a right-to-left (RTL) build of Windows, content rendered by an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) might be horizontally inverted when GDI copies it to its destination.</span></span> <span data-ttu-id="04fe5-154">Se il contenuto è effettivamente invertito dipende dalle impostazioni correnti del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="04fe5-154">Whether the content is actually inverted depends on the current settings of the DC.</span></span>

<span data-ttu-id="04fe5-155">A seconda del tipo di contenuto di cui viene eseguito il rendering, potrebbe essere necessario impedire l'inversione.</span><span class="sxs-lookup"><span data-stu-id="04fe5-155">Depending on the type of content being rendered, you might want to prevent the inversion.</span></span> <span data-ttu-id="04fe5-156">Se il contenuto Direct2D include il testo ClearType, questa inversione ridurrà la qualità del testo.</span><span class="sxs-lookup"><span data-stu-id="04fe5-156">If the Direct2D content includes ClearType text, this inversion will degrade the quality of the text.</span></span>

<span data-ttu-id="04fe5-157">È possibile controllare il comportamento di rendering RTL utilizzando la funzione GDI di [**selayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) .</span><span class="sxs-lookup"><span data-stu-id="04fe5-157">You can control RTL rendering behavior by using the [**SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) GDI function.</span></span> <span data-ttu-id="04fe5-158">Per evitare il mirroring, chiamare la funzione GDI di **selayout** e specificare **layout \_ BITMAPORIENTATIONPRESERVED** come unico valore per il secondo parametro (non combinarlo con **layout \_ RTL**), come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="04fe5-158">To prevent the mirroring, call the **SetLayout** GDI function and specify **LAYOUT\_BITMAPORIENTATIONPRESERVED** as the only value for the second parameter (do not combine it with **LAYOUT\_RTL**), as shown in the following example:</span></span>


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a><span data-ttu-id="04fe5-159">Disegnare contenuto GDI in una destinazione di rendering GDI-Compatible Direct2D</span><span class="sxs-lookup"><span data-stu-id="04fe5-159">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>

<span data-ttu-id="04fe5-160">Nella sezione precedente viene descritto come scrivere contenuto Direct2D in un controller di dominio GDI.</span><span class="sxs-lookup"><span data-stu-id="04fe5-160">The previous section describes how to write Direct2D content to a GDI DC.</span></span> <span data-ttu-id="04fe5-161">È anche possibile scrivere contenuto GDI in una destinazione di rendering compatibile con GDI Direct2D.</span><span class="sxs-lookup"><span data-stu-id="04fe5-161">You can also write GDI content to a Direct2D GDI-compatible render target.</span></span> <span data-ttu-id="04fe5-162">Questo approccio è utile per le applicazioni che eseguono principalmente il rendering con Direct2D ma hanno un modello di estendibilità o altri contenuti legacy che richiedono la possibilità di eseguire il rendering con GDI.</span><span class="sxs-lookup"><span data-stu-id="04fe5-162">This approach is useful for applications that primarily render with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span>

<span data-ttu-id="04fe5-163">Per eseguire il rendering del contenuto GDI in una destinazione di rendering compatibile con GDI Direct2D, usare [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), che fornisce l'accesso a un contesto di dispositivo che può accettare chiamate di disegnare GDI.</span><span class="sxs-lookup"><span data-stu-id="04fe5-163">To render GDI content to a Direct2D GDI-compatible render target, use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which provides access to a device context that can accept GDI draw calls.</span></span> <span data-ttu-id="04fe5-164">A differenza di altre interfacce, non viene creato direttamente un oggetto **ID2D1GdiInteropRenderTarget** .</span><span class="sxs-lookup"><span data-stu-id="04fe5-164">Unlike other interfaces, an **ID2D1GdiInteropRenderTarget** object is not created directly.</span></span> <span data-ttu-id="04fe5-165">Usare invece il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) di un'istanza di destinazione di rendering esistente.</span><span class="sxs-lookup"><span data-stu-id="04fe5-165">Instead, use the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of an existing render target instance.</span></span> <span data-ttu-id="04fe5-166">Nel codice seguente viene illustrato come eseguire questa operazione:</span><span class="sxs-lookup"><span data-stu-id="04fe5-166">The following code shows how to do this:</span></span>


```C++
        D2D1_RENDER_TARGET_PROPERTIES rtProps = D2D1::RenderTargetProperties();
        rtProps.usage =  D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE;

        // Create a GDI compatible Hwnd render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            rtProps,
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );


        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->QueryInterface(__uuidof(ID2D1GdiInteropRenderTarget), (void**)&m_pGDIRT); 
        }
```



<span data-ttu-id="04fe5-167">Nel codice precedente, *m \_ pD2DFactory* è un puntatore a un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)e *m \_ pGDIRT* è un puntatore a un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).</span><span class="sxs-lookup"><span data-stu-id="04fe5-167">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pGDIRT* is a pointer to an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).</span></span>

<span data-ttu-id="04fe5-168">Si noti che durante la creazione della destinazione di rendering compatibile con GDI GDI viene specificato il flag di [**\_ utilizzo della destinazione di rendering \_ \_ \_ \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) .</span><span class="sxs-lookup"><span data-stu-id="04fe5-168">Notice that the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag is specified when creating the Hwnd GDI-compatible render target.</span></span> <span data-ttu-id="04fe5-169">Se è necessario un formato pixel, usare [DXGI \_ Format \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="04fe5-169">If a pixel format is required, use [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="04fe5-170">Se è richiesta una modalità Alpha, utilizzare la modalità [**\_ alfa d2d1 \_ \_ premoltiplicata**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) o la **\_ modalità d2d1 Alpha \_ \_ Ignore**.</span><span class="sxs-lookup"><span data-stu-id="04fe5-170">If an alpha mode is required, use [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="04fe5-171">Si noti che il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ha sempre esito positivo.</span><span class="sxs-lookup"><span data-stu-id="04fe5-171">Note that the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method always succeeds.</span></span> <span data-ttu-id="04fe5-172">Per verificare se i metodi dell'interfaccia [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) funzioneranno per una determinata destinazione di rendering, creare [**una \_ \_ \_ proprietà di destinazione di rendering d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) che specifichi la compatibilità GDI e il formato pixel appropriato, quindi chiamare il metodo IsValid della destinazione di rendering per verificare se la destinazione di rendering è compatibile con GDI. [](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties))</span><span class="sxs-lookup"><span data-stu-id="04fe5-172">To test whether the [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) interface's methods will work for a given render target, create a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) that specifies GDI compatibility and the appropriate pixel format, and then call the render target's [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) method to see whether the render target is GDI-compatible.</span></span>

<span data-ttu-id="04fe5-173">Nell'esempio seguente viene illustrato come creare un grafico a torta (contenuto GDI) nella destinazione di rendering compatibile con GDI di HWND.</span><span class="sxs-lookup"><span data-stu-id="04fe5-173">The following example shows how to draw a pie chart (GDI content) to the Hwnd GDI-compatible render target.</span></span>


```C++
        HDC hDC = NULL;
        hr = m_pGDIRT->GetDC(D2D1_DC_INITIALIZE_MODE_COPY, &hDC);

        if (SUCCEEDED(hr))
        {
            // Draw the pie chart to the GDI render target associated with the Hwnd render target.
            HGDIOBJ original = NULL;
            original = SelectObject(
                hDC,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(hDC, blackPen);

            Ellipse(hDC, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);

            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(hDC, pntArray1, 2);
            Polyline(hDC, pntArray2, 2);
            Polyline(hDC, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(hDC, original);

            m_pGDIRT->ReleaseDC(NULL);
        }

```



<span data-ttu-id="04fe5-174">Il codice restituisce i grafici come illustrato nella figura seguente con i callout per evidenziare la differenza di qualità del rendering.</span><span class="sxs-lookup"><span data-stu-id="04fe5-174">The code outputs charts as shown in the following illustration with callouts to highlight the rendering quality difference.</span></span> <span data-ttu-id="04fe5-175">Il grafico a torta a destra (contenuto GDI) ha una qualità di rendering inferiore rispetto al grafico a torta a sinistra (contenuto Direct2D).</span><span class="sxs-lookup"><span data-stu-id="04fe5-175">The right pie chart (GDI content) has lower rendering quality than the left pie chart (Direct2D content).</span></span> <span data-ttu-id="04fe5-176">Questo perché Direct2D è in grado di eseguire il rendering con l'anti-aliasing</span><span class="sxs-lookup"><span data-stu-id="04fe5-176">This is because Direct2D is capable of rendering with antialiasing</span></span>

![illustrazione di due grafici circolari sottoposti a rendering in una destinazione di rendering compatibile con GDI Direct2D](images/gdicontentind2d.png)

## <a name="related-topics"></a><span data-ttu-id="04fe5-178">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04fe5-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04fe5-179">**ID2D1Factory:: CreateDCRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="04fe5-179">**ID2D1Factory::CreateDCRenderTarget**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[<span data-ttu-id="04fe5-180">**ID2D1DCRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="04fe5-180">**ID2D1DCRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[<span data-ttu-id="04fe5-181">**ID2D1GdiInteropRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="04fe5-181">**ID2D1GdiInteropRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[<span data-ttu-id="04fe5-182">**\_Proprietà di \_ destinazione di rendering d2d1 \_**</span><span class="sxs-lookup"><span data-stu-id="04fe5-182">**D2D1\_RENDER\_TARGET\_PROPERTIES**</span></span>](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[<span data-ttu-id="04fe5-183">Contesti di dispositivo GDI</span><span class="sxs-lookup"><span data-stu-id="04fe5-183">GDI Device Contexts</span></span>](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[<span data-ttu-id="04fe5-184">SDK PER GDI</span><span class="sxs-lookup"><span data-stu-id="04fe5-184">GDI SDK</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 