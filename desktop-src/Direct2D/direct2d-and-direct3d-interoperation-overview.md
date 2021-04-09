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
# <a name="direct2d-and-direct3d-interoperability-overview"></a>Panoramica sull'interoperabilità tra Direct2D e Direct3D

I grafici 2D e 3D con accelerazione hardware diventano sempre più una parte delle applicazioni non di gioco e la maggior parte delle applicazioni di gioco usa la grafica 2D sotto forma di menu e Heads-Up Visualizza (HUDs). È possibile aggiungere un numero elevato di valori, consentendo il rendering tradizionale 2D da combinare con il rendering Direct3D in modo efficiente.

Questo argomento descrive come integrare la grafica 2D e 3D tramite Direct2D e [Direct3D](../graphics-and-multimedia.md).

Include le sezioni seguenti:

-   [Prerequisiti](#prerequisites)
-   [Versioni Direct3D supportate](#supported-direct3d-versions)
-   [Interoperabilità tramite DXGI](#interoperability-through-dxgi)
-   [Scrittura in una superficie Direct3D con una destinazione di rendering della superficie DXGI](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [Creazione di una superficie DXGI](#creating-a-dxgi-surface)
-   [Scrittura di contenuto Direct2D in un buffer della catena di scambio](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [Esempio: creare uno sfondo 2D](#example-draw-a-2-d-background)
-   [Uso del contenuto Direct2D come trama](#using-direct2d-content-as-a-texture)
    -   [Esempio: usare il contenuto Direct2D come trama](#example-use-direct2d-content-as-a-texture)
-   [Ridimensionamento di una destinazione di rendering della superficie DXGI](#resizing-a-dxgi-surface-render-target)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

In questa panoramica si presuppone che l'utente abbia familiarità con le operazioni di disegno Direct2D di base. Per un'esercitazione, vedere la [Guida introduttiva di Direct2D](direct2d-quickstart.md). Si presuppone anche che sia possibile programmare usando [Direct3D 10,1](/windows/desktop/direct3d10/d3d10-graphics).

## <a name="supported-direct3d-versions"></a>Versioni Direct3D supportate

Con DirectX 11,0, Direct2D supporta l'interoperabilità solo con i dispositivi Direct3D 10,1. Con DirectX 11,1 o versioni successive, Direct2D supporta anche l'interoperabilità con Direct3D 11.

## <a name="interoperability-through-dxgi"></a>Interoperabilità tramite DXGI

A partire da Direct3D 10, il runtime Direct3D usa [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) per la gestione delle risorse. Il livello di runtime di DXGI fornisce la condivisione tra processi delle superfici di memoria video e funge da base per altre piattaforme di runtime basate sulla memoria video. Direct2D utilizza DXGI per interagire con Direct3D.

Sono disponibili due metodi principali per utilizzare Direct2D e Direct3D insieme:

-   È possibile scrivere contenuto Direct2D in una superficie Direct3D ottenendo un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) e usandolo con [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per creare un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). È quindi possibile utilizzare la destinazione di rendering per aggiungere un'interfaccia bidimensionale o uno sfondo a elementi grafici tridimensionali oppure utilizzare un disegno Direct2D come trama per un oggetto tridimensionale.
-   Usando [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) per creare un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) da un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), è possibile scrivere una scena Direct3D in una bitmap ed eseguirne il rendering con Direct2D.

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a>Scrittura in una superficie Direct3D con una destinazione di rendering della superficie DXGI

Per scrivere in una superficie Direct3D, ottenere un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) e passarlo al metodo [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per creare una destinazione di rendering della superficie di dxgi. È quindi possibile usare la destinazione di rendering della superficie di DXGI per disegnare contenuto 2D sulla superficie DXGI.

Una destinazione di rendering della superficie di DXGI è un tipo di [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). Analogamente ad altre destinazioni di rendering Direct2D, è possibile usarlo per creare risorse ed emettere comandi di disegno.

La destinazione di rendering della superficie DXGI e la superficie DXGI devono usare lo stesso formato DXGI. Se si specifica il formato [**DXGI \_ Format \_ sconosciuto**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) quando si crea la destinazione di rendering, verrà usato automaticamente il formato della superficie.

La destinazione di rendering della superficie di DXGI non esegue la sincronizzazione della superficie di DXGI.

### <a name="creating-a-dxgi-surface"></a>Creazione di una superficie DXGI

Con Direct3D 10, è possibile ottenere una superficie DXGI in diversi modi. È possibile creare un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) per un dispositivo, quindi usare il metodo [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) della catena di scambio per ottenere una superficie DXGI. In alternativa, è possibile usare un dispositivo per creare una trama, quindi usare tale trama come superficie DXGI.

Indipendentemente dalla modalità di creazione della superficie DXGI, è necessario che la superficie utilizzi uno dei formati DXGI supportati dalle destinazioni di rendering della superficie di DXGI. Per un elenco, vedere [formati di pixel supportati e modalità Alpha](supported-pixel-formats-and-alpha-modes.md).

Inoltre, i [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associati alla superficie DXGI devono supportare i formati BGRA DXGI per la superficie per l'utilizzo di Direct2D. Per garantire questo supporto, usare il flag di [**\_ supporto D3D10 create \_ Device \_ BGRA \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) quando si chiama il metodo [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) per creare il dispositivo.

Nel codice seguente viene definito un metodo che crea un [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1). Consente di selezionare il livello di funzionalità migliore disponibile e di eseguire il fallback a [Windows Advanced rasterizzation Platform (Warp)](./installing-the-direct2d-debug-layer.md) quando il rendering hardware non è disponibile.


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



Nell'esempio di codice successivo viene usato il `CreateD3DDevice` metodo illustrato nell'esempio precedente per creare un dispositivo Direct3D in grado di creare superfici DXGI per l'uso con Direct2D.


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

Il modo più semplice per aggiungere contenuto Direct2D a una scena Direct3D consiste nell'usare il metodo [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) di un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) per ottenere una superficie DXGI, quindi usare la superficie con il metodo [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per creare un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) con cui creare il contenuto 2D.

Questo approccio non esegue il rendering del contenuto in tre dimensioni. non avrà prospettive o profondità. Tuttavia, è utile per diverse attività comuni:

-   Creazione di uno sfondo 2D per una scena 3D.
-   Creazione di un'interfaccia 2D davanti a una scena 3D.
-   Uso del multicampionamento Direct3D durante il rendering del contenuto Direct2D.

Nella sezione successiva viene illustrato come creare uno sfondo 2D per una scena 3D.

### <a name="example-draw-a-2-d-background"></a>Esempio: creare uno sfondo 2D

I passaggi seguenti descrivono come creare una destinazione di rendering della superficie di DXGI e usarla per disegnare uno sfondo sfumato.

1.  Usare il metodo [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) per creare una catena di scambio per un [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (variabile *m \_ PDEVICE* ). La catena di scambio usa il formato [**DXGI \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, uno dei formati DXGI supportati da Direct2D.

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

    

2.  Usare il metodo [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) della catena di scambio per ottenere una superficie DXGI.

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  Utilizzare la superficie DXGI per creare una destinazione di rendering DXGI.
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



    

4.  Utilizzare la destinazione di rendering per disegnare uno sfondo sfumato.

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

Un altro modo per usare il contenuto Direct2D con Direct3D consiste nell'usare Direct2D per generare una trama 2D, quindi applicare tale trama a un modello 3D. A tale scopo, creare un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), ottenere una superficie DXGI dalla trama e quindi usare la superficie per creare una destinazione di rendering della superficie di dxgi. Per la superficie **ID3D10Texture2D** è necessario usare il flag di binding della [**destinazione di \_ \_ rendering \_ D3D10 bind**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) e usare un formato DXGI supportato dalle destinazioni di rendering della superficie DXGI. Per un elenco dei formati DXGI supportati, vedere [formati di pixel supportati e modalità Alpha](supported-pixel-formats-and-alpha-modes.md).

### <a name="example-use-direct2d-content-as-a-texture"></a>Esempio: usare il contenuto Direct2D come trama

Gli esempi seguenti illustrano come creare una destinazione di rendering della superficie DXGI che esegue il rendering in una trama 2D, rappresentata da un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d).

1.  Per prima cosa, usare un dispositivo Direct3D per creare una trama 2D. La trama usa i flag di associazione della [**\_ \_ \_ destinazione di rendering D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) e **D3D10 \_ Bind \_ shader \_** e usa il formato [**DXGI \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, uno dei formati DXGI supportati da Direct2D.

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



    

3.  Utilizzare la superficie con il metodo [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per ottenere una destinazione di rendering Direct2D.

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



    

Ora che è stata ottenuta una destinazione di rendering Direct2D e che è stata associata a una trama Direct3D, è possibile usare la destinazione di rendering per disegnare contenuto Direct2D in tale trama ed è possibile applicare tale trama alle primitive Direct3D.

Il codice viene omesso da questo esempio.

## <a name="resizing-a-dxgi-surface-render-target"></a>Ridimensionamento di una destinazione di rendering della superficie DXGI

Le destinazioni di rendering della superficie di DXGI non supportano il metodo [**ID2D1RenderTarget:: Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) . Per ridimensionare una destinazione di rendering della superficie di DXGI, l'applicazione deve rilasciare e ricrearla.

Questa operazione può causare problemi di prestazioni. La destinazione di rendering può essere l'ultima risorsa Direct2D attiva che mantiene un riferimento a [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associato alla superficie DXGI della destinazione di rendering. Se l'applicazione rilascia la destinazione di rendering e il riferimento **ID3D10Device1** viene eliminato definitivamente, è necessario ricrearne uno nuovo.

È possibile evitare questa operazione potenzialmente costosa mantenendo almeno una risorsa Direct2D creata dalla destinazione di rendering mentre si ricrea la destinazione di rendering. Di seguito sono riportate alcune risorse Direct2D che funzionano per questo approccio:

-   [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (che può essere mantenuto indirettamente da un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

Per gestire questo approccio, il metodo di ridimensionamento deve verificare se il dispositivo Direct3D è disponibile. Se è disponibile, rilasciare e ricreare le destinazioni di rendering della superficie di DXGI, mantenendo tutte le risorse create in precedenza e riutilizzarle. Questa operazione funziona perché, come descritto nella [Panoramica delle risorse](resources-and-resource-domains.md), le risorse create da due destinazioni di rendering sono compatibili quando entrambe le destinazioni di rendering sono associate allo stesso dispositivo Direct3D.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formati pixel e modalità alfa supportati](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))
</dt> <dt>

[Grafica di Windows DirectX](../graphics-and-multimedia.md)
</dt> </dl>

 

 