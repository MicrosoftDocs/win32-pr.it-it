---
description: Thread di streaming e Gestione Graph filtri
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Thread di streaming e Gestione Graph filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3501f984880fad22399cbda8710acaf2be1d6c4223e07a4c0f6e4c180d0699cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329771"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a>Thread di streaming e Gestione Graph filtri

Quando Filter Graph Manager arresta il grafico, attende l'arresto di tutti i thread di streaming. Questo ha le implicazioni seguenti per i filtri:

-   Un filtro non deve mai chiamare metodi in Filter Graph Manager da un thread di streaming.

    Gestione filtri Graph usa una sezione critica per sincronizzare le proprie operazioni. Se un thread di streaming tenta di contenere questa sezione critica, può causare un deadlock. Si supponga, ad esempio, che un altro thread arresti il grafico. Il thread accetta il blocco del grafo del filtro e attende che il filtro interrompi il recapito dei dati. Se il filtro è in attesa del blocco, non verrà mai interrotta, causando un deadlock.

-   Un filtro non deve mai **essere AddRef** o **QueryInterface,** il filtro Graph Manager da un thread di streaming.

    Se il filtro contiene un conteggio dei riferimenti in Filter Graph Manager (tramite **AddRef** o **QueryInterface),** potrebbe diventare l'ultimo oggetto a contenere un conteggio dei riferimenti. Quando il filtro chiama **Release,** il gestore di Graph elimina se stesso. All'interno della routine di pulizia, Filter Graph Manager tenta di arrestare il grafo, causando l'attesa dell'uscita del thread di streaming. Tuttavia, è in attesa all'interno del thread di streaming, quindi il thread di streaming non può uscire. Il risultato è un deadlock.

 

 



