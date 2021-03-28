---
title: Ridimensionamento di pool di riquadri
description: Usare l'API ResizeTilePool di ID3D11DeviceContext2 per aumentare il numero di sezioni se l'applicazione necessita di più working set per il mapping delle risorse affiancate o per compattarla se è necessario meno spazio.
ms.assetid: 529E874E-650B-4BFD-97F6-E66E743564A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86368da46f7c2219f42b5ecbc122b79fee19e72c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855553"
---
# <a name="tile-pool-resizing"></a>Ridimensionamento di pool di riquadri

Usare l'API [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) per espandere un pool di sezioni se l'applicazione necessita di più working set per il mapping delle risorse affiancate o per la compattazione se è necessario meno spazio. Un'altra opzione per le applicazioni consiste nell'allocare ulteriori pool di sezioni per nuove risorse affiancate. Tuttavia, se per una singola risorsa affiancata è necessario più spazio rispetto al primo disponibile nel pool di sezioni, la crescita del pool di riquadri è un'opzione efficace. Una risorsa affiancata non può disporre di mapping in più pool di riquadri nello stesso momento.

Quando si sviluppa un pool di sezioni, alla fine vengono aggiunti riquadri aggiuntivi tramite una o più nuove allocazioni dal driver di visualizzazione. Questa suddivisione in allocazioni non è visibile per l'applicazione. La memoria esistente nel pool di sezioni viene lasciata invariata e i mapping delle risorse affiancate esistenti in tale memoria rimangono intatti.

Quando un pool di sezioni viene compattato, i riquadri vengono rimossi dalla fine. I riquadri vengono rimossi anche sotto le dimensioni di allocazione iniziali, fino a 0, il che significa che non è possibile apportare nuovi mapping oltre le nuove dimensioni. Tuttavia, i mapping esistenti oltre la fine della nuova dimensione rimangono intatti e utilizzabili. Il driver di visualizzazione manterrà la memoria fino a quando i mapping a qualsiasi parte delle allocazioni utilizzate dal driver per la memoria del pool di sezioni rimangono. Se dopo la compattazione di una certa quantità di memoria è stata mantenuta attiva perché i mapping dei riquadri fanno riferimento a essa e il pool di sezioni viene nuovamente riattivato (in base a qualsiasi quantità), la memoria esistente viene riutilizzata prima prima delle allocazioni aggiuntive per il servizio delle dimensioni dell'operazione di aumento.

Per poter risparmiare memoria, un'applicazione non deve solo compattare un pool di sezioni, ma anche rimuovere/rimappare i mapping esistenti oltre la fine delle nuove dimensioni del pool di sezioni più piccole.

L'azione di compattazione (e di rimozione dei mapping) non produce necessariamente risparmi di memoria immediata. La liberazione della memoria dipende dalla granularità delle allocazioni sottostanti del driver di visualizzazione per il pool di sezioni. Quando la compattazione è sufficiente per rendere inutilizzata l'allocazione di un driver di visualizzazione, il driver visualizzato può liberarlo. Se un pool di sezioni è stato aumentato, la riduzione delle dimensioni precedenti (e la rimozione/rimappatura dei mapping dei riquadri corrispondenti) è più probabile che restituisca un risparmio di memoria, sebbene non sia garantita nel caso in cui le dimensioni non siano esattamente allineate con le dimensioni di allocazione sottostanti scelte dal driver di visualizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping inclusi in un pool di riquadri](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




