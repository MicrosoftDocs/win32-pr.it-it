---
description: Le funzioni di memoria virtuale modificano le pagine di memoria. Le funzioni utilizzano le dimensioni di una pagina nel computer corrente per arrotondare le dimensioni e gli indirizzi specificati.
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: Allocazione della memoria virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f42b4f7eb9d5de3c8c5e9339c9e5931a89e371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345371"
---
# <a name="allocating-virtual-memory"></a>Allocazione della memoria virtuale

Le funzioni di memoria virtuale modificano le pagine di memoria. Le funzioni utilizzano le dimensioni di una pagina nel computer corrente per arrotondare le dimensioni e gli indirizzi specificati.

La funzione [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) esegue una delle operazioni seguenti:

-   Riserva una o più pagine gratuite.
-   Viene eseguito il commit di una o più pagine riservate.
-   Consente di riservare ed eseguire il commit di una o più pagine gratuite.

È possibile specificare l'indirizzo iniziale delle pagine da riservare o sottoposte a commit oppure è possibile consentire al sistema di determinare l'indirizzo. La funzione arrotonda l'indirizzo specificato al limite della pagina appropriato. Le pagine riservate non sono accessibili, ma le pagine di cui è stato eseguito il commit possono essere allocate con l'accesso alla pagina **\_ ReadWrite**, alla **pagina \_ ReadOnly** o alla **pagina \_** . Quando si esegue il commit delle pagine, gli addebiti per la memoria vengono allocati dalla dimensione complessiva della RAM e dai file di paging sul disco, ma ogni pagina viene inizializzata e caricata nella memoria fisica solo al primo tentativo di lettura o scrittura in tale pagina. È possibile usare i riferimenti al puntatore normali per accedere alla memoria di cui è stato eseguito il commit dalla funzione [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) .

 

 
