---
title: Funzionalità di Direct3D 11,2
description: Le funzionalità seguenti sono state aggiunte in Direct3D 11,2, incluso in Windows 8.1, Windows RT 8,1 e Windows Server 2012 R2.
ms.assetid: 2A2D9BBB-F53A-4187-A25B-F4E58C896EE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299b720bfb91297043c8e7d76beb50067eb64e17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976730"
---
# <a name="direct3d-112-features"></a>Funzionalità di Direct3D 11,2

Le funzionalità seguenti sono state aggiunte in Direct3D 11,2, incluso in Windows 8.1, Windows RT 8,1 e Windows Server 2012 R2.

-   [Risorse affiancate](#tiled-resources)
    -   [Controllare il supporto delle risorse affiancate](#check-tiled-resources-support)
-   [Supporto esteso per i dispositivi WARP](#extended-support-for-warp-devices)
-   [Annotare i comandi di grafica](#annotate-graphics-commands)
-   [Collegamento dello shader HLSL](#hlsl-shader-linking)
    -   [Graph di collegamento a funzioni (FLG)](#function-linking-graph-flg)
-   [Compilatore HLSL della posta in arrivo](#inbox-hlsl-compiler)
-   [Argomenti correlati](#related-topics)

## <a name="tiled-resources"></a>Risorse affiancate

Direct3D 11,2 consente di creare risorse affiancate che possono essere considerate come risorse logiche di grandi dimensioni che utilizzano piccole quantità di memoria fisica. Le risorse affiancate sono utili, ad esempio, con il terreno nei giochi e l'interfaccia utente dell'app.

Le risorse affiancate vengono create specificando il flag di [**\_ \_ varie \_ risorse di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) . Per lavorare con la risorsa affiancata, usare queste API:

-   [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)
-   [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)
-   [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings)
-   [**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings)
-   [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)
-   **D3d11 \_ Funzionalità di DEBUG disabilitare il rilevamento e il flag di \_ \_ \_ \_ \_ \_ \_ \_ convalida del mapping delle risorse affiancati** con [ **ID3D11Debug:: SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)

Per altre informazioni sulle risorse affiancate, vedere [risorse affiancate](tiled-resources.md).

### <a name="check-tiled-resources-support"></a>Controllare il supporto delle risorse affiancate

Prima di usare le risorse affiancate, è necessario sapere se il dispositivo supporta le risorse affiancate. Ecco come verificare il supporto per le risorse affiancate:


```C++
HRESULT hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    creationFlags,              // Set debug and Direct2D compatibility flags.
    featureLevels,              // List of feature levels this app can support.
    ARRAYSIZE(featureLevels),   // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_d3dFeatureLevel,         // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (SUCCEEDED(hr))
{
    D3D11_FEATURE_DATA_D3D11_OPTIONS1 featureData;
    DX::ThrowIfFailed(
        device->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS1, &featureData, sizeof(featureData))
        );

    m_tiledResourcesTier = featureData.TiledResourcesTier;
}
```



## <a name="extended-support-for-warp-devices"></a>Supporto esteso per i dispositivi WARP

Direct3D 11,2 estende il supporto per i dispositivi [Warp](overviews-direct3d-11-devices-create-warp.md) , che è possibile creare passando il [**tipo di \_ driver D3D \_ \_ Warp**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) nel parametro *DriverType* di [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice). Il renderer software WARP in Direct3D 11,2 aggiunge il supporto completo per il [livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) Direct3D 11 \_ 1, incluse [le risorse affiancate](#tiled-resources), [**IDXGIDevice3:: Trim**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim), Shared BCN Surfaces, minblend e map default. È stato inoltre abilitato il [doppio](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) supporto in HLSL shader insieme al supporto per la funzionalità di MSAA MSAA.

## <a name="annotate-graphics-commands"></a>Annotare i comandi di grafica

Direct3D 11,2 consente di aggiungere annotazioni ai comandi grafici con queste API:

-   [**ID3D11DeviceContext2::IsAnnotationEnabled**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-isannotationenabled)
-   [**ID3D11DeviceContext2::BeginEventInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-begineventint)
-   [**ID3D11DeviceContext2::SetMarkerInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-setmarkerint)
-   [**ID3D11DeviceContext2:: chiamata endEvent**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-endevent)

## <a name="hlsl-shader-linking"></a>Collegamento dello shader HLSL

Windows 8.1 aggiunge la compilazione e il collegamento distinti di shader HLSL, che consente ai programmatori di grafica di creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione. Si tratta essenzialmente di un equivalente della compilazione, delle librerie e del collegamento separate da C/C++, che consente ai programmatori di comporre codice HLSL precompilato quando più informazioni diventano disponibili per finalizzare il calcolo. Per ulteriori informazioni sull'utilizzo del collegamento shader, vedere [utilizzo del collegamento shader](/windows/desktop/direct3dhlsl/using-shader-linking).

Completare questi passaggi per creare uno shader finale usando il collegamento dinamico in fase di esecuzione.

**Per creare e usare il collegamento dello shader**

1.  Creare un oggetto [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker) linker, che rappresenta un contesto di collegamento. Non è possibile usare un singolo contesto per produrre più shader; viene usato un contesto di collegamento per produrre un singolo shader e quindi viene eliminato il contesto di collegamento.
2.  Usare [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) per caricare e impostare le librerie dai BLOB di libreria.
3.  Usare [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) per caricare e impostare un BLOB di shader entry oppure creare uno [shader FLG](#function-linking-graph-flg).
4.  Usare [**ID3D11Module**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module)::[**CreateInstance**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11module-createinstance) per creare oggetti [**ID3D11ModuleInstance**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance) , quindi chiamare le funzioni su questi oggetti per riassociare le risorse agli slot finali.
5.  Aggiungere le librerie al linker, quindi chiamare [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker)::[**link**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11linker-link) per produrre il codice byte finale dello shader che può quindi essere caricato e usato nel runtime esattamente come uno shader completamente precompilato e collegato.

### <a name="function-linking-graph-flg"></a>Graph di collegamento a funzioni (FLG)

Windows 8.1 aggiunge anche il grafico di collegamento a funzioni (FLG). È possibile utilizzare FLG per costruire shader che sono costituiti da una sequenza di chiamate di funzioni precompilate che passano i valori tra loro. Quando si usa il FLG, non è necessario scrivere HLSL e richiamare il compilatore HLSL. Al contrario, la struttura dello shader viene specificata a livello di programmazione tramite le chiamate API C++. I nodi FLG rappresentano le firme di input e output e le chiamate delle funzioni della libreria precompilata. L'ordine di registrazione dei nodi di chiamata di funzione definisce la sequenza di chiamate. Il nodo della firma di input deve essere specificato per primo, mentre il nodo della firma di output deve essere specificato per ultimo. I bordi di FLG definiscono il modo in cui i valori vengono passati da un nodo a un altro. I tipi di dati dei valori passati devono essere uguali. non esiste alcuna conversione implicita di tipi. Le regole Shape e swizzling seguono il comportamento HLSL e i valori possono essere passati solo in futuro in questa sequenza. Per informazioni sull'API di FLG, vedere [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph).

## <a name="inbox-hlsl-compiler"></a>Compilatore HLSL della posta in arrivo

Il compilatore HLSL è ora posta in arrivo in Windows 8.1 e versioni successive. A questo punto, la maggior parte delle API per la programmazione dello shader può essere usata nelle app di Windows Store compilate per Windows 8.1 e versioni successive. Molte API per la programmazione dello shader non possono essere usate nelle app di Windows Store compilate per Windows 8. le pagine di riferimento per queste API sono state contrassegnate con una nota. Tuttavia, alcune API shader, ad esempio [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile), possono essere usate solo per sviluppare app di Windows Store e non nelle app inviate a Windows Store. le pagine di riferimento per queste API sono ancora contrassegnate con una nota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Novità di Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 