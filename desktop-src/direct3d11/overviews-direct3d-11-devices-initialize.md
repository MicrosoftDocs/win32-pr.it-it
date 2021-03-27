---
title: Come creare un dispositivo e un contesto immediato
description: Questo argomento illustra come inizializzare un dispositivo.
ms.assetid: 02a20ada-b3aa-435e-8d66-117a19222f9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530f2b9cbc77f5404b4e9e8973d326a8708d6436
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046774"
---
# <a name="how-to-create-a-device-and-immediate-context"></a><span data-ttu-id="3806a-103">Procedura: creare un dispositivo e un contesto immediato</span><span class="sxs-lookup"><span data-stu-id="3806a-103">How To: Create a Device and Immediate Context</span></span>

<span data-ttu-id="3806a-104">Questo argomento illustra come inizializzare un [dispositivo](overviews-direct3d-11-devices-intro.md).</span><span class="sxs-lookup"><span data-stu-id="3806a-104">This topics shows how to initialize a [device](overviews-direct3d-11-devices-intro.md).</span></span> <span data-ttu-id="3806a-105">L'inizializzazione di un [dispositivo](overviews-direct3d-11-devices-intro.md) è una delle prime attività che l'applicazione deve completare prima di poter eseguire il rendering della scena.</span><span class="sxs-lookup"><span data-stu-id="3806a-105">Initializing a [device](overviews-direct3d-11-devices-intro.md) is one of the first tasks that your application must complete before you can render your scene.</span></span>

<span data-ttu-id="3806a-106">**Per creare un dispositivo e un contesto immediato**</span><span class="sxs-lookup"><span data-stu-id="3806a-106">**To create a device and immediate context**</span></span>

<span data-ttu-id="3806a-107">Compilare la struttura [**\_ desc della \_ catena \_ di scambio DXGI**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) con informazioni sui formati e le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="3806a-107">Fill out the [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure with information about buffer formats and dimensions.</span></span> <span data-ttu-id="3806a-108">Per altre informazioni, vedere Creazione di una catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="3806a-108">For more information, see Creating a Swap Chain.</span></span>

<span data-ttu-id="3806a-109">Nell'esempio di codice seguente viene illustrato come compilare la [**struttura \_ \_ \_ desc della catena di scambio DXGI**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) .</span><span class="sxs-lookup"><span data-stu-id="3806a-109">The following code example demonstrates how to fill in the [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure.</span></span>


```
DXGI_SWAP_CHAIN_DESC sd;
ZeroMemory( &sd, sizeof( sd ) );
sd.BufferCount = 1;
sd.BufferDesc.Width = 640;
sd.BufferDesc.Height = 480;
sd.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
sd.BufferDesc.RefreshRate.Numerator = 60;
sd.BufferDesc.RefreshRate.Denominator = 1;
sd.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
sd.OutputWindow = g_hWnd;
sd.SampleDesc.Count = 1;
sd.SampleDesc.Quality = 0;
sd.Windowed = TRUE;
```



<span data-ttu-id="3806a-110">Usando la [**struttura \_ \_ \_ desc della catena di scambio DXGI**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) del passaggio uno, chiamare [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) per inizializzare il dispositivo e la catena di scambio nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="3806a-110">Using the [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure from step one, call [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) to initialize the device and swap chain at the same time.</span></span>


```
D3D_FEATURE_LEVEL  FeatureLevelsRequested = D3D_FEATURE_LEVEL_11_0;
UINT               numLevelsRequested = 1;
D3D_FEATURE_LEVEL  FeatureLevelsSupported;

if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                D3D_DRIVER_TYPE_HARDWARE, 
                NULL, 
                0,
                &FeatureLevelsRequested, 
                numFeatureLevelsRequested, 
                D3D11_SDK_VERSION, 
                &sd, 
                &g_pSwapChain, 
                &g_pd3dDevice, 
                &FeatureLevelsSupported,
                &g_pImmediateContext )))
{
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="3806a-111">Se si richiede un dispositivo di [**\_ \_ livello \_ \_ 1 di funzionalità D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) in un computer con solo il runtime Direct3D 11,0, [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) si chiude immediatamente con **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="3806a-111">If you request a [**D3D\_FEATURE\_LEVEL\_11\_1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) device on a computer with only the Direct3D 11.0 runtime, [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) immediately exits with **E\_INVALIDARG**.</span></span> <span data-ttu-id="3806a-112">Per richiedere in modo sicuro tutti i livelli di funzionalità possibili in un computer con il runtime DirectX 11,0 o DirectX 11,1, usare questo codice:</span><span class="sxs-lookup"><span data-stu-id="3806a-112">To safely request all possible feature levels on a computer with the DirectX 11.0 or DirectX 11.1 runtime, use this code:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>const D3D_FEATURE_LEVEL lvl[] = { D3D_FEATURE_LEVEL_11_1, D3D_FEATURE_LEVEL_11_0,
> D3D_FEATURE_LEVEL_10_1, D3D_FEATURE_LEVEL_10_0,
> D3D_FEATURE_LEVEL_9_3, D3D_FEATURE_LEVEL_9_2, D3D_FEATURE_LEVEL_9_1 };
>
> UINT createDeviceFlags = 0;
> #ifdef _DEBUG
> createDeviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
> #endif
>
> ID3D11Device* device = nullptr;
> HRESULT hr = D3D11CreateDeviceAndSwapChain( nullptr, D3D_DRIVER_TYPE_HARDWARE, nullptr, createDeviceFlags, lvl, _countof(lvl), D3D11_SDK_VERSION, &sd, &g_pSwapChain, &g_pd3ddevice, &FeatureLevelsSupported, &g_pImmediateContext );
> if ( hr == E_INVALIDARG )
> {
>     hr = D3D11CreateDeviceAndSwapChain( nullptr, D3D_DRIVER_TYPE_HARDWARE, nullptr, createDeviceFlags, &lvl[1], _countof(lvl) - 1, D3D11_SDK_VERSION, &sd, &g_pSwapChain, &g_pd3ddevice, &FeatureLevelsSupported, &g_pImmediateContext );
> }
>
> if (FAILED(hr))
>     return hr;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
>  
>
> <span data-ttu-id="3806a-113">Creare una visualizzazione di destinazione del rendering chiamando [**ID3D11Device:: CreateRenderTargetView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview) e associare il buffer nascosto come destinazione di rendering chiamando [**sul ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets).</span><span class="sxs-lookup"><span data-stu-id="3806a-113">Create a render-target view by calling [**ID3D11Device::CreateRenderTargetView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview) and bind the back-buffer as a render target by calling [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets).</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>ID3D11Texture2D* pBackBuffer;
>
> // Get a pointer to the back buffer
> hr = g_pSwapChain->GetBuffer( 0, __uuidof( ID3D11Texture2D ), 
>                              ( LPVOID* )&pBackBuffer );
>
> // Create a render-target view
> g_pd3dDevice->CreateRenderTargetView( pBackBuffer, NULL,
>                                       &g_pRenderTargetView );
>
> // Bind the view
> g_pImmediateContext->OMSetRenderTargets( 1, &g_pRenderTargetView, NULL );</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> <span data-ttu-id="3806a-114">Creare un viewport per definire quali parti della destinazione di rendering saranno visibili.</span><span class="sxs-lookup"><span data-stu-id="3806a-114">Create a viewport to define which parts of the render target will be visible.</span></span> <span data-ttu-id="3806a-115">Definire il viewport usando la struttura del [**\_ viewport d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) e impostare il viewport usando il metodo [**sul ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) .</span><span class="sxs-lookup"><span data-stu-id="3806a-115">Define the viewport using the [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) structure and set the viewport using the [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) method.</span></span>
>
> <span codelanguage="ManagedCPlusPlus"></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <thead>
> <tr class="header">
> <th><span data-ttu-id="3806a-116">C++</span><span class="sxs-lookup"><span data-stu-id="3806a-116">C++</span></span></th>
> </tr>
> </thead>
> <tbody>
> <tr class="odd">
> <td><pre><code>    // Setup the viewport
>     D3D11_VIEWPORT vp;
>     vp.Width = 640;
>     vp.Height = 480;
>     vp.MinDepth = 0.0f;
>     vp.MaxDepth = 1.0f;
>     vp.TopLeftX = 0;
>     vp.TopLeftY = 0;
>     g_pImmediateContext->RSSetViewports( 1, &vp );</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="related-topics"></a><span data-ttu-id="3806a-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3806a-117">Related topics</span></span>
>
> <dl> <dt>

[<span data-ttu-id="3806a-118">Dispositivi</span><span class="sxs-lookup"><span data-stu-id="3806a-118">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="3806a-119">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="3806a-119">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>
>
>  
>
>  
>