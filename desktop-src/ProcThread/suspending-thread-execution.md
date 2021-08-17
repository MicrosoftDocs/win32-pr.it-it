---
description: Un thread può sospendere e riprendere l'esecuzione di un altro thread. Mentre un thread è sospeso, non è pianificato per l'ora nel processore.
ms.assetid: b76d7af7-e3ec-4663-a9e7-832c01733c8c
title: Sospensione dell'esecuzione di thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf3ecf2bee1f14ae8571cb7e7402e32a636f4a35ca5c182d32a2a636ed85dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793158"
---
# <a name="suspending-thread-execution"></a>Sospensione dell'esecuzione di thread

Un thread può sospendere e riprendere l'esecuzione di un altro thread. Mentre un thread è sospeso, non è pianificato per l'ora nel processore.

Se un thread viene creato in uno stato sospeso (con il flag [**CREATE \_ SUSPENDED),**](process-creation-flags.md) non inizia l'esecuzione fino a quando un altro thread non chiama la funzione [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) con un handle per il thread sospeso. Ciò può essere utile per inizializzare lo stato del thread prima che inizi l'esecuzione. La sospensione di un thread al momento della creazione può essere utile per la sincronizzazione una sola volta, perché in questo modo il thread sospeso eseguirà il punto iniziale del codice quando si chiama **ResumeThread**.

La [**funzione SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) non deve essere usata per la sincronizzazione dei thread perché non controlla il punto nel codice in cui viene sospesa l'esecuzione del thread. Questa funzione è progettata principalmente per l'uso da parte dei debugger.

Un thread può cedere temporaneamente l'esecuzione per un intervallo specificato chiamando le funzioni [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) o [**SleepEx.**](/windows/win32/api/synchapi/nf-synchapi-sleepex) Ciò è utile in particolare nei casi in cui il thread risponde all'interazione dell'utente, perché può ritardare l'esecuzione abbastanza a lungo da consentire agli utenti di osservare i risultati delle azioni. Durante l'intervallo di sospensione, il thread non è pianificato per l'ora nel processore.

La [**funzione SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) è simile a [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) e [**SleepEx,**](/windows/win32/api/synchapi/nf-synchapi-sleepex)ad eccezione del fatto che non è possibile specificare l'intervallo. **SwitchToThread consente** al thread di rinunciare all'intervallo di tempo.

 

 
