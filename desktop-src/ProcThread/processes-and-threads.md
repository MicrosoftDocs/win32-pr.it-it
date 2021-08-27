---
description: Implementare il multitasking, pianificare le priorità e lavorare con processi, thread, pool di thread, oggetti processo e fiber. Usare la pianificazione in modalità utente per pianificare i thread.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Processi e thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482f9f394001503350d4e213bd51e441ea43d073aacd8d10a49512e04404ba17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081311"
---
# <a name="processes-and-threads"></a>Processi e thread

Un'applicazione è costituita da uno o più processi. Un *processo,* in termini più semplici, è un programma in esecuzione. Uno o più thread vengono eseguiti nel contesto del processo. Un *thread è* l'unità di base a cui il sistema operativo alloca il tempo del processore. Un thread può eseguire qualsiasi parte del codice del processo, incluse le parti attualmente in esecuzione da un altro thread.

Un *oggetto processo* consente di gestire gruppi di processi come unità. Gli oggetti processo sono oggetti rinominabili, a protezione diretta e gestibili che controllano gli attributi dei processi associati. Le operazioni eseguite sull'oggetto processo influiscono su tutti i processi associati all'oggetto processo.

Un *pool di thread* è una raccolta di thread di lavoro che eseguono in modo efficiente callback asincroni per conto dell'applicazione. Il pool di thread viene usato principalmente per ridurre il numero di thread dell'applicazione e fornire la gestione dei thread di lavoro.

Un *fiber* è un'unità di esecuzione che deve essere pianificata manualmente dall'applicazione. I fiber vengono eseguiti nel contesto dei thread che li pianificano.

*La pianificazione in modalità utente* è un meccanismo leggero che le applicazioni possono usare per pianificare i propri thread. I thread UMS differiscono [dai fiber,](fibers.md) in cui ogni thread UMS ha il proprio contesto di thread anziché condividere il contesto del thread di un singolo thread.

-   [Novità di processi e thread](what-s-new-in-processes-and-threads.md)
-   [Informazioni su processi e thread](about-processes-and-threads.md)
-   [Uso di processi e thread](using-processes-and-threads.md)
-   [Informazioni di riferimento su processi e thread](process-and-thread-reference.md)

 

 



