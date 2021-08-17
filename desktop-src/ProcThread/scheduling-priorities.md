---
description: L'esecuzione dei thread viene pianificata in base alla priorità di pianificazione.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Priorità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359f86e6ef78ffe1e549045eebbe435674b50f25f25bd30598fce8581c06092a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793313"
---
# <a name="scheduling-priorities"></a>Priorità di pianificazione

L'esecuzione dei thread è pianificata in base *alla priorità di pianificazione.* A ogni thread viene assegnata una priorità di pianificazione. I livelli di priorità sono da zero (priorità più bassa) a 31 (priorità più alta). Solo il thread di pagina zero può avere una priorità pari a zero. Il thread a pagina zero è un thread di sistema responsabile dell'azzeramento delle pagine libere quando non sono presenti altri thread che devono essere eseguiti.

Il sistema considera uguali tutti i thread con la stessa priorità. Il sistema assegna gli intervallo di tempo in modalità round robin a tutti i thread con la priorità più alta. Se nessuno di questi thread è pronto per l'esecuzione, il sistema assegna gli intervallo di tempo in modalità round robin a tutti i thread con la priorità più alta successiva. Se un thread con priorità più alta diventa disponibile per l'esecuzione, il sistema smette di eseguire il thread con priorità più bassa (senza consentire il completamento dell'uso dell'intervallo di tempo) e assegna un intervallo di tempo completo al thread con priorità più alta. Per altre informazioni, vedere [Context Switches](context-switches.md).

La priorità di ogni thread è determinata dai criteri seguenti:

-   Classe di priorità del processo
-   Livello di priorità del thread all'interno della classe di priorità del processo

La classe di priorità e il livello di priorità vengono combinati per formare la *priorità di base* di un thread. Per informazioni sulla priorità dinamica di un thread, vedere [Priority Boosts](priority-boosts.md).

## <a name="priority-class"></a>Classe Priority

Ogni processo appartiene a una delle classi di priorità seguenti:<dl> CLASSE \_ DI PRIORITÀ \_ INATTIVA  
SOTTO \_ LA CLASSE DI PRIORITÀ \_ \_ NORMALE  
CLASSE \_ DI PRIORITÀ \_ NORMALE  
SOPRA \_ LA CLASSE DI PRIORITÀ \_ \_ NORMALE  
CLASSE \_ CON \_ PRIORITÀ ALTA  
CLASSE \_ PRIORITY IN TEMPO \_ REALE  
</dl>

Per impostazione predefinita, la classe di priorità di un processo è NORMAL \_ PRIORITY \_ CLASS. Usare la [**funzione CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) per specificare la classe di priorità di un processo figlio quando viene creato. Se il processo chiamante è IDLE \_ PRIORITY CLASS o BELOW NORMAL PRIORITY \_ \_ \_ \_ CLASS, il nuovo processo erediterà questa classe. Usare la [**funzione GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) per determinare la classe di priorità corrente di un processo e la [**funzione SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) per modificare la classe di priorità di un processo.

I processi che monitorano il sistema, ad esempio screen saver o applicazioni che aggiornano periodicamente una visualizzazione, devono usare IDLE \_ PRIORITY \_ CLASS. In questo modo si impedisce ai thread di questo processo, che non hanno priorità alta, di interferire con i thread con priorità più alta.

Usare HIGH \_ PRIORITY \_ CLASS con cautela. Se un thread viene eseguito al livello di priorità più alto per periodi prolungati, gli altri thread nel sistema non otterrà il tempo del processore. Se più thread vengono impostati contemporaneamente con priorità alta, i thread perdono l'efficacia. La classe con priorità alta deve essere riservata ai thread che devono rispondere a eventi time critical. Se l'applicazione esegue un'attività che richiede la classe con priorità alta mentre le altre attività hanno priorità normale, usare [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) per aumentare temporaneamente la classe di priorità dell'applicazione. quindi ridurla dopo il completamento dell'attività di importanza critica. Un'altra strategia consiste nel creare un processo ad alta priorità con tutti i thread bloccati per la maggior parte del tempo, che ritagli i thread solo quando sono necessarie attività critiche. Il punto importante è che un thread ad alta priorità deve essere eseguito per un breve periodo di tempo e solo quando ha lavoro critico per l'esecuzione.

È consigliabile non usare quasi mai REALTIME PRIORITY CLASS, perché questo interrompe i thread di sistema che gestiscono l'input del mouse, l'input da tastiera e lo \_ \_ scaricamento del disco in background. Questa classe può essere appropriata per le applicazioni che "si collegano" direttamente all'hardware o che eseguono brevi attività che devono avere interruzioni limitate.

## <a name="priority-level"></a>Livello di priorità

Di seguito sono riportati i livelli di priorità all'interno di ogni classe di priorità:<dl> THREAD \_ PRIORITY \_ IDLE  
PRIORITÀ \_ THREAD \_ PIÙ BASSA  
PRIORITÀ \_ THREAD AL DI SOTTO DEL \_ \_ NORMALE  
PRIORITÀ \_ THREAD \_ NORMALE  
PRIORITÀ \_ DEI THREAD SUPERIORE ALLA \_ \_ NORMALE  
PRIORITÀ \_ THREAD \_ PIÙ ALTA  
THREAD \_ PRIORITY \_ TIME \_ CRITICAL  
</dl>

Tutti i thread vengono creati usando THREAD \_ PRIORITY \_ NORMAL. Ciò significa che la priorità del thread corrisponde alla classe di priorità del processo. Dopo aver creato un thread, usare la [**funzione SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) per modificarne la priorità rispetto ad altri thread del processo.

Una strategia tipica consiste nell'usare THREAD PRIORITY ABOVE NORMAL o THREAD PRIORITY HIGHEST per il thread di input del processo, per garantire che \_ \_ l'applicazione sia \_ \_ \_ reattiva all'utente. I thread in background, in particolare quelli che richiedono un utilizzo intensivo del processore, possono essere impostati su THREAD PRIORITY BELOW NORMAL o THREAD PRIORITY LOWEST, per garantire che possano essere in precedenza quando \_ \_ \_ \_ \_ necessario. Tuttavia, se si dispone di un thread in attesa di un altro thread con una priorità più bassa per completare un'attività, assicurarsi di bloccare l'esecuzione del thread ad alta priorità in attesa. A tale scopo, usare una [funzione wait](../sync/wait-functions.md), una [sezione critica](../sync/critical-section-objects.md)o la funzione [**Sleep,**](/windows/win32/api/synchapi/nf-synchapi-sleep) [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)o [**SwitchToThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) È preferibile fare in modo che il thread ese abbia eseguito un ciclo. In caso contrario, il processo potrebbe diventare in deadlock, perché il thread con priorità più bassa non è mai pianificato.

Per determinare il livello di priorità corrente di un thread, usare [**la funzione GetThreadPriority.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority)

## <a name="base-priority"></a>Priorità di base

La classe di priorità del processo e il livello di priorità del thread vengono combinati per formare la priorità di base di ogni thread.

Nella tabella seguente viene illustrata la priorità di base per le combinazioni di classe di priorità del processo e valore di priorità del thread.


<table>
<tr>
<th colspan="2">Classe di priorità del processo</th>
<th>Livello di priorità dei thread</th>
<th>Priorità di base</th>
</tr>
<tr>
<td rowspan="7" colspan="2">IDLE_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>2</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>3</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>4</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>5</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">BELOW_NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>4</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>5</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>7</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>7</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>9</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>10</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">ABOVE_NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>9</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>10</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>11</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>12</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">HIGH_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>11</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>12</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>13</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>14</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>15</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">REALTIME_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>16</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>22</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>23</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>24</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>25</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>26</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>31</td>
</tr>
</table>

 

 

 
