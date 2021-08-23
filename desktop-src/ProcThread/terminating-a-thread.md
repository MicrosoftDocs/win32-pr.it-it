---
description: "La terminazione di un thread ha i risultati seguenti: tutte le risorse di proprietà del thread, ad esempio finestre e hook, vengono liberate. Il codice di uscita del thread è impostato. L'oggetto thread viene segnalato. Se il thread è l'unico thread attivo nel processo, il processo viene terminato. Per altre informazioni, vedere Terminazione di un processo."
ms.assetid: 633e5d0c-e9d8-4f9a-9411-17cbe9e2e6e4
title: "  Terminazione di un thread"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef64729db5490ebdab3ba759b34a105c31d2cbc421a404d07b041aa9b611ba08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799041"
---
# <a name="terminating-a-thread"></a>  Terminazione di un thread

La terminazione di un thread ha i risultati seguenti:

-   Tutte le risorse di proprietà del thread, ad esempio finestre e hook, vengono liberate.
-   Il codice di uscita del thread è impostato.
-   L'oggetto thread viene segnalato.
-   Se il thread è l'unico thread attivo nel processo, il processo viene terminato. Per altre informazioni, vedere [Terminazione di un processo.](terminating-a-process.md)

La [**funzione GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread) restituisce lo stato di terminazione di un thread. Durante l'esecuzione di un thread, lo stato di terminazione è ANCORA \_ ATTIVO. Quando un thread termina, lo stato di terminazione cambia da STILL \_ ACTIVE al codice di uscita del thread.

Quando un thread termina, lo stato dell'oggetto thread cambia in segnalato, rilasciando tutti gli altri thread che erano in attesa del thread da terminare. Per altre informazioni sulla sincronizzazione, vedere [Sincronizzazione dell'esecuzione di più thread.](synchronizing-execution-of-multiple-threads.md)

Quando un thread termina, il relativo oggetto thread non viene liberato fino a quando non vengono chiusi tutti gli handle aperti per il thread.

## <a name="how-threads-are-terminated"></a>Modalità di terminazione dei thread

Un thread viene eseguito fino a quando non si verifica uno degli eventi seguenti:

-   Il thread chiama la [**funzione ExitThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)
-   Qualsiasi thread del processo chiama la [**funzione ExitProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)
-   La funzione thread restituisce .
-   Qualsiasi thread chiama [**la funzione TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) con un handle al thread.
-   Qualsiasi thread chiama [**la funzione TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) con un handle per il processo.

Il codice di uscita per un thread è il valore specificato nella chiamata a [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)o [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)oppure il valore restituito dalla funzione del thread.

Se un thread viene terminato da [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), il sistema chiama la funzione del punto di ingresso di ogni DLL collegata con un valore che indica che il thread si sta scollegando dalla DLL (a meno che non si chiami la funzione [**DisableThreadLibraryCalls).**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) Se un thread viene terminato da [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), le funzioni del punto di ingresso della DLL vengono richiamate una sola volta, per indicare che il processo è in corso di scollegamento. Le DLL non vengono notificate quando un thread viene terminato da [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) o [**TerminateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) Per altre informazioni sulle DLL, vedere [Librerie a collegamento dinamico.](../dlls/dynamic-link-libraries.md)

Le [**funzioni TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) e [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) devono essere usate solo in circostanze estremi, poiché non consentono la pulizia dei thread, non inviano notifiche alle DLL collegate e non liberano lo stack iniziale. Inoltre, gli handle agli oggetti di proprietà del thread non vengono chiusi fino al termine del processo. I passaggi seguenti offrono una soluzione migliore:

-   Creare un oggetto evento usando la [**funzione CreateEvent.**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
-   Creare i thread.
-   Ogni thread monitora lo stato dell'evento chiamando la [**funzione WaitForSingleObject.**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) Usare un intervallo di timeout di attesa pari a zero.
-   Ogni thread termina la propria esecuzione quando l'evento è impostato sullo stato segnalato ([**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) restituisce WAIT \_ OBJECT \_ 0).

 

 
