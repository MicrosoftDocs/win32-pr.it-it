---
title: Funzionalità di Direct3D 11.1
description: La funzionalità seguente è stata aggiunta in Direct3D 11.1, inclusa in Windows 8, Windows RT e Windows Server 2012.
ms.assetid: 2203D2D2-ECF6-4753-90FA-12A52678DFBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee5f4721a9f7ef7727539387603e839f36690ed5d4b6762121ceddefa0672ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535966"
---
# <a name="direct3d-111-features"></a>Funzionalità di Direct3D 11.1

La funzionalità seguente è stata aggiunta in Direct3D 11.1, inclusa in Windows 8, Windows RT e Windows Server 2012. Il supporto parziale per [Direct3D 11.1](direct3d-11-features.md) è disponibile in Windows 7 e Windows Server 2008 R2 tramite l'aggiornamento della piattaforma [per Windows 7,](/windows/desktop/direct3darticles/platform-update-for-windows-7)disponibile tramite l'aggiornamento della piattaforma per [Windows 7.](https://support.microsoft.com/kb/2670838)

-   [Funzionalità di traccia dello shader e miglioramenti del compilatore](#shader-tracing-and-compiler-enhancements)
-   [Condivisione di dispositivi Direct3D](#direct3d-device-sharing)
-   [Verificare il supporto delle nuove funzionalità e formati di Direct3D 11.1](#check-support-of-new-direct3d-111-features-and-formats)
-   [Usare la precisione minima HLSL](#use-hlsl-minimum-precision)
-   [Specificare i piani di ritaglio utente in HLSL a livello di funzionalità 9 e versioni successive](#specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Creare buffer costanti più grandi di quelli a cui può accedere uno shader](#create-larger-constant-buffers-than-a-shader-can-access)
-   [Usare operazioni logiche in una destinazione di rendering](#use-logical-operations-in-a-render-target)
-   [Forzare il conteggio dei campioni per creare uno stato di rasterizzazione](#force-the-sample-count-to-create-a-rasterizer-state)
-   [Elaborare risorse video con shader](#process-video-resources-with-shaders)
-   [Supporto esteso per le risorse Texture2D condivise](#extended-support-for-shared-texture2d-resources)
-   [Modificare le sottorisorse con le nuove opzioni di copia](#change-subresources-with-new-copy-options)
-   [Rimuovere le risorse e le visualizzazioni delle risorse](#discard-resources-and-resource-views)
-   [Supportare un numero maggiore di UAV](#support-a-larger-number-of-uavs)
-   [Associare un intervallo secondario di un buffer costante a uno shader](#bind-a-subrange-of-a-constant-buffer-to-a-shader)
-   [Recuperare l'intervallo secondario di un buffer costante associato a uno shader](#retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader)
-   [Cancellare tutto o parte di una visualizzazione delle risorse](#clear-all-or-part-of-a-resource-view)
-   [Eseguire il mapping dei buffer dinamici con NO \_ OVERWRITE](/windows)
-   [Usare UAV in ogni fase della pipeline](#use-uavs-at-every-pipeline-stage)
-   [Supporto esteso per i dispositivi WARP](#extended-support-for-warp-devices)
-   [Usare Direct3D nei sessione 0 processi](#use-direct3d-in-session-0-processes)
-   [Supporto per il buffer ombreggiato nel livello di funzionalità 9](#support-for-shadow-buffer-on-feature-level-9)
-   [Argomenti correlati](#related-topics)

## <a name="shader-tracing-and-compiler-enhancements"></a>Funzionalità di traccia dello shader e miglioramenti del compilatore

Direct3D 11.1 consente di usare la traccia shader per assicurarsi che il codice funzioni come previsto e, in caso contrario, è possibile individuare e risolvere il problema. Il Windows Software Development Kit (SDK) per Windows 8 contiene miglioramenti del compilatore HLSL. La traccia shader e il compilatore HLSL vengono implementati in D3dcompiler \_nn.dll.

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
-   [**ID3D11ShaderTrace::GetStep**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getstep)
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

La libreria D3dcompiler.lib richiede D3dcompiler \_nn.dll. Questa DLL non fa parte di Windows 8; si trova nella cartella bin di Windows SDK per Windows 8 insieme alla Fxc.exe della riga di comando del compilatore \\ HLSL.

> [!Note]  
> Anche se è possibile usare questa combinazione di libreria e DLL per lo sviluppo, non è possibile distribuire app Windows Store che usano questa combinazione. È quindi necessario compilare gli shader HLSL prima di spedire l'app Windows Store. È possibile scrivere file binari di compilazione HLSL su disco oppure il compilatore può generare intestazioni con matrici di byte statiche che contengono i dati BLOB shader. Usare [**l'interfaccia ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) per accedere ai dati BLOB. Per sviluppare l'app Windows Store, chiamare [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2) o [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) per compilare l'origine HLSL non elaborata e quindi compilare i dati BLOB risultanti in Direct3D.

 

## <a name="direct3d-device-sharing"></a>Condivisione di dispositivi Direct3D

Direct3D 11.1 consente alle API Direct3D 10 e Direct3D 11 di usare un dispositivo di rendering sottostante.

Questa funzionalità direct3D 11.1 è costituita dai metodi e dall'interfaccia seguenti.

-   [**ID3D11Device1::CreateDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate)
-   [**ID3D11DeviceContext1::SwapDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate)
-   [**ID3DDeviceContextState**](/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate)

## <a name="check-support-of-new-direct3d-111-features-and-formats"></a>Verificare il supporto delle nuove funzionalità e formati di Direct3D 11.1

Direct3D 11.1 consente di verificare la presenza di nuove funzionalità supportate dal driver di grafica e di nuovi modi in cui un formato è supportato in un dispositivo. Microsoft DirectX Graphic Infrastructure (DXGI) 1.2 specifica anche nuovi [**valori DXGI \_ FORMAT.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Questa funzionalità direct3D 11.1 è costituita dall'API seguente.

-   [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) [**D3D11 \_ FEATURE DATA ARCHITECTURE \_ \_ \_ INFO,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info) [**D3D11 \_ FEATURE DATA \_ \_ D3D9 \_ OPTIONS,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options) [**D3D11 \_ FEATURE DATA SHADER MIN PRECISION \_ \_ \_ \_ \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)e [**D3D11 \_ FEATURE DATA \_ \_ D3D9 \_ SHADOW \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support) structures
-   [**ID3D11Device::CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) with [**D3D11 \_ FORMAT SUPPORT \_ \_ DECODER \_ OUTPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), [**D3D11 FORMAT SUPPORT \_ VIDEO PROCESSOR \_ \_ \_ \_ OUTPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), [**D3D11 \_ FORMAT SUPPORT VIDEO PROCESSOR \_ \_ \_ \_ INPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), [**D3D11 \_ FORMAT SUPPORT VIDEO \_ \_ \_ ENCODER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)e [**D3D11 \_ FORMAT \_ SUPPORT2 OUTPUT MERGER LOGIC \_ \_ \_ \_ OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)

## <a name="use-hlsl-minimum-precision"></a>Usare la precisione minima HLSL

A partire da Windows 8, i driver di grafica possono implementare tipi di dati [scalari HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) con precisione minima usando qualsiasi precisione maggiore o uguale alla precisione in bit specificata. Quando il codice HLSL minimum precision shader viene usato nell'hardware che implementa la precisione minima HLSL, si usa una minore larghezza di banda di memoria e di conseguenza si usa anche meno potenza del sistema.

È possibile eseguire una query per ottenere il supporto della precisione minima fornito dal driver di grafica chiamando [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con il [**valore D3D11 \_ FEATURE SHADER MIN PRECISION \_ \_ \_ \_ SUPPORT.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) In questa chiamata **ID3D11Device::CheckFeatureSupport** passare un puntatore a una struttura [**D3D11 \_ FEATURE DATA SHADER MIN PRECISION \_ \_ \_ \_ \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support) che **ID3D11Device::CheckFeatureSupport** riempie con i livelli di precisione minimi supportati dal driver per la fase pixel shader e per altre fasi dello shader. Le informazioni restituite indicano semplicemente che l'hardware grafico può eseguire operazioni HLSL a una precisione inferiore rispetto alla precisione float standard a 32 bit, ma non garantisce che l'hardware grafico verrà effettivamente eseguito a una precisione inferiore.

Non è necessario creare più shader che esere e non usano la precisione minima. Creare invece shader con precisione minima e le variabili di precisione minima si comportano a una precisione a 32 bit completa se il driver di grafica segnala che non supporta alcuna precisione minima. Per altre informazioni sulla precisione minima HLSL, vedere [Uso della precisione minima HLSL.](/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision)

Gli shader di precisione minima HLSL non funzionano nei sistemi operativi precedenti a Windows 8.

## <a name="specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Specificare i piani di ritaglio utente in HLSL a livello di funzionalità 9 e versioni successive

A partire da Windows 8, è possibile usare l'attributo della [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-syntax) funzione **clipplanes** in una dichiarazione di funzione HLSL anziché [SV \_ ClipDistance](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) per far funzionare lo shader sul livello di funzionalità [9](overviews-direct3d-11-devices-downlevel-intro.md) x e sul livello di funzionalità 10 e versioni \_ successive. Per altre informazioni, vedere [Piani di ritaglio utente nell'hardware del livello di funzionalità 9.](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)

## <a name="create-larger-constant-buffers-than-a-shader-can-access"></a>Creare buffer costanti più grandi di quelli a cui può accedere uno shader

Direct3D 11.1 consente di creare buffer costanti maggiori della dimensione massima del buffer costante a cui può accedere uno shader (4096 costanti a 4 componenti a 32 bit \* - 64 KB). Successivamente, quando si associano i buffer alla pipeline, ad esempio tramite [**PSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers) o [**PSSetConstantBuffers1,**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)è possibile specificare un intervallo di buffer a cui lo shader può accedere entro il limite 4096.

Direct3D 11.1 aggiorna il [**metodo ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) per questa funzionalità.

## <a name="use-logical-operations-in-a-render-target"></a>Usare operazioni logiche in una destinazione di rendering

Direct3D 11.1 consente di usare operazioni logiche anziché la fusione in una destinazione di rendering. Tuttavia, non è possibile combinare le operazioni logiche con la fusione tra più destinazioni di rendering.

Questa funzionalità direct3D 11.1 è costituita dall'API seguente.

-   [**ID3D11Device1::CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1) con [ **D3D11 \_ LOGIC \_ OP**](/windows/desktop/api/D3D11_1/ne-d3d11_1-d3d11_logic_op)

## <a name="force-the-sample-count-to-create-a-rasterizer-state"></a>Forzare il conteggio dei campioni per creare uno stato di rasterizzazione

Direct3D 11.1 consente di specificare un conteggio dei campioni di forza quando si crea uno stato di rasterizzazione.

Questa funzionalità direct3D 11.1 è costituita dall'API seguente.

-   [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)

> [!Note]  
>
> Se si vuole eseguire il rendering con il numero di campioni forzato a 1 o superiore, è necessario seguire queste linee guida:
>
> -   Non associare visualizzazioni depth-stencil.
> -   Disabilitare il test di profondità.
> -   Verificare che lo shader non eserciti l'output della profondità.
> -   Se sono presenti visualizzazioni di destinazione di rendering associate ([**D3D11 \_ BIND \_ RENDER \_ TARGET**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)) ed è stato forzato il conteggio dei campioni su un valore maggiore di 1, assicurarsi che ogni destinazione di rendering abbia un solo campione.
> -   Non usare lo shader alla frequenza di campionamento. PERTANTO, [**ID3D11ShaderReflection::IsSampleFrequencyShader**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11shaderreflection-issamplefrequencyshader) restituisce **FALSE.**
>
> In caso contrario, il comportamento di rendering non è definito. Per informazioni su come configurare depth-stencil, vedere [Configuring Depth-Stencil Functionality](d3d10-graphics-programming-guide-depth-stencil.md).

 

## <a name="process-video-resources-with-shaders"></a>Elaborare risorse video con shader

Direct3D 11.1 consente di creare visualizzazioni (SRV/RTV/UAV) per le risorse video in modo che gli shader Direct3D possano elaborare tali risorse video. Il formato di una risorsa video sottostante limita i formati che la visualizzazione può usare. [**L'enumerazione DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) contiene nuovi valori di formato di risorsa video. Questi **valori DXGI \_ FORMAT** specificano i formati di visualizzazione validi che è possibile creare e il modo in cui il runtime Direct3D 11.1 esegue il mapping della vista. È possibile creare più viste di parti diverse della stessa superficie e, a seconda del formato, le dimensioni delle viste possono differire l'una dall'altra.

Direct3D 11.1 aggiorna i metodi seguenti per questa funzionalità.

-   [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)
-   [**ID3D11Device::CreateRenderTargetView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview)
-   [**ID3D11Device::CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview)

## <a name="extended-support-for-shared-texture2d-resources"></a>Supporto esteso per le risorse Texture2D condivise

Direct3D 11.1 garantisce la condivisione delle risorse Texture2D create con tipi e formati di risorse specifici. Per condividere le risorse Texture2D, usare [**D3D11 \_ RESOURCE \_ MISC \_ SHARED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag), [**D3D11 \_ RESOURCE \_ MISC SHARED \_ \_ KEYEDMUTEX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)o una combinazione dei flag **D3D11 \_ RESOURCE \_ MISC SHARED \_ \_ KEYEDMUTEX** e [**D3D11 \_ RESOURCE \_ MISC SHARED \_ \_ NTHANDLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) (novità per Windows 8) quando si creano tali risorse.

Direct3D 11.1 garantisce la condivisione delle risorse Texture2D create con questi [**valori DXGI \_ FORMAT:**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

-   FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM
-   FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM \_ SRGB
-   FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM
-   FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM \_ SRGB
-   FORMATO DXGI \_ \_ B8G8R8X8 \_ UNORM
-   FORMATO DXGI \_ \_ B8G8R8X8 \_ UNORM \_ SRGB
-   FORMATO DXGI \_ \_ R10G10B10A2 \_ UNORM
-   FORMATO DXGI \_ \_ R16G16B16A16 \_ FLOAT

Direct3D 11.1 garantisce inoltre che sia possibile condividere le risorse Texture2D create con un livello mipmap di 1, dimensioni della matrice di 1, flag di associazione della risorsa [**\_ BIND \_ SHADER \_ D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) e [**D3D11 \_ BIND RENDER \_ \_ TARGET**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) combinati, valore predefinito di utilizzo ([**D3D11 \_ USAGE \_ DEFAULT)**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)e solo questi valori [**D3D11 \_ RESOURCE \_ MISC \_ FLAG:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

-   [**RISORSA D3D11 \_ \_ CONDIVISA MISC \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**RISORSA D3D11 \_ \_ MISC \_ SHARED \_ KEYEDMUTEX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**RISORSA D3D11 \_ \_ MISC \_ \_ NTHANDLE CONDIVISO**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**RISORSA D3D11 \_ \_ COMPATIBILE CON \_ GDI MISC \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

Direct3D 11.1 consente di condividere una maggiore varietà di tipi e formati di risorse Texture2D. È possibile eseguire una query per verificare se il driver grafico e l'hardware supportano la condivisione estesa delle risorse Texture2D chiamando [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con il valore [**\_ \_ D3D11 FEATURE D3D11 \_ OPTIONS.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) In questa **chiamata ID3D11Device::CheckFeatureSupport** passare un puntatore a una [**struttura D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) **ID3D11Device::CheckFeatureSupport** imposta il membro **ExtendedResourceSharing** di **D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS** su **TRUE** se l'hardware e il driver supportano la condivisione estesa delle risorse Texture2D.

Se [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) restituisce **TRUE** in **ExtendedResourceSharing**, è possibile condividere le risorse create con questi [**valori DXGI \_ FORMAT:**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

-   FORMATO DXGI \_ \_ R32G32B32A32 \_ SENZA TIPI
-   FORMATO DXGI \_ \_ R32G32B32A32 \_ FLOAT
-   FORMATO DXGI \_ \_ R32G32B32A32 \_ UINT
-   FORMATO DXGI \_ \_ R32G32B32A32 \_ SINT
-   FORMATO DXGI \_ \_ R16G16B16A16 \_ SENZA TIPI
-   FORMATO DXGI \_ \_ R16G16B16A16 \_ FLOAT
-   FORMATO DXGI \_ \_ R16G16B16A16 \_ UNORM
-   FORMATO DXGI \_ \_ R16G16B16A16 \_ UINT
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM
-   FORMATO DXGI \_ \_ R16G16B16A16 \_ SINT
-   FORMATO DXGI \_ \_ R10G10B10A2 \_ UNORM
-   DXGI \_ FORMAT \_ R10G10B10A2 \_ UINT
-   FORMATO DXGI \_ \_ R8G8B8A8 \_ SENZA TIPI
-   FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM
-   FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ UINT
-   FORMATO DXGI \_ \_ R8G8B8A8 \_ SNORM
-   FORMATO DXGI \_ \_ R8G8B8A8 \_ SINT
-   FORMATO DXGI \_ \_ B8G8R8A8 \_ SENZA TIPO
-   FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM
-   FORMATO DXGI \_ \_ B8G8R8X8 \_ UNORM
-   FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM \_ SRGB
-   FORMATO DXGI \_ \_ B8G8R8X8 \_ SENZA TIPI
-   FORMATO DXGI \_ \_ B8G8R8X8 \_ UNORM \_ SRGB
-   FORMATO DXGI \_ \_ R32 \_ SENZA TIPI
-   FORMATO DXGI \_ \_ R32 \_ FLOAT
-   DXGI \_ FORMAT \_ R32 \_ UINT
-   SINT FORMATO DXGI \_ \_ R32 \_
-   FORMATO DXGI \_ \_ R16 \_ SENZA TIPI
-   FORMATO DXGI \_ \_ R16 \_ FLOAT
-   FORMATO DXGI \_ \_ R16 \_ UNORM
-   DXGI \_ FORMAT \_ R16 \_ UINT
-   DXGI \_ FORMAT \_ R16 \_ SNORM
-   SINT FORMATO DXGI \_ \_ R16 \_
-   FORMATO DXGI \_ \_ R8 \_ SENZA TIPI
-   FORMATO DXGI \_ \_ R8 \_ UNORM
-   DXGI \_ FORMAT \_ R8 \_ UINT
-   DXGI \_ FORMAT \_ R8 \_ SNORM
-   SINT FORMATO DXGI \_ \_ R8 \_
-   FORMATO DXGI \_ \_ A8 \_ UNORM
-   FORMATO DXGI \_ \_ AYUV
-   FORMATO DXGI \_ \_ YUY2
-   FORMATO DXGI \_ \_ NV12
-   FORMATO DXGI \_ \_ NV11
-   FORMATO DXGI \_ \_ P016
-   FORMATO DXGI \_ \_ P010
-   FORMATO DXGI \_ \_ Y216
-   FORMATO DXGI \_ \_ Y210
-   FORMATO DXGI \_ \_ Y416
-   FORMATO DXGI \_ \_ Y410

Se [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) restituisce **TRUE** in **ExtendedResourceSharing**, è possibile condividere le risorse create con queste funzionalità e flag:

-   [**D3D11 \_ USAGE \_ DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)
-   [**RISORSA BIND SHADER D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**DESTINAZIONE DI RENDERING DEL BINDING D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 \_ RESOURCE \_ MISC \_ GENERATE \_ MIPS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ BIND \_ UNORDERED \_ ACCESS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   Livelli mipmap (uno o più livelli) nelle risorse di trama 2D (specificati nel membro **MipLevels** di [**D3D11 \_ TEXTURE2D \_ DESC)**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)
-   Matrici di risorse trama 2D (una o più trame) (specificate nel membro **ArraySize** [**di D3D11 \_ TEXTURE2D \_ DESC)**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)
-   [**DECODIFICATORE D3D11 \_ \_ BIND**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**CONTENUTO CON RESTRIZIONI \_ \_ MISC DELLA RISORSA D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**RISORSA D3D11 \_ \_ MISC \_ RESTRICT SHARED \_ \_ RESOURCE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ RESOURCE \_ MISC \_ RESTRICT \_ SHARED \_ RESOURCE \_ DRIVER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

> [!Note]  
> Quando **ExtendedResourceSharing è** **TRUE,** si ha maggiore flessibilità quando si specificano flag di associazione per la condivisione delle risorse Texture2D. Non solo il driver grafico e l'hardware supportano più flag di associazione, ma anche combinazioni più possibili di flag di associazione. Ad esempio, è possibile specificare solo [**D3D11 \_ BIND \_ RENDER \_ TARGET**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) o nessun flag di associazione e così via.

 

Anche se [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) restituisce **TRUE** in **ExtendedResourceSharing,** non è comunque possibile condividere le risorse create con queste funzionalità e flag:

-   [**D3D11 \_ BIND \_ DEPTH \_ STENCIL**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   Risorse di trama 2D in modalità di anti-aliasing multicampionamento (MSAA) (specificata con [**DXGI \_ SAMPLE \_ DESC)**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
-   [**D3D11 \_ RESOURCE \_ MISC \_ RESOURCE \_ CLAMP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ USAGE \_ IMMUTABLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), [**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)o [**D3D11 \_ USAGE \_ STAGING**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) (ovvero mappabile)
-   [**RISORSA D3D11 \_ \_ MISC \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="change-subresources-with-new-copy-options"></a>Modificare le sottorisorse con le nuove opzioni di copia

Direct3D 11.1 consente di usare nuovi flag di copia per copiare e aggiornare le sottorisorse. Quando si copia una sottorisorsa, le risorse di origine e di destinazione possono essere identiche e le aree di origine e di destinazione possono sovrapporsi.

Questa funzionalità direct3D 11.1 è costituita dall'API seguente.

-   [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)
-   [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)

## <a name="discard-resources-and-resource-views"></a>Rimuovere le risorse e le visualizzazioni delle risorse

Direct3D 11.1 consente di rimuovere le risorse e le visualizzazioni delle risorse dal contesto di dispositivo. Questa nuova funzionalità informa la GPU che il contenuto esistente nelle risorse o nelle visualizzazioni delle risorse non è più necessario.

Questa funzionalità direct3D 11.1 è costituita dall'API seguente.

-   [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource)
-   [**ID3D11DeviceContext1::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview)
-   [**ID3D11DeviceContext1::D iscardView1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview1)

## <a name="support-a-larger-number-of-uavs"></a>Supportare un numero maggiore di UAV

Direct3D 11.1 consente di usare un numero maggiore di UAV quando si associano risorse alla fase di [unione dell'output](d3d10-graphics-programming-guide-output-merger-stage.md) e quando si imposta una matrice di viste per una risorsa non ordinata.

Direct3D 11.1 aggiorna i metodi seguenti per questa funzionalità.

-   [**ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews)
-   [**ID3D11DeviceContext::CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)

## <a name="bind-a-subrange-of-a-constant-buffer-to-a-shader"></a>Associare un intervallo secondario di un buffer costante a uno shader

Direct3D 11.1 consente di associare un intervallo secondario di un buffer costante a cui uno shader può accedere. È possibile fornire un buffer costante più grande e specificare l'intervallo secondario che lo shader può usare.

Questa funzionalità direct3D 11.1 è costituita dall'API seguente.

-   [**ID3D11DeviceContext1::CSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-cssetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dssetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gssetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hssetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vssetconstantbuffers1)

## <a name="retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader"></a>Recuperare l'intervallo secondario di un buffer costante associato a uno shader

Direct3D 11.1 consente di recuperare l'intervallo secondario di un buffer costante associato a uno shader.

Questa funzionalità direct3D 11.1 è costituita dall'API seguente.

-   [**ID3D11DeviceContext1::CSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-csgetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-psgetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vsgetconstantbuffers1)

## <a name="clear-all-or-part-of-a-resource-view"></a>Cancellare tutto o parte di una visualizzazione delle risorse

Direct3D 11.1 consente di cancellare una visualizzazione risorse (RTV, UAV o qualsiasi visualizzazione video di una superficie Texture2D). Lo stesso valore di colore viene applicato a tutte le parti della visualizzazione.

Questa funzionalità direct3D 11.1 è costituita dall'API seguente.

-   [**ID3D11DeviceContext1::ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview)

## <a name="map-srvs-of-dynamic-buffers-with-no_overwrite"></a>Eseguire il mapping degli SRV dei buffer dinamici con NO \_ OVERWRITE

Direct3D 11.1 consente di eseguire il mapping delle visualizzazioni delle risorse shader (SRV) dei buffer dinamici con D3D11 \_ MAP \_ WRITE NO \_ \_ OVERWRITE. I runtime Direct3D 11 e precedenti limitano il mapping ai buffer dei vertici o degli indici.

Direct3D 11.1 aggiorna il [**metodo ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) per questa funzionalità.

## <a name="use-uavs-at-every-pipeline-stage"></a>Usare gli UAV in ogni fase della pipeline

Direct3D 11.1 consente di usare le istruzioni del modello di shader 5.0 seguenti in tutte le fasi dello shader usate in precedenza solo in pixel shader e compute shader.

-   [dcl \_ uav \_ typed](/windows/desktop/direct3dhlsl/dcl-uav-typed--sm5---asm-)
-   [dcl \_ uav \_ raw](/windows/desktop/direct3dhlsl/dcl-uav-raw--sm5---asm-)
-   [dcl \_ uav \_ structured](/windows/desktop/direct3dhlsl/dcl-uav-structured--sm5---asm-)
-   [ld \_ raw](/windows/desktop/direct3dhlsl/ld-raw--sm5---asm-)
-   [ld \_ structured](/windows/desktop/direct3dhlsl/ld-structured--sm5---asm-)
-   [ld \_ uav \_ typed](/windows/desktop/direct3dhlsl/ld-uav-typed--sm5---asm-)
-   [archiviare dati \_ non elaborati](/windows/desktop/direct3dhlsl/store-raw--sm5---asm-)
-   [store \_ structured](/windows/desktop/direct3dhlsl/store-structured--sm5---asm-)
-   [store \_ uav \_ typed](/windows/desktop/direct3dhlsl/store-uav-typed--sm5---asm-)
-   [sync \_ uglobal](/windows/desktop/direct3dhlsl/sync--sm5---asm-)
-   Tutti gli atomici e gli atomici immediati (ad esempio [atomic \_ e](/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-) [e imm atomic \_ \_ e](/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-))

Direct3D 11.1 aggiorna i metodi seguenti per questa funzionalità.

-   [**ID3D11DeviceContext::CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**ID3D11DeviceContext::CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**ID3D11DeviceContext::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**ID3D11DeviceContext::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**ID3D11DeviceContext::CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Queste istruzioni erano disponibili in Direct3D 11.0 in ps \_ 5 \_ 0 e cs \_ 5 \_ 0. Poiché Direct3D 11.1 rende disponibili gli UAV in tutte le fasi dello shader, queste istruzioni sono disponibili in tutte le fasi dello shader.

Se si passano shader compilati (VS/HS/DS/HS) che usano una di queste istruzioni a una funzione di creazione shader, ad esempio [**CreateVertexShader,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)su dispositivi che non supportano UAV in ogni fase (inclusi i driver esistenti che non sono implementati con questa funzionalità), la funzione create-shader ha esito negativo. La funzione create-shader ha esito negativo anche se lo shader tenta di usare uno slot UAV oltre il set di slot UAV supportati dall'hardware.

Gli UAV a cui fanno riferimento queste istruzioni sono condivisi tra tutte le fasi della pipeline. Ad esempio, un UAV associato allo slot 0 nella fase di [unione dell'output](d3d10-graphics-programming-guide-output-merger-stage.md) è disponibile nello slot 0 a VS/HS/DS/GS/PS.

Gli accessi UAV rilasciati dall'interno o tra le fasi dello shader eseguite all'interno di un determinato draw () o rilasciati dal compute shader all'interno di un Dispatch () non sono garantiti per terminare nell'ordine in cui sono stati \* \* rilasciati. Ma tutti gli accessi UAV terminano alla fine di Draw \* () o Dispatch \* ().

## <a name="extended-support-for-warp-devices"></a>Supporto esteso per i dispositivi WARP

Direct3D 11.1 estende il supporto per i dispositivi [WARP,](overviews-direct3d-11-devices-create-warp.md) che vengono creati passando [**D3D \_ DRIVER TYPE \_ \_ WARP**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) nel *parametro DriverType* di [**D3D11CreateDevice.**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)

A partire dai dispositivi WARP Direct3D 11.1, è possibile:

-   Tutti i livelli di [funzionalità Direct3D](overviews-direct3d-11-devices-downlevel-intro.md) da 9.1 a 11.1
-   [Compute shaders](direct3d-11-advanced-stages-compute-shader.md) and [tessellation](direct3d-11-advanced-stages-tessellation.md)
-   Superfici condivise. Ciò significa che è possibile condividere completamente le superfici tra dispositivi WARP, nonché tra dispositivi WARP in processi diversi.

I dispositivi WARP non supportano queste funzionalità facoltative:

-   [Doppie](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)
-   [codifica o decodifica video](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)
-   [supporto per shader con precisione minima](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)

Quando si esegue una macchina virtuale (VM), Hyper-V, con l'unità di elaborazione grafica (GPU) disabilitata o senza un driver di visualizzazione, si ottiene un dispositivo WARP il cui nome descrittivo è "Scheda video Microsoft Basic". Questo dispositivo WARP può eseguire l'esperienza Windows, che include le app DWM, Internet Explorer e Windows Store. Questo dispositivo WARP supporta anche l'esecuzione di app legacy che usano [DirectDraw](/windows/desktop/directdraw/directdraw) o app in esecuzione che usano Direct3D da 3 a Direct3D 11.1.

## <a name="use-direct3d-in-session-0-processes"></a>Usare Direct3D in sessione 0 processi

A partire Windows 8 e Windows Server 2012, è possibile usare la maggior parte delle API Direct3D sessione 0 processi.

> [!Note]  
> Questi output, finestre, catena di scambio e API correlate alla presentazione non sono disponibili nei processi sessione 0 perché non si applicano all'ambiente sessione 0:
>
> -   [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)
> -   [**IDXGIFactory::GetWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-getwindowassociation)
> -   [**IDXGIFactory::MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation)
> -   [**IDXGIAdapter::EnumOutputs**](/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs)
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
> Se si chiama una delle API precedenti in un processo sessione 0, restituisce [**ERRORE DXGI \_ NON ATTUALMENTE \_ \_ \_ DISPONIBILE**](/windows/desktop/direct3ddxgi/dxgi-error).

 

## <a name="support-for-shadow-buffer-on-feature-level-9"></a>Supporto per il buffer ombreggiato nel livello di funzionalità 9

Usare un subset di funzionalità del buffer ombreggiatura Direct3D 10 0+ per implementare effetti di ombreggiatura sul \_ livello di [funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x. Per informazioni sulle attività da eseguire per implementare gli effetti di ombreggiatura sul livello di funzionalità 9 x, vedere Implementazione di buffer ombreggiatura per la funzionalità \_ [Direct3D livello 9.](/previous-versions/windows/apps/jj262110(v=win.10))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Novità di Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 