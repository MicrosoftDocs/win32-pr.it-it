---
title: Contatori di output di flusso
description: L'output di flusso è la capacità della GPU di scrivere vertici in un buffer. I contatori di output del flusso monitorano lo stato di avanzamento.
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00cc3d78314b5c9130f69c65ebc5fa056d51d7305135025ecf2e4329ecbe6350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989471"
---
# <a name="stream-output-counters"></a>Contatori di output di flusso

L'output di flusso è la capacità della GPU di scrivere vertici in un buffer. I contatori di output del flusso monitorano lo stato di avanzamento.

-   [Differenze nei contatori di flusso da Direct3D 11 a Direct3D 12](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [BufferFilledSize](#bufferfilledsize)
-   [Argomenti correlati](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a>Differenze nei contatori di flusso da Direct3D 11 a Direct3D 12

Come parte del processo di output del flusso, la GPU deve conoscere la posizione corrente nel buffer in cui sta scrivendo. In Direct3D 11 la memoria per archiviare questo percorso viene allocata dal driver e l'unico modo per modificare questo valore da parte delle applicazioni è tramite il metodo **SOSetTargets.** In Direct3D 12 le app allocano memoria per archiviare la posizione corrente. Non esistono modi speciali per modificare questo valore e le app possono leggere/scrivere il valore con la CPU o la GPU.

## <a name="bufferfilledsize"></a>BufferFilledSize

L'applicazione è responsabile dell'allocazione dell'archiviazione per una quantità a 32 bit denominata *BufferFilledSize*. Contiene il numero di byte di dati nel buffer di output del flusso. Questa risorsa di archiviazione può essere inserita nella stessa risorsa o in una risorsa diversa rispetto a quella che contiene i dati di output del flusso. Questo valore è accessibile dalla GPU nella fase stream-output per determinare dove aggiungere nuovi dati dei vertici nel buffer. Inoltre, questo valore è accessibile dalla GPU per determinare quando si è verificato l'overflow.

Fare riferimento alla struttura [**D3D12 \_ STREAM \_ OUTPUT \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).

Il livello di debug convaliderà quanto segue in [**ID3D12GraphicsCommandList::SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):

-   *BufferFilledSize* rientra nell'intervallo implicito tra {*OffsetInBytes*, *SizeInBytes*}, se viene specificata una risorsa non NULL.
-   *BufferFilledSizeOffsetInBytes* è un multiplo di 4.
-   *BufferFilledSizeOffsetInBytes* è compreso nell'intervallo della risorsa contenitore.
-   La risorsa specificata è un buffer.

Il runtime non convaliderà il tipo di heap associato al buffer di output del flusso, perché l'output del flusso è supportato in tutti i tipi di heap.

Le firme radice devono specificare se verrà usato l'output del flusso usando i flag [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)

D3D12 ROOT SIGNATURE FLAG ALLOW STREAM OUTPUT può essere specificato per le firme radice scritte \_ \_ in \_ \_ \_ \_ HLSL, in modo simile a come vengono specificati gli altri flag.

[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) avrà esito negativo se lo shader geometry contiene stream-output, ma per la firma radice non è impostato il flag D3D12 \_ ROOT SIGNATURE FLAG ALLOW STREAM \_ \_ \_ \_ \_ OUTPUT.

Quando una risorsa viene usata come destinazione di output di flusso, le risorse usate devono essere nello stato D3D12 \_ RESOURCE \_ STATE STREAM \_ \_ OUT. Questo vale sia per i dati dei vertici che *per BufferFilledSize* (che possono essere nella stessa risorsa o in risorse separate).

Non sono disponibili API speciali per impostare gli offset del buffer di output di flusso perché le applicazioni possono scrivere direttamente in *BufferFilledSize* con la CPU o la GPU.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contatori e query](counters-and-queries.md)
</dt> </dl>

 

 




