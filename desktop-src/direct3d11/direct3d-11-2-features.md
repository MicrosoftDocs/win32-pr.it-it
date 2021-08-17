---
title: Funzionalità di Direct3D 11.2
description: La funzionalità seguente è stata aggiunta in Direct3D 11.2, incluso in Windows 8.1, Windows RT 8.1 e Windows Server 2012 R2.
ms.assetid: 2A2D9BBB-F53A-4187-A25B-F4E58C896EE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cd253cf618b3915c4f303691cab86a11cc9268061d536892c0ff5ccf4fffe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124546"
---
# <a name="direct3d-112-features"></a>Funzionalità di Direct3D 11.2

La funzionalità seguente è stata aggiunta in Direct3D 11.2, incluso in Windows 8.1, Windows RT 8.1 e Windows Server 2012 R2.

-   [Risorse affiancate](#tiled-resources)
    -   [Controllare il supporto delle risorse in riquadri](#check-tiled-resources-support)
-   [Supporto esteso per i dispositivi WARP](#extended-support-for-warp-devices)
-   [Aggiungere annotazioni ai comandi di grafica](#annotate-graphics-commands)
-   [Collegamento di shader HLSL](#hlsl-shader-linking)
    -   [Grafico di collegamento delle funzioni (FLG)](#function-linking-graph-flg)
-   [Compilatore HLSL della posta in arrivo](#inbox-hlsl-compiler)
-   [Argomenti correlati](#related-topics)

## <a name="tiled-resources"></a>Risorse affiancate

Direct3D 11.2 consente di creare risorse affiancate che possono essere ritenute come risorse logiche di grandi dimensioni che usano piccole quantità di memoria fisica. Le risorse affiancate sono utili (ad esempio) con terreno nei giochi e interfaccia utente dell'app.

Le risorse affiancate vengono create specificando il flag [**D3D11 \_ RESOURCE \_ MISC \_ TILED.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Per usare la risorsa affiancata, usare queste API:

-   [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)
-   [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)
-   [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings)
-   [**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings)
-   [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)
-   **D3D11 \_ FUNZIONALITÀ \_ DI DEBUG DISABLE \_ \_ TILED RESOURCE MAPPING TRACKING \_ AND \_ \_ \_ \_ VALIDATION** flag with [ **ID3D11Debug::SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)

Per altre informazioni sulle risorse affiancate, vedere [Risorse affiancate.](tiled-resources.md)

### <a name="check-tiled-resources-support"></a>Controllare il supporto delle risorse in riquadri

Prima di usare le risorse affiancate, è necessario verificare se il dispositivo supporta le risorse affiancate. Ecco come verificare il supporto per le risorse affiancate:


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

Direct3D 11.2 estende il supporto per i dispositivi [WARP,](overviews-direct3d-11-devices-create-warp.md) che vengono creati passando [**D3D \_ DRIVER TYPE \_ \_ WARP**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) nel *parametro DriverType* di [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice). Il renderer software WARP in Direct3D 11.2 aggiunge il supporto [completo](overviews-direct3d-11-devices-downlevel-intro.md) per il livello di funzionalità Direct3D 11 1, incluse le risorse affiancate, \_ [**IDXGIDevice3::Trim**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim), le superfici BCn condivise, minblend e l'impostazione predefinita della mappa. [](#tiled-resources) [È](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) stato abilitato anche il supporto doppio negli shader HLSL insieme al supporto per MSAA 16x.

## <a name="annotate-graphics-commands"></a>Aggiungere annotazioni ai comandi di grafica

Direct3D 11.2 consente di annotare i comandi di grafica con queste API:

-   [**ID3D11DeviceContext2::IsAnnotationEnabled**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-isannotationenabled)
-   [**ID3D11DeviceContext2::BeginEventInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-begineventint)
-   [**ID3D11DeviceContext2::SetMarkerInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-setmarkerint)
-   [**ID3D11DeviceContext2::EndEvent**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-endevent)

## <a name="hlsl-shader-linking"></a>Collegamento di shader HLSL

Windows 8.1 aggiunge la compilazione e il collegamento separati degli shader HLSL, che consentono ai programmatori di grafica di creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione. Si tratta essenzialmente di un equivalente di compilazione, librerie e collegamento separati C/C++ e consente ai programmatori di comporre codice HLSL precompilato quando diventano disponibili altre informazioni per finalizzare il calcolo. Per altre informazioni su come usare il collegamento shader, vedere [Uso del collegamento dello shader.](/windows/desktop/direct3dhlsl/using-shader-linking)

Completare questi passaggi per creare uno shader finale usando il collegamento dinamico in fase di esecuzione.

**Per creare e usare il collegamento shader**

1.  Creare un [**oggetto linker ID3D11Linker,**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker) che rappresenta un contesto di collegamento. Non è possibile usare un singolo contesto per produrre più shader. un contesto di collegamento viene usato per produrre un singolo shader e quindi il contesto di collegamento viene buttato via.
2.  Usare [**D3DLoadModule per**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) caricare e impostare le librerie dai BLOB della libreria.
3.  Usare [**D3DLoadModule per**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) caricare e impostare un BLOB entry shader o creare uno [shader FLG.](#function-linking-graph-flg)
4.  Usare [**ID3D11Module**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module)::[**CreateInstance**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11module-createinstance) per creare oggetti [**ID3D11ModuleInstance,**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance) quindi chiamare funzioni su questi oggetti per riassociare le risorse agli slot finali.
5.  Aggiungere le librerie al linker, quindi chiamare [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker)::[**Link**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11linker-link) per produrre il codice byte finale dello shader che può quindi essere caricato e usato nel runtime proprio come uno shader completamente precompilato e collegato.

### <a name="function-linking-graph-flg"></a>Grafico di collegamento delle funzioni (FLG)

Windows 8.1 aggiunge anche function linking Graph (FLG). È possibile usare FLG per costruire shader costituiti da una sequenza di chiamate di funzioni precompilate che passano valori tra loro. Quando si usa FLG, non è necessario scrivere HLSL e richiamare il compilatore HLSL. La struttura dello shader viene invece specificata a livello di codice tramite chiamate API C++. I nodi FLG rappresentano firme di input e output e chiamate di funzioni di libreria precompilate. L'ordine di registrazione dei nodi di chiamata di funzione definisce la sequenza di chiamate. Il nodo della firma di input deve essere specificato per primo, mentre il nodo della firma di output deve essere specificato per ultimo. I bordi FLG definiscono il modo in cui i valori vengono passati da un nodo a un altro. I tipi di dati dei valori passati devono essere uguali. non esiste alcuna conversione implicita del tipo. Le regole di forma e scorrimento seguono il comportamento HLSL e i valori possono essere passati in avanti solo in questa sequenza. Per informazioni sull'API FLG, vedere [**ID3D11FunctionLinkingGraph.**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph)

## <a name="inbox-hlsl-compiler"></a>Compilatore HLSL della posta in arrivo

Il compilatore HLSL è ora disponibile in Windows 8.1 e versioni successive. A questo punto, la maggior parte delle API per la programmazione shader può essere usata nelle app Windows Store create per Windows 8.1 e versioni successive. Molte API per la programmazione shader non possono essere usate nelle app Windows Store create per Windows 8; Le pagine di riferimento per queste API sono state contrassegnate con una nota. Alcune API shader, ad esempio [**D3DCompileFromFile,**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)possono comunque essere usate solo per sviluppare app di Windows Store e non per le app inviate a Windows Store. Le pagine di riferimento per queste API sono ancora contrassegnate con una nota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Novità di Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 