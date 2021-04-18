---
description: Le funzioni di memoria virtuale consentono a un processo di modificare o determinare lo stato delle pagine nello spazio degli indirizzi virtuali.
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: Funzioni di memoria virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76866fd10dac01315622e8a4faef7bea436a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308199"
---
# <a name="virtual-memory-functions"></a>Funzioni di memoria virtuale

Le funzioni di memoria virtuale consentono a un processo di modificare o determinare lo stato delle pagine nello spazio degli indirizzi virtuali. Possono eseguire le operazioni seguenti:

-   Riservare un intervallo di spazio degli indirizzi virtuali di un processo. La riserva dello spazio degli indirizzi non alloca alcuna risorsa di archiviazione fisica, ma impedisce ad altre operazioni di allocazione di utilizzare l'intervallo specificato. Non influisce sugli spazi degli indirizzi virtuali di altri processi. La prenotazione di pagine impedisce il consumo di spazio di archiviazione fisico necessario, consentendo a un processo di riservare un intervallo di spazio degli indirizzi in cui è possibile aumentare la struttura dei dati dinamica. Il processo può allocare spazio di archiviazione fisico per lo spazio in base alle esigenze.
-   Eseguire il commit di un intervallo di pagine riservate nello spazio degli indirizzi virtuali di un processo, in modo che l'archiviazione fisica (in RAM o su disco) sia accessibile solo al processo di allocazione.
-   Specificare in lettura/scrittura, in sola lettura o nessun accesso per un intervallo di pagine di cui è stato eseguito il commit. Questo comportamento è diverso dalle funzioni di allocazione standard che allocano sempre pagine con accesso in lettura/scrittura.
-   Liberare un intervallo di pagine riservate, rendendo l'intervallo di indirizzi virtuali disponibili per le successive operazioni di allocazione da parte del processo chiamante.
-   Eseguire il decommit di un intervallo di pagine di cui è stato eseguito il commit, rilasciando l'archiviazione fisica e rendendola disponibile per l'allocazione successiva da qualsiasi processo.
-   Bloccare una o più pagine di memoria di cui è stato eseguito il commit nella memoria fisica (RAM), in modo che il sistema non possa scambiare le pagine nel file di paging.
-   Ottenere informazioni su un intervallo di pagine nello spazio degli indirizzi virtuali del processo chiamante o di un processo specificato.
-   Modificare la protezione dell'accesso per un intervallo specificato di pagine di cui è stato eseguito il commit nello spazio degli indirizzi virtuali del processo chiamante o in un processo specificato.

Per ulteriori informazioni, vedere gli argomenti seguenti.

-   [Allocazione della memoria virtuale](allocating-virtual-memory.md)
-   [Confronto tra i metodi di allocazione della memoria](comparing-memory-allocation-methods.md)
-   [Liberare memoria virtuale](freeing-virtual-memory.md)
-   [Uso delle pagine](working-with-pages.md)
-   [Funzioni di gestione della memoria](memory-management-functions.md)

 

 



