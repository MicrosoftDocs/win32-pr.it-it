---
title: Elaborare le informazioni sull'utilizzo della memoria
description: La funzione GetProcessMemoryInfo accetta un handle di processo come input e riempie una struttura PROCESS MEMORY COUNTERS con informazioni sulle statistiche \_ di memoria per il \_ processo.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac85a62853cf95dcf42380c76b914f23045152b32499870182a47ee2449e8ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094703"
---
# <a name="process-memory-usage-information"></a>Elaborare le informazioni sull'utilizzo della memoria

La [**funzione GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) accetta un handle di processo come input e riempie una [**struttura PROCESS MEMORY \_ \_ COUNTERS**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) con informazioni sulle statistiche di memoria per il processo. Il **membro cb** riceve le dimensioni della struttura . Il **membro PageFaultCount** riceve il numero di errori di pagina. I membri rimanenti ricevono l'utilizzo corrente e massimo della memoria nelle categorie seguenti:

-   working set
-   pool di paging
-   pool non di paging
-   Paging

Il *working set* è la quantità di memoria fisicamente mappata al contesto del processo in un determinato momento. La memoria nel *pool di paging* è la memoria di sistema che può essere trasferita al file di paging su disco (di paging) quando non è in uso. La memoria nel *pool non di* paging è memoria di sistema che non può essere paginata su disco purché siano allocati gli oggetti corrispondenti. *L'utilizzo del file* di paging rappresenta la quantità di memoria da riservare per il processo nel file di paging di sistema. Quando l'utilizzo della memoria è troppo elevato, il gestore della memoria virtuale esegue le pagine della memoria selezionata su disco. Quando un thread richiede una pagina non in memoria, il gestore della memoria la ricarica dal file di paging.

 

 




