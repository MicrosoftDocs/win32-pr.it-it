---
description: Il supporto di pagine di grandi dimensioni consente alle applicazioni server di stabilire aree di memoria di grandi dimensioni, che risulta particolarmente utile in Windows a 64 bit.
ms.assetid: 060115af-38d1-499c-b30c-47cd0cf42d20
title: Supporto Large-Page
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4578b5127e6613f2ff4b6e0b8a7cffcc53c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307264"
---
# <a name="large-page-support"></a>Supporto Large-Page

Il supporto di pagine di grandi dimensioni consente alle applicazioni server di stabilire aree di memoria di grandi dimensioni, che risulta particolarmente utile in Windows a 64 bit. Ogni traduzione di pagine di grandi dimensioni utilizza un solo buffer di traduzione all'interno della CPU. La dimensione di questo buffer è in genere di tre ordini di grandezza maggiore della dimensione nativa della pagina; in questo modo si aumenta l'efficienza del buffer di conversione, che può migliorare le prestazioni per la memoria a cui si accede di frequente.

Nella procedura riportata di seguito viene descritto come utilizzare il supporto di pagine di grandi dimensioni.

**Per utilizzare il supporto per pagine di grandi dimensioni**

1.  Ottenere il privilegio **SeLockMemoryPrivilege** chiamando la funzione [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) . Per altre informazioni, vedere [assegnazione di privilegi a un account](../secbp/assigning-privileges-to-an-account.md) e [modifica dei privilegi in un token](../secbp/changing-privileges-in-a-token.md).
2.  Recuperare le dimensioni minime della pagina di grandi dimensioni chiamando la funzione [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) .
3.  Quando si chiama la funzione [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) , includere il valore di **\_ \_ pagine di grandi dimensioni** . Le dimensioni e l'allineamento devono essere un multiplo del valore minimo per le pagine di grandi dimensioni.

Quando si scrivono applicazioni che utilizzano memoria di pagine di grandi dimensioni, tenere presenti le considerazioni seguenti:

-   Le aree di memoria di grandi dimensioni possono essere difficili da ottenere dopo che il sistema è stato eseguito per molto tempo perché lo spazio fisico per ogni pagina di grandi dimensioni deve essere contiguo, ma la memoria potrebbe essere stata frammentata. L'allocazione di pagine di grandi dimensioni in queste condizioni può influire significativamente sulle prestazioni del sistema. Pertanto, le applicazioni devono evitare di eseguire allocazioni ripetute di pagine di grandi dimensioni, allocando invece tutte le pagine di grandi dimensioni una volta all'avvio.
-   La memoria è sempre di lettura/scrittura e non paginabile (sempre residente nella memoria fisica).
-   La memoria fa parte del processo byte privati ma non fa parte dell'working set, perché il working set per definizione contiene solo la memoria paginabile.
-   Le allocazioni di pagine di grandi dimensioni non sono soggette ai limiti dei processi.
-   La memoria di una pagina di grandi dimensioni deve essere riservata e impegnata come singola operazione. In altre parole, le pagine di grandi dimensioni non possono essere usate per eseguire il commit di un intervallo di memoria precedentemente riservato.
-   WOW64 in sistemi basati su Intel Itanium non supporta le applicazioni a 32 bit che utilizzano questa funzionalità. Le applicazioni devono essere ricompilate come applicazioni native a 64 bit.

 

 
