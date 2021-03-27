---
title: Come creare un dispositivo di riferimento
description: In questo argomento viene illustrato come creare un dispositivo di riferimento che implementa un'implementazione software altamente accurata del runtime.
ms.assetid: 00d3f5f2-02c6-4ff4-82a9-0726ad4a8cb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dec5f3834bf1f10027da2a3f3a8e22acdee742b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396558"
---
# <a name="how-to-create-a-reference-device"></a>Procedura: creare un dispositivo di riferimento

In questo argomento viene illustrato come creare un dispositivo di riferimento che implementa un'implementazione software altamente accurata del runtime. Per creare un dispositivo di riferimento, è sufficiente specificare che il dispositivo che si sta creando utilizzerà un driver di riferimento. Questo esempio crea un dispositivo e una catena di scambio nello stesso momento.

**Per creare un dispositivo di riferimento**

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

    

2.  Richiedere un livello di funzionalità che implementi le funzionalità necessarie per l'applicazione. È possibile creare un dispositivo di riferimento per il runtime di Direct3D 11.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_11_0;
    ```

    

    Per altre informazioni sui livelli di funzionalità, vedere Enumerazione del [**\_ \_ livello di funzionalità D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .

3.  Creare il dispositivo chiamando [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).


```
    HRESULT hr = S_OK;
    D3D_FEATURE_LEVEL FeatureLevel;

    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_REFERENCE,
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



È necessario fornire la chiamata API con il tipo di driver di riferimento dall'enumerazione [**del \_ \_ tipo di driver D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) . Una volta che il metodo ha esito positivo, restituirà un'interfaccia della catena di scambio, un'interfaccia del dispositivo, un puntatore al livello di funzionalità concesso dal driver e un'interfaccia di contesto immediata.

Per informazioni sulle limitazioni della creazione di un dispositivo di riferimento a determinati livelli di funzionalità, vedere [limitazioni della creazione di dispositivi Warp e Reference](overviews-direct3d-11-devices-limitations.md). [Come usare Direct3D 11](how-to-use-direct3d-11.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




