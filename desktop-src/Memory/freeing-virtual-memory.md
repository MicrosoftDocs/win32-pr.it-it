---
description: La funzione VirtualFree decommits e rilascia le pagine in base alle regole seguenti.
ms.assetid: 8fbd7960-f3f0-4326-ad1d-12b636c0039e
title: Liberare memoria virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60c5f78da34573126cfb20d7bc16f803ec603c818a3147f388c9661245d6c408
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869697"
---
# <a name="freeing-virtual-memory"></a>Liberare memoria virtuale

La [**funzione VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) decommits e rilascia le pagine in base alle regole seguenti:

-   Disaccoda una o più pagine di cui è stato eseguito il commit, modificando lo stato delle pagine in pagine riservate. Il decommitting delle pagine rilascia l'archiviazione fisica associata alle pagine, rendendola disponibile per l'allocazione da parte di qualsiasi processo. È possibile eseguire il decommitted di qualsiasi blocco di pagine di cui è stato eseguito il commit.
-   Rilascia un blocco di una o più pagine riservate, modificando lo stato delle pagine in free. Il rilascio di un blocco di pagine rende disponibile l'intervallo di indirizzi riservati che il processo deve allocare. Le pagine riservate possono essere rilasciate solo liberando l'intero blocco inizialmente riservato da [**VirtualAlloc.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   Decommits and releases a block of one or more committed pages simultaneously, changing the state of the pages to free. Il blocco specificato deve includere l'intero blocco inizialmente riservato da [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)ed è attualmente necessario eseguire il commit di tutte le pagine.

Dopo il rilascio o il decommitted di un blocco di memoria, non è più possibile fare riferimento a esso. Tutte le informazioni che potrebbero essere presenti in tale memoria non sono più disponibili per sempre. Il tentativo di leggere o scrivere in una pagina gratuita genera un'eccezione di violazione di accesso. Se sono necessarie informazioni, non eseguire il decommit o liberare memoria contenente le informazioni.

Per specificare che i dati in un intervallo di memoria non sono più di interesse, chiamare [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) con **MEM \_ RESET.** Le pagine non verranno lette o scritte nel file di paging. Tuttavia, il blocco di memoria può essere usato di nuovo in un secondo momento.

 

 
