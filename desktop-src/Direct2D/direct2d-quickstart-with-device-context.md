---
title: Guida introduttiva di Direct2D per Windows 8
description: Riepiloga i passaggi necessari per disegnare con Direct2D per Windows 8 e fornisce codice di esempio. Direct2D è un'API di codice nativo per la creazione di grafica 2D.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D, esempio di codice per disegnare un rettangolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43442e57ed0949bdf39fc05ce1a69fded42b4b3d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406144"
---
# <a name="direct2d-quickstart-for-windows-8"></a><span data-ttu-id="9addf-105">Guida introduttiva di Direct2D per Windows 8</span><span class="sxs-lookup"><span data-stu-id="9addf-105">Direct2D Quickstart for Windows 8</span></span>

<span data-ttu-id="9addf-106">Direct2D è un'API in modalità immediata a codice nativo per la creazione di grafica 2D.</span><span class="sxs-lookup"><span data-stu-id="9addf-106">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="9addf-107">Questo argomento illustra come usare Direct2D per disegnare in un oggetto [**Windows::UI::Core::CoreWindow.**](/uwp/api/Windows.UI.Core.CoreWindow)</span><span class="sxs-lookup"><span data-stu-id="9addf-107">This topic illustrates how to use Direct2D to draw to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

<span data-ttu-id="9addf-108">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9addf-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="9addf-109">Disegno di un rettangolo semplice</span><span class="sxs-lookup"><span data-stu-id="9addf-109">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="9addf-110">Passaggio 1: Includere l'intestazione Direct2D</span><span class="sxs-lookup"><span data-stu-id="9addf-110">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="9addf-111">Passaggio 2: Creare un oggetto ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="9addf-111">Step 2: Create an ID2D1Factory1</span></span>](#step-2-create-an-id2d1factory1)
-   [<span data-ttu-id="9addf-112">Passaggio 3: Creare id2D1Device e ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="9addf-112">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [<span data-ttu-id="9addf-113">Passaggio 4: Creare un pennello</span><span class="sxs-lookup"><span data-stu-id="9addf-113">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="9addf-114">Passaggio 5: Disegnare il rettangolo</span><span class="sxs-lookup"><span data-stu-id="9addf-114">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="9addf-115">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="9addf-115">Example code</span></span>](#example-code)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="9addf-116">Disegno di un rettangolo semplice</span><span class="sxs-lookup"><span data-stu-id="9addf-116">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="9addf-117">Per disegnare un rettangolo usando [GDI,](/windows/desktop/gdi/windows-gdi)è possibile gestire il [**messaggio WM \_ PAINT,**](/windows/desktop/gdi/wm-paint) come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="9addf-117">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


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



<span data-ttu-id="9addf-118">Il codice per disegnare lo stesso rettangolo con Direct2D è simile: crea risorse di disegno, descrive una forma da disegnare, disegna la forma, quindi rilascia le risorse di disegno.</span><span class="sxs-lookup"><span data-stu-id="9addf-118">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="9addf-119">Le sezioni seguenti descrivono in dettaglio ognuno di questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="9addf-119">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="9addf-120">Passaggio 1: Includere l'intestazione Direct2D</span><span class="sxs-lookup"><span data-stu-id="9addf-120">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="9addf-121">Oltre alle intestazioni necessarie per l'applicazione, includere le intestazioni d2d1.h e d2d1 \_ 1.h.</span><span class="sxs-lookup"><span data-stu-id="9addf-121">In addition to the headers required for the application, include the d2d1.h and d2d1\_1.h headers.</span></span>

## <a name="step-2-create-an-id2d1factory1"></a><span data-ttu-id="9addf-122">Passaggio 2: Creare un oggetto ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="9addf-122">Step 2: Create an ID2D1Factory1</span></span>

<span data-ttu-id="9addf-123">Una delle prime operazioni che qualsiasi esempio direct2D esegue è la creazione di [**id2D1Factory1.**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1)</span><span class="sxs-lookup"><span data-stu-id="9addf-123">One of the first things that any Direct2D example does is create an [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span></span>


```C++
DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );
```



<span data-ttu-id="9addf-124">[**L'interfaccia ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) è il punto di partenza per l'uso di Direct2D; usare **id2D1Factory1** per creare risorse Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9addf-124">The [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface is the starting point for using Direct2D; use an **ID2D1Factory1** to create Direct2D resources.</span></span>

<span data-ttu-id="9addf-125">Quando si crea una factory, è possibile specificare se è multi-thread o a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="9addf-125">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="9addf-126">Per altre informazioni sulle factory multi-thread, vedere le osservazioni nella pagina di riferimento [**di ID2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) Questo esempio crea una factory a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="9addf-126">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="9addf-127">In generale, l'applicazione deve creare la factory una sola volta e conservarla per tutta la durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9addf-127">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a><span data-ttu-id="9addf-128">Passaggio 3: Creare id2D1Device e ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="9addf-128">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>

<span data-ttu-id="9addf-129">Dopo aver creato una factory, usarla per creare un dispositivo Direct2D e quindi usare il dispositivo per creare un contesto di dispositivo Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9addf-129">After you create a factory, use it to create a Direct2D device and then use the device to create a Direct2D device context.</span></span> <span data-ttu-id="9addf-130">Per creare questi oggetti Direct2D, è necessario disporre di un dispositivo [**Direct3D 11,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) di un [**dispositivo DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)e di una [**catena di scambio DXGI.**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)</span><span class="sxs-lookup"><span data-stu-id="9addf-130">In order to create these Direct2D objects, you must have a [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , a [**DXGI device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice), and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="9addf-131">Per informazioni sulla creazione dei prerequisiti [necessari,](devices-and-device-contexts.md) vedere Dispositivi e contesti di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9addf-131">See [Devices and Device Contexts](devices-and-device-contexts.md) for info on creating the necessary prerequisites.</span></span>


```C++

    // Obtain the underlying DXGI device of the Direct3D11.1 device.
    DX::ThrowIfFailed(
        m_d3dDevice.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // And get its corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



<span data-ttu-id="9addf-132">Un contesto di dispositivo è un dispositivo che può eseguire operazioni di disegno e creare risorse di disegno dipendenti dal dispositivo, ad esempio i pennelli.</span><span class="sxs-lookup"><span data-stu-id="9addf-132">A device context is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="9addf-133">Si usa anche il contesto di dispositivo per collegare un [**oggetto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a una superficie DXGI da usare come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="9addf-133">You also use the device context to link a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) to a DXGI surface to use as a render target.</span></span> <span data-ttu-id="9addf-134">Il rendering del contesto di dispositivo può essere eseguito in tipi diversi di destinazioni.</span><span class="sxs-lookup"><span data-stu-id="9addf-134">The device context can render to different types of targets.</span></span>

<span data-ttu-id="9addf-135">Il codice qui dichiara le proprietà per bitmap che si collegano a una catena di scambio DXGI di cui viene eseguito il rendering in [**un oggetto CoreWindow.**](/uwp/api/Windows.UI.Core.CoreWindow)</span><span class="sxs-lookup"><span data-stu-id="9addf-135">The code here declares the properties for bitmap that links to a DXGI swap chain that renders to a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span> <span data-ttu-id="9addf-136">Il [**metodo ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) ottiene una superficie Direct2D dalla superficie DXGI.</span><span class="sxs-lookup"><span data-stu-id="9addf-136">The [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method gets a Direct2D surface from the DXGI surface.</span></span> <span data-ttu-id="9addf-137">In questo modo viene eseguito il rendering di qualsiasi elemento di cui viene eseguito il rendering nell'oggetto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) di destinazione sulla superficie della catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="9addf-137">This makes it so anything rendered to the target [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is rendered to the surface of the swap chain.</span></span>

<span data-ttu-id="9addf-138">Dopo aver creato la superficie Direct2D, usa il metodo [**ID2D1DeviceContext::SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) per impostarla come destinazione di rendering attiva.</span><span class="sxs-lookup"><span data-stu-id="9addf-138">Once you have the Direct2D surface, use the [**ID2D1DeviceContext::SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) method to set it as the active render target.</span></span>


```C++
    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it will be directly rendered to the 
    // swapchain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // So now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



## <a name="step-4-create-a-brush"></a><span data-ttu-id="9addf-139">Passaggio 4: Creare un pennello</span><span class="sxs-lookup"><span data-stu-id="9addf-139">Step 4: Create a Brush</span></span>

<span data-ttu-id="9addf-140">Analogamente a una factory, un contesto di dispositivo può creare risorse di disegno.</span><span class="sxs-lookup"><span data-stu-id="9addf-140">Like a factory, a device context can create drawing resources.</span></span> <span data-ttu-id="9addf-141">In questo esempio il contesto di dispositivo crea un pennello.</span><span class="sxs-lookup"><span data-stu-id="9addf-141">In this example, the device context creates a brush.</span></span>


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



<span data-ttu-id="9addf-142">Un pennello è un oggetto che disegna un'area, ad esempio il tratto di una forma o il riempimento di una geometria.</span><span class="sxs-lookup"><span data-stu-id="9addf-142">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="9addf-143">Il pennello in questo esempio disegna un'area con un colore a tinta unita predefinito, il nero.</span><span class="sxs-lookup"><span data-stu-id="9addf-143">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="9addf-144">Direct2D offre anche altri tipi di pennelli: pennelli sfumatura per disegnare sfumature lineari e radiali, un [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) pennello [**bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) per il disegno con bitmap e pattern e a partire da Windows 8, un pennello immagine per disegnare con un'immagine sottoposta a rendering.</span><span class="sxs-lookup"><span data-stu-id="9addf-144">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, a [**bitmap brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) for painting with bitmaps and patterns, and starting in Windows 8, an [**image brush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) for painting with a rendered image.</span></span>

<span data-ttu-id="9addf-145">Alcune API di disegno forniscono penne per disegnare contorni e pennelli per il riempimento delle forme.</span><span class="sxs-lookup"><span data-stu-id="9addf-145">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="9addf-146">Direct2D è diverso: non fornisce un oggetto penna, ma usa un pennello per disegnare i contorni e riempire le forme.</span><span class="sxs-lookup"><span data-stu-id="9addf-146">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="9addf-147">Quando si disegnano i contorni, usare l'interfaccia [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) o Windows 8 partire [**dall'interfaccia ID2D1StrokeStyle1,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) con un pennello per controllare le operazioni di selezione del percorso.</span><span class="sxs-lookup"><span data-stu-id="9addf-147">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface, or starting in Windows 8 the [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) interface, with a brush to control path stroking operations.</span></span>

<span data-ttu-id="9addf-148">Un pennello può essere usato solo con la destinazione di rendering che lo ha creato e con altre destinazioni di rendering nello stesso dominio di risorse.</span><span class="sxs-lookup"><span data-stu-id="9addf-148">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="9addf-149">In generale, è consigliabile creare i pennelli una sola volta e conservarli per tutta la durata della destinazione di rendering che li ha creati.</span><span class="sxs-lookup"><span data-stu-id="9addf-149">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="9addf-150">[**ID2D1SolidColorBrush è**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) l'unica eccezione. Poiché è relativamente conveniente da creare, è possibile creare un **oggetto ID2D1SolidColorBrush** ogni volta che si disegna un frame, senza alcun impatto notevole sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="9addf-150">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="9addf-151">È anche possibile usare un singolo **oggetto ID2D1SolidColorBrush** e modificarne il colore o l'opacità ogni volta che lo si usa.</span><span class="sxs-lookup"><span data-stu-id="9addf-151">You can also use a single **ID2D1SolidColorBrush** and just change its color or opacity every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="9addf-152">Passaggio 5: Disegnare il rettangolo</span><span class="sxs-lookup"><span data-stu-id="9addf-152">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="9addf-153">Usare quindi il contesto di dispositivo per disegnare il rettangolo.</span><span class="sxs-lookup"><span data-stu-id="9addf-153">Next, use the device context to draw the rectangle.</span></span>


```C++
 
m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



<span data-ttu-id="9addf-154">Il [**metodo DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) accetta due parametri: il rettangolo da disegnare e il pennello da usare per disegnare il contorno del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="9addf-154">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="9addf-155">Facoltativamente, è anche possibile specificare le opzioni relative a spessore tratto, motivo trattino, join di linee e estremità finale.</span><span class="sxs-lookup"><span data-stu-id="9addf-155">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="9addf-156">È necessario chiamare il [**metodo BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) prima di eseguire qualsiasi comando di disegno ed è necessario chiamare il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) dopo aver completato l'emissione dei comandi di disegno.</span><span class="sxs-lookup"><span data-stu-id="9addf-156">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="9addf-157">Il **metodo EndDraw** restituisce un **HRESULT** che indica se i comandi di disegno sono riusciti.</span><span class="sxs-lookup"><span data-stu-id="9addf-157">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span> <span data-ttu-id="9addf-158">Se l'operazione non riesce, la funzione helper ThrowIfFailed genererà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="9addf-158">If it is not successful, the ThrowIfFailed helper function will throw an exception.</span></span>

<span data-ttu-id="9addf-159">Il [**metodo IDXGISwapChain::P resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) scambia la superficie del buffer con l'oggetto sulla superficie dello schermo per visualizzare il risultato.</span><span class="sxs-lookup"><span data-stu-id="9addf-159">The [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method swaps the buffer surface with the on screen surface to display the result.</span></span>

## <a name="example-code"></a><span data-ttu-id="9addf-160">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="9addf-160">Example code</span></span>

<span data-ttu-id="9addf-161">Il codice in questo argomento illustra gli elementi di base di un'applicazione Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9addf-161">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="9addf-162">Per brevità, l'argomento omette il framework applicazione e il codice di gestione degli errori caratteristica di un'applicazione ben scritta.</span><span class="sxs-lookup"><span data-stu-id="9addf-162">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span>

 

 