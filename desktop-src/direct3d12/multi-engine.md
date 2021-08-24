---
title: Sistemi con più schede
description: Descrive il supporto in Direct3D 12 per i sistemi in cui sono installate più schede, illustrando scenari in cui l'applicazione è destinata in modo esplicito a più schede GPU e scenari in cui i driver usano in modo implicito più schede GPU per conto dell'applicazione.
ms.assetid: CC4C6594-D48F-40C1-93EE-9F98532BC038
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: e76c5c1295dab8858ff04830030efb479fe3ae8a09bcdb37ff8c4820f4fd08c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728817"
---
# <a name="multi-adapter-systems"></a>Sistemi con più schede

Descrive il supporto in Direct3D 12 per i sistemi in cui sono installate più schede, illustrando scenari in cui l'applicazione è destinata in modo esplicito a più schede GPU e scenari in cui i driver usano in modo implicito più schede GPU per conto dell'applicazione.

## <a name="multi-adapter-overview"></a>Panoramica di più schede

Un adattatore GPU può essere qualsiasi scheda (grafica o calcolo, discreta o integrata), di qualsiasi produttore, che supporta Direct3D 12.

A più adattatori viene fatto riferimento come *nodi*. Una serie di elementi, ad esempio le code, si applicano a ogni nodo, quindi se sono presenti due nodi, saranno presenti due code 3D predefinite. Altri elementi, ad esempio lo stato della pipeline e le firme radice e comando, possono fare riferimento a uno o più o a tutti i nodi, come illustrato nel diagramma.

![Le code si applicano a ogni scheda grafica](images/multigpu.png)

## <a name="sharing-heaps-across-adapters"></a>Condivisione di heap tra schede

Vedere [l'argomento Heap](shared-heaps.md) condivisi.

## <a name="multi-adapter-apis-and-node-masks"></a>API con più adattatori e maschere di nodo

Analogamente alle API Direct3D precedenti, ogni set di adattatori collegati viene enumerato come singolo [**oggetto IDXGIAdapter3.**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) Tutti gli output collegati a qualsiasi adattatore nel collegamento vengono enumerati come associati al singolo **oggetto IDXGIAdapter3.**

L'applicazione può determinare il numero di schede fisiche associate a un determinato dispositivo chiamando [**ID3D12Device::GetNodeCount**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount).

Molte API in Direct3D 12 accettano una maschera di nodo *(maschera* di bit), che indica il set di nodi a cui fa riferimento la chiamata API. Ogni nodo ha un indice in base zero. Nella maschera del nodo, tuttavia, zero viene tradotto nel bit 1. 1 viene tradotto nel bit 2; E così via.

### <a name="single-nodes"></a>Nodi singoli

Quando si chiamano le API (nodo singolo) seguenti, l'applicazione specifica un singolo nodo a cui verrà associata la chiamata API. Nella maggior parte dei casi, questo valore viene specificato da una maschera di nodo. Ogni bit nella maschera corrisponde a un singolo nodo. Per tutte le API descritte in questa sezione, è necessario impostare esattamente un bit nella maschera del nodo.

-   [**D3D12 \_ COMMAND \_ QUEUE \_ DESC:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) ha un *membro NodeMask.*
-   [**CreateCommandQueue:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) crea una coda da una [**struttura D3D12 \_ COMMAND QUEUE \_ \_ DESC.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)
-   [**CreateCommandList:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) accetta un *parametro nodeMask.*
-   [**D3D12 \_ DESCRIPTOR \_ HEAP \_ DESC:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) ha un *membro NodeMask.*
-   [**CreateDescriptorHeap:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap) crea un heap descrittore da una [**struttura \_ \_ \_ DESC DELL'HEAP del descrittore D3D12.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)
-   [**D3D12 \_ QUERY \_ HEAP \_ DESC:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) ha un *membro NodeMask.*
-   [**CreateQueryHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap) : crea un heap di query da una [**struttura \_ \_ \_ DESC DELL'HEAP DI QUERY D3D12.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc)

### <a name="multiple-nodes"></a>Più nodi

Quando si chiamano le API seguenti (più nodi), l'applicazione specifica un set di nodi a cui verrà associata la chiamata API. L'affinità dei nodi viene specificata come maschera di nodo, potenzialmente con più bit impostati. Se l'applicazione passa 0 per questa maschera di bit, il driver Direct3D 12 lo converte nella maschera di bit 1 (a indicare che l'oggetto è associato al nodo 0).

-   [**D3D12 \_ LIVELLO \_ DI CONDIVISIONE TRA NODI: \_ \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier) determina il supporto per la condivisione tra nodi.
-   [**D3D12 \_ FEATURE \_ DATA \_ D3D12 \_ OPTIONS:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) struttura che fa riferimento a [**D3D12 \_ CROSS NODE SHARING \_ \_ \_ TIER.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier)
-   [**D3D12 \_ FEATURE \_ DATA \_ ARCHITECTURE:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture) contiene un *membro NodeIndex.*
-   [**D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) ha un *membro NodeMask.*
-   [**CreateGraphicsPipelineState:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) crea un oggetto stato della pipeline grafica da una struttura [**DESC D3D12 \_ GRAPHICS PIPELINE \_ \_ STATE. \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
-   [**D3D12 \_ COMPUTE \_ PIPELINE \_ STATE \_ DESC:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) ha un *membro NodeMask.*
-   [**CreateComputePipelineState:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) crea un oggetto stato della pipeline di calcolo da una struttura [**\_ \_ \_ \_ DESC D3D12 COMPUTE PIPELINE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) STATE.
-   [**CreateRootSignature:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)accetta un *parametro nodeMask.*
-   [**D3D12 \_ COMMAND \_ SIGNATURE \_ DESC:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc)ha un *membro NodeMask.*
-   [**CreateCommandSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) : crea un oggetto firma comando da una [**struttura D3D12 \_ COMMAND SIGNATURE \_ \_ DESC.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc)

### <a name="resource-creation-apis"></a>API di creazione delle risorse

Le API seguenti fanno riferimento alle maschere dei nodi.

-   [**D3D12 \_ PROPRIETÀ \_ HEAP**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) : ha membri *CreationNodeMask* *e VisibleNodeMask.*
-   [**GetResourceAllocationInfo:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) ha un *parametro visibleMask.*
-   [**GetCustomHeapProperties:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) ha un *parametro nodeMask.*

Quando si crea una risorsa riservata, non viene specificato alcun indice di nodo o maschera. La risorsa riservata può essere mappata su un heap in qualsiasi nodo (seguendo le regole di condivisione tra nodi).

Il metodo [**MakeResident**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident) funziona internamente con le code dell'adapter. L'applicazione non deve specificare alcun elemento a questo scopo.

Quando si chiamano le API [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) seguenti, l'applicazione non deve specificare un set di nodi a cui verrà associata la chiamata API perché la chiamata API si applica a tutti i nodi.

-   [**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
-   [**GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
-   [**SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
-   [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
-   [**CreateSampler**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsampler)
-   [**CopyDescriptors**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
-   [**CopyDescriptorsSimple**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
-   [**CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
-   [**OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle) : con un *limite* come parametro. Con una *risorsa o* un *heap come* parametri questo metodo non accetta nodi come parametri perché le maschere di nodo vengono ereditate da oggetti creati in precedenza.
-   [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
-   [**CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)
-   [**CreateUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
-   [**CreateDepthStencilView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview)
-   [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)

## <a name="related-topics"></a>Argomenti correlati

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)