---
title: Uso del livello di debug per eseguire il debug delle app
description: Di seguito viene descritto come abilitare il livello di debug e alcuni dei problemi che è possibile evitare usando il livello di debug.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c6ac5492b96c40b4395b2c501b764c646a8edbb06d3a6386a15cbb2534778d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912735"
---
# <a name="using-the-debug-layer-to-debug-apps"></a>Uso del livello di debug per eseguire il debug delle app

È consigliabile usare il livello [di debug per](overviews-direct3d-11-devices-layers.md) eseguire il debug delle app per assicurarsi che non siano presenti errori e avvisi. Il livello di debug consente di scrivere codice Direct3D. Inoltre, la produttività può aumentare quando si usa il livello di debug perché è possibile vedere immediatamente le cause di errori di rendering nascosti o persino di schermate nere all'origine. Il livello di debug fornisce avvisi per molti problemi. Ad esempio, il livello di debug fornisce avvisi per questi problemi:

-   Si è dimenticato di impostare una trama, ma di leggerla nel pixel shader
-   Profondità di output ma senza stato depth-stencil associato
-   Creazione della trama non riuscita con INVALIDARG

Di seguito viene descritto come abilitare il livello [di debug](overviews-direct3d-11-devices-layers.md) e alcuni dei problemi che è possibile evitare usando il livello di debug.

-   [Abilitazione del livello di debug](#enabling-the-debug-layer)
-   [Prevenzione degli errori nell'app con il livello di debug](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [Non passare puntatori NULL a Map](#dont-pass-null-pointers-to-map)
    -   [Limitare la casella di origine all'interno delle risorse di origine e di destinazione](#confine-source-box-within-source-and-destination-resources)
    -   [Non eliminare DiscardResource o DiscardView](#dont-drop-discardresource-or-discardview)
-   [Argomenti correlati](#related-topics)

## <a name="enabling-the-debug-layer"></a>Abilitazione del livello di debug

Per abilitare il [livello di debug](overviews-direct3d-11-devices-layers.md), specificare il flag [**D3D11 \_ CREATE DEVICE \_ \_ DEBUG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) nel parametro *Flags* quando si chiama la funzione [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) per creare il dispositivo di rendering. Questo codice di esempio illustra come abilitare il livello di debug quando il Microsoft Visual Studio si trova in una build di debug:


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a>Prevenzione degli errori nell'app con il livello di debug

Se si usa in modo improprio l'API Direct3D 11 o si passano parametri non validi, l'output di debug del livello [di debug](overviews-direct3d-11-devices-layers.md) segnala un errore o un avviso. È quindi possibile correggere l'errore. Successivamente, si osservano alcuni problemi di codifica che possono causare un comportamento indefinito o persino l'arresto anomalo del sistema operativo. È possibile rilevare e impedire questi problemi usando il livello di debug.

### <a name="dont-pass-null-pointers-to-map"></a>Non passare puntatori NULL a Map

Se si passa **NULL** al *parametro pResource* o *pMappedResource* del metodo [**ID3D11DeviceContext::Map,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) il comportamento di **Map** non è definito. Se è stato creato un dispositivo che supporta solo il livello [principale](overviews-direct3d-11-devices-layers.md), i parametri non validi per **Map** possono determinare l'arresto anomalo del sistema operativo. Se è stato creato un dispositivo che supporta il livello [di debug](overviews-direct3d-11-devices-layers.md), l'output di debug segnala un errore in questa chiamata **map non** valida.

### <a name="confine-source-box-within-source-and-destination-resources"></a>Limitare la casella di origine all'interno delle risorse di origine e di destinazione

In una chiamata al metodo [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) la casella di origine deve essere all'interno della risorsa di origine. Gli offset di destinazione (x, y e z) consentono l'offset della casella di origine durante la scrittura nella risorsa di destinazione, ma le dimensioni della casella di origine e gli offset devono essere all'interno delle dimensioni della risorsa. Se si prova a eseguire la copia all'esterno della risorsa di destinazione o si specifica una casella di origine maggiore della risorsa di origine, il comportamento di **CopySubresourceRegion** non è definito. Se è stato creato un dispositivo che supporta il livello [di debug](overviews-direct3d-11-devices-layers.md), l'output di debug segnala un errore in questa chiamata **CopySubresourceRegion non** valida. I parametri non validi **per CopySubresourceRegion** causano un comportamento indefinito e potrebbero causare rendering non corretto, ritaglio, nessuna copia o persino la rimozione del dispositivo di rendering.

### <a name="dont-drop-discardresource-or-discardview"></a>Non eliminare DiscardResource o DiscardView

Il runtime elimina una chiamata a [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) o [**ID3D11DeviceContext1::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) a meno che la risorsa non venga creata correttamente.

La risorsa passata a [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) deve essere stata creata usando [**D3D11 \_ USAGE \_ DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) o [**D3D11 \_ USAGE \_ DYNAMIC,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)in caso contrario il runtime elimina la chiamata a **DiscardResource.**

La risorsa alla base della visualizzazione passata a [**ID3D11DeviceContext1::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) deve essere stata creata usando [**D3D11 \_ USAGE \_ DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) o [**D3D11 \_ USAGE \_ DYNAMIC,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)in caso contrario il runtime elimina la chiamata a **DiscardView.**

Se è stato creato un dispositivo che supporta il livello [di debug](overviews-direct3d-11-devices-layers.md), l'output di debug segnala un errore relativo alla chiamata rilasciata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Livelli software](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




