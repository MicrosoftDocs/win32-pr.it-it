---
description: Thread di streaming e gestione del grafo dei filtri
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Thread di streaming e gestione del grafo dei filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a8c5b8fa972a8118563ae8f9e73d480ac15e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314843"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a>Thread di streaming e gestione del grafo dei filtri

Quando il gestore del grafico del filtro arresta il grafico, attende che tutti i thread di streaming vengano arrestati. Questa operazione presenta le implicazioni seguenti per i filtri:

-   Un filtro non deve mai chiamare i metodi sul gestore del grafo del filtro da un thread di streaming.

    Filter Graph Manager usa una sezione critica per sincronizzare le proprie operazioni. Se un thread di streaming tenta di conservare questa sezione critica, può causare un deadlock. Ad esempio, si supponga che un altro thread interrompa il grafo. Il thread accetta il blocco del grafico del filtro e attende che il filtro interrompa la distribuzione dei dati. Se il filtro è in attesa del blocco, non verrà mai arrestato, causando un deadlock.

-   Un filtro non deve mai **AddRef** o **QueryInterface** Filter Graph Manager da un thread di streaming.

    Se il filtro include un conteggio dei riferimenti nel gestore del grafo del filtro (tramite **AddRef** o **QueryInterface**), potrebbe diventare l'ultimo oggetto a contenere un conteggio dei riferimenti. Quando il filtro chiama il **rilascio**, il gestore del grafico del filtro viene distrutto automaticamente. All'interno della routine di pulitura, il gestore del grafico del filtro tenta di arrestare il grafo, facendo in modo che il thread di streaming venga chiuso. Tuttavia, è in attesa all'interno del thread di streaming, quindi il thread di streaming non può uscire. Il risultato è un deadlock.

 

 



