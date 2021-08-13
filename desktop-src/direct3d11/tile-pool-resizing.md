---
title: Ridimensionamento di pool di riquadri
description: Usare l'API ResizeTilePool ID3D11DeviceContext2 per aumentare le dimensioni di un pool di riquadri se l'applicazione richiede più working set per il mapping delle risorse affiancate o per ridurlo se è necessario meno spazio.
ms.assetid: 529E874E-650B-4BFD-97F6-E66E743564A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b91e3942e5da88c58c391f652a2b23a7b02513777060d78e86522b892da478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119375811"
---
# <a name="tile-pool-resizing"></a>Ridimensionamento di pool di riquadri

Usare l'API [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) per aumentare le dimensioni di un pool di riquadri se l'applicazione necessita di più working set per il mapping delle risorse affiancate o per ridurlo se è necessario meno spazio. Un'altra opzione per le applicazioni è allocare pool di riquadri aggiuntivi per le nuove risorse affiancate. Tuttavia, se una singola risorsa affiancata necessita di più spazio rispetto a quanto inizialmente disponibile nel pool di riquadri, l'aumento del pool di riquadri è un'opzione valida. Una risorsa affiancata non può avere mapping in più pool di riquadri contemporaneamente.

Quando un pool di riquadri aumenta, vengono aggiunti riquadri aggiuntivi alla fine tramite una o più nuove allocazioni da parte del driver video. Questa suddivisione in allocazioni non è visibile all'applicazione. La memoria esistente nel pool di riquadri rimane invariata e i mapping delle risorse affiancate esistenti in tale memoria rimangono intatti.

Quando un pool di riquadri viene ridotto, i riquadri vengono rimossi dalla fine. I riquadri vengono rimossi anche al di sotto delle dimensioni di allocazione iniziale, fino a 0, il che significa che non è possibile creare nuovi mapping oltre le nuove dimensioni. Tuttavia, i mapping esistenti oltre la fine della nuova dimensione rimangono intatti e utilizzabili. Il driver di visualizzazione manterà la memoria fino a quando rimangono i mapping a qualsiasi parte delle allocazioni utilizzate dal driver per la memoria del pool di riquadri. Se dopo la compattazione della memoria è stata mantenuta attiva perché i mapping dei riquadri puntano a essa e quindi il pool di riquadri viene rieffezione (di qualsiasi quantità), la memoria esistente viene riutilizzata prima che si verifichino allocazioni aggiuntive per supportare le dimensioni dell'operazione di crescita.

Per risparmiare memoria, un'applicazione deve non solo compattare un pool di riquadri, ma anche rimuovere/modificare il mapping dei mapping esistenti oltre la fine delle nuove dimensioni del pool di riquadri più piccole.

L'azione di compattazione (e rimozione dei mapping) non produce necessariamente risparmi immediati sulla memoria. La liberazione della memoria dipende dal livello di granularità delle allocazioni sottostanti del driver video per il pool di riquadri. Quando la compattazione è sufficiente per rendere inutilizzata l'allocazione di un driver video, il driver di visualizzazione può liberarlo. Se un pool di riquadri è stato aumentato, la riduzione delle dimensioni precedenti (e la rimozione o il mapping corrispondente dei mapping dei riquadri) hanno maggiori probabilità di produrre risparmi di memoria, anche se non garantiti nel caso in cui le dimensioni non siano esattamente allineate con le dimensioni di allocazione sottostanti scelte dal driver video.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping inclusi in un pool di riquadri](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




