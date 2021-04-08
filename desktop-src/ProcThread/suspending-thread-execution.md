---
description: Un thread può sospendere e riprendere l'esecuzione di un altro thread. Mentre un thread è sospeso, non è pianificato per l'ora del processore.
ms.assetid: b76d7af7-e3ec-4663-a9e7-832c01733c8c
title: Sospensione dell'esecuzione del thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3688b0327ecf5fd21f07e9be6be6ecab17d64617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967480"
---
# <a name="suspending-thread-execution"></a>Sospensione dell'esecuzione del thread

Un thread può sospendere e riprendere l'esecuzione di un altro thread. Mentre un thread è sospeso, non è pianificato per l'ora del processore.

Se un thread viene creato in uno stato sospeso (con il flag di [**creazione \_ sospesa**](process-creation-flags.md) ), non inizia l'esecuzione fino a quando un altro thread non chiama la funzione [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) con un handle per il thread sospeso. Questa operazione può essere utile per inizializzare lo stato del thread prima che inizi l'esecuzione. La sospensione di un thread in fase di creazione può essere utile per la sincronizzazione monouso, perché in questo modo il thread sospeso eseguirà il punto iniziale del codice quando si chiama **ResumeThread**.

La funzione [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) non deve essere usata per la sincronizzazione dei thread perché non controlla il punto nel codice in cui viene sospesa l'esecuzione del thread. Questa funzione è progettata principalmente per essere utilizzata dai debugger.

Un thread può restituire temporaneamente l'esecuzione per un intervallo specificato chiamando le funzioni [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) o [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) . questa operazione è utile in particolare nei casi in cui il thread risponde all'interazione dell'utente, perché può ritardare l'esecuzione per un tempo sufficiente a consentire agli utenti di osservare i risultati delle proprie azioni. Durante l'intervallo di sospensione, il thread non è pianificato per l'ora del processore.

La funzione [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) è simile a [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) e [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), ad eccezione del fatto che non è possibile specificare l'intervallo. **SwitchToThread** consente al thread di rinunciare all'intervallo di tempo.

 

 
