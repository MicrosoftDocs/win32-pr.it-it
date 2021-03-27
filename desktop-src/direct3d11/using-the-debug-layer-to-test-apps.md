---
title: Uso del livello di debug per eseguire il debug di app
description: In questo articolo viene illustrato come abilitare il livello di debug e alcuni dei problemi che è possibile prevenire utilizzando il livello di debug.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa3f4748da6893470e3bb6631c4228ec1ae3d48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708176"
---
# <a name="using-the-debug-layer-to-debug-apps"></a>Uso del livello di debug per eseguire il debug di app

Si consiglia di usare il [livello di debug](overviews-direct3d-11-devices-layers.md) per eseguire il debug delle app per assicurarsi che siano puliti da errori e avvisi. Il livello di debug consente di scrivere codice Direct3D. Inoltre, la produttività può aumentare quando si usa il livello di debug, in quanto è possibile visualizzare immediatamente le cause degli errori di rendering oscuri o persino le schermate nere nell'origine. Il livello di debug fornisce avvisi per molti problemi. Ad esempio, il livello di debug fornisce avvisi per i problemi seguenti:

-   Non è stato possibile impostare una trama ma è possibile leggerla nel pixel shader
-   Profondità di output senza associazione di stato depth-stencil
-   Creazione trama non riuscita con INVALIDARG

In questo articolo viene illustrato come abilitare il [livello di debug](overviews-direct3d-11-devices-layers.md) e alcuni dei problemi che è possibile prevenire utilizzando il livello di debug.

-   [Abilitazione del livello di debug](#enabling-the-debug-layer)
-   [Prevenzione degli errori nell'app con il livello di debug](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [Non passare puntatori NULL a map](#dont-pass-null-pointers-to-map)
    -   [Casella origine limite all'interno delle risorse di origine e di destinazione](#confine-source-box-within-source-and-destination-resources)
    -   [Non eliminare DiscardResource o DiscardView](#dont-drop-discardresource-or-discardview)
-   [Argomenti correlati](#related-topics)

## <a name="enabling-the-debug-layer"></a>Abilitazione del livello di debug

Per abilitare il [livello di debug](overviews-direct3d-11-devices-layers.md), specificare il flag [**d3d11 \_ Create \_ Device \_ debug**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) nel parametro *Flags* quando si chiama la funzione [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) per creare il dispositivo di rendering. Questo esempio di codice illustra come abilitare il livello di debug quando il progetto Microsoft Visual Studio si trova in una build di debug:


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

Se si utilizza l'API Direct3D 11 o si passano parametri non validi, l'output di debug del [livello di debug](overviews-direct3d-11-devices-layers.md) segnala un errore o un avviso. È quindi possibile correggere l'errore. Verranno ora esaminati alcuni problemi di codifica che possono causare un comportamento indefinito o anche il sistema operativo. È possibile intercettare e impedire tali problemi utilizzando il livello debug.

### <a name="dont-pass-null-pointers-to-map"></a>Non passare puntatori NULL a map

Se si passa **null** al parametro *PreSource* o *pMappedResource* del metodo [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) , il comportamento di **Map** non è definito. Se è stato creato un dispositivo che supporta solo il [livello di base](overviews-direct3d-11-devices-layers.md), i parametri non validi per la **mappa** possono causare l'arresto anomalo del sistema operativo. Se è stato creato un dispositivo che supporta il [livello di debug](overviews-direct3d-11-devices-layers.md), l'output di debug restituisce un errore in questa chiamata della **mappa** non valida.

### <a name="confine-source-box-within-source-and-destination-resources"></a>Casella origine limite all'interno delle risorse di origine e di destinazione

In una chiamata al metodo [**sul ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) la casella di origine deve trovarsi all'interno della risorsa di origine. Gli offset di destinazione, (x, y e z) consentono l'offset della casella di origine durante la scrittura nella risorsa di destinazione, ma le dimensioni della casella di origine e degli offset devono essere comprese tra le dimensioni della risorsa. Se si tenta di copiare al di fuori della risorsa di destinazione o di specificare una casella di origine maggiore della risorsa di origine, il comportamento di **CopySubresourceRegion** non è definito. Se è stato creato un dispositivo che supporta il [livello di debug](overviews-direct3d-11-devices-layers.md), l'output di debug restituisce un errore in questa chiamata **CopySubresourceRegion** non valida. I parametri non validi per **CopySubresourceRegion** causano un comportamento non definito e potrebbero comportare il rendering errato, il ritaglio, nessuna copia o persino la rimozione del dispositivo di rendering.

### <a name="dont-drop-discardresource-or-discardview"></a>Non eliminare DiscardResource o DiscardView

Il runtime rilascia una chiamata a [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) o [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) a meno che non si crei correttamente la risorsa.

La risorsa passata a [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) deve essere stata creata usando il [**\_ \_ valore predefinito di utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) o la [**\_ \_ dinamica di utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). in caso contrario, il runtime elimina la chiamata a **DiscardResource**.

La risorsa sottostante la visualizzazione passata a [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) deve essere stata creata usando il [**\_ \_ valore predefinito di utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) o la [**\_ \_ dinamica di utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). in caso contrario, il runtime elimina la chiamata a **DiscardView**.

Se è stato creato un dispositivo che supporta il [livello di debug](overviews-direct3d-11-devices-layers.md), l'output di debug restituisce un errore relativo alla chiamata eliminata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Livelli software](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




