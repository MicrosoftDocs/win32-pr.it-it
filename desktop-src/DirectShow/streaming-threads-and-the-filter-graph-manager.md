---
description: Thread di streaming e Gestione Graph filtro
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Thread di streaming e Gestione Graph filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3501f984880fad22399cbda8710acaf2be1d6c4223e07a4c0f6e4c180d0699cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329771"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a>Thread di streaming e Gestione Graph filtro

Quando Gestione Graph filtro arresta il grafo, attende l'arresto di tutti i thread di streaming. Ciò ha le implicazioni seguenti per i filtri:

-   Un filtro non deve mai chiamare metodi in Filter Graph Manager da un thread di streaming.

    Filter Graph Manager usa una sezione critica per sincronizzare le proprie operazioni. Se un thread di streaming tenta di contenere questa sezione critica, può causare un deadlock. Si supponga, ad esempio, che un altro thread arresti il grafo. Il thread accetta il blocco del grafo del filtro e attende che il filtro interrompi il recapito dei dati. Se il filtro è in attesa del blocco, non si arresterà mai, causando un deadlock.

-   Un filtro non deve mai **AggiungereRef** o **QueryInterface** per filtrare Graph Manager da un thread di streaming.

    Se il filtro contiene un conteggio dei riferimenti in Filter Graph Manager (tramite **AddRef** o **QueryInterface),** potrebbe diventare l'ultimo oggetto a contenere un conteggio dei riferimenti. Quando il filtro chiama **Release**, l'Graph di gestione dei filtri si elimina automaticamente. All'interno della routine di pulizia, Filter Graph Manager tenta di arrestare il grafo, causando l'attesa della chiusura del thread di streaming. Tuttavia, è in attesa all'interno del thread di streaming, quindi il thread di streaming non può uscire. Il risultato è un deadlock.

 

 



