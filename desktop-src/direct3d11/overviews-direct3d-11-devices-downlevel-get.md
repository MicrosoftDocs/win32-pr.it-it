---
title: Come ottenere il livello di funzionalità del dispositivo
description: In questo argomento viene illustrato come ottenere il livello di funzionalità massimo supportato da un dispositivo.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e587ad488a84641a92f0058d201014030e3467e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856701"
---
# <a name="how-to-get-the-device-feature-level"></a>Procedura: ottenere il livello di funzionalità del dispositivo

In questo argomento viene illustrato come ottenere il [livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) massimo supportato da un [dispositivo](overviews-direct3d-11-devices-intro.md). I dispositivi Direct3D 11 supportano un set fisso di livelli di funzionalità definiti nell'enumerazione [**del \_ \_ livello di funzionalità D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) . Quando si conosce il [livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) più elevato supportato da un dispositivo, è possibile eseguire i percorsi del codice appropriati per tale dispositivo.

**Per ottenere il livello di funzionalità del dispositivo**

1.  Chiamare la funzione [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o le funzioni [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) specificando **null** per il parametro *ppDevice* . Questa operazione può essere eseguita prima della creazione del dispositivo.

    \- - oppure -

    Chiamare [**ID3D11Device:: GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) dopo la creazione del dispositivo.

2.  Esaminare il valore dell'enumerazione del [**\_ \_ livello di funzionalità D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) restituito dall'ultimo passaggio per determinare il livello di funzionalità supportato.

Nell'esempio di codice seguente viene illustrato come determinare il livello di funzionalità massimo supportato chiamando la funzione [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) . **D3D11CreateDevice** archivia il livello di funzionalità massimo supportato nella variabile FeatureLevel. È possibile utilizzare questo codice per esaminare il valore del tipo enumerato del [**\_ \_ livello di funzionalità D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) restituito da **D3D11CreateDevice** . Si noti che questo codice elenca tutti i livelli di funzionalità in modo esplicito (per Direct3D 11,1 e Direct3D 11,2).

> [!Note]  
> Se il runtime Direct3D 11,1 è presente nel computer e *pFeatureLevels* è impostato su **null**, questa funzione non creerà un dispositivo [**D3D a \_ livello di funzionalità \_ \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) . Per creare un dispositivo **D3D a \_ livello di funzionalità \_ \_ 11 \_ 1** , è necessario specificare in modo esplicito una matrice a **\_ \_ livello di funzionalità D3D** che includa il **livello di \_ funzionalità D3D \_ \_ 11 \_ 1**. Se si specifica una matrice a **\_ \_ livello di funzionalità D3D** che contiene il **livello di \_ funzionalità D3D \_ \_ 11 \_ 1** in un computer in cui non è installato il runtime Direct3D 11,1, questa funzione non riesce immediatamente con E \_ INVALIDARG.

 


```C++
HRESULT hr = E_FAIL;
D3D_FEATURE_LEVEL MaxSupportedFeatureLevel = D3D_FEATURE_LEVEL_9_1;
D3D_FEATURE_LEVEL FeatureLevels[] = {
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1
    };

hr = D3D11CreateDevice(
    NULL,
    D3D_DRIVER_TYPE_HARDWARE,
    NULL, 
    0, 
    &FeatureLevels, 
    ARRAYSIZE(FeatureLevels), 
    D3D11_SDK_VERSION, 
    NULL, 
    &MaxSupportedFeatureLevel, 
    NULL 
    );

if(FAILED(hr))
{
    return hr;
}
```



Nella sezione di [riferimento 10Level9](d3d11-graphics-reference-10level9.md) sono elencate le differenze tra il comportamento di diversi metodi [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) a diversi livelli di funzionalità di 10Level9.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direct3D 11 su hardware di livello inferiore](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




