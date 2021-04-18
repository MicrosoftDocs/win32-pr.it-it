---
description: Implementare il multitasking, pianificare le priorità e usare processi, thread, pool di thread, oggetti processo e Fiber. Utilizzare la pianificazione in modalità utente per pianificare i thread.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Processi e thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f469806a5f803910a773c78c9847d0f7b0ecc7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311966"
---
# <a name="processes-and-threads"></a>Processi e thread

Un'applicazione è costituita da uno o più processi. Un *processo*, in termini più semplici, è un programma in esecuzione. Uno o più thread vengono eseguiti nel contesto del processo. Un *thread* è l'unità di base in cui il sistema operativo alloca il tempo del processore. Un thread può eseguire qualsiasi parte del codice del processo, incluse le parti attualmente eseguite da un altro thread.

Un *oggetto processo* consente la gestione di gruppi di processi come unità. Gli oggetti processo sono oggetti namable, a protezione diretta e condivisibili che controllano gli attributi dei processi ad essi associati. Le operazioni eseguite sull'oggetto processo hanno effetto su tutti i processi associati all'oggetto processo.

Un *pool di thread* è una raccolta di thread di lavoro che eseguono in modo efficiente callback asincroni per conto dell'applicazione. Il pool di thread viene utilizzato principalmente per ridurre il numero di thread dell'applicazione e fornire la gestione dei thread di lavoro.

Un *Fiber* è un'unità di esecuzione che deve essere pianificata manualmente dall'applicazione. I fiber vengono eseguiti nel contesto dei thread che li pianificano.

La *pianificazione in modalità utente* è un meccanismo leggero che le applicazioni possono utilizzare per pianificare i propri thread. I thread UMS differiscono dalle [fibre](fibers.md) in quanto ogni thread UMS dispone di un proprio contesto di thread invece di condividere il contesto del thread di un singolo thread.

-   [Novità di processi e thread](what-s-new-in-processes-and-threads.md)
-   [Informazioni su processi e thread](about-processes-and-threads.md)
-   [Uso di processi e thread](using-processes-and-threads.md)
-   [Riferimento a processi e thread](process-and-thread-reference.md)

 

 



