---
title: Cenni preliminari sulle tabelle dei descrittori
description: "Ogni tabella dei descrittori archivia i descrittori di uno o più tipi: SRV, UAVe, CBV e Sampler. Una tabella del descrittore non è un'allocazione di memoria. è semplicemente un offset e una lunghezza in un heap descrittore."
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3edae00c37a451aa0fb71355a1dea5860de4398f
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813120"
---
# <a name="descriptor-tables-overview"></a>Cenni preliminari sulle tabelle dei descrittori

Ogni tabella dei descrittori archivia i descrittori di uno o più &mdash; tipi di SRV, UAVe, CBV e campionatori. Una tabella descrittore non è un'allocazione di memoria. è semplicemente un offset e una lunghezza in un heap descrittore.

## <a name="referencing-descriptor-tables"></a>Riferimento alle tabelle dei descrittori

La pipeline grafica, tramite la firma radice, ottiene l'accesso alle risorse facendo riferimento alle tabelle dei descrittori in base all'indice.

Una tabella del descrittore è in realtà solo un intervallo secondario di un heap dei descrittori. Gli heap dei descrittori rappresentano l'allocazione di memoria sottostante per una raccolta di descrittori. Poiché l'allocazione di memoria è una proprietà di un heap di creazione di un descrittore, la definizione di una tabella descrittore da una è garantita economica quanto l'identificazione di un'area nell'heap nell'hardware. Le tabelle dei descrittori non devono essere create o distrutte a livello di API. Vengono semplicemente identificate ai driver come offset e dimensioni di un heap ogni volta che si fa riferimento.

È certamente possibile per un'app definire tabelle descrittori molto grandi quando i relativi shader vogliono la libertà di selezionare da un ampio set di descrittori disponibili (spesso facendo riferimento a trame) in tempo reale (forse guidati da dati materiali).

La firma radice fa riferimento alla voce della tabella del descrittore con un riferimento all'heap, alla posizione iniziale della tabella (un offset dall'inizio dell'heap) e alla lunghezza (in voci) della tabella. L'immagine seguente illustra questi concetti: i puntatori di tabella del descrittore dalla firma radice e i descrittori all'interno dell'heap del descrittore che fanno riferimento alla trama completa o ai dati del buffer in un heap (nel caso di una trama, l'heap predefinito).

![tabelle dei descrittori](images/descriptor-table.png)

## <a name="related-topics"></a>Argomenti correlati

* [Tabelle dei descrittori](descriptor-tables.md)
