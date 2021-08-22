---
title: Contatori UAV
description: È possibile usare i contatori unordered-access-view (UAV) per associare un contatore atomico a 32 bit a un UAV (Unordered-access-view).
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: c33321b02f22378f4d039137b8ff65559a25a32ed219c2bf336528913777791d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460791"
---
# <a name="uav-counters"></a>Contatori UAV
È possibile usare i contatori unordered-access-view (UAV) per associare un contatore atomico a 32 bit a un UAV (Unordered-access-view).

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a>Differenze nei contatori UAV da Direct3D 11 a Direct3D 12
Le app Direct3D 12 e Direct3D 11 usano entrambe le stesse funzioni shader HLSL (High-Level Shader Language) per accedere ai contatori UAV.

-   **IncrementCounter**
-   **DecrementCounter**
-   **Accoda**
-   **Utilizzo**

### <a name="direct3d-12"></a>Direct3D 12
In Direct3D 12 i valori a 32 bit vengono allocati dall'applicazione, quindi i valori a 32 bit possono essere letti e scritti dalla CPU o dalla GPU, come qualsiasi altra risorsa Direct3D 12.

### <a name="direct3d-11"></a>Direct3D 11
All'esterno degli shader, con Direct3D 11 è necessario chiamare i metodi API per accedere ai contatori , ad esempio [ID3D11DeviceContext::CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount).

## <a name="using-uav-counters"></a>Uso dei contatori UAV
L'app è responsabile dell'allocazione di 32 bit di spazio di archiviazione per i contatori UAV. Questa risorsa di archiviazione può essere allocata in una risorsa diversa come quella che contiene i dati accessibili tramite UAV.

Vedere [**CreateUnorderedAccessView,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview) [**D3D12 \_ BUFFER \_ UAV \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) e [**D3D12 \_ BUFFER \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).

Se *pCounterResource* viene specificato nella chiamata a [**CreateUnorderedAccessView,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)all'UAV è associato un contatore. In questo caso:

-   *StructureByteStride* deve essere maggiore di zero
-   Il formato deve essere DXGI \_ FORMAT \_ UNKNOWN
-   Il flag RAW non deve essere impostato
-   Entrambe le risorse devono essere buffer
-   *CounterOffsetInBytes* deve essere un multiplo di 4 byte
-   *CounterOffsetInBytes* deve essere compreso nell'intervallo della risorsa contatore
-   *pDesc* non può essere NULL
-   *pResource non* può essere NULL

Si notino anche i casi d'uso seguenti:

-   Se *pCounterResource* non viene specificato, *CounterOffsetInBytes* deve essere 0.
-   Se il flag RAW è impostato, il formato deve essere DXGI FORMAT R32 TYPELESS e la risorsa \_ \_ \_ UAV deve essere un buffer.
-   Se *pCounterResource* non è impostato, *CounterOffsetInBytes* deve essere 0.
-   Se il flag RAW non è impostato e *StructureByteStride* = 0, il formato deve essere un formato UAV valido.

Direct3D 12 rimuove la distinzione tra UAV append e counter (anche se la distinzione esiste ancora nel bytecode HLSL).

Il runtime di base convaliderà queste restrizioni all'interno di [**CreateUnorderedAccessView.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)

Durante l'esecuzione di Draw/Dispatch, la risorsa contatore deve essere nello stato [**D3D12 \_ RESOURCE \_ STATE \_ UNORDERED \_ ACCESS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states). Inoltre, all'interno di una singola chiamata Draw/Dispatch, un'applicazione non può accedere alla stessa posizione di memoria a 32 bit tramite due contatori UAV separati. Il livello di debug emettere errori se viene rilevato uno di questi.

Non sono disponibili metodi "SetUnorderedAccessViewCounterValue" o "CopyStructureCount" perché le app possono semplicemente copiare i dati da e verso il valore del contatore direttamente.

È supportata l'indicizzazione dinamica di UAV con contatori.

Se uno shader tenta di accedere al contatore di un UAV a cui non è associato un contatore, il livello di debug genera un avviso e si verifica un errore di pagina GPU che causa la rimozione del dispositivo delle app.

I contatori UAV sono supportati in tutti i tipi di heap (impostazione predefinita, caricamento, readback).

## <a name="related-topics"></a>Argomenti correlati

* [Contatori e query](counters-and-queries.md)