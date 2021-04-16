---
title: Come eseguire il rendering usando un contesto di dispositivo Direct2D
description: In questo argomento si apprenderà come creare Direct2D \ 32; contesto di dispositivo in Windows 8.
ms.assetid: D4563FEA-767E-4B16-8F3C-3D548A64B206
keywords:
- Dispositivo Direct2D
- Contesto di dispositivo Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2858861956a40bf969309be474105052e4692cde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104551210"
---
# <a name="how-to-render-by-using-a-direct2d-device-context"></a><span data-ttu-id="e906e-105">Come eseguire il rendering usando un contesto di dispositivo Direct2D</span><span class="sxs-lookup"><span data-stu-id="e906e-105">How to render by using a Direct2D device context</span></span>

<span data-ttu-id="e906e-106">In questo argomento si apprenderà come creare il [**contesto di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](./direct2d-portal.md) in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e906e-106">In this topic you will learn about creating [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) in Windows 8.</span></span> <span data-ttu-id="e906e-107">Queste informazioni si applicano a se si sviluppano app di Windows Store o un'app desktop tramite Direct2D.</span><span class="sxs-lookup"><span data-stu-id="e906e-107">This information applies to you if you are developing Windows Store apps or a desktop app by using Direct2D.</span></span> <span data-ttu-id="e906e-108">Questo argomento descrive lo scopo degli oggetti di contesto di dispositivo Direct2D, come creare l'oggetto e una guida dettagliata sul rendering e sulla visualizzazione di immagini e primitive Direct2D.</span><span class="sxs-lookup"><span data-stu-id="e906e-108">This topic describes the purpose of Direct2D device context objects, how to create that object , and a step by step guide about rendering and displaying Direct2D primitives and images.</span></span> <span data-ttu-id="e906e-109">Si apprenderà anche come cambiare le destinazioni di rendering e aggiungere effetti all'app.</span><span class="sxs-lookup"><span data-stu-id="e906e-109">You will also learn about switching render targets and adding effects to your app.</span></span>

-   [<span data-ttu-id="e906e-110">Che cos'è un dispositivo Direct2D?</span><span class="sxs-lookup"><span data-stu-id="e906e-110">What is a Direct2D device?</span></span>](#what-is-a-direct2d-device)
-   [<span data-ttu-id="e906e-111">Che cos'è un contesto di dispositivo Direct2D?</span><span class="sxs-lookup"><span data-stu-id="e906e-111">What is a Direct2D device context?</span></span>](#what-is-a-direct2d-device-context)
-   [<span data-ttu-id="e906e-112">Rendering con Direct2D in Windows 8</span><span class="sxs-lookup"><span data-stu-id="e906e-112">Rendering with Direct2D on Windows 8</span></span>](#rendering-with-direct2d-on-windows-8)
-   [<span data-ttu-id="e906e-113">Perché usare un contesto di dispositivo per il rendering?</span><span class="sxs-lookup"><span data-stu-id="e906e-113">Why use a device context to render?</span></span>](#why-use-a-device-context-to-render)
-   [<span data-ttu-id="e906e-114">Come creare un contesto di dispositivo Direct2D per il rendering</span><span class="sxs-lookup"><span data-stu-id="e906e-114">How to create a Direct2D device context for rendering</span></span>](#how-to-create-a-direct2d-device-context-for-rendering)
-   [<span data-ttu-id="e906e-115">Selezione di una destinazione</span><span class="sxs-lookup"><span data-stu-id="e906e-115">Selecting a target</span></span>](#selecting-a-target)
-   [<span data-ttu-id="e906e-116">Come eseguire il rendering e la visualizzazione</span><span class="sxs-lookup"><span data-stu-id="e906e-116">How to render and display</span></span>](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a><span data-ttu-id="e906e-117">Che cos'è un dispositivo Direct2D?</span><span class="sxs-lookup"><span data-stu-id="e906e-117">What is a Direct2D device?</span></span>

<span data-ttu-id="e906e-118">Per creare un contesto di dispositivo Direct2D è necessario un dispositivo Direct2D e un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e906e-118">You need a Direct2D device and a Direct3D device to create a Direct2D device context.</span></span> <span data-ttu-id="e906e-119">Un [**dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (espone un puntatore all'interfaccia **ID2D1Device** ) rappresenta una scheda di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e906e-119">A [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (exposes an **ID2D1Device** interface pointer) represents a display adapter.</span></span> <span data-ttu-id="e906e-120">Un dispositivo Direct3D (espone un puntatore all'interfaccia [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) ) è associato a un dispositivo Direct2D.</span><span class="sxs-lookup"><span data-stu-id="e906e-120">A Direct3D device (exposes an [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) interface pointer) is associated with a Direct2D device.</span></span> <span data-ttu-id="e906e-121">Ogni app deve avere un solo **dispositivo Direct2D**, ma può avere più di un **dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="e906e-121">Each app must have one **Direct2D device**, but can have more than one **device**.</span></span>

## <a name="what-is-a-direct2d-device-context"></a><span data-ttu-id="e906e-122">Che cos'è un contesto di dispositivo Direct2D?</span><span class="sxs-lookup"><span data-stu-id="e906e-122">What is a Direct2D device context?</span></span>

<span data-ttu-id="e906e-123">Un [](./direct2d-portal.md) [**contesto di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D (espone un puntatore all'interfaccia **ID2D1DeviceContext** ) rappresenta un set di buffer di stato e di comando usati per eseguire il rendering in una destinazione.</span><span class="sxs-lookup"><span data-stu-id="e906e-123">A [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) (exposes an **ID2D1DeviceContext** interface pointer) represents a set of state and command buffers that you use to render to a target.</span></span> <span data-ttu-id="e906e-124">È possibile chiamare i metodi nel contesto di dispositivo per impostare lo stato della pipeline e generare i comandi di rendering usando le risorse di proprietà di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e906e-124">You can call methods on the device context to set pipeline state and generate rendering commands by using the resources owned by a device.</span></span>

## <a name="rendering-with-direct2d-on-windows-8"></a><span data-ttu-id="e906e-125">Rendering con Direct2D in Windows 8</span><span class="sxs-lookup"><span data-stu-id="e906e-125">Rendering with Direct2D on Windows 8</span></span>

<span data-ttu-id="e906e-126">In Windows 7 e versioni precedenti si usa un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) o un'altra interfaccia di destinazione di rendering per eseguire il rendering in una finestra o in una superficie.</span><span class="sxs-lookup"><span data-stu-id="e906e-126">On Windows 7 and earlier, you use a [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) or another render target interface to render to a window or surface.</span></span> <span data-ttu-id="e906e-127">A partire da Windows 8, non è consigliabile eseguire il rendering usando metodi basati su interfacce come **ID2D1HwndRenderTarget** , in quanto non funzionano con le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="e906e-127">Starting with Windows 8, we do not recommend rendering by using methods that rely on interfaces like **ID2D1HwndRenderTarget** because they won't work with Windows Store apps.</span></span> <span data-ttu-id="e906e-128">È possibile usare un [**contesto di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) per eseguire il rendering in un HWND se si vuole creare un'app desktop e sfruttare ancora le funzionalità aggiuntive del **contesto di dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="e906e-128">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to render to an Hwnd if you want to make a desktop app and still take advantage of the **device context's** additional features.</span></span> <span data-ttu-id="e906e-129">Tuttavia, il **contesto di dispositivo** è necessario per eseguire il rendering del contenuto in un'app di Windows Store con [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="e906e-129">However, the **device context** is required to render content in a Windows Store apps with [Direct2D](./direct2d-portal.md).</span></span>

## <a name="why-use-a-device-context-to-render"></a><span data-ttu-id="e906e-130">Perché usare un contesto di dispositivo per il rendering?</span><span class="sxs-lookup"><span data-stu-id="e906e-130">Why use a device context to render?</span></span>

-   <span data-ttu-id="e906e-131">È possibile eseguire il rendering per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="e906e-131">You can render for Windows Store apps.</span></span>
-   <span data-ttu-id="e906e-132">È possibile modificare la destinazione di rendering in qualsiasi momento prima, durante e dopo il rendering.</span><span class="sxs-lookup"><span data-stu-id="e906e-132">You can change the render target at any time before, during, and after rendering.</span></span> <span data-ttu-id="e906e-133">Il contesto di dispositivo garantisce che le chiamate ai metodi di disegno vengano eseguite nell'ordine e le applichino quando si passa alla destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="e906e-133">The device context ensures that the calls to drawing methods are executed in order and applies them when you switch the render target.</span></span>
-   <span data-ttu-id="e906e-134">È possibile usare più di un tipo di finestra con un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e906e-134">You can use more than one type of window with a device context.</span></span> <span data-ttu-id="e906e-135">È possibile usare un [**contesto di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) e [**una catena di scambio DXGI**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) per eseguire il rendering direttamente in [**Windows:: UI:: Core:: COREWINDOW**](/uwp/api/Windows.UI.Core.CoreWindow) o [**Windows:: UI:: XAML:: SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).</span><span class="sxs-lookup"><span data-stu-id="e906e-135">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) to render directly to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) or a [**Windows::UI::XAML::SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).</span></span>
-   <span data-ttu-id="e906e-136">È possibile usare il [](./direct2d-portal.md) [**contesto di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2d per creare [effetti Direct2D](effects-overview.md) e per eseguire il rendering dell'output di un effetto immagine o di un grafico effetto in una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="e906e-136">You can use the [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to create [Direct2D effects](effects-overview.md) and to render the output of an image effect or effect graph to a render target.</span></span>
-   <span data-ttu-id="e906e-137">È possibile avere più [**contesti di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), che possono essere utili per migliorare le prestazioni in un'app a thread.</span><span class="sxs-lookup"><span data-stu-id="e906e-137">You can have multiple [**device contexts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), which can be helpful for improving performance in a threaded app.</span></span> <span data-ttu-id="e906e-138">Per altre informazioni, vedere [app Direct2D multithread](multi-threaded-direct2d-apps.md) .</span><span class="sxs-lookup"><span data-stu-id="e906e-138">See [Multithreaded Direct2D apps](multi-threaded-direct2d-apps.md) for more information.</span></span>
-   <span data-ttu-id="e906e-139">Il [**contesto di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interagisce strettamente con Direct3D, offrendo maggiore accesso alle opzioni Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e906e-139">The [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interoperates closely with Direct3D, giving you more access to Direct3D options.</span></span>

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a><span data-ttu-id="e906e-140">Come creare un contesto di dispositivo Direct2D per il rendering</span><span class="sxs-lookup"><span data-stu-id="e906e-140">How to create a Direct2D device context for rendering</span></span>

<span data-ttu-id="e906e-141">Il codice seguente illustra come creare un dispositivo Direct3D11, ottenere il dispositivo DXGI associato, creare un [**dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)e infine creare il [**contesto di periferica**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D per il rendering.</span><span class="sxs-lookup"><span data-stu-id="e906e-141">The code here shows you how to create a Direct3D11 device, get the associated DXGI device, create a [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device), and then finally create the Direct2D [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) for rendering.</span></span>

<span data-ttu-id="e906e-142">Di seguito è riportato un diagramma delle chiamate al metodo e delle interfacce utilizzate dal codice.</span><span class="sxs-lookup"><span data-stu-id="e906e-142">Here is a diagram of the method calls and the interfaces this code uses.</span></span>

![diagramma dei dispositivi Direct2D e Direct3D e dei contesti di dispositivo.](images/devicecontextdiagram.png)

> [!Note]  
> <span data-ttu-id="e906e-144">Questo codice presuppone che sia già presente un oggetto [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) . per altre informazioni, vedere la [**pagina di riferimento di ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="e906e-144">This code assumes you already have an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) object, for more information see the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>

 


```C++
    // This flag adds support for surfaces with a different color channel ordering than the API default.
    // You need it for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    
    // This array defines the set of DirectX hardware feature levels this app  supports.
    // The ordering is important and you should  preserve it.
    // Don't forget to declare your app's minimum required feature level in its
    // description.  All apps are assumed to support 9.1 unless otherwise stated.
    D3D_FEATURE_LEVEL featureLevels[] = 
    {
        D3D_FEATURE_LEVEL_11_1,
        D3D_FEATURE_LEVEL_11_0,
        D3D_FEATURE_LEVEL_10_1,
        D3D_FEATURE_LEVEL_10_0,
        D3D_FEATURE_LEVEL_9_3,
        D3D_FEATURE_LEVEL_9_2,
        D3D_FEATURE_LEVEL_9_1
    };

    // Create the DX11 API device object, and get a corresponding context.
    ComPtr<ID3D11Device> device;
    ComPtr<ID3D11DeviceContext> context;

    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of possible feature levels
            D3D11_SDK_VERSION,          
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );

    ComPtr<IDXGIDevice> dxgiDevice;
    // Obtain the underlying DXGI device of the Direct3D11 device.
    DX::ThrowIfFailed(
        device.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // Get Direct2D device's corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



<span data-ttu-id="e906e-145">Verranno esaminati i passaggi dell'esempio di codice precedente.</span><span class="sxs-lookup"><span data-stu-id="e906e-145">Let's walk through the steps in the preceding code sample.</span></span>

1.  <span data-ttu-id="e906e-146">Ottenere un puntatore a interfaccia ID3D11Device che sarà necessario per creare il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e906e-146">Get an ID3D11Device interface pointer you will need this to create the device context.</span></span>

    -   <span data-ttu-id="e906e-147">Dichiarare i flag di creazione per configurare il dispositivo [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) per il supporto di BGRA.</span><span class="sxs-lookup"><span data-stu-id="e906e-147">Declare the creation flags to set up the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) device for BGRA support.</span></span> <span data-ttu-id="e906e-148">[Direct2D](./direct2d-portal.md) richiede l'ordine di colore BGRA.</span><span class="sxs-lookup"><span data-stu-id="e906e-148">[Direct2D](./direct2d-portal.md) requires BGRA color order.</span></span>
    -   <span data-ttu-id="e906e-149">Dichiarare una matrice di voci a [**\_ \_ livello di funzionalità D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) che rappresentano il set di livelli di funzionalità che l'app supporterà.</span><span class="sxs-lookup"><span data-stu-id="e906e-149">Declare an array of [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) entries representing the set of feature levels that your app will support.</span></span>
        > [!Note]  
        > <span data-ttu-id="e906e-150">[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) Cerca nell'elenco fino a quando non trova il livello di funzionalità supportato dal sistema host.</span><span class="sxs-lookup"><span data-stu-id="e906e-150">[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) searches your list until it finds the feature level supported by the host system.</span></span>

         

    -   <span data-ttu-id="e906e-151">Usare la funzione [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) per creare un oggetto [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) . la funzione restituirà anche un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) , ma tale oggetto non è necessario per questo esempio.</span><span class="sxs-lookup"><span data-stu-id="e906e-151">Use the [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) function to create an [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) object, the function will also return an [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) object, but that object is not needed for this example.</span></span>

2.  <span data-ttu-id="e906e-152">Eseguire una query sul [**dispositivo Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) per la relativa interfaccia del [**dispositivo DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="e906e-152">Query the [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) for its [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) interface.</span></span>
3.  <span data-ttu-id="e906e-153">Creare un oggetto [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) chiamando il metodo [**ID2D1Factory:: CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) e passando l'oggetto [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="e906e-153">Create an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) object by calling the [**ID2D1Factory::CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) method and passing in the [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) object.</span></span>
4.  <span data-ttu-id="e906e-154">Creare un puntatore [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) usando il metodo [**ID2D1Device:: CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) .</span><span class="sxs-lookup"><span data-stu-id="e906e-154">Create an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pointer using the [**ID2D1Device::CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) method.</span></span>

## <a name="selecting-a-target"></a><span data-ttu-id="e906e-155">Selezione di una destinazione</span><span class="sxs-lookup"><span data-stu-id="e906e-155">Selecting a target</span></span>

<span data-ttu-id="e906e-156">Il codice seguente illustra come ottenere la [**trama Direct3D a 2 dimensioni**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) per il buffer nascosto della finestra e creare una destinazione bitmap che si collega a questa trama a cui viene eseguito il rendering del [**contesto di dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="e906e-156">The code here shows you how to get the [**2 dimensional Direct3D texture**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) for the window back buffer and create a bitmap target that links to this texture to which the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) renders.</span></span>


```C++
        // Allocate a descriptor.
        DXGI_SWAP_CHAIN_DESC1 swapChainDesc = {0};
        swapChainDesc.Width = 0;                           // use automatic sizing
        swapChainDesc.Height = 0;
        swapChainDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM; // this is the most common swapchain format
        swapChainDesc.Stereo = false; 
        swapChainDesc.SampleDesc.Count = 1;                // don't use multi-sampling
        swapChainDesc.SampleDesc.Quality = 0;
        swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapChainDesc.BufferCount = 2;                     // use double buffering to enable flip
        swapChainDesc.Scaling = DXGI_SCALING_NONE;
        swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL; // all apps must use this SwapEffect
        swapChainDesc.Flags = 0;

        // Identify the physical adapter (GPU or card) this device is runs on.
        ComPtr<IDXGIAdapter> dxgiAdapter;
        DX::ThrowIfFailed(
            dxgiDevice->GetAdapter(&dxgiAdapter)
            );

        // Get the factory object that created the DXGI device.
        ComPtr<IDXGIFactory2> dxgiFactory;
        DX::ThrowIfFailed(
            dxgiAdapter->GetParent(IID_PPV_ARGS(&dxgiFactory))
            );

        // Get the final swap chain for this window from the DXGI factory.
        DX::ThrowIfFailed(
            dxgiFactory->CreateSwapChainForCoreWindow(
                device.Get(),
                reinterpret_cast<IUnknown*>(m_window),
                &swapChainDesc,
                nullptr,    // allow on all displays
                &m_swapChain
                )
            );

        // Ensure that DXGI doesn't queue more than one frame at a time.
        DX::ThrowIfFailed(
            dxgiDevice->SetMaximumFrameLatency(1)
            );

    // Get the backbuffer for this window which is be the final 3D render target.
    ComPtr<ID3D11Texture2D> backBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&backBuffer))
        );

    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it is directly rendered to the 
    // swap chain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_IGNORE),
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

    // Now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



<span data-ttu-id="e906e-157">Verranno esaminati i passaggi dell'esempio di codice precedente.</span><span class="sxs-lookup"><span data-stu-id="e906e-157">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="e906e-158">Allocare una struttura [**DESC1 della \_ catena di scambio \_ \_ DXGI**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) e definire le impostazioni per la [**catena di scambio**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="e906e-158">Allocate a [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) structure and define the settings for the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

    <span data-ttu-id="e906e-159">Queste impostazioni mostrano un esempio di come creare una catena di scambio che può essere usata da un'app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="e906e-159">These settings show an example of how to create a swap chain that a Windows Store app can use.</span></span>

2.  <span data-ttu-id="e906e-160">Ottenere la scheda in cui è in esecuzione il [**dispositivo Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) e il [**dispositivo DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) e ottenere l'oggetto [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) associato.</span><span class="sxs-lookup"><span data-stu-id="e906e-160">Get the adapter that the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) are running on and get the [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) object associated with them.</span></span> <span data-ttu-id="e906e-161">È necessario usare questa **Factory DXGI** per assicurarsi che la [**catena di scambio**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) venga creata sulla stessa scheda.</span><span class="sxs-lookup"><span data-stu-id="e906e-161">You must use this **DXGI factory** to ensure the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) is created on the same adapter.</span></span>

3.  <span data-ttu-id="e906e-162">Chiamare il metodo [**IDXGIFactory2:: CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) per creare la catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="e906e-162">Call the [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) method to create the swap chain.</span></span> <span data-ttu-id="e906e-163">Usare la classe [**Windows:: UI:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) per la finestra principale di un'app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="e906e-163">Use the [**Windows::UI::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) class for the main window of a Windows Store app.</span></span>

    <span data-ttu-id="e906e-164">Assicurarsi di impostare la latenza massima del frame su 1 per ridurre al minimo il consumo di energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="e906e-164">Make sure to set the maximum frame latency to 1 to minimize power consumption.</span></span>

    <span data-ttu-id="e906e-165">Se si vuole eseguire il rendering del contenuto Direct2D in un'app di Windows Store, vedere il metodo [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) .</span><span class="sxs-lookup"><span data-stu-id="e906e-165">If you want to render Direct2D content in a Windows Store app, see the [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method.</span></span>

4.  <span data-ttu-id="e906e-166">Ottenere il buffer nascosto dalla [**catena di scambio**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="e906e-166">Get the back buffer from the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span> <span data-ttu-id="e906e-167">Il buffer nascosto espone un'interfaccia [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) allocata dalla **catena di scambio**</span><span class="sxs-lookup"><span data-stu-id="e906e-167">The back buffer exposes an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) interface allocated by the **swap chain**</span></span>

5.  <span data-ttu-id="e906e-168">Dichiarare uno struct [**d2d1 \_ bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) e impostare i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e906e-168">Declare a [**D2D1\_BITMAP\_PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) struct and set the property values.</span></span> <span data-ttu-id="e906e-169">Impostare il formato pixel su BGRA perché si tratta del formato utilizzato dal dispositivo [**Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) e dal [**dispositivo DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="e906e-169">Set the pixel format to BGRA because this is the format the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) use.</span></span>

6.  <span data-ttu-id="e906e-170">Ottenere il buffer nascosto come [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) da passare a Direct2D.</span><span class="sxs-lookup"><span data-stu-id="e906e-170">Get the back buffer as an [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) to pass to Direct2D.</span></span> <span data-ttu-id="e906e-171">Direct2D non accetta direttamente un [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) .</span><span class="sxs-lookup"><span data-stu-id="e906e-171">Direct2D doesn't accept an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) directly.</span></span>

    <span data-ttu-id="e906e-172">Creare un oggetto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) dal buffer nascosto usando il metodo [**ID2D1DeviceContext:: CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) .</span><span class="sxs-lookup"><span data-stu-id="e906e-172">Create a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object from the back buffer using the [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method.</span></span>

7.  <span data-ttu-id="e906e-173">A questo punto la [**bitmap Direct2D**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) è collegata al buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="e906e-173">Now the [**Direct2D bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is linked to the back buffer.</span></span> <span data-ttu-id="e906e-174">Impostare la destinazione nel [**contesto di periferica Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) sulla **bitmap**.</span><span class="sxs-lookup"><span data-stu-id="e906e-174">Set the target on the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to the **bitmap**.</span></span>

## <a name="how-to-render-and-display"></a><span data-ttu-id="e906e-175">Come eseguire il rendering e la visualizzazione</span><span class="sxs-lookup"><span data-stu-id="e906e-175">How to render and display</span></span>

<span data-ttu-id="e906e-176">Ora che si dispone di una bitmap di destinazione, è possibile creare primitive, immagini, effetti di immagini e testo utilizzando il [**contesto di periferica Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span><span class="sxs-lookup"><span data-stu-id="e906e-176">Now that you have a target bitmap, you can draw primitives, images, image effects, and text to it using the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span></span> <span data-ttu-id="e906e-177">Il codice seguente illustra come creare un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="e906e-177">The code here shows you how to draw a rectangle.</span></span>


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);

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



<span data-ttu-id="e906e-178">Verranno esaminati i passaggi dell'esempio di codice precedente.</span><span class="sxs-lookup"><span data-stu-id="e906e-178">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="e906e-179">Chiamare [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) per creare un pennello per disegnare il rettangolo.</span><span class="sxs-lookup"><span data-stu-id="e906e-179">Call the [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) to create a brush to paint the rectangle.</span></span>
2.  <span data-ttu-id="e906e-180">Chiamare il metodo [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) prima di emettere comandi di disegno.</span><span class="sxs-lookup"><span data-stu-id="e906e-180">Call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands.</span></span>
3.  <span data-ttu-id="e906e-181">Chiamare il metodo [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) il rettangolo da disegnare e il pennello.</span><span class="sxs-lookup"><span data-stu-id="e906e-181">Call the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method the rectangle to be drawn and the brush.</span></span>
4.  <span data-ttu-id="e906e-182">Chiamare il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) dopo aver emesso i comandi di disegno.</span><span class="sxs-lookup"><span data-stu-id="e906e-182">Call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span>
5.  <span data-ttu-id="e906e-183">Visualizzare il risultato chiamando il metodo [**IDXGISwapChain::P reinviato**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) .</span><span class="sxs-lookup"><span data-stu-id="e906e-183">Display the result by calling the [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method.</span></span>

<span data-ttu-id="e906e-184">A questo punto è possibile usare il [**contesto di dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) per creare primitive, immagini, effetti di immagini e testo sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="e906e-184">Now you can use the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) draw primitives, images, image effects, and text to the screen.</span></span>

 

 