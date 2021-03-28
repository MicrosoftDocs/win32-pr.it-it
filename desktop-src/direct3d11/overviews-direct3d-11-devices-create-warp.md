---
title: Come creare un dispositivo WARP
description: In questo argomento viene illustrato come creare un dispositivo WARP che implementa un'unità di rasterizzazione software ad alta velocità.
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deda409971d22f46132a1cb9b008d3dd1eb7c407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993485"
---
# <a name="how-to-create-a-warp-device"></a><span data-ttu-id="9685d-103">Procedura: creare un dispositivo WARP</span><span class="sxs-lookup"><span data-stu-id="9685d-103">How To: Create a WARP Device</span></span>

<span data-ttu-id="9685d-104">In questo argomento viene illustrato come creare un dispositivo WARP che implementa un'unità di rasterizzazione software ad alta velocità.</span><span class="sxs-lookup"><span data-stu-id="9685d-104">This topic shows how to create a WARP device that implements a high speed software rasterizer.</span></span> <span data-ttu-id="9685d-105">Per creare un dispositivo WARP, è sufficiente specificare che il dispositivo che si sta creando utilizzerà un driver WARP.</span><span class="sxs-lookup"><span data-stu-id="9685d-105">To create a WARP device, simply specify that the device you are creating will use a WARP driver.</span></span> <span data-ttu-id="9685d-106">Questo esempio crea un dispositivo e una catena di scambio nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="9685d-106">This example creates a device and a swap chain at the same time.</span></span>

<span data-ttu-id="9685d-107">**Per creare un dispositivo WARP**</span><span class="sxs-lookup"><span data-stu-id="9685d-107">**To create a WARP device**</span></span>

1.  <span data-ttu-id="9685d-108">Definire i parametri iniziali per una catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="9685d-108">Define initial parameters for a swap chain.</span></span>
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

    

2.  <span data-ttu-id="9685d-109">Richiedere un livello di funzionalità che implementi le funzionalità necessarie per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9685d-109">Request a feature level that implements the features your application will need.</span></span> <span data-ttu-id="9685d-110">È possibile creare un dispositivo a curva per i livelli di funzionalità **D3D \_ \_ livello \_ 9 \_ 1** tramite il **livello di \_ funzionalità D3D \_ \_ 10 \_ 1** e a partire da Windows 8 per tutti i livelli di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="9685d-110">A WARP device can be successfully created for feature levels **D3D\_FEATURE\_LEVEL\_9\_1** through **D3D\_FEATURE\_LEVEL\_10\_1** and starting with Windows 8 for all feature levels.</span></span>

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    <span data-ttu-id="9685d-111">Per altre informazioni sui livelli di funzionalità, vedere Enumerazione del [**\_ \_ livello di funzionalità D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="9685d-111">See more about feature levels in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span>

3.  <span data-ttu-id="9685d-112">Creare il dispositivo chiamando [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="9685d-112">Create the device by calling [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>


```
    HRESULT hr = S_OK;
    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_WARP,
                    NULL, 
                    0,
                    &FeatureLevels, 
                    1, 
                    D3D11_SDK_VERSION, 
                    &sd, 
                    &g_pSwapChain, 
                    &g_pd3dDevice, 
                    &FeatureLevel,
                    &g_pImmediateContext )))
    {
        return hr;
    }
```



<span data-ttu-id="9685d-113">Sarà necessario fornire la chiamata API con il tipo di driver WARP dall'enumerazione del [**\_ \_ tipo di driver D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="9685d-113">You will need to supply the API call with the WARP driver type from the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) enumeration.</span></span> <span data-ttu-id="9685d-114">Una volta che il metodo ha esito positivo, restituirà un'interfaccia della catena di scambio, un'interfaccia del dispositivo, un puntatore al livello di funzionalità concesso dal driver e un'interfaccia di contesto immediata.</span><span class="sxs-lookup"><span data-stu-id="9685d-114">After the method succeeds, it will return a swap chain interface, a device interface, a pointer to the feature level that was granted by the driver, and an immediate context interface.</span></span>

<span data-ttu-id="9685d-115">Per informazioni sulle limitazioni della creazione di un dispositivo WARP a determinati livelli di funzionalità, vedere [limitazioni della creazione di dispositivi Warp e Reference](overviews-direct3d-11-devices-limitations.md).</span><span class="sxs-lookup"><span data-stu-id="9685d-115">For information about limitations creating a WARP device on certain feature levels, see [Limitations Creating WARP and Reference Devices](overviews-direct3d-11-devices-limitations.md).</span></span>

## <a name="new-for-windows-8"></a><span data-ttu-id="9685d-116">Novità per Windows 8</span><span class="sxs-lookup"><span data-stu-id="9685d-116">New for Windows 8</span></span>

<span data-ttu-id="9685d-117">Quando la scheda di visualizzazione principale di un computer è "Microsoft Basic Display Adapter" (scheda WARP), il computer dispone anche di un secondo adapter.</span><span class="sxs-lookup"><span data-stu-id="9685d-117">When a computer's primary display adapter is the "Microsoft Basic Display Adapter" (WARP adapter), that computer also has a second adapter.</span></span> <span data-ttu-id="9685d-118">Questa seconda scheda è il dispositivo solo di rendering senza output di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9685d-118">This second adapter is the render-only device that has no display outputs.</span></span> <span data-ttu-id="9685d-119">Per ulteriori informazioni sul dispositivo di solo rendering, vedere la pagina relativa alle [nuove informazioni in Windows 8 sull'enumerazione degli adapter](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).</span><span class="sxs-lookup"><span data-stu-id="9685d-119">For more info about the render-only device, see [new info in Windows 8 about enumerating adapters](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9685d-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9685d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9685d-121">Dispositivi</span><span class="sxs-lookup"><span data-stu-id="9685d-121">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="9685d-122">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="9685d-122">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 