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
# <a name="how-to-render-by-using-a-direct2d-device-context"></a>Come eseguire il rendering usando un contesto di dispositivo Direct2D

In questo argomento si apprenderà come creare il [**contesto di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](./direct2d-portal.md) in Windows 8. Queste informazioni si applicano a se si sviluppano app di Windows Store o un'app desktop tramite Direct2D. Questo argomento descrive lo scopo degli oggetti di contesto di dispositivo Direct2D, come creare l'oggetto e una guida dettagliata sul rendering e sulla visualizzazione di immagini e primitive Direct2D. Si apprenderà anche come cambiare le destinazioni di rendering e aggiungere effetti all'app.

-   [Che cos'è un dispositivo Direct2D?](#what-is-a-direct2d-device)
-   [Che cos'è un contesto di dispositivo Direct2D?](#what-is-a-direct2d-device-context)
-   [Rendering con Direct2D in Windows 8](#rendering-with-direct2d-on-windows-8)
-   [Perché usare un contesto di dispositivo per il rendering?](#why-use-a-device-context-to-render)
-   [Come creare un contesto di dispositivo Direct2D per il rendering](#how-to-create-a-direct2d-device-context-for-rendering)
-   [Selezione di una destinazione](#selecting-a-target)
-   [Come eseguire il rendering e la visualizzazione](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a>Che cos'è un dispositivo Direct2D?

Per creare un contesto di dispositivo Direct2D è necessario un dispositivo Direct2D e un dispositivo Direct3D. Un [**dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (espone un puntatore all'interfaccia **ID2D1Device** ) rappresenta una scheda di visualizzazione. Un dispositivo Direct3D (espone un puntatore all'interfaccia [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) ) è associato a un dispositivo Direct2D. Ogni app deve avere un solo **dispositivo Direct2D**, ma può avere più di un **dispositivo**.

## <a name="what-is-a-direct2d-device-context"></a>Che cos'è un contesto di dispositivo Direct2D?

Un [](./direct2d-portal.md) [**contesto di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D (espone un puntatore all'interfaccia **ID2D1DeviceContext** ) rappresenta un set di buffer di stato e di comando usati per eseguire il rendering in una destinazione. È possibile chiamare i metodi nel contesto di dispositivo per impostare lo stato della pipeline e generare i comandi di rendering usando le risorse di proprietà di un dispositivo.

## <a name="rendering-with-direct2d-on-windows-8"></a>Rendering con Direct2D in Windows 8

In Windows 7 e versioni precedenti si usa un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) o un'altra interfaccia di destinazione di rendering per eseguire il rendering in una finestra o in una superficie. A partire da Windows 8, non è consigliabile eseguire il rendering usando metodi basati su interfacce come **ID2D1HwndRenderTarget** , in quanto non funzionano con le app di Windows Store. È possibile usare un [**contesto di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) per eseguire il rendering in un HWND se si vuole creare un'app desktop e sfruttare ancora le funzionalità aggiuntive del **contesto di dispositivo** . Tuttavia, il **contesto di dispositivo** è necessario per eseguire il rendering del contenuto in un'app di Windows Store con [Direct2D](./direct2d-portal.md).

## <a name="why-use-a-device-context-to-render"></a>Perché usare un contesto di dispositivo per il rendering?

-   È possibile eseguire il rendering per le app di Windows Store.
-   È possibile modificare la destinazione di rendering in qualsiasi momento prima, durante e dopo il rendering. Il contesto di dispositivo garantisce che le chiamate ai metodi di disegno vengano eseguite nell'ordine e le applichino quando si passa alla destinazione di rendering.
-   È possibile usare più di un tipo di finestra con un contesto di dispositivo. È possibile usare un [**contesto di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) e [**una catena di scambio DXGI**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) per eseguire il rendering direttamente in [**Windows:: UI:: Core:: COREWINDOW**](/uwp/api/Windows.UI.Core.CoreWindow) o [**Windows:: UI:: XAML:: SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).
-   È possibile usare il [](./direct2d-portal.md) [**contesto di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2d per creare [effetti Direct2D](effects-overview.md) e per eseguire il rendering dell'output di un effetto immagine o di un grafico effetto in una destinazione di rendering.
-   È possibile avere più [**contesti di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), che possono essere utili per migliorare le prestazioni in un'app a thread. Per altre informazioni, vedere [app Direct2D multithread](multi-threaded-direct2d-apps.md) .
-   Il [**contesto di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interagisce strettamente con Direct3D, offrendo maggiore accesso alle opzioni Direct3D.

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a>Come creare un contesto di dispositivo Direct2D per il rendering

Il codice seguente illustra come creare un dispositivo Direct3D11, ottenere il dispositivo DXGI associato, creare un [**dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)e infine creare il [**contesto di periferica**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D per il rendering.

Di seguito è riportato un diagramma delle chiamate al metodo e delle interfacce utilizzate dal codice.

![diagramma dei dispositivi Direct2D e Direct3D e dei contesti di dispositivo.](images/devicecontextdiagram.png)

> [!Note]  
> Questo codice presuppone che sia già presente un oggetto [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) . per altre informazioni, vedere la [**pagina di riferimento di ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).

 


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



Verranno esaminati i passaggi dell'esempio di codice precedente.

1.  Ottenere un puntatore a interfaccia ID3D11Device che sarà necessario per creare il contesto di dispositivo.

    -   Dichiarare i flag di creazione per configurare il dispositivo [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) per il supporto di BGRA. [Direct2D](./direct2d-portal.md) richiede l'ordine di colore BGRA.
    -   Dichiarare una matrice di voci a [**\_ \_ livello di funzionalità D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) che rappresentano il set di livelli di funzionalità che l'app supporterà.
        > [!Note]  
        > [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) Cerca nell'elenco fino a quando non trova il livello di funzionalità supportato dal sistema host.

         

    -   Usare la funzione [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) per creare un oggetto [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) . la funzione restituirà anche un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) , ma tale oggetto non è necessario per questo esempio.

2.  Eseguire una query sul [**dispositivo Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) per la relativa interfaccia del [**dispositivo DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .
3.  Creare un oggetto [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) chiamando il metodo [**ID2D1Factory:: CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) e passando l'oggetto [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .
4.  Creare un puntatore [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) usando il metodo [**ID2D1Device:: CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) .

## <a name="selecting-a-target"></a>Selezione di una destinazione

Il codice seguente illustra come ottenere la [**trama Direct3D a 2 dimensioni**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) per il buffer nascosto della finestra e creare una destinazione bitmap che si collega a questa trama a cui viene eseguito il rendering del [**contesto di dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) .


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



Verranno esaminati i passaggi dell'esempio di codice precedente.

1.  Allocare una struttura [**DESC1 della \_ catena di scambio \_ \_ DXGI**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) e definire le impostazioni per la [**catena di scambio**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).

    Queste impostazioni mostrano un esempio di come creare una catena di scambio che può essere usata da un'app di Windows Store.

2.  Ottenere la scheda in cui è in esecuzione il [**dispositivo Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) e il [**dispositivo DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) e ottenere l'oggetto [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) associato. È necessario usare questa **Factory DXGI** per assicurarsi che la [**catena di scambio**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) venga creata sulla stessa scheda.

3.  Chiamare il metodo [**IDXGIFactory2:: CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) per creare la catena di scambio. Usare la classe [**Windows:: UI:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) per la finestra principale di un'app di Windows Store.

    Assicurarsi di impostare la latenza massima del frame su 1 per ridurre al minimo il consumo di energia elettrica.

    Se si vuole eseguire il rendering del contenuto Direct2D in un'app di Windows Store, vedere il metodo [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) .

4.  Ottenere il buffer nascosto dalla [**catena di scambio**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain). Il buffer nascosto espone un'interfaccia [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) allocata dalla **catena di scambio**

5.  Dichiarare uno struct [**d2d1 \_ bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) e impostare i valori delle proprietà. Impostare il formato pixel su BGRA perché si tratta del formato utilizzato dal dispositivo [**Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) e dal [**dispositivo DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .

6.  Ottenere il buffer nascosto come [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) da passare a Direct2D. Direct2D non accetta direttamente un [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) .

    Creare un oggetto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) dal buffer nascosto usando il metodo [**ID2D1DeviceContext:: CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) .

7.  A questo punto la [**bitmap Direct2D**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) è collegata al buffer nascosto. Impostare la destinazione nel [**contesto di periferica Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) sulla **bitmap**.

## <a name="how-to-render-and-display"></a>Come eseguire il rendering e la visualizzazione

Ora che si dispone di una bitmap di destinazione, è possibile creare primitive, immagini, effetti di immagini e testo utilizzando il [**contesto di periferica Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext). Il codice seguente illustra come creare un rettangolo.


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



Verranno esaminati i passaggi dell'esempio di codice precedente.

1.  Chiamare [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) per creare un pennello per disegnare il rettangolo.
2.  Chiamare il metodo [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) prima di emettere comandi di disegno.
3.  Chiamare il metodo [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) il rettangolo da disegnare e il pennello.
4.  Chiamare il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) dopo aver emesso i comandi di disegno.
5.  Visualizzare il risultato chiamando il metodo [**IDXGISwapChain::P reinviato**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) .

A questo punto è possibile usare il [**contesto di dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) per creare primitive, immagini, effetti di immagini e testo sullo schermo.

 

 