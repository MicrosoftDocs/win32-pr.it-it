---
title: Sottoallocazione all'interno dei buffer
description: I buffer hanno tutte le funzionalità necessarie in D3D12 per le applicazioni per trasferire un'ampia gamma di dati temporanei dalla CPU alla GPU. Questa sezione illustra quattro scenari comuni per l'uso e la gestione di risorse e buffer.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63175bdb8b3937a01abe3ffc57032db78ea978768ee19e2c31d0c50db4103573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123814"
---
# <a name="suballocation-within-buffers"></a>Sottoallocazione all'interno dei buffer

I buffer hanno tutte le funzionalità necessarie in D3D12 per le applicazioni per trasferire un'ampia gamma di dati temporanei dalla CPU alla GPU. Questa sezione illustra quattro scenari comuni per l'uso e la gestione di risorse e buffer.

Analogamente a D3D11, le applicazioni in D3D12 devono comunque dichiarare l'utilizzo della memoria durante l'allocazione di buffer in D3D12 rispetto alle risorse dinamiche/di staging in D3D11, ma in D3D12 gli sviluppatori hanno una maggiore flessibilità e un controllo più stretto sull'utilizzo della memoria. I buffer, tramite la sottoallocazione, hanno tutte le funzionalità necessarie per la gestione della memoria di basso livello.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Caricamento di diversi tipi di risorse](uploading-resources.md)<br/>                 | Illustra come usare un buffer per caricare sia i dati costanti del buffer che i dati del buffer dei vertici nella GPU e come sottoallocare e inserire correttamente i dati all'interno dei buffer. L'uso di un singolo buffer aumenta la flessibilità di utilizzo della memoria e offre alle applicazioni un controllo più stretto sull'utilizzo della memoria. Illustra anche le differenze tra i modelli D3D11 e D3D12 per il caricamento di diversi tipi di risorse.<br/> |
| [Caricamento dei dati di trama tramite buffer](upload-and-readback-of-texture-data.md)<br/> | Il caricamento di dati di trama 2D o 3D è simile al caricamento di dati 1D, ad eccezione del fatto che le applicazioni devono prestare maggiore attenzione all'allineamento dei dati correlati all'intonazione delle righe. I buffer possono essere usati in modo ortogonale e simultaneo da più parti della pipeline grafica e sono molto flessibili. <br/>                                                                                                                       |
| [Leggere i dati tramite un buffer](readback-data-using-heaps.md)<br/>                    | La lettura dei dati dalla GPU, ad esempio l'acquisizione di uno screenshot, comporta l'uso dell'heap readback. <br/>                                                                                                                                                                                                                                                                                                     |
| [Gestione delle risorse basata su recinto](fence-based-resource-management.md)<br/>            | Illustra come gestire l'intervallo di vita dei dati delle risorse verificando lo stato della GPU tramite i recinti. La memoria può essere usata di nuovo in modo efficace con i recinti gestendo attentamente la disponibilità di spazio disponibile in memoria, ad esempio in un'implementazione del buffer circolare per un heap Upload memoria. <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della memoria](memory-management.md)
</dt> </dl>

 

 





