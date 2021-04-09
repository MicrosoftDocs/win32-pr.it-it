---
title: Panoramica sull'interoperabilità tra Direct2D e Direct3D
description: .
ms.assetid: 27680714-dc68-44eb-ab16-2cae3529b352
keywords:
- Direct2D, interoperatività Direct3D
- Direct2D, interoperabilità
- interoperabilità, Direct2D
- interoperabilità, Direct3D
- Direct3D, interoperabilità
- Direct3D, interoperatività Direct2D
- Direct2D, DXGI
- DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6854481ec2a8d869467aa912252e3649e17f2501
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2020
ms.locfileid: "104118622"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a><span data-ttu-id="6772d-111">Panoramica sull'interoperabilità tra Direct2D e Direct3D</span><span class="sxs-lookup"><span data-stu-id="6772d-111">Direct2D and Direct3D Interoperability Overview</span></span>

<span data-ttu-id="6772d-112">I grafici 2D e 3D con accelerazione hardware diventano sempre più una parte delle applicazioni non di gioco e la maggior parte delle applicazioni di gioco usa la grafica 2D sotto forma di menu e Heads-Up Visualizza (HUDs).</span><span class="sxs-lookup"><span data-stu-id="6772d-112">Hardware accelerated 2-D and 3-D graphics are increasingly becoming a part of non-gaming applications, and most gaming applications use 2-D graphics in the form of menus and Heads-Up Displays (HUDs).</span></span> <span data-ttu-id="6772d-113">È possibile aggiungere un numero elevato di valori, consentendo il rendering tradizionale 2D da combinare con il rendering Direct3D in modo efficiente.</span><span class="sxs-lookup"><span data-stu-id="6772d-113">There is lots of value that can be added by enabling traditional 2-D rendering to be mixed with Direct3D rendering in an efficient manner.</span></span>

<span data-ttu-id="6772d-114">Questo argomento descrive come integrare la grafica 2D e 3D tramite Direct2D e [Direct3D](../graphics-and-multimedia.md).</span><span class="sxs-lookup"><span data-stu-id="6772d-114">This topic describes how to integrate 2-D and 3-D graphics by using Direct2D and [Direct3D](../graphics-and-multimedia.md).</span></span>

<span data-ttu-id="6772d-115">Include le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6772d-115">It contains the following sections.</span></span>

-   [<span data-ttu-id="6772d-116">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="6772d-116">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="6772d-117">Versioni Direct3D supportate</span><span class="sxs-lookup"><span data-stu-id="6772d-117">Supported Direct3D Versions</span></span>](#supported-direct3d-versions)
-   [<span data-ttu-id="6772d-118">Interoperabilità tramite DXGI</span><span class="sxs-lookup"><span data-stu-id="6772d-118">Interoperability Through DXGI</span></span>](#interoperability-through-dxgi)
-   [<span data-ttu-id="6772d-119">Scrittura in una superficie Direct3D con una destinazione di rendering della superficie DXGI</span><span class="sxs-lookup"><span data-stu-id="6772d-119">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [<span data-ttu-id="6772d-120">Creazione di una superficie DXGI</span><span class="sxs-lookup"><span data-stu-id="6772d-120">Creating a DXGI Surface</span></span>](#creating-a-dxgi-surface)
-   [<span data-ttu-id="6772d-121">Scrittura di contenuto Direct2D in un buffer della catena di scambio</span><span class="sxs-lookup"><span data-stu-id="6772d-121">Writing Direct2D Content to a Swap Chain Buffer</span></span>](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [<span data-ttu-id="6772d-122">Esempio: creare uno sfondo 2D</span><span class="sxs-lookup"><span data-stu-id="6772d-122">Example: Draw a 2-D Background</span></span>](#example-draw-a-2-d-background)
-   [<span data-ttu-id="6772d-123">Uso del contenuto Direct2D come trama</span><span class="sxs-lookup"><span data-stu-id="6772d-123">Using Direct2D Content as a Texture</span></span>](#using-direct2d-content-as-a-texture)
    -   [<span data-ttu-id="6772d-124">Esempio: usare il contenuto Direct2D come trama</span><span class="sxs-lookup"><span data-stu-id="6772d-124">Example: Use Direct2D Content as a Texture</span></span>](#example-use-direct2d-content-as-a-texture)
-   [<span data-ttu-id="6772d-125">Ridimensionamento di una destinazione di rendering della superficie DXGI</span><span class="sxs-lookup"><span data-stu-id="6772d-125">Resizing a DXGI Surface Render Target</span></span>](#resizing-a-dxgi-surface-render-target)
-   [<span data-ttu-id="6772d-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6772d-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="6772d-127">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="6772d-127">Prerequisites</span></span>

<span data-ttu-id="6772d-128">In questa panoramica si presuppone che l'utente abbia familiarità con le operazioni di disegno Direct2D di base.</span><span class="sxs-lookup"><span data-stu-id="6772d-128">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="6772d-129">Per un'esercitazione, vedere la [Guida introduttiva di Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="6772d-129">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="6772d-130">Si presuppone anche che sia possibile programmare usando [Direct3D 10,1](/windows/desktop/direct3d10/d3d10-graphics).</span><span class="sxs-lookup"><span data-stu-id="6772d-130">It also assumes that you can program by using [Direct3D 10.1](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

## <a name="supported-direct3d-versions"></a><span data-ttu-id="6772d-131">Versioni Direct3D supportate</span><span class="sxs-lookup"><span data-stu-id="6772d-131">Supported Direct3D Versions</span></span>

<span data-ttu-id="6772d-132">Con DirectX 11,0, Direct2D supporta l'interoperabilità solo con i dispositivi Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="6772d-132">With DirectX 11.0, Direct2D supports interoperability with Direct3D 10.1 devices only.</span></span> <span data-ttu-id="6772d-133">Con DirectX 11,1 o versioni successive, Direct2D supporta anche l'interoperabilità con Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="6772d-133">With DirectX 11.1 or later, Direct2D supports interoperability with Direct3D 11 as well.</span></span>

## <a name="interoperability-through-dxgi"></a><span data-ttu-id="6772d-134">Interoperabilità tramite DXGI</span><span class="sxs-lookup"><span data-stu-id="6772d-134">Interoperability Through DXGI</span></span>

<span data-ttu-id="6772d-135">A partire da Direct3D 10, il runtime Direct3D usa [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) per la gestione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6772d-135">As of Direct3D 10, the Direct3D runtime uses [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) for resource management.</span></span> <span data-ttu-id="6772d-136">Il livello di runtime di DXGI fornisce la condivisione tra processi delle superfici di memoria video e funge da base per altre piattaforme di runtime basate sulla memoria video.</span><span class="sxs-lookup"><span data-stu-id="6772d-136">The DXGI runtime layer provides cross-process sharing of video memory surfaces and serves as the foundation for other video memory-based runtime platforms.</span></span> <span data-ttu-id="6772d-137">Direct2D utilizza DXGI per interagire con Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6772d-137">Direct2D uses DXGI to interoperate with Direct3D.</span></span>

<span data-ttu-id="6772d-138">Sono disponibili due metodi principali per utilizzare Direct2D e Direct3D insieme:</span><span class="sxs-lookup"><span data-stu-id="6772d-138">There are two primary ways to use Direct2D and Direct3D together:</span></span>

-   <span data-ttu-id="6772d-139">È possibile scrivere contenuto Direct2D in una superficie Direct3D ottenendo un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) e usandolo con [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per creare un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span><span class="sxs-lookup"><span data-stu-id="6772d-139">You can write Direct2D content to a Direct3D surface by obtaining an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and using it with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="6772d-140">È quindi possibile utilizzare la destinazione di rendering per aggiungere un'interfaccia bidimensionale o uno sfondo a elementi grafici tridimensionali oppure utilizzare un disegno Direct2D come trama per un oggetto tridimensionale.</span><span class="sxs-lookup"><span data-stu-id="6772d-140">You can then use the render target to add a two-dimensional interface or background to three-dimensional graphics, or use a Direct2D drawing as a texture for a three dimensional object.</span></span>
-   <span data-ttu-id="6772d-141">Usando [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) per creare un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) da un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), è possibile scrivere una scena Direct3D in una bitmap ed eseguirne il rendering con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6772d-141">By using [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) from an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), you can write a Direct3D scene to a bitmap and render it with Direct2D.</span></span>

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a><span data-ttu-id="6772d-142">Scrittura in una superficie Direct3D con una destinazione di rendering della superficie DXGI</span><span class="sxs-lookup"><span data-stu-id="6772d-142">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>

<span data-ttu-id="6772d-143">Per scrivere in una superficie Direct3D, ottenere un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) e passarlo al metodo [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per creare una destinazione di rendering della superficie di dxgi.</span><span class="sxs-lookup"><span data-stu-id="6772d-143">To write to a Direct3D surface, you obtain an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and pass it to the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create a DXGI surface render target.</span></span> <span data-ttu-id="6772d-144">È quindi possibile usare la destinazione di rendering della superficie di DXGI per disegnare contenuto 2D sulla superficie DXGI.</span><span class="sxs-lookup"><span data-stu-id="6772d-144">You can then use the DXGI surface render target to draw 2-D content to the DXGI surface.</span></span>

<span data-ttu-id="6772d-145">Una destinazione di rendering della superficie di DXGI è un tipo di [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span><span class="sxs-lookup"><span data-stu-id="6772d-145">A DXGI surface render target is a kind of [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="6772d-146">Analogamente ad altre destinazioni di rendering Direct2D, è possibile usarlo per creare risorse ed emettere comandi di disegno.</span><span class="sxs-lookup"><span data-stu-id="6772d-146">Like other Direct2D render targets, you can use it to create resources and issue drawing commands.</span></span>

<span data-ttu-id="6772d-147">La destinazione di rendering della superficie DXGI e la superficie DXGI devono usare lo stesso formato DXGI.</span><span class="sxs-lookup"><span data-stu-id="6772d-147">The DXGI surface render target and the DXGI surface must use the same DXGI format.</span></span> <span data-ttu-id="6772d-148">Se si specifica il formato [**DXGI \_ Format \_ sconosciuto**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) quando si crea la destinazione di rendering, verrà usato automaticamente il formato della superficie.</span><span class="sxs-lookup"><span data-stu-id="6772d-148">If you specify the [**DXGI\_FORMAT\_UNKOWN**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format when you create the render target, it will automatically use the surface's format.</span></span>

<span data-ttu-id="6772d-149">La destinazione di rendering della superficie di DXGI non esegue la sincronizzazione della superficie di DXGI.</span><span class="sxs-lookup"><span data-stu-id="6772d-149">The DXGI surface render target does not perform DXGI surface synchronization.</span></span>

### <a name="creating-a-dxgi-surface"></a><span data-ttu-id="6772d-150">Creazione di una superficie DXGI</span><span class="sxs-lookup"><span data-stu-id="6772d-150">Creating a DXGI Surface</span></span>

<span data-ttu-id="6772d-151">Con Direct3D 10, è possibile ottenere una superficie DXGI in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="6772d-151">With Direct3D 10, there are several ways to obtain a DXGI surface.</span></span> <span data-ttu-id="6772d-152">È possibile creare un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) per un dispositivo, quindi usare il metodo [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) della catena di scambio per ottenere una superficie DXGI.</span><span class="sxs-lookup"><span data-stu-id="6772d-152">You can create an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) for a device, then use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span> <span data-ttu-id="6772d-153">In alternativa, è possibile usare un dispositivo per creare una trama, quindi usare tale trama come superficie DXGI.</span><span class="sxs-lookup"><span data-stu-id="6772d-153">Or, you can use a device to create a texture, then use that texture as a DXGI surface.</span></span>

<span data-ttu-id="6772d-154">Indipendentemente dalla modalità di creazione della superficie DXGI, è necessario che la superficie utilizzi uno dei formati DXGI supportati dalle destinazioni di rendering della superficie di DXGI.</span><span class="sxs-lookup"><span data-stu-id="6772d-154">Regardless of how you create the DXGI surface, the surface must use one of the DXGI formats supported by DXGI surface render targets.</span></span> <span data-ttu-id="6772d-155">Per un elenco, vedere [formati di pixel supportati e modalità Alpha](supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="6772d-155">For a list, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

<span data-ttu-id="6772d-156">Inoltre, i [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associati alla superficie DXGI devono supportare i formati BGRA DXGI per la superficie per l'utilizzo di Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6772d-156">Additionally, the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the DXGI surface must support BGRA DXGI formats for the surface to work with Direct2D.</span></span> <span data-ttu-id="6772d-157">Per garantire questo supporto, usare il flag di [**\_ supporto D3D10 create \_ Device \_ BGRA \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) quando si chiama il metodo [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) per creare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6772d-157">To ensure this support, use the [**D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag when you call the [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) method to create the device.</span></span>

<span data-ttu-id="6772d-158">Nel codice seguente viene definito un metodo che crea un [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1).</span><span class="sxs-lookup"><span data-stu-id="6772d-158">The following code defines a method that creates an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1).</span></span> <span data-ttu-id="6772d-159">Consente di selezionare il livello di funzionalità migliore disponibile e di eseguire il fallback a [Windows Advanced rasterizzation Platform (Warp)](./installing-the-direct2d-debug-layer.md) quando il rendering hardware non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="6772d-159">It selects the best feature level available and falls back to [Windows Advanced Rasterization Platform (WARP)](./installing-the-direct2d-debug-layer.md) when hardware rendering is not available.</span></span>


```C++
HRESULT DXGISampleApp::CreateD3DDevice(
    IDXGIAdapter *pAdapter,
    D3D10_DRIVER_TYPE driverType,
    UINT flags,
    ID3D10Device1 **ppDevice
    )
{
    HRESULT hr = S_OK;

    static const D3D10_FEATURE_LEVEL1 levelAttempts[] =
    {
        D3D10_FEATURE_LEVEL_10_0,
        D3D10_FEATURE_LEVEL_9_3,
        D3D10_FEATURE_LEVEL_9_2,
        D3D10_FEATURE_LEVEL_9_1,
    };

    for (UINT level = 0; level < ARRAYSIZE(levelAttempts); level++)
    {
        ID3D10Device1 *pDevice = NULL;
        hr = D3D10CreateDevice1(
            pAdapter,
            driverType,
            NULL,
            flags,
            levelAttempts[level],
            D3D10_1_SDK_VERSION,
            &pDevice
            );

        if (SUCCEEDED(hr))
        {
            // transfer reference
            *ppDevice = pDevice;
            pDevice = NULL;
            break;
        }

    }

    return hr;
}
```



<span data-ttu-id="6772d-160">Nell'esempio di codice successivo viene usato il `CreateD3DDevice` metodo illustrato nell'esempio precedente per creare un dispositivo Direct3D in grado di creare superfici DXGI per l'uso con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6772d-160">The next code example uses the `CreateD3DDevice` method shown in the previous example to create a Direct3D device that can create DXGI surfaces for use with Direct2D.</span></span>


```C++
// Create device
hr = CreateD3DDevice(
    NULL,
    D3D10_DRIVER_TYPE_HARDWARE,
    nDeviceFlags,
    &pDevice
    );

if (FAILED(hr))
{
    hr = CreateD3DDevice(
        NULL,
        D3D10_DRIVER_TYPE_WARP,
        nDeviceFlags,
        &pDevice
        );
}
```



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a><span data-ttu-id="6772d-161">Scrittura di contenuto Direct2D in un buffer della catena di scambio</span><span class="sxs-lookup"><span data-stu-id="6772d-161">Writing Direct2D Content to a Swap Chain Buffer</span></span>

<span data-ttu-id="6772d-162">Il modo più semplice per aggiungere contenuto Direct2D a una scena Direct3D consiste nell'usare il metodo [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) di un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) per ottenere una superficie DXGI, quindi usare la superficie con il metodo [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per creare un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) con cui creare il contenuto 2D.</span><span class="sxs-lookup"><span data-stu-id="6772d-162">The simplest way to add Direct2D content to a Direct3D scene is to use the [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method of an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) to obtain a DXGI surface, then use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) with which to draw your 2-D content.</span></span>

<span data-ttu-id="6772d-163">Questo approccio non esegue il rendering del contenuto in tre dimensioni. non avrà prospettive o profondità.</span><span class="sxs-lookup"><span data-stu-id="6772d-163">This approach does not render your content in three dimensions; it will not have perspective or depth.</span></span> <span data-ttu-id="6772d-164">Tuttavia, è utile per diverse attività comuni:</span><span class="sxs-lookup"><span data-stu-id="6772d-164">However, it is useful for several common tasks:</span></span>

-   <span data-ttu-id="6772d-165">Creazione di uno sfondo 2D per una scena 3D.</span><span class="sxs-lookup"><span data-stu-id="6772d-165">Creating a 2-D background for a 3-D scene.</span></span>
-   <span data-ttu-id="6772d-166">Creazione di un'interfaccia 2D davanti a una scena 3D.</span><span class="sxs-lookup"><span data-stu-id="6772d-166">Creating a 2-D interface in front of a 3-D scene.</span></span>
-   <span data-ttu-id="6772d-167">Uso del multicampionamento Direct3D durante il rendering del contenuto Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6772d-167">Using Direct3D multisampling when rendering Direct2D content.</span></span>

<span data-ttu-id="6772d-168">Nella sezione successiva viene illustrato come creare uno sfondo 2D per una scena 3D.</span><span class="sxs-lookup"><span data-stu-id="6772d-168">The next section shows how to create a 2-D background for a 3-D scene.</span></span>

### <a name="example-draw-a-2-d-background"></a><span data-ttu-id="6772d-169">Esempio: creare uno sfondo 2D</span><span class="sxs-lookup"><span data-stu-id="6772d-169">Example: Draw a 2-D Background</span></span>

<span data-ttu-id="6772d-170">I passaggi seguenti descrivono come creare una destinazione di rendering della superficie di DXGI e usarla per disegnare uno sfondo sfumato.</span><span class="sxs-lookup"><span data-stu-id="6772d-170">The following steps describe how to create a DXGI surface render target and use it to draw a gradient background.</span></span>

1.  <span data-ttu-id="6772d-171">Usare il metodo [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) per creare una catena di scambio per un [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (variabile *m \_ PDEVICE* ).</span><span class="sxs-lookup"><span data-stu-id="6772d-171">Use the [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) method to create a swap chain for an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (the *m\_pDevice* variable).</span></span> <span data-ttu-id="6772d-172">La catena di scambio usa il formato [**DXGI \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, uno dei formati DXGI supportati da Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6772d-172">The swap chain uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

```C++
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&m_pDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&pDXGIDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDXGIDevice->GetAdapter(&pAdapter);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAdapter->GetParent(IID_PPV_ARGS(&pDXGIFactory));
    }
    if (SUCCEEDED(hr))
    {
        DXGI_SWAP_CHAIN_DESC swapDesc;
        ::ZeroMemory(&swapDesc, sizeof(swapDesc));

        swapDesc.BufferDesc.Width = nWidth;
        swapDesc.BufferDesc.Height = nHeight;
        swapDesc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
        swapDesc.BufferDesc.RefreshRate.Numerator = 60;
        swapDesc.BufferDesc.RefreshRate.Denominator = 1;
        swapDesc.SampleDesc.Count = 1;
        swapDesc.SampleDesc.Quality = 0;
        swapDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapDesc.BufferCount = 1;
        swapDesc.OutputWindow = m_hwnd;
        swapDesc.Windowed = TRUE;

        hr = pDXGIFactory->CreateSwapChain(m_pDevice, &swapDesc, &m_pSwapChain);
    }
```

    

2.  <span data-ttu-id="6772d-173">Usare il metodo [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) della catena di scambio per ottenere una superficie DXGI.</span><span class="sxs-lookup"><span data-stu-id="6772d-173">Use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span>

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  <span data-ttu-id="6772d-174">Utilizzare la superficie DXGI per creare una destinazione di rendering DXGI.</span><span class="sxs-lookup"><span data-stu-id="6772d-174">Use the DXGI surface to create a DXGI render target.</span></span>
```C++
    // Create the DXGI Surface Render Target.
    FLOAT dpiX;
    FLOAT dpiY;
    m_pD2DFactory->GetDesktopDpi(&dpiX, &dpiY);

    D2D1_RENDER_TARGET_PROPERTIES props =
        D2D1::RenderTargetProperties(
            D2D1_RENDER_TARGET_TYPE_DEFAULT,
            D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
            dpiX,
            dpiY
            );

    // Create a Direct2D render target which can draw into the surface in the swap chain

    
hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pBackBuffer,
        &props,
        &m_pBackBufferRT
        );
    
```



    

4.  <span data-ttu-id="6772d-175">Utilizzare la destinazione di rendering per disegnare uno sfondo sfumato.</span><span class="sxs-lookup"><span data-stu-id="6772d-175">Use the render target to draw a gradient background.</span></span>

```C++
    // Swap chain will tell us how big the back buffer is
    DXGI_SWAP_CHAIN_DESC swapDesc;
    hr = m_pSwapChain->GetDesc(&swapDesc);

    if (SUCCEEDED(hr))
    {

    
// Draw a gradient background.
    if (m_pBackBufferRT)
    {
        D2D1_SIZE_F targetSize = m_pBackBufferRT->GetSize();

        m_pBackBufferRT->BeginDraw();

        m_pBackBufferGradientBrush->SetTransform(
            D2D1::Matrix3x2F::Scale(targetSize)
            );

        D2D1_RECT_F rect = D2D1::RectF(
            0.0f,
            0.0f,
            targetSize.width,
            targetSize.height
            );

        m_pBackBufferRT->FillRectangle(&rect, m_pBackBufferGradientBrush);

        hr = m_pBackBufferRT->EndDraw();
    }
```



    

<span data-ttu-id="6772d-176">Il codice viene omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="6772d-176">Code is omitted from this sample.</span></span>

## <a name="using-direct2d-content-as-a-texture"></a><span data-ttu-id="6772d-177">Uso del contenuto Direct2D come trama</span><span class="sxs-lookup"><span data-stu-id="6772d-177">Using Direct2D Content as a Texture</span></span>

<span data-ttu-id="6772d-178">Un altro modo per usare il contenuto Direct2D con Direct3D consiste nell'usare Direct2D per generare una trama 2D, quindi applicare tale trama a un modello 3D.</span><span class="sxs-lookup"><span data-stu-id="6772d-178">Another way to use Direct2D content with Direct3D is to use Direct2D to generate a 2-D texture and then apply that texture to a 3-D model.</span></span> <span data-ttu-id="6772d-179">A tale scopo, creare un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), ottenere una superficie DXGI dalla trama e quindi usare la superficie per creare una destinazione di rendering della superficie di dxgi.</span><span class="sxs-lookup"><span data-stu-id="6772d-179">You do this by creating an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), obtaining a DXGI surface from the texture, and then using the surface to create a DXGI surface render target.</span></span> <span data-ttu-id="6772d-180">Per la superficie **ID3D10Texture2D** è necessario usare il flag di binding della [**destinazione di \_ \_ rendering \_ D3D10 bind**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) e usare un formato DXGI supportato dalle destinazioni di rendering della superficie DXGI.</span><span class="sxs-lookup"><span data-stu-id="6772d-180">The **ID3D10Texture2D** surface must use the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) bind flag and use a DXGI format supported by DXGI surface render targets.</span></span> <span data-ttu-id="6772d-181">Per un elenco dei formati DXGI supportati, vedere [formati di pixel supportati e modalità Alpha](supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="6772d-181">For a list of supported DXGI formats, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

### <a name="example-use-direct2d-content-as-a-texture"></a><span data-ttu-id="6772d-182">Esempio: usare il contenuto Direct2D come trama</span><span class="sxs-lookup"><span data-stu-id="6772d-182">Example: Use Direct2D Content as a Texture</span></span>

<span data-ttu-id="6772d-183">Gli esempi seguenti illustrano come creare una destinazione di rendering della superficie DXGI che esegue il rendering in una trama 2D, rappresentata da un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d).</span><span class="sxs-lookup"><span data-stu-id="6772d-183">The following examples show how to create a DXGI surface render target that renders to a 2-D texture (represented by an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).</span></span>

1.  <span data-ttu-id="6772d-184">Per prima cosa, usare un dispositivo Direct3D per creare una trama 2D.</span><span class="sxs-lookup"><span data-stu-id="6772d-184">First, use a Direct3D device to create a 2-D texture.</span></span> <span data-ttu-id="6772d-185">La trama usa i flag di associazione della [**\_ \_ \_ destinazione di rendering D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) e **D3D10 \_ Bind \_ shader \_** e usa il formato [**DXGI \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, uno dei formati DXGI supportati da Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6772d-185">The texture uses the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) and **D3D10\_BIND\_SHADER\_RESOURCE** bind flags, and it uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

```C++
    // Allocate a offscreen D3D surface for D2D to render our 2D content into
    D3D10_TEXTURE2D_DESC texDesc;
    texDesc.ArraySize = 1;
    texDesc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
    texDesc.CPUAccessFlags = 0;
    texDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
    texDesc.Height = 512;
    texDesc.Width = 512;
    texDesc.MipLevels = 1;
    texDesc.MiscFlags = 0;
    texDesc.SampleDesc.Count = 1;
    texDesc.SampleDesc.Quality = 0;
    texDesc.Usage = D3D10_USAGE_DEFAULT;

    hr = m_pDevice->CreateTexture2D(&texDesc, NULL, &m_pOffscreenTexture);
```

    

2.  <span data-ttu-id="6772d-186">Usare la trama per ottenere una superficie DXGI.</span><span class="sxs-lookup"><span data-stu-id="6772d-186">Use the texture to obtain a DXGI surface.</span></span>

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  <span data-ttu-id="6772d-187">Utilizzare la superficie con il metodo [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per ottenere una destinazione di rendering Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6772d-187">Use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to obtain a Direct2D render target.</span></span>

```C++
    if (SUCCEEDED(hr))
    {
        // Create a D2D render target which can draw into our offscreen D3D
        // surface. Given that we use a constant size for the texture, we
        // fix the DPI at 96.
        D2D1_RENDER_TARGET_PROPERTIES props =
            D2D1::RenderTargetProperties(
                D2D1_RENDER_TARGET_TYPE_DEFAULT,
                D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
                96,
                96
                );

    
    hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
            pDxgiSurface,
            &props,
            &m_pRenderTarget
            );
    }
```



    

<span data-ttu-id="6772d-188">Ora che è stata ottenuta una destinazione di rendering Direct2D e che è stata associata a una trama Direct3D, è possibile usare la destinazione di rendering per disegnare contenuto Direct2D in tale trama ed è possibile applicare tale trama alle primitive Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6772d-188">Now that you have obtained a Direct2D render target and associated it with a Direct3D texture, you can use the render target to draw Direct2D content to that texture, and you can apply that texture to Direct3D primitives.</span></span>

<span data-ttu-id="6772d-189">Il codice viene omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="6772d-189">Code is omitted from this sample.</span></span>

## <a name="resizing-a-dxgi-surface-render-target"></a><span data-ttu-id="6772d-190">Ridimensionamento di una destinazione di rendering della superficie DXGI</span><span class="sxs-lookup"><span data-stu-id="6772d-190">Resizing a DXGI Surface Render Target</span></span>

<span data-ttu-id="6772d-191">Le destinazioni di rendering della superficie di DXGI non supportano il metodo [**ID2D1RenderTarget:: Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) .</span><span class="sxs-lookup"><span data-stu-id="6772d-191">DXGI surface render targets do not support the [**ID2D1RenderTarget::Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) method.</span></span> <span data-ttu-id="6772d-192">Per ridimensionare una destinazione di rendering della superficie di DXGI, l'applicazione deve rilasciare e ricrearla.</span><span class="sxs-lookup"><span data-stu-id="6772d-192">To resize a DXGI surface render target, the application must release and re-create it.</span></span>

<span data-ttu-id="6772d-193">Questa operazione può causare problemi di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="6772d-193">This operation can potentially create performance issues.</span></span> <span data-ttu-id="6772d-194">La destinazione di rendering può essere l'ultima risorsa Direct2D attiva che mantiene un riferimento a [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associato alla superficie DXGI della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="6772d-194">The render target might be the last active Direct2D resource that keeps a reference to the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the render target's DXGI surface.</span></span> <span data-ttu-id="6772d-195">Se l'applicazione rilascia la destinazione di rendering e il riferimento **ID3D10Device1** viene eliminato definitivamente, è necessario ricrearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="6772d-195">If the application releases the render target and the **ID3D10Device1** reference is destroyed, a new one must be recreated.</span></span>

<span data-ttu-id="6772d-196">È possibile evitare questa operazione potenzialmente costosa mantenendo almeno una risorsa Direct2D creata dalla destinazione di rendering mentre si ricrea la destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="6772d-196">You can avoid this potentially expensive operation by keeping at least one Direct2D resource that was created by the render target while you re-create that render target.</span></span> <span data-ttu-id="6772d-197">Di seguito sono riportate alcune risorse Direct2D che funzionano per questo approccio:</span><span class="sxs-lookup"><span data-stu-id="6772d-197">The following are some Direct2D resources that work for this approach:</span></span>

-   <span data-ttu-id="6772d-198">[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (che può essere mantenuto indirettamente da un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))</span><span class="sxs-lookup"><span data-stu-id="6772d-198">[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (which may be held indirectly by an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))</span></span>
-   [<span data-ttu-id="6772d-199">**ID2D1Layer**</span><span class="sxs-lookup"><span data-stu-id="6772d-199">**ID2D1Layer**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [<span data-ttu-id="6772d-200">**ID2D1Mesh**</span><span class="sxs-lookup"><span data-stu-id="6772d-200">**ID2D1Mesh**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

<span data-ttu-id="6772d-201">Per gestire questo approccio, il metodo di ridimensionamento deve verificare se il dispositivo Direct3D è disponibile.</span><span class="sxs-lookup"><span data-stu-id="6772d-201">To accommodate this approach, your resize method should test to see whether the Direct3D device is available.</span></span> <span data-ttu-id="6772d-202">Se è disponibile, rilasciare e ricreare le destinazioni di rendering della superficie di DXGI, mantenendo tutte le risorse create in precedenza e riutilizzarle.</span><span class="sxs-lookup"><span data-stu-id="6772d-202">If it is available, release and re-create your DXGI surface render targets, but keep all the resources that they created previously and reuse them.</span></span> <span data-ttu-id="6772d-203">Questa operazione funziona perché, come descritto nella [Panoramica delle risorse](resources-and-resource-domains.md), le risorse create da due destinazioni di rendering sono compatibili quando entrambe le destinazioni di rendering sono associate allo stesso dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6772d-203">This works because, as described in the [Resources Overview](resources-and-resource-domains.md), resources created by two render targets are compatible when both render targets are associated with the same Direct3D device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6772d-204">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6772d-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6772d-205">Formati pixel e modalità alfa supportati</span><span class="sxs-lookup"><span data-stu-id="6772d-205">Supported Pixel Formats and Alpha Modes</span></span>](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

<span data-ttu-id="6772d-206">[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="6772d-206">[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span></span>
</dt> <dt>

[<span data-ttu-id="6772d-207">Grafica di Windows DirectX</span><span class="sxs-lookup"><span data-stu-id="6772d-207">Windows DirectX Graphics</span></span>](../graphics-and-multimedia.md)
</dt> </dl>

 

 