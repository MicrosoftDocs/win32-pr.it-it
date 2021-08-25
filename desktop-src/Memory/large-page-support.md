---
description: Il supporto di pagine di grandi dimensioni consente alle applicazioni server di stabilire aree di memoria di pagine di grandi dimensioni, particolarmente utili nelle applicazioni a 64 bit Windows.
ms.assetid: 060115af-38d1-499c-b30c-47cd0cf42d20
title: Large-Page supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad61873c80d2d3fe8de6a915f5eb93f527049a437860deabedbe232cdf9cb885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869681"
---
# <a name="large-page-support"></a>Large-Page supporto

Il supporto di pagine di grandi dimensioni consente alle applicazioni server di stabilire aree di memoria di pagine di grandi dimensioni, particolarmente utili nelle applicazioni a 64 bit Windows. Ogni traduzione di pagine di grandi dimensioni usa un singolo buffer di conversione all'interno della CPU. Le dimensioni di questo buffer sono in genere di tre ordini di grandezza maggiori rispetto alle dimensioni della pagina nativa. Ciò aumenta l'efficienza del buffer di conversione, che può migliorare le prestazioni per la memoria a cui si accede di frequente.

La procedura seguente descrive come usare il supporto per pagine di grandi dimensioni.

**Per usare il supporto per pagine di grandi dimensioni**

1.  Ottenere il **privilegio SeLockMemoryPrivilege** chiamando la [**funzione AdjustTokenPrivileges.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) Per altre informazioni, vedere [Assegnazione di privilegi a un account e](../secbp/assigning-privileges-to-an-account.md) Modifica dei privilegi in un [token.](../secbp/changing-privileges-in-a-token.md)
2.  Recuperare le dimensioni minime delle pagine grandi chiamando la [**funzione GetLargePageMinimum.**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum)
3.  Includere il **valore MEM \_ LARGE \_ PAGES** quando si chiama la [**funzione VirtualAlloc.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) Le dimensioni e l'allineamento devono essere multipli del numero minimo di pagine di grandi dimensioni.

Quando si scrivono applicazioni che usano memoria di pagine di grandi dimensioni, tenere presenti le considerazioni seguenti:

-   Le aree di memoria di grandi dimensioni possono essere difficili da ottenere dopo che il sistema è stato eseguito per molto tempo perché lo spazio fisico per ogni pagina di grandi dimensioni deve essere contiguo, ma la memoria potrebbe essere stata frammentata. L'allocazione di pagine di grandi dimensioni in queste condizioni può influire in modo significativo sulle prestazioni del sistema. Pertanto, le applicazioni devono evitare di eseguire allocazioni ripetute di pagine di grandi dimensioni e allocare tutte le pagine di grandi dimensioni una volta all'avvio.
-   La memoria è sempre di lettura/scrittura e non paginabile (sempre residenti nella memoria fisica).
-   La memoria fa parte dei byte privati del processo, ma non fa parte del working set, perché il working set per definizione contiene solo memoria di paging.
-   Le allocazioni di pagine di grandi dimensioni non sono soggette ai limiti dei processi.
-   La memoria di grandi dimensioni deve essere riservata e di cui è stato eseguito il commit come singola operazione. In altre parole, non è possibile usare pagine di grandi dimensioni per eseguire il commit di un intervallo di memoria precedentemente riservato.
-   WOW64 nei sistemi basati su Intel Itanium non supporta le applicazioni a 32 bit che usano questa funzionalità. Le applicazioni devono essere ricompilate come applicazioni native a 64 bit.

 

 
