---
title: Informazioni sull'utilizzo della memoria del processo
description: La funzione GetProcessMemoryInfo accetta un handle di processo come input e riempie una \_ struttura di contatori della memoria \_ del processo con informazioni sulle statistiche della memoria per il processo.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133032b8cfb8a9af4ccea5661c9e0e0181ab4d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856606"
---
# <a name="process-memory-usage-information"></a>Informazioni sull'utilizzo della memoria del processo

La funzione [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) accetta un handle di processo come input e riempie una struttura di [**\_ \_ contatori della memoria del processo**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) con informazioni sulle statistiche della memoria per il processo. Il membro **CB** riceve le dimensioni della struttura. Il membro **PageFaultCount** riceve il numero di errori di pagina. I membri rimanenti ricevono l'utilizzo di memoria corrente e massimo nelle categorie seguenti:

-   working set
-   pool di paging
-   pool non di paging
-   paging

Il *working set* è la quantità di memoria mappata fisicamente al contesto del processo in un determinato momento. La memoria nel *pool* di paging è una memoria di sistema che può essere trasferita nel file di paging su disco (di paging) quando non è in uso. La memoria nel *pool* non di paging è una memoria di sistema di cui non è possibile eseguire il paging su disco fino a quando vengono allocati gli oggetti corrispondenti. L'utilizzo del file di *paging* rappresenta la quantità di memoria riservata per il processo nel file di paging del sistema. Quando l'utilizzo della memoria è troppo elevato, le pagine del gestore della memoria virtuale hanno selezionato la memoria su disco. Quando un thread richiede una pagina che non si trova in memoria, il gestore della memoria lo ricarica dal file di paging.

 

 




