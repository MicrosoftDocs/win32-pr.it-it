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
# <a name="how-to-create-a-warp-device"></a>Procedura: creare un dispositivo WARP

In questo argomento viene illustrato come creare un dispositivo WARP che implementa un'unità di rasterizzazione software ad alta velocità. Per creare un dispositivo WARP, è sufficiente specificare che il dispositivo che si sta creando utilizzerà un driver WARP. Questo esempio crea un dispositivo e una catena di scambio nello stesso momento.

**Per creare un dispositivo WARP**

1.  Definire i parametri iniziali per una catena di scambio.
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

    

2.  Richiedere un livello di funzionalità che implementi le funzionalità necessarie per l'applicazione. È possibile creare un dispositivo a curva per i livelli di funzionalità **D3D \_ \_ livello \_ 9 \_ 1** tramite il **livello di \_ funzionalità D3D \_ \_ 10 \_ 1** e a partire da Windows 8 per tutti i livelli di funzionalità.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    Per altre informazioni sui livelli di funzionalità, vedere Enumerazione del [**\_ \_ livello di funzionalità D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .

3.  Creare il dispositivo chiamando [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).


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



Sarà necessario fornire la chiamata API con il tipo di driver WARP dall'enumerazione del [**\_ \_ tipo di driver D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) . Una volta che il metodo ha esito positivo, restituirà un'interfaccia della catena di scambio, un'interfaccia del dispositivo, un puntatore al livello di funzionalità concesso dal driver e un'interfaccia di contesto immediata.

Per informazioni sulle limitazioni della creazione di un dispositivo WARP a determinati livelli di funzionalità, vedere [limitazioni della creazione di dispositivi Warp e Reference](overviews-direct3d-11-devices-limitations.md).

## <a name="new-for-windows-8"></a>Novità per Windows 8

Quando la scheda di visualizzazione principale di un computer è "Microsoft Basic Display Adapter" (scheda WARP), il computer dispone anche di un secondo adapter. Questa seconda scheda è il dispositivo solo di rendering senza output di visualizzazione. Per ulteriori informazioni sul dispositivo di solo rendering, vedere la pagina relativa alle [nuove informazioni in Windows 8 sull'enumerazione degli adapter](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 