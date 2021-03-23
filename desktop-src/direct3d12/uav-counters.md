---
title: Contatori UAV
description: È possibile usare i contatori di Access-View (UAV) non ordinati per associare un contatore atomico a 32 bit a una visualizzazione non ordinata (UAV).
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: 94bc1492e3b984d96c76788430d2e63c0672ca76
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104548817"
---
# <a name="uav-counters"></a>Contatori UAV
È possibile usare i contatori di Access-View (UAV) non ordinati per associare un contatore atomico a 32 bit a una visualizzazione non ordinata (UAV).

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a>Differenze nei contatori UAV da Direct3D 11 a Direct3D 12
Le app Direct3D 12 e Direct3D 11 usano entrambe le stesse funzioni shader HLSL (High-Level Shader Language) per accedere ai contatori UAV.

-   **IncrementCounter**
-   **DecrementCounter**
-   **Accoda**
-   **Utilizzo**

### <a name="direct3d-12"></a>Direct3D 12
In Direct3D 12, i valori a 32 bit vengono allocati dall'applicazione, quindi i valori a 32 bit possono essere letti e scritti dalla CPU o dalla GPU, esattamente come qualsiasi altra risorsa Direct3D 12.

### <a name="direct3d-11"></a>Direct3D 11
Al di fuori degli shader, con Direct3D 11 è necessario chiamare i metodi API per accedere ai contatori (ad esempio, [sul ID3D11DeviceContext:: CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).

## <a name="using-uav-counters"></a>Uso dei contatori UAV
L'app è responsabile dell'allocazione di 32 bit di archiviazione per i contatori UAV. Questo spazio di archiviazione può essere allocato in una risorsa diversa da quella che contiene i dati accessibili tramite il UAV.

Vedere [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12 \_ buffer \_ UAV \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) e [**D3D12 \_ buffer \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).

Se nella chiamata a [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)è specificato *pCounterResource* , è presente un contatore associato a UAV. In questo caso:

-   *StructureByteStride* deve essere maggiore di zero
-   Il formato del formato deve essere DXGI \_ \_ sconosciuto
-   Non è necessario impostare il flag RAW
-   Entrambe le risorse devono essere buffer
-   *CounterOffsetInBytes* deve essere un multiplo di 4 byte
-   *CounterOffsetInBytes* deve essere compreso nell'intervallo della risorsa contatore
-   *pDesc* non può essere null
-   la *preorigine* non può essere null

E si notino i casi d'uso seguenti:

-   Se *pCounterResource* non è specificato, *CounterOffsetInBytes* deve essere 0.
-   Se viene impostato il flag RAW, il formato deve essere DXGI \_ Format \_ R32 senza \_ tipo e la risorsa UAV deve essere un buffer.
-   Se *pCounterResource* non è impostato, *CounterOffsetInBytes* deve essere 0.
-   Se il flag RAW non è impostato e *StructureByteStride* = 0, il formato deve essere un formato UAV valido.

Direct3D 12 rimuove la distinzione tra Append e Counter UAV (anche se la distinzione esiste ancora nel bytecode HLSL).

Il runtime di base convaliderà queste restrizioni all'interno di [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).

Durante il progetto o la distribuzione, la risorsa contatore deve trovarsi nello stato della [**\_ risorsa D3D12 \_ \_ \_ accesso non ordinato**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states). Inoltre, all'interno di una singola chiamata di estrazione/invio, non è valido per un'applicazione accedere alla stessa posizione di memoria a 32 bit tramite due contatori UAV distinti. Il livello di debug emetterà errori se viene rilevata una di queste.

Non sono disponibili metodi "SetUnorderedAccessViewCounterValue" o "CopyStructureCount" perché le app possono semplicemente copiare i dati direttamente da e verso il valore del contatore.

L'indicizzazione dinamica di UAV con contatori è supportata.

Se uno shader tenta di accedere al contatore di un UAV a cui non è associato alcun contatore, il livello di debug emetterà un avviso e si verificherà un errore di pagina GPU causando la rimozione del dispositivo dell'app.

I contatori UAV sono supportati in tutti i tipi di heap (impostazione predefinita, upload, readback).

## <a name="related-topics"></a>Argomenti correlati

* [Contatori e query](counters-and-queries.md)