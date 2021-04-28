---
title: Panoramica sull'interoperabilità tra Direct2D e Direct3D
description: Panoramica sull'interoperabilità tra Direct2D e Direct3D
ms.assetid: 27680714-dc68-44eb-ab16-2cae3529b352
keywords:
- Interoperabilità Direct2D,Direct3D
- Direct2D, interoperabilità
- interoperabilità, Direct2D
- interoperabilità, Direct3D
- Direct3D, interoperabilità
- Interoperabilità Direct3D,Direct2D
- Direct2D, DXGI
- DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cf7cfa41c3decc964492258dad9c6a3a497f504b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089189"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a>Panoramica sull'interoperabilità tra Direct2D e Direct3D

La grafica 2D e 3D accelerata dall'hardware sta diventando sempre più una parte delle applicazioni non di gioco e la maggior parte delle applicazioni di gioco usa la grafica 2D sotto forma di menu e display Heads-Up (HUD). È possibile aggiungere molti valori abilitando il rendering 2D tradizionale in modo efficiente con il rendering Direct3D.

Questo argomento descrive come integrare grafica 2D e 3D usando Direct2D [e Direct3D.](../graphics-and-multimedia.md)

Include le sezioni seguenti:

-   [Prerequisiti](#prerequisites)
-   [Versioni direct3D supportate](#supported-direct3d-versions)
-   [Interoperabilità tramite DXGI](#interoperability-through-dxgi)
-   [Scrittura in una superficie Direct3D con una destinazione di rendering della superficie DXGI](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [Creazione di una superficie DXGI](#creating-a-dxgi-surface)
-   [Scrittura di contenuto Direct2D in un buffer della catena di scambio](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [Esempio: Disegnare uno sfondo 2D](#example-draw-a-2-d-background)
-   [Uso del contenuto Direct2D come trama](#using-direct2d-content-as-a-texture)
    -   [Esempio: Usare contenuto Direct2D come trama](#example-use-direct2d-content-as-a-texture)
-   [Ridimensionamento di una destinazione di rendering della superficie DXGI](#resizing-a-dxgi-surface-render-target)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Questa panoramica presuppone che si abbia familiarità con le operazioni di disegno Direct2D di base. Per un'esercitazione, vedere [l'avvio rapido di Direct2D.](direct2d-quickstart.md) Presuppone anche che sia possibile programmare usando [Direct3D 10.1.](/windows/desktop/direct3d10/d3d10-graphics)

## <a name="supported-direct3d-versions"></a>Versioni di Direct3D supportate

Con DirectX 11.0, Direct2D supporta solo l'interoperabilità con i dispositivi Direct3D 10.1. Con DirectX 11.1 o versione successiva, Direct2D supporta anche l'interoperabilità con Direct3D 11.

## <a name="interoperability-through-dxgi"></a>Interoperabilità tramite DXGI

A data di Direct3D 10, il runtime Direct3D usa [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) per la gestione delle risorse. Il livello di runtime DXGI offre la condivisione tra processi delle superfici di memoria video e funge da base per altre piattaforme di runtime basate sulla memoria video. Direct2D usa DXGI per interagire con Direct3D.

Esistono due modi principali per usare Direct2D e Direct3D insieme:

-   È possibile scrivere contenuto Direct2D in una superficie Direct3D ottenendo un [**oggetto IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) e usandolo con [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per creare un [**ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) È quindi possibile usare la destinazione di rendering per aggiungere un'interfaccia bidimensionale o uno sfondo a grafica tridimensionale oppure usare un disegno Direct2D come trama per un oggetto tridimensionale.
-   Usando [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) per creare un oggetto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) da [**idXGISurface,**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface)è possibile scrivere una scena Direct3D in una bitmap ed eseguirne il rendering con Direct2D.

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a>Scrittura in una superficie Direct3D con una destinazione di rendering della superficie DXGI

Per scrivere in una superficie Direct3D, ottenere un [**oggetto IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) e passarlo al [**metodo CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per creare una destinazione di rendering della superficie DXGI. È quindi possibile usare la destinazione di rendering della superficie DXGI per disegnare contenuto 2D sulla superficie DXGI.

Una destinazione di rendering della superficie DXGI è un tipo [**di ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Come altre destinazioni di rendering Direct2D, è possibile usarla per creare risorse ed eseguire comandi di disegno.

La destinazione di rendering della superficie DXGI e la superficie DXGI devono usare lo stesso formato DXGI. Se si specifica il [**formato DXGI \_ FORMAT \_ UNKOWN**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) quando si crea la destinazione di rendering, verrà automaticamente utilizzato il formato della superficie.

La destinazione di rendering della superficie DXGI non esegue la sincronizzazione della superficie DXGI.

### <a name="creating-a-dxgi-surface"></a>Creazione di una superficie DXGI

Con Direct3D 10 è possibile ottenere una superficie DXGI in diversi modi. È possibile creare un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) per un dispositivo, quindi usare il metodo [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) della catena di scambio per ottenere una superficie DXGI. In caso contrario, è possibile usare un dispositivo per creare una trama e quindi usarla come superficie DXGI.

Indipendentemente dalla modalità di creazione della superficie DXGI, la superficie deve usare uno dei formati DXGI supportati dalle destinazioni di rendering della superficie DXGI. Per un elenco, vedere [Formati di pixel supportati e Modalità alfa](supported-pixel-formats-and-alpha-modes.md).

Inoltre, [**il dispositivo ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associato alla superficie DXGI deve supportare i formati DXGI BGRA perché la superficie funzioni con Direct2D. Per garantire questo supporto, usare il flag [**D3D10 \_ CREATE \_ DEVICE \_ BGRA \_ SUPPORT**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) quando si chiama il metodo [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) per creare il dispositivo.

Il codice seguente definisce un metodo che crea un [**ID3D10Device1.**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) Seleziona il livello di funzionalità migliore disponibile ed esegue il rollback a [Windows Advanced Rasterization Platform (WARP)](./installing-the-direct2d-debug-layer.md) quando il rendering hardware non è disponibile.


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



L'esempio di codice successivo usa il metodo illustrato nell'esempio precedente per creare un dispositivo Direct3D in grado di creare superfici DXGI da usare `CreateD3DDevice` con Direct2D.


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



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a>Scrittura di contenuto Direct2D in un buffer della catena di scambio

Il modo più semplice per aggiungere contenuto Direct2D a una scena Direct3D è usare il metodo [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) di [**idXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) per ottenere una superficie DXGI, quindi usare la superficie con il [**metodo CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per creare un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) con cui disegnare il contenuto 2D.

Questo approccio non esegue il rendering del contenuto in tre dimensioni. non avrà prospettiva o profondità. Tuttavia, è utile per diverse attività comuni:

-   Creazione di uno sfondo 2D per una scena 3D.
-   Creazione di un'interfaccia 2D davanti a una scena 3D.
-   Uso del multicampionamento Direct3D durante il rendering del contenuto Direct2D.

La sezione successiva illustra come creare uno sfondo 2D per una scena 3D.

### <a name="example-draw-a-2-d-background"></a>Esempio: Disegnare uno sfondo 2D

La procedura seguente descrive come creare una destinazione di rendering della superficie DXGI e usarla per disegnare uno sfondo sfumato.

1.  Usare il [**metodo CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) per creare una catena di scambio per [**id3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) *(variabile \_ m pDevice).* La catena di scambio usa il formato [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, uno dei formati DXGI supportati da Direct2D.

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

    

2.  Usare il metodo [**GetBuffer della**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) catena di scambio per ottenere una superficie DXGI.

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  Usare la superficie DXGI per creare una destinazione di rendering DXGI.
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



    

4.  Usare la destinazione di rendering per disegnare uno sfondo sfumato.

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



    

Il codice viene omesso da questo esempio.

## <a name="using-direct2d-content-as-a-texture"></a>Uso del contenuto Direct2D come trama

Un altro modo per usare il contenuto Direct2D con Direct3D consiste nell'usare Direct2D per generare una trama 2D e quindi applicare tale trama a un modello 3D. A tale scopo, creare un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), ottenere una superficie DXGI dalla trama e quindi usare la superficie per creare una destinazione di rendering della superficie DXGI. La superficie **ID3D10Texture2D** deve usare il flag di associazione [**D3D10 \_ BIND RENDER \_ \_ TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) e usare un formato DXGI supportato dalle destinazioni di rendering della superficie DXGI. Per un elenco dei formati DXGI supportati, vedere [Formati di pixel supportati e modalità alfa](supported-pixel-formats-and-alpha-modes.md).

### <a name="example-use-direct2d-content-as-a-texture"></a>Esempio: Usare contenuto Direct2D come trama

Gli esempi seguenti illustrano come creare una destinazione di rendering della superficie DXGI che esegue il rendering su una trama 2D (rappresentata da [**id3D10Texture2D).**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)

1.  Per prima cosa, usare un dispositivo Direct3D per creare una trama 2D. La trama usa i flag di associazione [**D3D10 \_ BIND \_ RENDER \_ TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) e **D3D10 \_ BIND SHADER \_ \_ RESOURCE** e usa il formato [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, uno dei formati DXGI supportati da Direct2D.

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

    

2.  Usare la trama per ottenere una superficie DXGI.

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  Usare la superficie con il [**metodo CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per ottenere una destinazione di rendering Direct2D.

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



    

Ora che è stata ottenuta una destinazione di rendering Direct2D e la si è associata a una trama Direct3D, è possibile usare la destinazione di rendering per disegnare contenuto Direct2D a tale trama ed è possibile applicare tale trama alle primitive Direct3D.

Il codice viene omesso da questo esempio.

## <a name="resizing-a-dxgi-surface-render-target"></a>Ridimensionamento di una destinazione di rendering della superficie DXGI

Le destinazioni di rendering della superficie DXGI non supportano il [**metodo ID2D1RenderTarget::Resize.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) Per ridimensionare una destinazione di rendering della superficie DXGI, l'applicazione deve rilasciarla e crearla nuovamente.

Questa operazione può potenzialmente creare problemi di prestazioni. La destinazione di rendering potrebbe essere l'ultima risorsa Direct2D attiva che mantiene un riferimento [**all'ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associato alla superficie DXGI della destinazione di rendering. Se l'applicazione rilascia la destinazione di rendering e il riferimento **ID3D10Device1** viene eliminato, è necessario ricreare una nuova destinazione.

È possibile evitare questa operazione potenzialmente dispendiosa mantenendo almeno una risorsa Direct2D creata dalla destinazione di rendering mentre si rieseguono le operazioni di creazione della destinazione di rendering. Di seguito sono riportate alcune risorse Direct2D che funzionano per questo approccio:

-   [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (che può essere mantenuto indirettamente da [**un oggetto ID2D1BitmapBrush)**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

Per supportare questo approccio, il metodo di ridimensionamento deve verificare se il dispositivo Direct3D è disponibile. Se è disponibile, rilasciare e creare nuovamente le destinazioni di rendering della superficie DXGI, ma mantenere tutte le risorse create in precedenza e riutilizzarle. Ciò funziona perché, come descritto in Panoramica delle [risorse,](resources-and-resource-domains.md)le risorse create da due destinazioni di rendering sono compatibili quando entrambe le destinazioni di rendering sono associate allo stesso dispositivo Direct3D.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formati pixel e modalità alfa supportati](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))
</dt> <dt>

[Grafica DirectX di Windows](../graphics-and-multimedia.md)
</dt> </dl>

 

 
