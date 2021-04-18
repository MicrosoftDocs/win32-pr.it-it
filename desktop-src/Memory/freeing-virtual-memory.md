---
description: La funzione VirtualFree consente di eseguire il commit e rilasciare le pagine in base alle regole seguenti.
ms.assetid: 8fbd7960-f3f0-4326-ad1d-12b636c0039e
title: Liberare memoria virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7628ed53f956d5cd13f0c7d2d1157443d529129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306584"
---
# <a name="freeing-virtual-memory"></a>Liberare memoria virtuale

La funzione [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) consente di eseguire il commit e rilasciare le pagine in base alle regole seguenti:

-   Esegue il commit di una o più pagine di cui è stato eseguito il commit, modificando lo stato delle pagine in riservato. Il commit delle pagine rilascia lo spazio di archiviazione fisico associato alle pagine, rendendolo disponibile per l'allocazione da parte di qualsiasi processo. È possibile eseguire il commit di qualsiasi blocco di pagine con commit.
-   Rilascia un blocco di una o più pagine riservate, modificando lo stato delle pagine su Free. Il rilascio di un blocco di pagine rende l'intervallo di indirizzi riservati disponibile per l'allocazione da parte del processo. Le pagine riservate possono essere rilasciate solo liberando l'intero blocco inizialmente riservato da [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc).
-   Esegue il commit e rilascia un blocco di una o più pagine di cui è stato eseguito il commit simultaneamente, modificando lo stato delle pagine in libero. Il blocco specificato deve includere l'intero blocco inizialmente riservato da [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)ed è necessario che sia attualmente eseguito il commit di tutte le pagine.

Dopo il rilascio o il decommit di un blocco di memoria, non è mai possibile farvi riferimento. Tutte le informazioni che potrebbero essere state apportate in tale memoria sono finite per sempre. Il tentativo di leggere o scrivere in una pagina gratuita comporta un'eccezione di violazione di accesso. Se sono necessarie informazioni, non eseguire il decommit o liberare memoria contenente tali informazioni.

Per specificare che i dati in un intervallo di memoria non sono più di interesse, chiamare [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) con la **\_ reimpostazione della MEM**. Le pagine non verranno lette o scritte nel file di paging. Tuttavia, il blocco di memoria può essere usato di nuovo in un secondo momento.

 

 
