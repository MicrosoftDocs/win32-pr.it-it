---
title: Cenni preliminari sulle tabelle descrittori
description: Ogni tabella dei descrittori archivia i descrittori di uno o più tipi, ovvero SRVs, UAVe, CBVs e Samplers. Una tabella descrittore non è un'allocazione di memoria; è semplicemente un offset e una lunghezza in un heap del descrittore.
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d446a0570cf813eacaa4d036781e8cd4b8def3c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103578"
---
# <a name="descriptor-tables-overview"></a>Cenni preliminari sulle tabelle descrittori

Ogni tabella dei descrittori archivia i descrittori di uno o più tipi, ovvero SRVs, UAVe, CBVs e Samplers. Una tabella descrittore non è un'allocazione di memoria; è semplicemente un offset e una lunghezza in un heap del descrittore.

-   [Riferimento a tabelle di descrittori](#referencing-descriptor-tables)
-   [Argomenti correlati](#related-topics)

## <a name="referencing-descriptor-tables"></a>Riferimento a tabelle di descrittori

La pipeline grafica, tramite la firma radice, ottiene l'accesso alle risorse facendo riferimento a tabelle descrittore in base all'indice.

Una tabella dei descrittori è in realtà solo un intervallo secondario di un heap del descrittore. Gli heap del descrittore rappresentano l'allocazione di memoria sottostante per una raccolta di descrittori. Poiché l'allocazione di memoria è una proprietà di un heap di descrittore, la definizione di una tabella del descrittore su uno di essi è garantita come l'identificazione di un'area nell'heap per l'hardware. Le tabelle dei descrittori non devono essere create o distrutte a livello di API, ma sono semplicemente identificate come offset e le dimensioni di un heap ogni volta che vi si fa riferimento.

È certamente possibile che un'app definisca le tabelle dei descrittori di dimensioni molto grandi quando i relativi shader desiderano che la libertà di selezione da un vasto set di descrittori disponibili (spesso che fanno riferimento a trame) in tempo reale (probabilmente basati sui dati del materiale).

La firma radice fa riferimento alla voce della tabella descrittore con un riferimento all'heap, la posizione iniziale della tabella (un offset dall'inizio dell'heap) e la lunghezza (in voci) della tabella. Nell'immagine seguente vengono illustrati questi concetti: i puntatori alla tabella descrittore della firma radice e i descrittori all'interno dell'heap del descrittore che fanno riferimento alla trama completa o ai dati del buffer in un heap di caricamento.

![tabelle descrittore](images/descriptor-table.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabelle descrittore](descriptor-tables.md)
</dt> </dl>

 

 




