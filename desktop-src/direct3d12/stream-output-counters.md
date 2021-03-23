---
title: Contatori output flusso
description: L'output del flusso è la capacità della GPU di scrivere i vertici in un buffer. Lo stato del monitoraggio dei contatori di output del flusso.
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d2f3a823f5f4b5d2d5f365235d7e3f8817207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103408"
---
# <a name="stream-output-counters"></a>Contatori output flusso

L'output del flusso è la capacità della GPU di scrivere i vertici in un buffer. Lo stato del monitoraggio dei contatori di output del flusso.

-   [Differenze nei contatori dei flussi da Direct3D 11 a Direct3D 12](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [BufferFilledSize](#bufferfilledsize)
-   [Argomenti correlati](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a>Differenze nei contatori dei flussi da Direct3D 11 a Direct3D 12

Come parte del processo di output del flusso, la GPU deve conoscerne la posizione corrente nel buffer in cui sta scrivendo. In Direct3D 11 la memoria per archiviare questo percorso viene allocata dal driver e l'unico modo per le applicazioni di modificare questo valore è tramite il metodo **SOSetTargets** . In Direct3D 12, le app allocano memoria per archiviare questo percorso corrente. Non esistono metodi speciali per modificare questo valore e le app possono leggere/scrivere il valore con CPU o GPU.

## <a name="bufferfilledsize"></a>BufferFilledSize

L'applicazione è responsabile dell'allocazione di spazio di archiviazione per una quantità a 32 bit denominata *BufferFilledSize*. Contiene il numero di byte di dati nel buffer di output del flusso. Questo spazio di archiviazione può essere inserito nello stesso o in una risorsa diversa da quella che contiene i dati di output del flusso. Questo valore è accessibile dalla GPU nella fase Stream-output per determinare la posizione in cui aggiungere i nuovi dati dei vertici nel buffer. Questo valore è inoltre accessibile dalla GPU per determinare quando si è verificato l'overflow.

Vedere la struttura [**D3D12 \_ Stream \_ output \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).

Il livello di debug convaliderà quanto segue in [**ID3D12GraphicsCommandList:: SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):

-   *BufferFilledSize* rientra nell'intervallo implicito da {*OffsetInBytes*, *sizeInBytes*} se è specificata una risorsa non null.
-   *BufferFilledSizeOffsetInBytes* è un multiplo di 4.
-   *BufferFilledSizeOffsetInBytes* è compreso nell'intervallo della risorsa che lo contiene.
-   La risorsa specificata è un buffer.

Il runtime non convaliderà il tipo di heap associato al buffer di output del flusso, perché l'output del flusso è supportato in tutti i tipi di heap.

Le firme radice devono specificare se l'output del flusso verrà usato, usando i flag dei [**\_ \_ \_ flag di firma radice D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) .

\_ \_ Il flag di firma radice D3D12 consente di \_ \_ \_ \_ specificare l'output del flusso per le firme radice create in HLSL, in modo analogo a come vengono specificati gli altri flag.

[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) avrà esito negativo se il geometry shader contiene l'output del flusso ma la firma radice non ha il flag di \_ firma radice D3D12 \_ \_ \_ Consenti \_ set di flag di output del flusso \_ .

Quando una risorsa viene usata come destinazione di output del flusso, le risorse usate devono trovarsi nello \_ stato del flusso di stato della risorsa D3D12 \_ \_ \_ . Questo vale sia per i dati dei vertici sia per i *BufferFilledSize* (che possono trovarsi nelle stesse risorse o in risorse separate).

Non sono disponibili API speciali per impostare gli offset del buffer di output del flusso perché le applicazioni possono scrivere direttamente nella *BufferFilledSize* con la CPU o la GPU.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contatori e query](counters-and-queries.md)
</dt> </dl>

 

 




