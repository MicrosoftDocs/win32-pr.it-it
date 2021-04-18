---
description: I thread sono pianificati per l'esecuzione in base alla relativa priorità di pianificazione.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Priorità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e80c8baf4ed066ec7034c97850248f81c298c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311964"
---
# <a name="scheduling-priorities"></a>Priorità di pianificazione

I thread sono pianificati per l'esecuzione in base alla relativa *priorità di pianificazione*. A ogni thread viene assegnata una priorità di pianificazione. I livelli di priorità variano da zero (priorità più bassa) a 31 (priorità più alta). Solo il thread di pagina zero può avere una priorità pari a zero. (Il thread di pagina zero è un thread di sistema responsabile dell'azzeramento di tutte le pagine libere quando non è necessario eseguire altri thread).

Il sistema considera tutti i thread con la stessa priorità uguale a. Il sistema assegna intervalli temporali in modo round robin a tutti i thread con la priorità più alta. Se nessuno di questi thread è pronto per l'esecuzione, il sistema assegna intervalli temporali in modo round robin a tutti i thread con la priorità più alta successiva. Se un thread con priorità più alta diventa disponibile per l'esecuzione, il sistema smette di eseguire il thread con priorità inferiore (senza consentirne il completamento utilizzando il relativo intervallo di tempo) e assegna un intervallo di tempo completo al thread con priorità più alta. Per altre informazioni, vedere [commutazioni di contesto](context-switches.md).

La priorità di ogni thread è determinata dai criteri seguenti:

-   Classe di priorità del processo
-   Livello di priorità del thread all'interno della classe di priorità del processo

La classe di priorità e il livello di priorità vengono combinati per formare la *priorità di base* di un thread. Per informazioni sulla priorità dinamica di un thread, vedere [priorità Boost](priority-boosts.md).

## <a name="priority-class"></a>Classe Priority

Ogni processo appartiene a una delle seguenti classi di priorità:<dl> \_classe priorità INattiva \_  
classe di priorità inferiore al \_ normale \_ \_  
\_classe di priorità normale \_  
\_classe di \_ priorità \_ normale sopra  
\_classe con priorità alta \_  
\_classe priorità in tempo reale \_  
</dl>

Per impostazione predefinita, la classe di priorità di un processo è la \_ classe di priorità normale \_ . Utilizzare la funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) per specificare la classe di priorità di un processo figlio quando viene creata. Se il processo chiamante è una \_ classe di priorità inattiva \_ o una classe di \_ \_ priorità normale \_ , il nuovo processo erediterà questa classe. Utilizzare la funzione [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) per determinare la classe di priorità corrente di un processo e la funzione [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) per modificare la classe di priorità di un processo.

I processi che monitorano il sistema, ad esempio screen saver o applicazioni che aggiornano periodicamente una visualizzazione, devono usare la classe di priorità di inattività \_ \_ . In questo modo si impedisce che i thread di questo processo, che non hanno priorità elevata, interferiscano con i thread con priorità più elevata.

Usare \_ \_ la classe con priorità alta con cautela. Se un thread viene eseguito con il livello di priorità più alto per i periodi prolungati, gli altri thread del sistema non otterranno il tempo del processore. Se più thread vengono impostati con priorità alta allo stesso tempo, i thread perdono la loro efficacia. La classe con priorità alta deve essere riservata ai thread che devono rispondere a eventi critici per il tempo. Se l'applicazione esegue un'attività che richiede la classe con priorità alta mentre le altre attività sono la priorità normale, usare [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) per generare temporaneamente la classe di priorità dell'applicazione; quindi ridurlo dopo aver completato l'attività critica. Un'altra strategia consiste nel creare un processo con priorità alta con tutti i thread bloccati nella maggior parte dei casi, riattivando i thread solo quando sono necessarie attività critiche. Il punto importante è che un thread ad alta priorità deve essere eseguito per un breve periodo di tempo e solo quando è necessario eseguire un lavoro critico nel tempo.

Non usare quasi mai la classe di priorità in tempo reale \_ \_ , perché questo interrompe i thread di sistema che gestiscono l'input del mouse, l'input da tastiera e lo scaricamento del disco in background. Questa classe può essere appropriata per le applicazioni che "comunicano" direttamente con l'hardware o che eseguono brevi attività che devono avere interruzioni limitate.

## <a name="priority-level"></a>Livello di priorità

Di seguito sono riportati i livelli di priorità all'interno di ogni classe di priorità:<dl> \_priorità thread \_ inattiva  
\_priorità thread \_ più bassa  
priorità THREAD al di \_ \_ sotto del \_ normale  
priorità THREAD- \_ \_ normale  
\_priorità thread \_ superiore al \_ normale  
\_priorità thread \_ più elevata  
\_tempo di priorità thread \_ \_ critico  
</dl>

Tutti i thread vengono creati utilizzando la priorità di THREAD \_ \_ normale. Ciò significa che la priorità del thread corrisponde alla classe di priorità del processo. Dopo aver creato un thread, usare la funzione [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) per regolarne la priorità rispetto agli altri thread nel processo.

Una strategia tipica consiste nell'usare la \_ priorità \_ dei thread sopra la \_ priorità normale o thread \_ \_ più elevata per il thread di input del processo, per garantire che l'applicazione sia reattiva all'utente. I thread in background, in particolare quelli che richiedono un utilizzo intensivo del processore, possono essere impostati sulla priorità del THREAD al di \_ \_ sotto della \_ priorità normale o della priorità del thread \_ \_ più bassa, per assicurarsi che possano essere interrotti quando necessario. Tuttavia, se si dispone di un thread in attesa di un altro thread con una priorità più bassa per completare un'attività, assicurarsi di bloccare l'esecuzione del thread con priorità alta in attesa. A tale scopo, usare una [funzione wait](../sync/wait-functions.md), una [sezione critica](../sync/critical-section-objects.md)o la funzione [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) , [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)o [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) . Questa operazione è preferibile quando il thread esegue un ciclo. In caso contrario, il processo potrebbe diventare un deadlock, perché il thread con priorità inferiore non viene mai pianificato.

Per determinare il livello di priorità corrente di un thread, usare la funzione [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) .

## <a name="base-priority"></a>Priorità di base

La classe di priorità del processo e il livello di priorità del thread vengono combinati per formare la priorità di base di ogni thread.

Nella tabella seguente viene illustrata la priorità di base per le combinazioni di classe priorità processo e valore Priorità thread.


<table>
<tr>
<th colspan="2">Classe di priorità del processo</th>
<th>Livello di priorità thread</th>
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

 

 

 
