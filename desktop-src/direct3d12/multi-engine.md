---
title: Sistemi con più adapter
description: Viene descritto il supporto in Direct3D 12 per i sistemi in cui sono installati più adapter, coprendo scenari in cui l'applicazione è destinata in modo esplicito a più adapter GPU e scenari in cui i driver utilizzano in modo implicito più schede GPU per conto dell'applicazione.
ms.assetid: CC4C6594-D48F-40C1-93EE-9F98532BC038
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d7d3985c880c4d1732a96b98ac6d3c6579dab8e6
ms.sourcegitcommit: 9d530b0a2396f2274e9ed693c1f5f10556aadebb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/09/2020
ms.locfileid: "104548791"
---
# <a name="multi-adapter-systems"></a>Sistemi con più adapter

Viene descritto il supporto in Direct3D 12 per i sistemi in cui sono installati più adapter, coprendo scenari in cui l'applicazione è destinata in modo esplicito a più adapter GPU e scenari in cui i driver utilizzano in modo implicito più schede GPU per conto dell'applicazione.

## <a name="multi-adapter-overview"></a>Panoramica di più adapter

Un adattatore GPU può essere qualsiasi adattatore (grafica o calcolo, discreto o integrato), da qualsiasi produttore, che supporta Direct3D 12.

Viene fatto riferimento a più adapter come *nodi*. Un numero di elementi, ad esempio le code, si applica a ogni nodo, quindi se sono presenti due nodi, saranno presenti due code 3D predefinite. Altri elementi, ad esempio lo stato della pipeline e le firme dei comandi e della radice, possono fare riferimento a uno o più o a tutti i nodi, come illustrato nel diagramma.

![le code si applicano a ogni scheda grafica](images/multigpu.png)

## <a name="sharing-heaps-across-adapters"></a>Condivisione degli heap tra gli adapter

Vedere l'argomento [heap condivisi](shared-heaps.md) .

## <a name="multi-adapter-apis-and-node-masks"></a>API per più adapter e maschere di nodi

Analogamente alle API Direct3D precedenti, ogni set di adattatori collegati viene enumerato come un singolo oggetto [**IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) . Tutti gli output collegati a qualsiasi adapter nel collegamento vengono enumerati come allegati al singolo oggetto **IDXGIAdapter3** .

L'applicazione può determinare il numero di schede fisiche associate a un determinato dispositivo chiamando [**ID3D12Device:: GetNodeCount**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount).

Molte API in Direct3D 12 accettano una *maschera del nodo* (maschera di bit), che indica il set di nodi a cui fa riferimento la chiamata API. Ogni nodo dispone di un indice in base zero. Tuttavia, nella maschera del nodo, zero viene convertito in bit 1; 1 viene convertito in bit 2; E così via.

### <a name="single-nodes"></a>Nodi singoli

Quando si chiamano le API seguenti (nodo singolo), l'applicazione specifica un singolo nodo a cui verrà associata la chiamata API. Nella maggior parte dei casi, questa impostazione è specificata da una maschera del nodo. Ogni bit nella maschera corrisponde a un singolo nodo. Per tutte le API descritte in questa sezione, è necessario impostare esattamente un bit nella maschera del nodo.

-   [**D3D12 \_ \_Coda comandi \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) : è membro di *node mask* .
-   [**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : crea una coda da una [**struttura \_ \_ \_ desc della coda dei comandi di D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .
-   [**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : accetta un parametro *node mask* .
-   [**D3D12 \_ Descrizione \_ heap \_ descrittore**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) : ha un membro *node mask* .
-   [**CreateDescriptorHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap) : crea un heap descrittore da una struttura di [**\_ Descrizione dell' \_ heap \_ del descrittore D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) .
-   [**D3D12 \_ QUERY \_ heap \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) : ha un membro *node mask* .
-   [**CreateQueryHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap) : crea un heap di query da una struttura di [**\_ Descrizione dell' \_ heap \_ della query D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) .

### <a name="multiple-nodes"></a>Più nodi

Quando si chiamano le API seguenti (più nodi), l'applicazione specifica un set di nodi a cui verrà associata la chiamata API. È possibile specificare l'affinità del nodo come una maschera del nodo, potenzialmente con più bit impostati. Se l'applicazione passa 0 per questa maschera di bit, il driver Direct3D 12 lo converte nella maschera di bit 1 (a indicare che l'oggetto è associato al nodo 0).

-   [**D3D12 \_ \_Livello di \_ condivisione \_ tra nodi**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier) : determina il supporto per la condivisione tra nodi.
-   [**D3D12 \_ FUNZIONALITÀ \_ dati \_ D3D12 \_ Opzioni**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : struttura che fa riferimento al [**\_ \_ livello di \_ condivisione \_ tra nodi D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier).
-   [**D3D12 \_ \_ \_ Architettura dei dati delle funzionalità**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture) : contiene un membro *NodeIndex* .
-   [**D3D12 \_ \_Stato della pipeline grafica \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) : è membro di *node mask* .
-   [**CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) : crea un oggetto di stato della pipeline grafica da una struttura [**\_ desc di \_ \_ stato \_ della pipeline grafica D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) .
-   [**D3D12 \_ Compute \_ pipeline \_ state \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) : ha un membro *node mask* .
-   [**CreateComputePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) : crea un oggetto di stato della pipeline di calcolo dalla struttura [**desc di stato della \_ pipeline di calcolo \_ \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) .
-   [**CreateRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature): accetta un parametro *node mask* .
-   [**D3D12 \_ Firma del comando \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc): è membro di *node mask* .
-   [**CreateCommandSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) : crea un oggetto della firma del comando dalla struttura [**\_ desc della \_ firma \_ del comando D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc) .

### <a name="resource-creation-apis"></a>API per la creazione di risorse

Le API seguenti fanno riferimento a maschere del nodo.

-   [**D3D12 \_ \_Proprietà heap**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) : include sia membri *CreationNodeMask* che *VisibleNodeMask* .
-   [**GetResourceAllocationInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) : ha un parametro *visibleMask* .
-   [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) : ha un parametro *node mask* .

Quando si crea una risorsa riservata, non viene specificato alcun indice o maschera del nodo. È possibile eseguire il mapping della risorsa riservata a un heap in qualsiasi nodo, seguendo le regole di condivisione tra nodi.

Il metodo [**MakeResident**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident) funziona internamente con le code degli adapter. non è necessario che l'applicazione specifichi alcun elemento per questo.

Quando si chiamano le API [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) seguenti, l'applicazione non deve specificare un set di nodi a cui verrà associata la chiamata API perché la chiamata API viene applicata a tutti i nodi.

-   [**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
-   [**GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
-   [**SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
-   [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
-   [**CreateSampler**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsampler)
-   [**CopyDescriptors**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
-   [**CopyDescriptorsSimple**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
-   [**CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
-   [**OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle) : con una *recinzione* come parametro. Con una *risorsa* o un *heap* come parametri questo metodo non accetta nodi come parametri perché le maschere del nodo vengono ereditate dagli oggetti creati in precedenza.
-   [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
-   [**CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)
-   [**CreateUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
-   [**CreateDepthStencilView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview)
-   [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)

## <a name="related-topics"></a>Argomenti correlati

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)