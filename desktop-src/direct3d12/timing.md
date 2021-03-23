---
title: Temporizzazione (grafica Direct3D 12)
description: In questa sezione viene illustrata l'esecuzione di query sui timestamp e la calibratura dei contatori di timestamp CPU e GPU.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: a1f58e231315e95bbf9178994f8c52303fc0d4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/21/2020
ms.locfileid: "104548897"
---
# <a name="timing-direct3d-12-graphics"></a>Temporizzazione (grafica Direct3D 12)

In questa sezione viene illustrata l'esecuzione di query sui timestamp e la calibratura dei contatori di timestamp CPU e GPU.

## <a name="timestamp-frequency"></a>Frequenza timestamp

L'applicazione può eseguire una query sulla frequenza del timestamp GPU in base alla coda per ogni comando (vedere il metodo [**ID3D12CommandQueue:: GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) ).

La frequenza restituita è misurata in Hz (cicli/sec). Se la coda di comandi specificata non supporta i timestamp (vedere la tabella nella sezione [query](queries.md) ), l'API ha esito negativo e restituisce **E_FAIL**. [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) e [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) supportano sempre i timestamp. [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) supporta facoltativamente i timestamp se il membro [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) è **true**.

## <a name="timestamp-calibration"></a>Calibrazione timestamp

D3D12 consente alle applicazioni di correlare i risultati ottenuti dalle query timestamp con i risultati ottenuti dalla chiamata a `QueryPerformanceCounter` . Questo è abilitato dalla chiamata [**ID3D12CommandQueue:: GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).

[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) campiona il contatore dei timestamp della GPU per una coda di comandi specificata ed esegue il campionamento del contatore della CPU `QueryPerformanceCounter` quasi allo stesso tempo. Anche in questo caso, l'API ha esito negativo \_ , se la coda di comandi specificata non supporta i timestamp, ovvero la restituzione di un errore. vedere la tabella nell'argomento [query](queries.md) .

Si noti che i contatori di timestamp della GPU e della CPU non sono necessariamente correlati direttamente alla velocità di clock di questi processori, ma funzionano invece con i tick del timestamp.

## <a name="timestamp-queries"></a>Query timestamp

È possibile ottenere i timestamp come parte di un elenco di comandi, anziché una chiamata lato CPU in una coda di comandi, tramite le query timestamp. (Per altre informazioni sulle query in generale, vedere [query](queries.md) ). 

Tutte le query timestamp utilizzano il tipo [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) per la query effettiva. Tuttavia, a causa delle limitazioni hardware, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) e [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) utilizzano un [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) diverso da quello utilizzato da [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) .

Le code Direct e COMPUTE utilizzano [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Le code di copia utilizzano [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Le query della coda di copia sono supportate solo se il membro [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) è **true**.

Le query timestamp, dopo essere state risolte tramite [**ID3D12GraphicsCommandList:: ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), sono un **UInt64** che rappresenta i cicli, così come viene restituito da [**ID3D12CommandQueue:: GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)e, di conseguenza, deve essere diviso per la frequenza della coda per ottenere la lunghezza in secondi.

> [!IMPORTANT]
> Per maggiore precisione, usare l'aritmetica a virgola mobile durante il calcolo di intervalli di secondi o millisecondi di timestamp. Usare, ad esempio, `queriedTicks / (double)Frequency` invece di `queriedTicks / Frequency`.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contatori e query](counters-and-queries.md)
</dt> <dt>

[**ID3D12Device::SetStablePowerState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[**ID3D12Object:: nome**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[Misurazione delle prestazioni](performance-measurement.md)
</dt> </dl>
