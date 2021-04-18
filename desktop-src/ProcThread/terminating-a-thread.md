---
description: "La terminazione di un thread presenta i risultati seguenti: le risorse di proprietà del thread, ad esempio Windows e Hook, vengono liberate. Il codice di uscita del thread è impostato. L'oggetto thread viene segnalato. Se il thread è l'unico thread attivo nel processo, il processo viene terminato. Per ulteriori informazioni, vedere terminazione di un processo."
ms.assetid: 633e5d0c-e9d8-4f9a-9411-17cbe9e2e6e4
title: "  Terminazione di un thread"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada421356666316072aabff8281787cc140ad114
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311953"
---
# <a name="terminating-a-thread"></a>  Terminazione di un thread

La chiusura di un thread presenta i risultati seguenti:

-   Tutte le risorse di proprietà del thread, ad esempio Windows e Hook, vengono liberate.
-   Il codice di uscita del thread è impostato.
-   L'oggetto thread viene segnalato.
-   Se il thread è l'unico thread attivo nel processo, il processo viene terminato. Per ulteriori informazioni, vedere [terminazione di un processo](terminating-a-process.md).

La funzione [**GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread) restituisce lo stato di terminazione di un thread. Mentre un thread è in esecuzione, lo stato di chiusura è ancora \_ attivo. Quando un thread termina, lo stato di chiusura passa da ancora \_ attivo al codice di uscita del thread.

Quando un thread termina, lo stato dell'oggetto thread passa a segnalato, rilasciando tutti gli altri thread in attesa che il thread venga terminato. Per ulteriori informazioni sulla sincronizzazione, vedere [sincronizzazione dell'esecuzione di più thread](synchronizing-execution-of-multiple-threads.md).

Quando un thread termina, il relativo oggetto thread non viene liberato fino a quando non vengono chiusi tutti gli handle aperti per il thread.

## <a name="how-threads-are-terminated"></a>Come vengono terminati i thread

Un thread viene eseguito fino a quando non si verifica uno degli eventi seguenti:

-   Il thread chiama la funzione [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) .
-   Qualsiasi thread del processo chiama la funzione [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) .
-   La funzione thread restituisce.
-   Qualsiasi thread chiama la funzione [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) con un handle per il thread.
-   Qualsiasi thread chiama la funzione [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) con un handle per il processo.

Il codice di uscita per un thread è il valore specificato nella chiamata a [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)o [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)oppure il valore restituito dalla funzione thread.

Se un thread viene terminato da [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), il sistema chiama la funzione del punto di ingresso di ogni DLL collegata con un valore che indica che il thread viene scollegato dalla dll (a meno che non si chiami la funzione [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) ). Se un thread viene terminato da [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), le funzioni del punto di ingresso della dll vengono richiamate una volta per indicare che il processo è scollegato. Le dll non ricevono notifiche quando un thread viene terminato da [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) o [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Per altre informazioni sulle dll, vedere [librerie a collegamento dinamico](../dlls/dynamic-link-libraries.md).

Le funzioni [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) e [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) devono essere utilizzate solo in casi estremi, poiché non consentono la pulizia dei thread, non inviano notifiche a DLL collegate e non liberano lo stack iniziale. Inoltre, gli handle per gli oggetti di proprietà del thread non vengono chiusi fino al termine del processo. I passaggi seguenti offrono una soluzione migliore:

-   Creare un oggetto evento usando la funzione [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) .
-   Creare i thread.
-   Ogni thread monitora lo stato dell'evento chiamando la funzione [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) . Usare un intervallo di timeout di attesa pari a zero.
-   Ogni thread termina la propria esecuzione quando l'evento è impostato sullo stato segnalato ([**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) restituisce l' \_ oggetto Wait \_ 0).

 

 
