---
title: D2D con D3D11on12
description: L'esempio D3D1211on12 illustra come eseguire il rendering del contenuto di D2D sul contenuto di D3D12 condividendo le risorse tra un dispositivo basato su 11 e un dispositivo basato su 12.
ms.assetid: FAEF1412-053C-4B5F-80FA-85396C2586B4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d18399b85499787f74dab725d562b6a299878b35
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104548907"
---
# <a name="d2d-using-d3d11on12"></a>D2D con D3D11on12

L'esempio **D3D1211on12** illustra come eseguire il rendering del contenuto di D2D sul contenuto di D3D12 condividendo le risorse tra un dispositivo basato su 11 e un dispositivo basato su 12.

-   [Creare un ID3D11On12Device](#create-an-id3d11on12device)
-   [Creare una factory D2D](#create-a-d2d-factory)
-   [Creare una destinazione di rendering per D2D](#create-a-render-target-for-d2d)
-   [Creare oggetti di testo D2D di base](#create-basic-d2d-text-objects)
-   [Aggiornamento del ciclo di rendering principale](#updating-the-main-render-loop)
-   [Eseguire l'esempio](#run-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="create-an-id3d11on12device"></a>Creare un ID3D11On12Device

Il primo passaggio consiste nel creare un [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) dopo la creazione di [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) , che comporta la creazione di un [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) di cui è stato eseguito il WRAPPED intorno al **ID3D12Device** tramite l'API [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice). Questa API accetta anche, tra gli altri parametri, un [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) , in modo che il dispositivo 11On12 possa inviare i propri comandi. Dopo aver creato il **ID3D11Device** , è possibile eseguire una query sull'interfaccia **ID3D11On12Device** . Si tratta dell'oggetto dispositivo primario che verrà usato per configurare D2D.

Nel metodo **LoadPipeline** impostare i dispositivi.

``` syntax
 // Create an 11 device wrapped around the 12 device and share
    // 12's command queue.
    ComPtr<ID3D11Device> d3d11Device;
    ThrowIfFailed(D3D11On12CreateDevice(
        m_d3d12Device.Get(),
        d3d11DeviceFlags,
        nullptr,
        0,
        reinterpret_cast<IUnknown**>(m_commandQueue.GetAddressOf()),
        1,
        0,
        &d3d11Device,
        &m_d3d11DeviceContext,
        nullptr
        ));

    // Query the 11On12 device from the 11 device.
    ThrowIfFailed(d3d11Device.As(&m_d3d11On12Device));
```



| Flusso di chiamate                                              | Parametri |
|--------------------------------------------------------|------------|
| [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device)            |            |
| [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice) |            |



 

## <a name="create-a-d2d-factory"></a>Creare una factory D2D

Ora che si dispone di un dispositivo 11On12, viene usato per creare una factory D2D e un dispositivo Analogamente a quanto normalmente accade con D3D11.

Aggiungere al metodo **LoadAssets** .

``` syntax
 // Create D2D/DWrite components.
    {
        D2D1_DEVICE_CONTEXT_OPTIONS deviceOptions = D2D1_DEVICE_CONTEXT_OPTIONS_NONE;
        ThrowIfFailed(D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, __uuidof(ID2D1Factory3), &d2dFactoryOptions, &m_d2dFactory));
        ComPtr<IDXGIDevice> dxgiDevice;
        ThrowIfFailed(m_d3d11On12Device.As(&dxgiDevice));
        ThrowIfFailed(m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice));
        ThrowIfFailed(m_d2dDevice->CreateDeviceContext(deviceOptions, &m_d2dDeviceContext));
        ThrowIfFailed(DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED, __uuidof(IDWriteFactory), &m_dWriteFactory));
    }
```



| Flusso di chiamate                                                                        | Parametri                                                   |
|----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**\_Opzioni del \_ contesto del dispositivo d2d1 \_**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_device_context_options)     |                                                              |
| [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)                              | [**\_Tipo di Factory d2d1 \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)        |
| [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)                                      |                                                              |
| [**ID2D1Factory3:: CreateDevice**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1factory3-createdevice)           |                                                              |
| [**ID2D1Device::CreateDeviceContext**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) |                                                              |
| [**DWriteCreateFactory**](/windows/desktop/api/dwrite/nf-dwrite-dwritecreatefactory)                       | [**\_tipo di Factory DWrite \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_factory_type) |



 

## <a name="create-a-render-target-for-d2d"></a>Creare una destinazione di rendering per D2D

D3D12 è proprietario della catena di scambio, quindi se si vuole eseguire il rendering nel buffer nascosto usando il dispositivo 11On12 (contenuto D2D), è necessario creare risorse incapsulate di tipo [**ID3D11Resource**](/windows/desktop/api/d3d11/nn-d3d11-id3d11resource) dai buffer back di tipo [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource). Viene collegato il **ID3D12Resource** con un'interfaccia basata su d3d11 in modo da poterlo usare con il dispositivo 11On12. Dopo aver creato una risorsa di cui è stato eseguito il wrapper, è possibile creare una superficie di destinazione di rendering per D2D di cui eseguire il rendering, anche nel metodo **LoadAssets** .

``` syntax
 // Query the desktop's dpi settings, which will be used to create
    // D2D's render targets.
    float dpiX;
    float dpiY;
    m_d2dFactory->GetDesktopDpi(&dpiX, &dpiY);
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = D2D1::BitmapProperties1(
        D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
        D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX,
        dpiY
        );  

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    }
```



<table>
<thead>
<tr class="header">
<th>Flusso di chiamate</th>
<th>Parametri</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi"><strong>ID2D1Factory:: GetDesktopDpi</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1"><strong>D2D1_BITMAP_PROPERTIES1</strong></a></td>
<td><dl><a href="/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-bitmapproperties1"><strong>BitmapProperties1</strong></a><br />
[<strong>D2D1_BITMAP_OPTIONS</strong>] (/Windows/Desktop/API/d2d1_1/ne-d2d1_1-d2d1_bitmap_options)<br />
[<strong>PixelFormat</strong>] (/windows/desktop/api/d2d1helper/nf-d2d1helper-pixelformat)<br />
[<strong>DXGI_FORMAT</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format)<br />
[<strong>D2D1_ALPHA_MODE</strong>] (/Windows/Desktop/API/dcommon/ne-dcommon-d2d1_alpha_mode)<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer"><strong>IDXGISwapChain:: GetBuffer</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview"><strong>CreateRenderTargetView</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11on12/ns-d3d11on12-d3d11_resource_flags"><strong>D3D11_RESOURCE_FLAGS</strong></a></td>
<td><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag"><strong>D3D11_BIND_FLAG</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource"><strong>CreateWrappedResource</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface"><strong>IDXGISurface</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1)"><strong>ID2D1DeviceContext::CreateBitmapFromDxgiSurface</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator"><strong>CreateCommandAllocator</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type"><strong>D3D12_COMMAND_LIST_TYPE</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="create-basic-d2d-text-objects"></a>Creare oggetti di testo D2D di base

A questo punto è disponibile un [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) per eseguire il rendering del contenuto 3D, un [**ID2D1Device**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device) condiviso con i 12 dispositivi tramite un [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) , che è possibile usare per eseguire il rendering del contenuto 2D, e sono entrambi configurati per il rendering nella stessa catena di scambio. Questo esempio usa semplicemente il dispositivo D2D per eseguire il rendering del testo sulla scena 3D, analogamente a come i giochi eseguono il rendering della propria interfaccia utente. A tale proposito, è necessario creare alcuni oggetti D2D di base, ancora nel metodo **LoadAssets** .

``` syntax
 // Create D2D/DWrite objects for rendering text.
    {
        ThrowIfFailed(m_d2dDeviceContext->CreateSolidColorBrush(D2D1::ColorF(D2D1::ColorF::Black), &m_textBrush));
        ThrowIfFailed(m_dWriteFactory->CreateTextFormat(
            L"Verdana",
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            50,
            L"en-us",
            &m_textFormat
            ));
        ThrowIfFailed(m_textFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER));
        ThrowIfFailed(m_textFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER));
    }
```



| Flusso di chiamate                                                                                           | Parametri                                                                 |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush))    | [**ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf)                                              |
| [**IDWriteFactory archiviata nei:: CreateTextFormat**](/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-createtextformat)                 | [**\_Spessore carattere \_ DWrite**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_font_weight)                 |
| [**IDWriteTextFormat:: SetTextAlignment**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)           | [**\_allineamento del testo DWrite \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_text_alignment)           |
| [**IDWriteTextFormat:: SetParagraphAlignment**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) | [**\_Allineamento paragrafo \_ DWrite**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_paragraph_alignment) |



 

## <a name="updating-the-main-render-loop"></a>Aggiornamento del ciclo di rendering principale

Ora che l'inizializzazione dell'esempio è completa, è possibile passare al ciclo di rendering principale.

``` syntax
// Render the scene.
void D3D1211on12::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    RenderUI();

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(0, 0));

    MoveToNextFrame();
}
```



| Flusso di chiamate                                                              | Parametri |
|------------------------------------------------------------------------|------------|
| [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [**Oggetti executecommandlist**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [**IDXGISwapChain1::Present1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

L'unico elemento nuovo del ciclo di rendering è la chiamata **RenderUI** , che userà D2D per eseguire il rendering dell'interfaccia utente. Si noti che vengono eseguiti prima tutti gli elenchi di comandi di D3D12 per eseguire il rendering della scena 3D, quindi viene eseguito il rendering dell'interfaccia utente. Prima di approfondire il **RenderUI**, è necessario esaminare una modifica a **PopulateCommandLists**. In altri esempi, in genere si inserisce una barriera delle risorse nell'elenco dei comandi prima di chiuderla per eseguire la transizione del buffer nascosto dallo stato di destinazione di rendering allo stato attuale. Tuttavia, in questo esempio viene rimossa la barriera delle risorse, perché è ancora necessario eseguire il rendering nei buffer indietro con D2D. Si noti che quando sono state create le risorse sottoposte a incapsulamento del buffer nascosto IN cui è stato specificato lo stato di destinazione di rendering come stato "IN" e lo stato attuale come stato "OUT".

**RenderUI** è relativamente semplice in termini di utilizzo di D2D. La destinazione di rendering è stata impostata ed è stato eseguito il rendering del testo. Tuttavia, prima di usare le risorse incapsulate in un dispositivo 11On12, ad esempio le destinazioni di rendering del buffer nascosto, è necessario chiamare l'API [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) sul dispositivo 11On12. Dopo il rendering viene chiamata l'API [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) nel dispositivo 11On12. La chiamata a **ReleaseWrappedResources** comporta una barriera delle risorse dietro le quinte che eseguirà la transizione della risorsa specificata allo stato "out" specificato al momento della creazione. In questo caso, si tratta dello stato attuale. Infine, per inviare tutti i comandi eseguiti sul dispositivo 11On12 al [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue)condiviso, è necessario chiamare [**Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) sul [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext).

``` syntax
// Render text over D3D12 using D2D via the 11On12 device.
void D3D1211on12::RenderUI()
{
    D2D1_SIZE_F rtSize = m_d2dRenderTargets[m_frameIndex]->GetSize();
    D2D1_RECT_F textRect = D2D1::RectF(0, 0, rtSize.width, rtSize.height);
    static const WCHAR text[] = L"11On12";

    // Acquire our wrapped render target resource for the current back buffer.
    m_d3d11On12Device->AcquireWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Render text directly to the back buffer.
    m_d2dDeviceContext->SetTarget(m_d2dRenderTargets[m_frameIndex].Get());
    m_d2dDeviceContext->BeginDraw();
    m_d2dDeviceContext->SetTransform(D2D1::Matrix3x2F::Identity());
    m_d2dDeviceContext->DrawTextW(
        text,
        _countof(text) - 1,
        m_textFormat.Get(),
        &textRect,
        m_textBrush.Get()
        );
    ThrowIfFailed(m_d2dDeviceContext->EndDraw());

    // Release our wrapped render target resource. Releasing 
    // transitions the back buffer resource to the state specified
    // as the OutState when the wrapped resource was created.
    m_d3d11On12Device->ReleaseWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Flush to submit the 11 command list to the shared command queue.
    m_d3d11DeviceContext->Flush();
}
```



| Flusso di chiamate                                                                                                                                                                                 | Parametri                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [**\_Dimensioni d2d1 \_ F**](/windows/desktop/Direct2D/d2d1-size-f)                                                                                                                                                 |                                       |
| [**D2D1 \_ Rect \_ F**](/windows/desktop/Direct2D/d2d1-rect-f)                                                                                                                                                 | [**RectF**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rectf)           |
| [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)                                                                                                               |                                       |
| [**ID2D1DeviceContext:: setarget**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget)                                                                                                                |                                       |
| [**ID2D1RenderTarget:: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)                                                                                                                  |                                       |
| [**ID2D1RenderTarget:: setransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform)                                                                                                            | [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) |
| [**ID2D1RenderTarget::D rawTextW**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) |                                       |
| [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)                                                                                                                      |                                       |
| [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)                                                                                                               |                                       |
| [**Sul ID3D11DeviceContext:: Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush)                                                                                                                    |                                       |



 

## <a name="run-the-sample"></a>Eseguire l'esempio

![output finale dell'esempio 11 su 12](images/11on12image.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure dettagliate per il codice D3D12](d3d12-code-walk-throughs.md)
</dt> <dt>

[D3D11On12](direct3d-11-on-12.md)
</dt> <dt>

[Interoperabilità di Direct3D 12](direct3d-12-interop.md)
</dt> <dt>

[Riferimento a 11on12](direct3d-11on12-reference.md)
</dt> </dl>

 

 