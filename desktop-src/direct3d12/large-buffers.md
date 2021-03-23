---
title: Sottoallocazione nei buffer
description: I buffer hanno tutte le funzionalità necessarie in D3D12 per le applicazioni per trasferire una vasta gamma di dati temporanei dalla CPU alla GPU. Questa sezione illustra quattro scenari comuni per l'uso e la gestione delle risorse e dei buffer.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64944cb11507b8dc437d075938fad419f333433
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103651"
---
# <a name="suballocation-within-buffers"></a>Sottoallocazione nei buffer

I buffer hanno tutte le funzionalità necessarie in D3D12 per le applicazioni per trasferire una vasta gamma di dati temporanei dalla CPU alla GPU. Questa sezione illustra quattro scenari comuni per l'uso e la gestione delle risorse e dei buffer.

Analogamente a D3D11, le applicazioni in D3D12 devono ancora dichiarare l'utilizzo della memoria durante l'allocazione dei buffer in D3D12 rispetto alle risorse dinamiche/di staging in D3D11, ma in D3D12 gli sviluppatori hanno maggiore flessibilità e un controllo più rigoroso sull'utilizzo della memoria. Per la gestione della memoria di basso livello, i buffer, tramite la suballocazione, hanno tutte le funzionalità necessarie.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Caricamento di diversi tipi di risorse](uploading-resources.md)<br/>                 | Viene illustrato come utilizzare un buffer per caricare sia i dati del buffer costante che i dati del buffer dei vertici nella GPU e come suddividere e collocare correttamente i dati all'interno dei buffer. L'utilizzo di un singolo buffer aumenta la flessibilità di utilizzo della memoria e fornisce alle applicazioni un controllo più rigoroso sull'utilizzo della memoria. Mostra anche le differenze tra i modelli D3D11 e D3D12 per il caricamento di diversi tipi di risorse.<br/> |
| [Caricamento dei dati di trama tramite buffer](upload-and-readback-of-texture-data.md)<br/> | Il caricamento di dati di trama 2D o 3D è simile al caricamento di dati 1D, ad eccezione del fatto che le applicazioni devono prestare maggiore attenzione all'allineamento dei dati correlato al passo della riga. I buffer possono essere usati in modo ortogonale e simultaneamente da più parti della pipeline grafica e sono molto flessibili. <br/>                                                                                                                       |
| [Eseguire la lettura dei dati tramite un buffer](readback-data-using-heaps.md)<br/>                    | La lettura dei dati dalla GPU, ad esempio l'acquisizione di uno screenshot, comporta l'uso dell'heap readback. <br/>                                                                                                                                                                                                                                                                                                     |
| [Gestione delle risorse basata su recinzioni](fence-based-resource-management.md)<br/>            | Viene illustrato come gestire il ciclo di vita dei dati delle risorse tenendo traccia dello stato di avanzamento della GPU tramite le recinzioni. La memoria può essere riutilizzata in modo efficace con le barriere gestendo con attenzione la disponibilità dello spazio disponibile in memoria, ad esempio in un'implementazione del buffer circolare per un heap di caricamento. <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della memoria](memory-management.md)
</dt> </dl>

 

 





