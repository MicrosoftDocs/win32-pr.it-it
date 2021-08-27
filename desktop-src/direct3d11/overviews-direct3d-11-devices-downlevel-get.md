---
title: Come ottenere il livello di funzionalità del dispositivo
description: Questo argomento illustra come ottenere il livello di funzionalità più elevato supportato da un dispositivo.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac21d00aeef8ae6c82ffd9f55a40415b6af1d0a780cc6878d8c30bf453457eb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119601"
---
# <a name="how-to-get-the-device-feature-level"></a>Procedura: Ottenere il livello di funzionalità del dispositivo

In questo argomento viene illustrato come ottenere il livello [di funzionalità più elevato](overviews-direct3d-11-devices-downlevel-intro.md) supportato da un [dispositivo](overviews-direct3d-11-devices-intro.md). I dispositivi Direct3D 11 supportano un set fisso di livelli di funzionalità definiti [**nell'enumerazione FEATURE \_ \_ LEVEL D3D.**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) Quando si conosce il livello [di funzionalità più](overviews-direct3d-11-devices-downlevel-intro.md) alto supportato da un dispositivo, è possibile eseguire percorsi di codice appropriati per tale dispositivo.

**Per ottenere il livello di funzionalità del dispositivo**

1.  Chiamare la [**funzione D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o le funzioni [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) specificando **NULL** per il *parametro ppDevice.* È possibile eseguire questa operazione prima della creazione del dispositivo.

    \- - oppure -

    Chiamare [**ID3D11Device::GetFeatureLevel dopo**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) la creazione del dispositivo.

2.  Esaminare il valore dell'enumerazione [**D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) restituita dall'ultimo passaggio per determinare il livello di funzionalità supportato.

L'esempio di codice seguente illustra come determinare il livello di funzionalità più alto supportato chiamando la [**funzione D3D11CreateDevice.**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) **D3D11CreateDevice archivia** il livello di funzionalità più alto supportato nella variabile FeatureLevel. È possibile usare questo codice per esaminare il valore del tipo [**enumerato D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) restituito da **D3D11CreateDevice.** Si noti che questo codice elenca tutti i livelli di funzionalità in modo esplicito (per Direct3D 11.1 e Direct3D 11.2).

> [!Note]  
> Se il runtime direct3D 11.1 è presente nel computer e *pFeatureLevels* è impostato su **NULL,** questa funzione non creerà un [**dispositivo D3D \_ FEATURE LEVEL \_ \_ 11 \_ 1.**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) Per creare un **dispositivo D3D \_ FEATURE LEVEL \_ \_ 11 \_ 1,** è necessario fornire in modo esplicito una matrice **D3D \_ FEATURE \_ LEVEL** che includa **D3D \_ FEATURE LEVEL \_ \_ 11 \_ 1.** Se si specifica una matrice **D3D \_ FEATURE \_ LEVEL** che contiene **D3D \_ FEATURE LEVEL \_ \_ 11 \_ 1** in un computer in cui non è installato il runtime Direct3D 11.1, questa funzione ha immediatamente esito negativo con E \_ INVALIDARG.

 


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



La sezione 10Level9 Reference (Informazioni di riferimento su [10Level9)](d3d11-graphics-reference-10level9.md) elenca le differenze tra il comportamento dei vari metodi [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) a vari livelli di funzionalità 10Level9.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direct3D 11 su hardware di livello inferiore](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




