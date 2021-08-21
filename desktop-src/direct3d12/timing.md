---
title: Intervallo (grafica Direct3D 12)
description: Questa sezione illustra l'esecuzione di query dei timestamp e la calibrazione dei contatori dei timestamp della GPU e della CPU.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84676d36523fe23d33946e164d245e1619eb41d0af11a898acc52194348e439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045369"
---
# <a name="timing-direct3d-12-graphics"></a>Intervallo (grafica Direct3D 12)

Questa sezione illustra l'esecuzione di query dei timestamp e la calibrazione dei contatori dei timestamp della GPU e della CPU.

## <a name="timestamp-frequency"></a>Frequenza timestamp

L'applicazione può eseguire query sulla frequenza del timestamp GPU in base alla coda per comando (fare riferimento al [**metodo ID3D12CommandQueue::GetTimestampFrequency).**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)

La frequenza restituita viene misurata in Hz (tick/sec). Se la coda di comandi specificata non supporta i [](queries.md) timestamp (vedere la tabella nella sezione Query), l'API ha esito negativo e restituisce **E_FAIL**). [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) e [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) supportano sempre i timestamp. [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) supporta facoltativamente i timestamp se il membro [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) è **TRUE.**

## <a name="timestamp-calibration"></a>Calibrazione del timestamp

D3D12 consente alle applicazioni di correlare i risultati ottenuti dalle query timestamp con i risultati ottenuti dalla chiamata a `QueryPerformanceCounter` . Questa funzionalità è abilitata dalla chiamata [**ID3D12CommandQueue::GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).

[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) esegue il contatore timestamp GPU per una determinata coda di comandi ed esegue il contatore della CPU tramite `QueryPerformanceCounter` quasi nello stesso momento. Anche in questo caso l'API ha esito negativo (restituisce E FAIL) se la coda di comandi specificata non supporta i timestamp (vedere la \_ tabella [nell'argomento Query).](queries.md)

Si noti che i contatori di timestamp DELLA GPU e CPU non sono necessariamente direttamente correlati alla velocità di clock di questi processori, ma funzionano dai tick di timestamp.

## <a name="timestamp-queries"></a>Query timestamp

È possibile ottenere timestamp come parte di un elenco di comandi (anziché una chiamata sul lato CPU in una coda di comandi) tramite query timestamp. Per altre [informazioni sulle](queries.md) query in generale, vedere Query. 

Tutte le query timestamp usano il [**tipo D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) per la query effettiva. Tuttavia, a causa di limitazioni [**hardware,**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) D3D12_COMMAND_LIST_TYPE_DIRECT e [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) [](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) usano un D3D12_QUERY_HEAP_TYPE diverso da quello che D3D12_COMMAND_LIST_TYPE_COPY [**usa.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)

Le code dirette e di calcolo [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Le code di copia usano [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Le query della coda di copia sono [**supportate solo se il membro D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) è **TRUE.**

Le query timestamp, una volta risolte tramite [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), sono **un UINT64** che rappresenta i tick, come viene restituito da [**ID3D12CommandQueue::GetClockCalibration,**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)e di conseguenza deve essere diviso per la frequenza della coda per ottenere la lunghezza in secondi.

> [!IMPORTANT]
> Per l'accuratezza, usare l'aritmetica a virgola mobile quando si calcolano intervalli di secondi o millisecondi di timestamp. Usare, ad esempio, `queriedTicks / (double)Frequency` invece di `queriedTicks / Frequency`.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contatori e query](counters-and-queries.md)
</dt> <dt>

[**ID3D12Device::SetStablePowerState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[**ID3D12Object::SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[Misurazione delle prestazioni](performance-measurement.md)
</dt> </dl>
