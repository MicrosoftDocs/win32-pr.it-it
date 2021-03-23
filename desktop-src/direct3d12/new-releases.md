---
title: Novità di Direct3D 12
description: In questo argomento viene descritta la nuova documentazione più significativa di Direct3D 12 disponibile per diverse versioni.
ms.assetid: 38F41E05-FECB-41DE-8D30-09733FBEAC48
ms.localizationpriority: high
ms.topic: article
ms.date: 12/05/2019
ms.openlocfilehash: ec3ecc9e68fc4711def2c364793eca32804d8d04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548773"
---
# <a name="whats-new-in-direct3d-12"></a>Novità di Direct3D 12

In questo argomento viene descritta la nuova documentazione più significativa di Direct3D 12 disponibile per diverse versioni.

Per informazioni su come ottenere e installare Direct3D, vedere [configurazione dell'ambiente di programmazione Direct3D 12](./directx-12-programming-environment-set-up.md).

## <a name="direct3d-12-on-windows-7"></a>Direct3D 12 in Windows 7

- [Direct3D 12 in Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/) è ora disponibile per l'uso da parte degli sviluppatori.

## <a name="windows-10-may-2019-update"></a>Aggiornamento di Windows 10 di maggio 2019

Queste funzionalità e API sono state aggiunte o aggiornate per Windows 10, versione 1903 (10,0; Build 18362) &mdash; Nota anche come Windows 10 May 2019 Update.

- [Ombreggiatura a frequenza variabile (VRS)](./vrs.md). Consente di allocare prestazioni/potenza di rendering a frequenze che variano nell'immagine di cui è stato eseguito il rendering.
- [Modello HLSL shader 6,4](../direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12.md). Descrive gli intrinseci di Machine Learning aggiunti al modello HLSL shader 6,4.
- Enumerazione [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version) . Definisce le costanti che specificano una versione del dispositivo rimossi dati estesi (eseguire).
- Struttura [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) . Indica il livello di supporto fornito dall'adapter per i metacomandi.
- Struttura [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command) . Indica il livello di supporto fornito dall'adapter per i metacomandi.
- Enumerazione [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) . Definisce le costanti che specificano un livello di frequenza ombreggiatura (per l'ombreggiatura a frequenza variabile o VRS).
- Interfaccia [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) e relativi metodi. Utilizzato per impostare la modalità per le ottimizzazioni di elaborazione in background del driver. Vedere anche [ottimizzazioni dello shader di background](https://devblogs.microsoft.com/directx/background-shader-optimizations/).
- Interfaccia [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) e relativi metodi. Fornisce l'accesso in fase di esecuzione ai dati dei dati estesi (eseguire) rimossi dal dispositivo.
- Interfaccia [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) e relativi metodi. Controlla le impostazioni dei dati estesi (eseguire) rimossi dal dispositivo.
- Interfaccia [**D3D12GraphicsCommandList5**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist5) e relativi metodi. Supporto per l'ombreggiatura a frequenza variabile (VRS).

L'enumerazione [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) è stata aggiornata con l'aggiunta della costante **D3D_SHADER_MODEL_6_5** (una funzionalità a livello sperimentale).

L'enumerazione [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) è stata aggiornata con l'aggiunta della costante **D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE** .

L'enumerazione [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) è stata aggiornata con l'aggiunta delle costanti **D3D12_FEATURE_D3D12_OPTIONS6** e **D3D12_FEATURE_QUERY_META_COMMAND** .

L'enumerazione [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) è stata aggiornata con l'aggiunta della costante **D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE** .

## <a name="windows-10-version-1809"></a>Windows 10, versione 1809

Queste funzionalità e API sono state aggiunte o aggiornate per Windows 10, versione 1809 (10,0; Build 17763) &mdash; Nota anche come aggiornamento di Windows 10 ottobre 2018.

- [Direct3D 12 raytracing](./direct3d-12-raytracing.md)
- [Passaggi di rendering di Direct3D 12](./direct3d-12-render-passes.md)

## <a name="windows-10-version-1709"></a>Windows 10, versione 1709

Queste interfacce sono state aggiunte alla documentazione di Direct3D per Windows 10, versione 1709.

-   [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) estende la funzionalità di creazione di recinzioni supportando il recupero dei flag passati per creare la recinzione.
-   [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) estende l'elenco dei comandi grafici disponibili, supportando la scrittura di valori immediati direttamente in un buffer.
-   [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) estende la funzionalità della scheda virtuale creando heap di diagnostica per scopi specifici nella memoria di sistema che permangono anche in caso di errore GPU o di uno scenario rimosso da dispositivo.

Per descrivere il modello di shader 6,1, è stata aggiunta l'enumerazione del [**\_ \_ modello D3D Shader**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) con un nuovo valore di **D3D \_ shader \_ Model \_ 6 \_ 1** .

L'enumerazione della [**\_ funzionalità D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) include anche la **nuova \_ funzionalità D3D12 \_ D3D12 \_ OPTIONS3** e **D3D12 sono presenti valori di \_ \_ \_ heap esistenti** . Come implicano i nomi, questi valori consentono di controllare altre opzioni di Direct3D12, oltre a verificare il supporto degli heap esistenti.

## <a name="windows-10-version-1703"></a>Windows 10 versione 1703

Questi argomenti sono stati aggiunti alla documentazione di Direct3D per Windows 10, versione 1703.

-   Il metodo [**ID3D12Device2:: CreatePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) e la struttura del flusso di stato della [**\_ pipeline \_ \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) rappresentano un modo nuovo e più affidabile per creare PSO e unificano i interfaccia per la creazione di pipeline di calcolo e grafica.
-   Il metodo [**ID3D12Device1:: CreatePipelineLibrary1**](https://www.bing.com/search?q=**ID3D12Device1::CreatePipelineLibrary1**) espande l'interfaccia della libreria di pipeline per accettare il PSO creato con la nuova struttura unificata del flusso di stato della [**\_ pipeline \_ \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) .
-   La funzione [**D3D12EnableExperimentalFeatures**](/windows/win32/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) consente agli sviluppatori di sperimentare determinate funzionalità di sviluppo usando un computer in modalità sviluppatore.
-   Sono disponibili cinque nuove interfacce (fare riferimento alla [gerarchia](interface-hierarchy.md)delle interfacce):
    -   [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1)
    -   [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1)
    -   [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2)
    -   [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2)
    -   [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools)
-   Vedere la [Panoramica del modello di shader HLSL 6,0](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md), che descrive le operazioni intrinseche Wave per pixel e compute shader multithread.
-   L'uso di [**ID3D12Device:: SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) è stato modificato.
-   Alcune nuove funzionalità per Direct3D 11 sono descritte in [funzionalità di direct3d 11,4](../direct3d11/direct3d-11-4-features.md).
-   [**AtomicCopyBufferUINT**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint) e [**AtomicCopyBufferUINT64**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64) abilitano il **latch tardivo** per ridurre la latenza pervieved.
-   [**ID3D12Device2:: CreatePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) e [**OMSetDepthBounds**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-omsetdepthbounds) consentono di **testare i limiti di profondità** nell'hardware supportato.
-   [**ResolveSubresourceRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion) consente la **risoluzione parziale** delle sottorisorse per consentire l'ottimizzazione delle prestazioni.
-   [**SetSamplePositions**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) Abilita le **posizioni di esempio programmabili** nell'hardware supportato.

## <a name="november-2016-documentation-update"></a>Aggiornamento della documentazione di novembre 2016

-   Revisione delle osservazioni per [**ID3D12GraphicsCommandList::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource).
-   Chiarimento del "decadimento dello stato in comune" (vedere [uso delle barriere delle risorse per sincronizzare gli Stati delle risorse in Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)).
-   Il file di intestazione D3dx12. h, a cui si fa riferimento in [strutture e funzioni helper per D3D12](helper-structures-and-functions-for-d3d12.md), può essere scaricato direttamente dalla [libreria helper D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).

## <a name="august-2016-documentation-update-2"></a>Aggiornamento della documentazione di 2016 agosto 2

-   Una nuova sezione della guida intitolata [informazioni sul livello di debug di D3D12](understanding-the-d3d12-debug-layer.md).

    Sono descritte tre nuove interfacce del livello di debug (in modalità di anteprima): [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1), [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1), [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1).

## <a name="august-2016-documentation-update-1"></a>Aggiornamento 1 della documentazione di agosto 2016

-   Revisione dell' [utilizzo delle barriere delle risorse per sincronizzare gli Stati delle risorse in Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).
-   Revisione dell' [accesso alle risorse](./user-mode-heap-synchronization.md#multi-queue-resource-access)con più code.

## <a name="windows-10-version-1607"></a>Windows 10 versione 1607

Questi argomenti sono stati aggiunti alla documentazione di Direct3D per Windows 10, versione 1607.

-   [Firma radice versione 1,1](root-signature-version-1-1.md) : Panoramica delle firme radice aggiornate, che consentono alle app di specificare come descrittori e dati statici o volatili sono in grado di supportare le ottimizzazioni dei driver grafici.
-   Il metodo [**ID3D12Device1:: CreatePipelineLibrary**](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary) descrive i vantaggi della creazione di una libreria di pipeline.
-   Sono disponibili tre nuove interfacce (fare riferimento alla [gerarchia](interface-hierarchy.md)delle interfacce):
    -   [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary)
    -   [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1)
    -   [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer)
-   Vedere la [Panoramica del modello di shader HLSL 6,0](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md), che descrive le operazioni intrinseche Wave per pixel e compute shader multithread.
-   L'uso di [**ID3D12Device:: SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) è stato modificato.
-   Alcune nuove funzionalità per Direct3D 11 sono descritte in [funzionalità di direct3d 11,4](../direct3d11/direct3d-11-4-features.md).
-   L'intervallo di librerie supportate per Direct3D 12 è stato aggiornato. vedere la sezione **strumenti e librerie supportate** della pagina relativa alla [configurazione dell'ambiente di programmazione Direct3D 12](directx-12-programming-environment-set-up.md).
-   [Uso di DirectX con schermi HDR e colori avanzati](../direct3darticles/high-dynamic-range.md)
-   [Visualizzazione frequenza di aggiornamento variabili](../direct3ddxgi/variable-refresh-rate-displays.md)
-   [Miglioramenti di DXGI 1,5](../direct3ddxgi/dxgi-1-5-improvements.md)

## <a name="related-topics"></a>Argomenti correlati

* [Guida per programmatori Direct3D 12](directx-12-programming-guide.md)