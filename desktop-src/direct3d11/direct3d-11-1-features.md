---
title: Funzionalità di Direct3D 11,1
description: Le funzionalità seguenti sono state aggiunte in Direct3D 11,1, incluso in Windows 8, Windows RT e Windows Server 2012.
ms.assetid: 2203D2D2-ECF6-4753-90FA-12A52678DFBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dece9ed6e0a40ade28857277c344be0e9f2e7ce1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727495"
---
# <a name="direct3d-111-features"></a>Funzionalità di Direct3D 11,1

Le funzionalità seguenti sono state aggiunte in Direct3D 11,1, incluso in Windows 8, Windows RT e Windows Server 2012. Il supporto parziale per [Direct3D 11,1](direct3d-11-features.md) è disponibile in Windows 7 e windows Server 2008 R2 tramite l' [aggiornamento della piattaforma per Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), disponibile tramite l' [aggiornamento della piattaforma per Windows 7](https://support.microsoft.com/kb/2670838).

-   [Miglioramenti del compilatore e della traccia dello shader](#shader-tracing-and-compiler-enhancements)
-   [Condivisione di dispositivi Direct3D](#direct3d-device-sharing)
-   [Verificare il supporto delle nuove funzionalità e dei formati Direct3D 11,1](#check-support-of-new-direct3d-111-features-and-formats)
-   [USA precisione minima HLSL](#use-hlsl-minimum-precision)
-   [Specificare i piani di ritaglio utente in HLSL sul livello di funzionalità 9 e versioni successive](#specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Creare buffer costanti più grandi di quelli a cui uno shader può accedere](#create-larger-constant-buffers-than-a-shader-can-access)
-   [Usare le operazioni logiche in una destinazione di rendering](#use-logical-operations-in-a-render-target)
-   [Forzare il numero di campioni a creare uno stato di rasterizzazione](#force-the-sample-count-to-create-a-rasterizer-state)
-   [Elaborare risorse video con shader](#process-video-resources-with-shaders)
-   [Supporto esteso per le risorse Texture2D condivise](#extended-support-for-shared-texture2d-resources)
-   [Modificare le sottorisorse con le nuove opzioni di copia](#change-subresources-with-new-copy-options)
-   [Elimina risorse e visualizzazioni risorse](#discard-resources-and-resource-views)
-   [Supporto di un numero maggiore di UAV](#support-a-larger-number-of-uavs)
-   [Associare un intervallo secondario di un buffer costante a uno shader](#bind-a-subrange-of-a-constant-buffer-to-a-shader)
-   [Recuperare l'intervallo secondario di un buffer costante associato a uno shader](#retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader)
-   [Cancella tutta o parte di una visualizzazione risorse](#clear-all-or-part-of-a-resource-view)
-   [Mappare SRVs di buffer dinamici senza \_ sovrascrittura](/windows)
-   [Usare UAV in ogni fase della pipeline](#use-uavs-at-every-pipeline-stage)
-   [Supporto esteso per i dispositivi WARP](#extended-support-for-warp-devices)
-   [Usare Direct3D nei processi della sessione 0](#use-direct3d-in-session-0-processes)
-   [Supporto per il buffer shadow sul livello di funzionalità 9](#support-for-shadow-buffer-on-feature-level-9)
-   [Argomenti correlati](#related-topics)

## <a name="shader-tracing-and-compiler-enhancements"></a>Miglioramenti del compilatore e della traccia dello shader

Direct3D 11,1 consente di usare la traccia dello shader per assicurarsi che il codice venga effettuato come previsto e in caso contrario è possibile individuare e risolvere il problema. Windows Software Development Kit (SDK) per Windows 8 contiene i miglioramenti del compilatore HLSL. La traccia dello shader e il compilatore HLSL sono implementati in D3dcompiler \_nn.dll.

L'API di traccia dello shader e i miglioramenti apportati al compilatore HLSL sono costituiti dai metodi e dalle funzioni seguenti.

-   [**ID3D11RefDefaultTrackingOptions::SetTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11refdefaulttrackingoptions-settrackingoptions)
-   [**ID3D11RefTrackingOptions::SetTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11reftrackingoptions-settrackingoptions)
-   [**ID3D11TracingDevice::SetShaderTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11TracingDevice::SetShaderTrackingOptionsByType**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11ShaderTraceFactory::CreateShaderTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertracefactory-createshadertrace)
-   [**ID3D11ShaderTrace::TraceReady**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-traceready)
-   [**ID3D11ShaderTrace::ResetTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-resettrace)
-   [**ID3D11ShaderTrace::GetTraceStats**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-gettracestats)
-   [**ID3D11ShaderTrace::P SSelectStamp**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-psselectstamp)
-   [**ID3D11ShaderTrace::GetInitialRegisterContents**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents)
-   [**ID3D11ShaderTrace:: getstep**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getstep)
-   [**ID3D11ShaderTrace::GetWrittenRegister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getwrittenregister)
-   [**ID3D11ShaderTrace::GetReadRegister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getreadregister)
-   [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2)
-   [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)
-   [**D3DDisassemble11Trace**](/windows/desktop/direct3dhlsl/d3ddisassemble11trace)
-   [**D3DDisassembleRegion**](/windows/desktop/direct3dhlsl/d3ddisassembleregion)
-   [**D3DGetTraceInstructionOffsets**](/windows/desktop/direct3dhlsl/d3dgettraceinstructionoffsets)
-   [**D3DReadFileToBlob**](/windows/desktop/direct3dhlsl/d3dreadfiletoblob)
-   [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart)
-   [**D3DWriteBlobToFile**](/windows/desktop/direct3dhlsl/d3dwriteblobtofile)

La libreria D3dcompiler. lib richiede D3dcompiler \_nn.dll. Questa DLL non fa parte di Windows 8. si trova nella \\ cartella bin del Windows SDK per Windows 8 insieme alla versione della riga di comando Fxc.exe del compilatore HLSL.

> [!Note]  
> Sebbene sia possibile usare questa combinazione di libreria e DLL per lo sviluppo, non è possibile distribuire app di Windows Store che usano questa combinazione. È pertanto necessario compilare HLSL shader prima di distribuire l'app di Windows Store. È possibile scrivere file binari di compilazione HLSL su disco oppure il compilatore può generare intestazioni con matrici di byte statiche che contengono i dati BLOB dello shader. Per accedere ai dati BLOB, è possibile usare l'interfaccia [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) . Per sviluppare un'app di Windows Store, chiamare [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2) o [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) per compilare l'origine HLSL non elaborata e quindi inserire i dati BLOB risultanti in Direct3D.

 

## <a name="direct3d-device-sharing"></a>Condivisione di dispositivi Direct3D

Direct3D 11,1 Abilita le API Direct3D 10 e le API Direct3D 11 a usare un dispositivo di rendering sottostante.

Questa funzionalità Direct3D 11,1 è costituita dai metodi e dall'interfaccia seguenti.

-   [**ID3D11Device1::CreateDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate)
-   [**ID3D11DeviceContext1::SwapDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate)
-   [**ID3DDeviceContextState**](/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate)

## <a name="check-support-of-new-direct3d-111-features-and-formats"></a>Verificare il supporto delle nuove funzionalità e dei formati Direct3D 11,1

Direct3D 11,1 consente di verificare la presenza di nuove funzionalità che possono essere supportate dal driver grafico e nuove modalità di supporto di un formato in un dispositivo. Microsoft DirectX Graphics Infrastructure (DXGI) 1,2 specifica anche i nuovi valori del [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

Questa funzionalità Direct3D 11,1 è costituita dall'API seguente.

-   [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con [**d3d11 \_ funzionalità \_ dati \_ d3d11 \_ Opzioni**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), [**d3d11 \_ funzionalità \_ \_ \_ informazioni architettura dati**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info), [**d3d11 \_ funzionalità \_ dati \_ d3d9 \_ Opzioni**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options), [**d3d11 \_ funzionalità \_ data \_ shader \_ Min \_ precisione \_ supporto**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)e [**d3d11 funzionalità dati d3d9 strutture di \_ \_ \_ \_ \_ supporto shadow**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support)
-   [**ID3D11Device:: CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) con [**\_ formato d3d11 \_ supporta \_ l' \_ output del decodificatore**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), il [**\_ formato d3d11 supporta l' \_ \_ \_ \_ output del processore video**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), il [**\_ formato d3d11 \_ supporta \_ \_ \_ input del processore video**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), il [**\_ formato d3d11 supporta il \_ \_ \_ codificatore video**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)e [**d3d11 formato SUPPORT2 \_ \_ \_ output \_ \_ logica \_ operazione di merge**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)

## <a name="use-hlsl-minimum-precision"></a>USA precisione minima HLSL

A partire da Windows 8, i driver grafici possono implementare i [tipi di dati scalari HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) precisione minima usando una precisione maggiore o uguale alla precisione dei bit specificata. Quando il codice shader con precisione minima di HLSL viene usato nell'hardware che implementa la precisione minima di HLSL, si usa una minore larghezza di banda di memoria e, di conseguenza, si usa meno energia del sistema.

È possibile eseguire una query per il supporto di precisione minima fornito dal driver di grafica chiamando [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con il valore di supporto della precisione minima dello [**\_ shader della funzionalità \_ \_ \_ \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) . In questa chiamata **ID3D11Device:: CheckFeatureSupport** passare un puntatore a una struttura [**di \_ \_ supporto di data \_ shader \_ Min \_ \_ della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support) che **ID3D11Device:: CheckFeatureSupport** riempie i livelli di precisione minimi supportati dal driver per la fase pixel shader e per altre fasi dello shader. Le informazioni restituite indicano semplicemente che l'hardware grafico può eseguire operazioni HLSL con una precisione inferiore rispetto alla precisione mobile a 32 bit standard, ma non garantisce che l'hardware grafico venga effettivamente eseguito a una precisione inferiore.

Non è necessario creare più shader che non usano la precisione minima. Al contrario, creare shader con precisione minima e le variabili di precisione minime si comportano con una precisione a 32 bit completa se il driver di grafica segnala che non supporta alcuna precisione minima. Per altre informazioni sulla precisione minima di HLSL, vedere [uso della precisione minima di HLSL](/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision).

Gli shader con precisione minima HLSL non funzionano con i sistemi operativi precedenti a Windows 8.

## <a name="specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Specificare i piani di ritaglio utente in HLSL sul livello di funzionalità 9 e versioni successive

A partire da Windows 8, è possibile usare l'attributo della funzione **clipplanes** in una [dichiarazione di funzione](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-syntax) HLSL anziché [SV \_ Clipdistance](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) per fare in modo che lo shader funzioni con il [livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, nonché con il livello di funzionalità 10 e versioni successive. Per altre informazioni, vedere la pagina [relativa ai piani di ritaglio utente su hardware di livello funzionalità 9](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).

## <a name="create-larger-constant-buffers-than-a-shader-can-access"></a>Creare buffer costanti più grandi di quelli a cui uno shader può accedere

Direct3D 11,1 consente di creare buffer costanti superiori alle dimensioni massime del buffer costante a cui uno shader può accedere (costanti a 4 componenti a 4096 32 bit \* – 64KB). In seguito, quando si associano i buffer alla pipeline, ad esempio tramite [**PSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers) o [**PSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1), è possibile specificare un intervallo di buffer a cui lo shader può accedere che rientra nel limite di 4096.

Direct3D 11,1 Aggiorna il metodo [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) per questa funzionalità.

## <a name="use-logical-operations-in-a-render-target"></a>Usare le operazioni logiche in una destinazione di rendering

Direct3D 11,1 consente di usare le operazioni logiche anziché la fusione in una destinazione di rendering. Tuttavia, non è possibile combinare le operazioni logiche con la fusione tra più destinazioni di rendering.

Questa funzionalità Direct3D 11,1 è costituita dall'API seguente.

-   [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1) con [ **d3d11 \_ logica \_ op**](/windows/desktop/api/D3D11_1/ne-d3d11_1-d3d11_logic_op)

## <a name="force-the-sample-count-to-create-a-rasterizer-state"></a>Forzare il numero di campioni a creare uno stato di rasterizzazione

Direct3D 11,1 consente di specificare un numero di campionamento forzato quando si crea uno stato di rasterizzazione.

Questa funzionalità Direct3D 11,1 è costituita dall'API seguente.

-   [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)

> [!Note]  
>
> Se si desidera eseguire il rendering con il numero di campioni forzato a 1 o superiore, è necessario attenersi alle linee guida seguenti:
>
> -   Non associare le visualizzazioni degli stencil di profondità.
> -   Disabilitare i test di profondità.
> -   Assicurarsi che lo shader non restituisca la profondità.
> -   Se sono presenti viste di destinazione di rendering associate ([**\_ destinazione di \_ rendering \_ di binding d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)) e il numero di campioni è stato forzato su un valore maggiore di 1, assicurarsi che ogni destinazione di rendering includa solo un singolo campione.
> -   Non usare lo shader alla frequenza di campionamento. Pertanto, [**ID3D11ShaderReflection:: IsSampleFrequencyShader**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11shaderreflection-issamplefrequencyshader) restituisce **false**.
>
> In caso contrario, il comportamento di rendering non è definito. Per informazioni su come configurare depth-stencil, vedere [configurazione di Depth-Stencil funzionalità](d3d10-graphics-programming-guide-depth-stencil.md).

 

## <a name="process-video-resources-with-shaders"></a>Elaborare risorse video con shader

Direct3D 11,1 consente di creare visualizzazioni (SRV/RTV/UAV) per le risorse video in modo che gli shader Direct3D possano elaborare tali risorse video. Il formato di una risorsa video sottostante limita i formati che possono essere usati dalla visualizzazione. L'enumerazione del [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) contiene nuovi valori del formato di risorsa video. Questi valori di **\_ formato DXGI** specificano i formati di vista validi che è possibile creare e il modo in cui il runtime Direct3D 11,1 esegue il mapping della vista. È possibile creare più viste di parti diverse della stessa area e, a seconda del formato, le dimensioni delle visualizzazioni possono essere diverse.

Direct3D 11,1 Aggiorna i metodi seguenti per questa funzionalità.

-   [**ID3D11Device:: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)
-   [**ID3D11Device:: CreateRenderTargetView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview)
-   [**ID3D11Device:: CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview)

## <a name="extended-support-for-shared-texture2d-resources"></a>Supporto esteso per le risorse Texture2D condivise

Direct3D 11,1 garantisce che sia possibile condividere le risorse di Texture2D create con tipi di risorse e formati specifici. Per condividere le risorse Texture2D, usare la risorsa [**d3d11 \_ \_ \_ Shared varie**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag), [**d3d11 \_ Resource \_ varie \_ Shared \_ KEYEDMUTEX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)o una combinazione dei flag **d3d11 \_ Resource \_ varie \_ \_** KEYEDMUTEX e d3d11 Shared varie Resource NTHANDLE (New for Windows 8) quando si creano tali risorse. [**\_ \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

Direct3D 11,1 garantisce che sia possibile condividere le risorse Texture2D create con questi valori [**di \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) :

-   \_Formato DXGI \_ R8G8B8A8 \_ UNORM
-   \_Formato DXGI \_ R8G8B8A8 \_ UNORM \_ sRGB
-   \_Formato DXGI \_ B8G8R8A8 \_ UNORM
-   \_Formato DXGI \_ B8G8R8A8 \_ UNORM \_ sRGB
-   \_Formato DXGI \_ B8G8R8X8 \_ UNORM
-   \_Formato DXGI \_ B8G8R8X8 \_ UNORM \_ sRGB
-   \_Formato DXGI \_ R10G10B10A2 \_ UNORM
-   \_Formato DXGI \_ R16G16B16A16 \_ float

Inoltre, Direct3D 11,1 garantisce che sia possibile condividere le risorse Texture2D create con un livello di mipmap pari a 1, le dimensioni della matrice pari a 1, i flag di binding della [**\_ risorsa dello \_ shader \_ di binding d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) e la [**destinazione di rendering del binding d3d11 combinata, \_ \_ il \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) valore predefinito di utilizzo ([**\_ \_ impostazione predefinita dell'utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) e solo i valori dei [**\_ \_ \_ flag varie della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) :

-   [**\_Risorse d3d11 \_ varie \_ condivise**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ risorse \_ varie \_ \_ KEYEDMUTEX condivise**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ risorse \_ varie \_ \_ NTHANDLE condivise**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_Risorsa d3d11 \_ \_ \_ compatibile con GDI varie**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

Direct3D 11,1 consente di condividere una maggiore varietà di formati e tipi di risorse Texture2D. È possibile eseguire una query per verificare se il driver di grafica e l'hardware supportano la condivisione di risorse Texture2D estesa chiamando [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con il valore delle [**\_ \_ \_ Opzioni d3d11 della funzionalità d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) . In questa chiamata **ID3D11Device:: CheckFeatureSupport** passare un puntatore a una struttura [**di \_ \_ Opzioni di \_ d3d11 \_ di dati della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) . **ID3D11Device:: CheckFeatureSupport** imposta il membro **ExtendedResourceSharing** delle **\_ \_ \_ \_ Opzioni d3d11 dei dati della funzionalità d3d11** su **true** se l'hardware e il driver supportano la condivisione di risorse Texture2D estese.

Se [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) restituisce **true** in **ExtendedResourceSharing**, è possibile condividere le risorse create con i valori [**di \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) seguenti:

-   \_Formato DXGI \_ R32G32B32A32 non \_ tipizzato
-   \_Formato DXGI \_ R32G32B32A32 \_ float
-   \_Formato DXGI \_ R32G32B32A32 \_ uint
-   \_Formato DXGI \_ R32G32B32A32 \_ Sint
-   \_Formato DXGI \_ R16G16B16A16 non \_ tipizzato
-   \_Formato DXGI \_ R16G16B16A16 \_ float
-   \_Formato DXGI \_ R16G16B16A16 \_ UNORM
-   \_Formato DXGI \_ R16G16B16A16 \_ uint
-   DXGI \_ Format \_ R16G16B16A16 \_ russar
-   \_Formato DXGI \_ R16G16B16A16 \_ Sint
-   \_Formato DXGI \_ R10G10B10A2 \_ UNORM
-   \_Formato DXGI \_ R10G10B10A2 \_ uint
-   \_Formato DXGI \_ R8G8B8A8 non \_ tipizzato
-   \_Formato DXGI \_ R8G8B8A8 \_ UNORM
-   \_Formato DXGI \_ R8G8B8A8 \_ UNORM \_ sRGB
-   \_Formato DXGI \_ R8G8B8A8 \_ uint
-   DXGI \_ Format \_ R8G8B8A8 \_ russar
-   \_Formato DXGI \_ R8G8B8A8 \_ Sint
-   \_Formato DXGI \_ B8G8R8A8 non \_ tipizzato
-   \_Formato DXGI \_ B8G8R8A8 \_ UNORM
-   \_Formato DXGI \_ B8G8R8X8 \_ UNORM
-   \_Formato DXGI \_ B8G8R8A8 \_ UNORM \_ sRGB
-   \_Formato DXGI \_ B8G8R8X8 non \_ tipizzato
-   \_Formato DXGI \_ B8G8R8X8 \_ UNORM \_ sRGB
-   \_Formato DXGI \_ R32 non \_ tipizzato
-   \_Formato DXGI \_ R32 \_ float
-   \_Formato DXGI \_ R32 \_ uint
-   \_Formato DXGI \_ R32 \_ Sint
-   \_Formato DXGI \_ R16 non \_ tipizzato
-   \_Formato DXGI \_ R16 \_ float
-   \_Formato DXGI \_ R16 \_ UNORM
-   \_Formato DXGI \_ R16 \_ uint
-   DXGI \_ Format \_ R16 \_ russar
-   \_Formato DXGI \_ R16 \_ Sint
-   \_Formato DXGI \_ R8 con \_ tipo
-   DXGI \_ formato \_ R8 \_ UNORM
-   DXGI \_ formato \_ R8 \_ uint
-   DXGI \_ formato \_ R8 \_ russamento
-   DXGI \_ formato \_ R8 \_ Sint
-   \_Formato DXGI \_ a8 \_ UNORM
-   \_formato DXGI \_ AYUV
-   \_Formato DXGI \_ YUY2
-   \_Formato DXGI \_ NV12
-   \_Formato DXGI \_ NV11
-   \_Formato DXGI \_ P016
-   \_Formato DXGI \_ P010
-   \_Formato DXGI \_ y216
-   \_Formato DXGI \_ Y210
-   \_Formato DXGI \_ Y416
-   \_Formato DXGI \_ Y410

Se [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) restituisce **true** in **ExtendedResourceSharing**, è possibile condividere le risorse create con le funzionalità e i flag seguenti:

-   [**\_ \_ Impostazione predefinita utilizzo d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)
-   [**\_ \_ Risorsa shader bind d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**\_Destinazione di \_ rendering \_ Bind d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**\_Risorsa d3d11 \_ varie \_ genera \_ MIPS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ associa \_ accesso non ordinato \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   Livelli di mipmap (uno o più livelli) nelle risorse di trama 2D (specificate nel membro **MipLevels** di [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc))
-   Matrici di risorse di trama 2D (una o più trame) (specificate nel membro **arraySize** di [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc))
-   [**\_Decodificatore bind d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**\_Contenuto con \_ restrizioni per varie risorse \_ d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**Risorsa D3D11 per limitare le risorse \_ \_ \_ \_ condivise \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ risorse \_ \_ condivise- \_ limita \_ driver risorse condivise \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

> [!Note]  
> Quando **ExtendedResourceSharing** è **true**, è possibile specificare una maggiore flessibilità quando si specificano i flag di binding per la condivisione delle risorse di Texture2D. Non solo il driver di grafica e l'hardware supportano più flag di associazione, ma anche combinazioni più possibili di flag di binding. Ad esempio, è possibile specificare solo [**la \_ \_ \_ destinazione di rendering bind d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) o nessun flag di binding e così via.

 

Anche se [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) restituisce **true** in **ExtendedResourceSharing**, non è ancora possibile condividere le risorse create con le funzionalità e i flag seguenti:

-   [**\_ \_ Stencil profondità di binding d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   risorse di trama 2D in modalità di anti-aliasing di multicampionamento (specificato con [**DXGI \_ Sample \_ desc**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc))
-   [**D3D11 \_ risorse \_ varie \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3d11 \_ UTILIZZO non \_ modificabile**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), [**\_ utilizzo d3d11 \_ dinamico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)o [**\_ \_ gestione temporanea utilizzo d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) (mappabili)
-   [**\_Risorsa d3d11 \_ varie \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="change-subresources-with-new-copy-options"></a>Modificare le sottorisorse con le nuove opzioni di copia

Direct3D 11,1 consente di usare nuovi flag di copia per copiare e aggiornare le sottorisorse. Quando si copia una sottorisorsa, le risorse di origine e di destinazione possono essere identiche e le aree di origine e di destinazione possono sovrapporsi.

Questa funzionalità Direct3D 11,1 è costituita dall'API seguente.

-   [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)
-   [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)

## <a name="discard-resources-and-resource-views"></a>Elimina risorse e visualizzazioni risorse

Direct3D 11,1 consente di scartare le risorse e le visualizzazioni delle risorse dal contesto di dispositivo. Questa nuova funzionalità informa la GPU che il contenuto esistente nelle risorse o nelle visualizzazioni delle risorse non è più necessario.

Questa funzionalità Direct3D 11,1 è costituita dall'API seguente.

-   [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource)
-   [**ID3D11DeviceContext1::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview)
-   [**ID3D11DeviceContext1::D iscardView1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview1)

## <a name="support-a-larger-number-of-uavs"></a>Supporto di un numero maggiore di UAV

Direct3D 11,1 consente di usare un numero maggiore di UAV quando si associano risorse alla [fase di Unione dell'output](d3d10-graphics-programming-guide-output-merger-stage.md) e quando si imposta una matrice di visualizzazioni per una risorsa non ordinata.

Direct3D 11,1 Aggiorna i metodi seguenti per questa funzionalità.

-   [**Sul ID3D11DeviceContext:: OMSetRenderTargetsAndUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews)
-   [**Sul ID3D11DeviceContext:: CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)

## <a name="bind-a-subrange-of-a-constant-buffer-to-a-shader"></a>Associare un intervallo secondario di un buffer costante a uno shader

Direct3D 11,1 consente di associare un intervallo secondario di un buffer costante per l'accesso a uno shader. È possibile fornire un buffer costante più grande e specificare l'intervallo secondario che può essere utilizzato dallo shader.

Questa funzionalità Direct3D 11,1 è costituita dall'API seguente.

-   [**ID3D11DeviceContext1::CSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-cssetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dssetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gssetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hssetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vssetconstantbuffers1)

## <a name="retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader"></a>Recuperare l'intervallo secondario di un buffer costante associato a uno shader

Direct3D 11,1 consente di recuperare l'intervallo secondario di un buffer costante associato a uno shader.

Questa funzionalità Direct3D 11,1 è costituita dall'API seguente.

-   [**ID3D11DeviceContext1::CSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-csgetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-psgetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vsgetconstantbuffers1)

## <a name="clear-all-or-part-of-a-resource-view"></a>Cancella tutta o parte di una visualizzazione risorse

Direct3D 11,1 consente di cancellare una visualizzazione risorse (RTV, UAV o qualsiasi visualizzazione video di una superficie Texture2D). Si applica lo stesso valore di colore a tutte le parti della visualizzazione.

Questa funzionalità Direct3D 11,1 è costituita dall'API seguente.

-   [**ID3D11DeviceContext1:: ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview)

## <a name="map-srvs-of-dynamic-buffers-with-no_overwrite"></a>Mappare SRVs di buffer dinamici senza \_ sovrascrittura

Direct3D 11,1 consente di mappare le visualizzazioni delle risorse dello shader (SRV) dei buffer dinamici con D3D11 \_ Map \_ Write \_ No \_ overwrite. I runtime Direct3D 11 e versioni precedenti hanno limitato il mapping ai buffer di indice o vertex.

Direct3D 11,1 Aggiorna il metodo [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) per questa funzionalità.

## <a name="use-uavs-at-every-pipeline-stage"></a>Usare UAV in ogni fase della pipeline

Direct3D 11,1 consente di usare le istruzioni seguenti per il modello di shader 5,0 in tutte le fasi dello shader usate in precedenza in solo pixel shader e compute shader.

-   [UAV di DCL \_ \_ tipizzato](/windows/desktop/direct3dhlsl/dcl-uav-typed--sm5---asm-)
-   [\_RAW UAV di DCL \_](/windows/desktop/direct3dhlsl/dcl-uav-raw--sm5---asm-)
-   [\_struttura UAV di DCL \_](/windows/desktop/direct3dhlsl/dcl-uav-structured--sm5---asm-)
-   [LD \_ RAW](/windows/desktop/direct3dhlsl/ld-raw--sm5---asm-)
-   [\_struttura LD](/windows/desktop/direct3dhlsl/ld-structured--sm5---asm-)
-   [LD \_ UAV \_ tipizzato](/windows/desktop/direct3dhlsl/ld-uav-typed--sm5---asm-)
-   [Archivio non \_ elaborato](/windows/desktop/direct3dhlsl/store-raw--sm5---asm-)
-   [archivio \_ strutturato](/windows/desktop/direct3dhlsl/store-structured--sm5---asm-)
-   [archivio \_ UAV \_ tipizzato](/windows/desktop/direct3dhlsl/store-uav-typed--sm5---asm-)
-   [Sincronizza \_ uglobal](/windows/desktop/direct3dhlsl/sync--sm5---asm-)
-   Tutti gli atomici e gli atomici immediati (ad esempio [Atomic \_ and](/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-) e [IMM \_ Atomic \_ e](/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-))

Direct3D 11,1 Aggiorna i metodi seguenti per questa funzionalità.

-   [**Sul ID3D11DeviceContext:: CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**Sul ID3D11DeviceContext:: CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**Sul ID3D11DeviceContext:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**Sul ID3D11DeviceContext:: CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**Sul ID3D11DeviceContext:: CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Queste istruzioni erano disponibili in Direct3D 11,0 in PS \_ 5 \_ 0 e cs \_ 5 \_ 0. Poiché Direct3D 11,1 rende disponibili UAV a tutte le fasi dello shader, queste istruzioni sono disponibili in tutte le fasi dello shader.

Se si passano shader compilati (VS/HS/DS/HS) che usano una di queste istruzioni a una funzione create-shader, ad esempio [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader), nei dispositivi che non supportano UAV in ogni fase (inclusi i driver esistenti non implementati con questa funzionalità), la funzione create-shader ha esito negativo. La funzione create-shader ha esito negativo anche se lo shader tenta di usare uno slot UAV oltre il set di slot UAV supportati dall'hardware.

Le UAV a cui fanno riferimento queste istruzioni sono condivise tra tutte le fasi della pipeline. Ad esempio, un UAV associato allo slot 0 alla [fase di Unione dell'output](d3d10-graphics-programming-guide-output-merger-stage.md) è disponibile nello slot 0 per vs/HS/DS/GS/PS.

Gli accessi UAV che vengono eseguiti all'interno o attraverso fasi dello shader eseguite all'interno di un determinato progetto \* () o che si rilascia dal compute shader all'interno di un dispatch \* () non sono garantiti il completamento nell'ordine in cui sono stati emessi. Tutti gli accessi UAV, tuttavia, terminano alla fine del progetto \* () o dell'invio \* ().

## <a name="extended-support-for-warp-devices"></a>Supporto esteso per i dispositivi WARP

Direct3D 11,1 estende il supporto per i dispositivi [Warp](overviews-direct3d-11-devices-create-warp.md) , che è possibile creare passando il [**tipo di \_ driver D3D \_ \_ Warp**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) nel parametro *DriverType* di [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice).

A partire da Direct3D 11,1 WARP devices support:

-   Tutti i [livelli di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) Direct3D da 9,1 a 11,1
-   [Compute shader](direct3d-11-advanced-stages-compute-shader.md) e [mosaico](direct3d-11-advanced-stages-tessellation.md)
-   Aree condivise. Ovvero è possibile condividere completamente le superfici tra i dispositivi WARP, nonché tra dispositivi WARP in processi diversi.

I dispositivi WARP non supportano le funzionalità facoltative seguenti:

-   [valori Double](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)
-   [codifica o decodifica video](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)
-   [supporto dello shader con precisione minima](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)

Quando si esegue una macchina virtuale (VM), Hyper-V, con la GPU (Graphics Processing Unit) disabilitata o senza un driver visualizzato, si ottiene un dispositivo WARP il cui nome descrittivo è "Microsoft Basic Display Adapter". Questo dispositivo WARP può eseguire l'esperienza completa di Windows, che include DWM, Internet Explorer e app di Windows Store. Questo dispositivo WARP supporta anche l'esecuzione di app legacy che usano [DirectDraw](/windows/desktop/directdraw/directdraw) o app in esecuzione che usano Direct3D 3 con Direct3D 11,1.

## <a name="use-direct3d-in-session-0-processes"></a>Usare Direct3D nei processi della sessione 0

A partire da Windows 8 e Windows Server 2012, è possibile usare la maggior parte delle API Direct3D nei processi della sessione 0.

> [!Note]  
> Queste API di output, di finestra, della catena di scambio e di presentazione non sono disponibili nei processi di sessione 0 perché non si applicano all'ambiente della sessione 0:
>
> -   [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)
> -   [**IDXGIFactory::GetWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-getwindowassociation)
> -   [**IDXGIFactory::MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation)
> -   [**IDXGIAdapter:: EnumOutputs**](/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs)
> -   [**ID3D11Debug::SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)
> -   [**ID3D11Debug::SetPresentPerRenderOpDelay**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setpresentperrenderopdelay)
> -   [**ID3D11Debug::SetSwapChain**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setswapchain)
> -   [**ID3D10Debug::SetFeatureMask**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setfeaturemask)
> -   [**ID3D10Debug::SetPresentPerRenderOpDelay**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setpresentperrenderopdelay)
> -   [**ID3D10Debug::SetSwapChain**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setswapchain)
> -   [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdeviceandswapchain)
> -   [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)
> -   [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)
>
> Se si chiama una delle API precedenti in un processo di sessione 0, viene restituito [**l' \_ errore \_ DXGI \_ attualmente non \_ disponibile**](/windows/desktop/direct3ddxgi/dxgi-error).

 

## <a name="support-for-shadow-buffer-on-feature-level-9"></a>Supporto per il buffer shadow sul livello di funzionalità 9

Usare un subset di Direct3D 10 \_ 0 + funzionalità del buffer shadow per implementare gli effetti di ombreggiatura sul [livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x. Per informazioni sulle operazioni necessarie per implementare gli effetti di ombreggiatura sul livello di funzionalità 9 \_ x, vedere [implementazione di buffer shadow per il livello di funzionalità Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Novità di Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 