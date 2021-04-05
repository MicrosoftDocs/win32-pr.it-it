---
title: Avvio rapido di Direct2D
description: Vengono riepilogati i passaggi necessari per creare con Direct2D e viene fornito codice di esempio.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D, esempio di codice rettangolo di richiamo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa59d7da057a7a9922e270d83937307762b06a40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117803"
---
# <a name="direct2d-quickstart"></a><span data-ttu-id="b7cfc-104">Avvio rapido di Direct2D</span><span class="sxs-lookup"><span data-stu-id="b7cfc-104">Direct2D QuickStart</span></span>

<span data-ttu-id="b7cfc-105">Direct2D è un'API in modalità immediata e di codice nativo per la creazione di immagini 2D.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-105">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="b7cfc-106">In questo argomento viene illustrato come utilizzare Direct2D all'interno di una tipica applicazione Win32 per creare un oggetto **HWND**.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-106">This topic illustrates how to use Direct2D within a typical Win32 application to draw to an **HWND**.</span></span>

> [!Note]  
> <span data-ttu-id="b7cfc-107">Se si vuole creare un'app di Windows Store che usa Direct2D, vedere l'argomento [avvio rapido di Direct2D per Windows 8](direct2d-quickstart-with-device-context.md) .</span><span class="sxs-lookup"><span data-stu-id="b7cfc-107">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="b7cfc-108">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b7cfc-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b7cfc-109">Disegno di un rettangolo semplice</span><span class="sxs-lookup"><span data-stu-id="b7cfc-109">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="b7cfc-110">Passaggio 1: includere l'intestazione Direct2D</span><span class="sxs-lookup"><span data-stu-id="b7cfc-110">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="b7cfc-111">Passaggio 2: creare un ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="b7cfc-111">Step 2: Create an ID2D1Factory</span></span>](#step-2-create-an-id2d1factory)
-   [<span data-ttu-id="b7cfc-112">Passaggio 3: creare un ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="b7cfc-112">Step 3: Create an ID2D1HwndRenderTarget</span></span>](#step-3-create-an-id2d1hwndrendertarget)
-   [<span data-ttu-id="b7cfc-113">Passaggio 4: creare un pennello</span><span class="sxs-lookup"><span data-stu-id="b7cfc-113">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="b7cfc-114">Passaggio 5: creare il rettangolo</span><span class="sxs-lookup"><span data-stu-id="b7cfc-114">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="b7cfc-115">Passaggio 6: rilasciare le risorse</span><span class="sxs-lookup"><span data-stu-id="b7cfc-115">Step 6: Release Resources</span></span>](#step-6-release-resources)
-   [<span data-ttu-id="b7cfc-116">Creare un'applicazione Direct2D semplice</span><span class="sxs-lookup"><span data-stu-id="b7cfc-116">Create a Simple Direct2D Application</span></span>](#create-a-simple-direct2d-application)
-   [<span data-ttu-id="b7cfc-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b7cfc-117">Related topics</span></span>](#related-topics)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="b7cfc-118">Disegno di un rettangolo semplice</span><span class="sxs-lookup"><span data-stu-id="b7cfc-118">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="b7cfc-119">Per disegnare un rettangolo utilizzando [GDI](/windows/desktop/gdi/windows-gdi), è possibile gestire il messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-119">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



<span data-ttu-id="b7cfc-120">Il codice per disegnare lo stesso rettangolo con Direct2D è simile: crea risorse di disegno, descrive una forma da disegnare, disegna la forma, quindi rilascia le risorse di disegno.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-120">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="b7cfc-121">Le sezioni seguenti descrivono ognuno di questi passaggi in dettaglio.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-121">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="b7cfc-122">Passaggio 1: includere l'intestazione Direct2D</span><span class="sxs-lookup"><span data-stu-id="b7cfc-122">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="b7cfc-123">Oltre alle intestazioni necessarie per un'applicazione Win32, includere l'intestazione d2d1. h.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-123">In addition to the headers required for a Win32 application, include the d2d1.h header.</span></span>

## <a name="step-2-create-an-id2d1factory"></a><span data-ttu-id="b7cfc-124">Passaggio 2: creare un ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="b7cfc-124">Step 2: Create an ID2D1Factory</span></span>

<span data-ttu-id="b7cfc-125">Uno dei primi elementi di un esempio Direct2D è creare un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="b7cfc-125">One of the first things that any Direct2D example does is create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



<span data-ttu-id="b7cfc-126">L'interfaccia [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) è il punto di partenza per l'utilizzo di Direct2D; usare un **ID2D1Factory** per creare risorse Direct2D.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-126">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface is the starting point for using Direct2D; use an **ID2D1Factory** to create Direct2D resources.</span></span>

<span data-ttu-id="b7cfc-127">Quando si crea una factory, è possibile specificare se è a thread multipli o a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-127">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="b7cfc-128">Per ulteriori informazioni sulle Factory multithread, vedere la sezione Osservazioni nella pagina di riferimento di [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory). In questo esempio viene creata una factory a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-128">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="b7cfc-129">In generale, l'applicazione deve creare la Factory una volta e conservarla per la durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-129">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1hwndrendertarget"></a><span data-ttu-id="b7cfc-130">Passaggio 3: creare un ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="b7cfc-130">Step 3: Create an ID2D1HwndRenderTarget</span></span>

<span data-ttu-id="b7cfc-131">Dopo aver creato una factory, usarla per creare una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-131">After you create a factory, use it to create a render target.</span></span>


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



<span data-ttu-id="b7cfc-132">Una destinazione di rendering è un dispositivo che può eseguire operazioni di disegno e creare risorse di disegno dipendenti dal dispositivo, ad esempio i pennelli.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-132">A render target is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="b7cfc-133">Diversi tipi di destinazioni di rendering eseguono il rendering in dispositivi diversi.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-133">Different types of render targets render to different devices.</span></span> <span data-ttu-id="b7cfc-134">Nell'esempio precedente viene usato un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), che esegue il rendering in una parte dello schermo.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-134">The preceding example uses an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), which renders to a portion of the screen.</span></span>

<span data-ttu-id="b7cfc-135">Quando possibile, una destinazione di rendering usa la GPU per accelerare le operazioni di rendering e creare risorse di disegno.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-135">When possible, a render target uses the GPU to accelerate rendering operations and create drawing resources.</span></span> <span data-ttu-id="b7cfc-136">In caso contrario, la destinazione di rendering utilizza la CPU per elaborare le istruzioni di rendering e creare risorse.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-136">Otherwise, the render target uses the CPU to process rendering instructions and create resources.</span></span> <span data-ttu-id="b7cfc-137">È possibile modificare questo comportamento usando i flag del [**\_ tipo di \_ destinazione \_ di rendering d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) quando si crea la destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-137">(You can modify this behavior by using the [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) flags when you create the render target.)</span></span>

<span data-ttu-id="b7cfc-138">Il metodo [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) accetta tre parametri.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-138">The [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method takes three parameters.</span></span> <span data-ttu-id="b7cfc-139">Il primo parametro, uno struct delle [**\_ proprietà della \_ destinazione \_ di rendering d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , specifica le opzioni di visualizzazione remote, se forzare il rendering della destinazione di rendering sul software o sull'hardware e sul valore dpi.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-139">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) struct, specifies remote display options, whether to force the render target to render to software or hardware, and the DPI.</span></span> <span data-ttu-id="b7cfc-140">Il codice in questo esempio usa la funzione helper [**D2D1:: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) per accettare le proprietà di destinazione di rendering predefinite.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-140">The code in this example uses the [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) helper function to accept default render target properties.</span></span>

<span data-ttu-id="b7cfc-141">Il secondo parametro, uno struct delle [**proprietà della \_ \_ \_ destinazione \_ di rendering HWND d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) , specifica l' **HWND** a cui viene eseguito il rendering del contenuto, le dimensioni iniziali della destinazione di rendering (in pixel) e le relative [**Opzioni di presentazione**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options).</span><span class="sxs-lookup"><span data-stu-id="b7cfc-141">The second parameter, a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) struct, specifies the **HWND** to which content is rendered, the initial size of the render target (in pixels), and its [**presentation options**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options).</span></span> <span data-ttu-id="b7cfc-142">In questo esempio viene usata la funzione helper [**D2D1:: HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) per specificare HWND e dimensioni iniziali.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-142">This example uses the [**D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) helper function to specify an HWND and initial size.</span></span> <span data-ttu-id="b7cfc-143">Usa le opzioni di presentazione predefinite.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-143">It uses default presentation options.</span></span>

<span data-ttu-id="b7cfc-144">Il terzo parametro è l'indirizzo del puntatore che riceve il riferimento alla destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-144">The third parameter is the address of the pointer that receives the render target reference.</span></span>

<span data-ttu-id="b7cfc-145">Quando si crea una destinazione di rendering e l'accelerazione hardware è disponibile, è necessario allocare risorse sulla GPU del computer.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-145">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="b7cfc-146">Creando una destinazione di rendering una volta e mantenendola il più a lungo possibile, si ottengono vantaggi in termini di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-146">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="b7cfc-147">L'applicazione deve creare le destinazioni di rendering una sola volta e mantenerle per la durata dell'applicazione o fino a quando non viene ricevuto l'errore di [**\_ \_ destinazione D2DERR ricreate**](direct2d-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b7cfc-147">Your application should create render targets once and hold on to them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="b7cfc-148">Quando si riceve questo errore, è necessario ricreare la destinazione di rendering (e tutte le risorse create).</span><span class="sxs-lookup"><span data-stu-id="b7cfc-148">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="step-4-create-a-brush"></a><span data-ttu-id="b7cfc-149">Passaggio 4: creare un pennello</span><span class="sxs-lookup"><span data-stu-id="b7cfc-149">Step 4: Create a Brush</span></span>

<span data-ttu-id="b7cfc-150">Analogamente a una factory, una destinazione di rendering può creare risorse di disegno.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-150">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="b7cfc-151">In questo esempio, la destinazione di rendering crea un pennello.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-151">In this example, the render target creates a brush.</span></span>


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



<span data-ttu-id="b7cfc-152">Un pennello è un oggetto che disegna un'area, ad esempio il tratto di una forma o il riempimento di una geometria.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-152">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="b7cfc-153">Il pennello in questo esempio disegna un'area con un colore a tinta unita predefinito (nero).</span><span class="sxs-lookup"><span data-stu-id="b7cfc-153">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="b7cfc-154">Direct2D fornisce anche altri tipi di pennelli: pennelli sfumatura per il disegno di sfumature lineari e radiali e un pennello bitmap per la verniciatura con bitmap e pattern.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-154">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, and a bitmap brush for painting with bitmaps and patterns.</span></span>

<span data-ttu-id="b7cfc-155">Alcune API di disegno forniscono penne per il disegno di strutture e pennelli per la compilazione di forme.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-155">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="b7cfc-156">Direct2D è diverso: non fornisce un oggetto Pen ma usa un pennello per il disegno di strutture e riempimento di forme.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-156">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="b7cfc-157">Quando si disegnano le strutture, usare l'interfaccia [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) con un pennello per controllare le operazioni di traccia del percorso.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-157">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface with a brush to control path stroking operations.</span></span>

<span data-ttu-id="b7cfc-158">Un pennello può essere usato solo con la destinazione di rendering che lo ha creato e con altre destinazioni di rendering nello stesso dominio delle risorse.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-158">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="b7cfc-159">In generale, è consigliabile creare pennelli una volta e conservarli per la durata della destinazione di rendering che li ha creati.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-159">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="b7cfc-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) è l'eccezione Lone; Poiché è relativamente economico creare, è possibile creare un **ID2D1SolidColorBrush** ogni volta che si crea un frame, senza alcun impatto significativo sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="b7cfc-161">È anche possibile usare un solo **ID2D1SolidColorBrush** e modificarne il colore ogni volta che viene usato.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-161">You can also use a single **ID2D1SolidColorBrush** and just change its color every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="b7cfc-162">Passaggio 5: creare il rettangolo</span><span class="sxs-lookup"><span data-stu-id="b7cfc-162">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="b7cfc-163">Usare quindi la destinazione di rendering per disegnare il rettangolo.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-163">Next, use the render target to draw the rectangle.</span></span>


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



<span data-ttu-id="b7cfc-164">Il metodo [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) accetta due parametri: il rettangolo da disegnare e il pennello da usare per disegnare il contorno del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-164">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="b7cfc-165">Facoltativamente, è anche possibile specificare le opzioni Larghezza tratto, motivo trattino, join a linee e estremità.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-165">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="b7cfc-166">È necessario chiamare il metodo [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) prima di eseguire qualsiasi comando di disegno ed è necessario chiamare il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) dopo aver eseguito i comandi di disegno.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-166">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="b7cfc-167">Il metodo **EndDraw** restituisce un valore **HRESULT** che indica se i comandi di disegno hanno avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-167">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span>

## <a name="step-6-release-resources"></a><span data-ttu-id="b7cfc-168">Passaggio 6: rilasciare le risorse</span><span class="sxs-lookup"><span data-stu-id="b7cfc-168">Step 6: Release Resources</span></span>

<span data-ttu-id="b7cfc-169">Quando non sono più presenti frame da disegnare o quando si riceve l'errore [**D2DERR \_ ricrea \_ destinazione**](direct2d-error-codes.md) , rilasciare la destinazione di rendering e tutti i dispositivi creati.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-169">When there are no more frames to draw, or when you receive the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error, release the render target and any devices it created.</span></span>


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



<span data-ttu-id="b7cfc-170">Quando l'applicazione ha terminato di usare le risorse Direct2D, ad esempio quando sta per uscire, rilascia la factory Direct2D.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-170">When your application has finished using Direct2D resources (such as when it is about to exit), release the Direct2D factory.</span></span>


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a><span data-ttu-id="b7cfc-171">Creare un'applicazione Direct2D semplice</span><span class="sxs-lookup"><span data-stu-id="b7cfc-171">Create a Simple Direct2D Application</span></span>

<span data-ttu-id="b7cfc-172">Il codice in questo argomento illustra gli elementi di base di un'applicazione Direct2D.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-172">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="b7cfc-173">Per brevità, l'argomento omette il Framework dell'applicazione e il codice di gestione degli errori caratteristico di un'applicazione ben scritta.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-173">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span> <span data-ttu-id="b7cfc-174">Per una procedura dettagliata più dettagliata che mostra il codice completo per la creazione di un'applicazione Direct2D semplice e illustra le procedure consigliate per la progettazione, vedere [creazione di una semplice applicazione Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="b7cfc-174">For a more detailed walk-through that shows the complete code for creating a simple Direct2D application and demonstrates best design practices, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7cfc-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b7cfc-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7cfc-176">Creazione di un'applicazione Direct2D semplice</span><span class="sxs-lookup"><span data-stu-id="b7cfc-176">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> </dl>

 

 