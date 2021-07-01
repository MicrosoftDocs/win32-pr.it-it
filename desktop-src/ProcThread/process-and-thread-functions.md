---
description: Questo argomento descrive le funzioni di processo e thread.
ms.assetid: 8c8e8af0-bf50-4a4b-945c-83bae1eff7dd
title: Funzioni di processi e thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebb1e281feb83b4a0da0c230792399d8e21684f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120998"
---
# <a name="process-and-thread-functions"></a>Funzioni di processi e thread

Questo argomento descrive le funzioni di processo e thread.

-   [Funzione Dispatch Queue](#dispatch-queue-function)
-   [Funzioni di elaborazione](#process-functions)
-   [Funzioni di enumerazione dei processi](#process-enumeration-functions)
-   [Funzioni dei criteri](#policy-functions)
-   [Funzioni thread](#thread-functions)
-   [Funzioni degli attributi estesi di processo e thread](#process-and-thread-extended-attribute-functions)
-   [Funzioni WOW64](#wow64-functions)
-   [Funzioni degli oggetti processo](#job-object-functions)
-   [Funzioni del pool di thread](#thread-pool-functions)
-   [Funzioni del servizio di ordinamento dei thread](#thread-ordering-service-functions)
-   [Funzioni del servizio Utilità di pianificazione classi multimediali](#multimedia-class-scheduler-service-functions)
-   [Funzioni fiber](#fiber-functions)
-   [Funzioni di supporto NUMA](#numa-support-functions)
-   [Funzioni del processore](#processor-functions)
-   [Funzioni di pianificazione in modalità utente](#user-mode-scheduling-functions)
-   [Funzioni obsolete](#obsolete-functions)

## <a name="dispatch-queue-function"></a>Funzione Dispatch Queue

La funzione seguente crea un [oggetto DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).



| Funzione                                                                   | Descrizione                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDispatcherQueueController**](/windows/desktop/api/DispatcherQueue/nf-dispatcherqueue-createdispatcherqueuecontroller) | Crea un [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller) che gestisce la durata di [un oggetto DispatcherQueue](/uwp/api/windows.system.dispatcherqueue) che esegue attività in coda in ordine di priorità in un altro thread. |



 

## <a name="process-functions"></a>Funzioni di elaborazione

Le funzioni seguenti vengono usate con [i processi](child-processes.md).



| Funzione                                                                 | Descrizione                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)                                   | Crea un nuovo processo e il relativo thread primario.                                                                                                                                                 |
| [**Createprocessasuser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)                       | Crea un nuovo processo e il relativo thread primario. Il nuovo processo viene eseguito nel contesto di sicurezza dell'utente rappresentato dal token specificato.                                                    |
| [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw)               | Crea un nuovo processo e il relativo thread primario. Il nuovo processo esegue quindi il file eseguibile specificato nel contesto di sicurezza delle credenziali specificate (utente, dominio e password).      |
| [**CreateProcessWithTokenW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithtokenw)               | Crea un nuovo processo e il relativo thread primario. Il nuovo processo viene eseguito nel contesto di sicurezza del token specificato.                                                                            |
| [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)                                       | Termina il processo chiamante e tutti i relativi thread.                                                                                                                                                 |
| [**FlushProcessWriteBuffers**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushprocesswritebuffers)             | Scarica la coda di scrittura di ogni processore che esegue un thread del processo corrente.                                                                                                    |
| [**FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa)                 | Libera un blocco di stringhe di ambiente.                                                                                                                                                         |
| [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea)                                 | Recupera la stringa della riga di comando per il processo corrente.                                                                                                                                    |
| [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess)                           | Recupera uno pseudo handle per il processo corrente.                                                                                                                                            |
| [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid)                       | Recupera l'identificatore di processo del processo chiamante.                                                                                                                                      |
| [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)           | Recupera il numero del processore su cui era in esecuzione il thread corrente durante la chiamata a questa funzione.                                                                                     |
| [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings)                   | Recupera il blocco di ambiente per il processo corrente.                                                                                                                                      |
| [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable)                 | Recupera il valore della variabile specificata dal blocco di ambiente del processo chiamante.                                                                                              |
| [**GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess)                         | Recupera lo stato di terminazione del processo specificato.                                                                                                                                    |
| [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources)                               | Recupera il numero di handle per gli oggetti dell'interfaccia utente grafica in uso dal processo specificato.                                                                                     |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Recupera informazioni sui processori logici e sull'hardware correlato.                                                                                                                          |
| [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass)                             | Recupera la classe di priorità per il processo specificato.                                                                                                                                       |
| [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask)                 | Recupera una maschera di affinità di processo per il processo specificato e la maschera di affinità di sistema per il sistema.                                                                                      |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)               | Recupera l'affinità del gruppo di processori del processo specificato.                                                                                                                              |
| [**GetProcessHandleCount**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)                   | Recupera il numero di handle aperti che appartengono al processo specificato.                                                                                                                    |
| [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)                                     | Recupera l'identificatore di processo del processo specificato.                                                                                                                                    |
| [**GetProcessIdOfThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread)                     | Recupera l'identificatore di processo del processo associato al thread specificato.                                                                                                         |
| [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters)                     | Recupera le informazioni di accounting per tutte le operazioni di I/O eseguite dal processo specificato.                                                                                                   |
| [**GetProcessMitigationPolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy)         | Recupera le impostazioni dei criteri di mitigazione per il processo chiamante.                                                                                                                                 |
| [**GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost)               | Recupera lo stato priority boost controllo del processo specificato.                                                                                                                          |
| [**GetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessshutdownparameters)     | Recupera i parametri di arresto per il processo attualmente chiamante.                                                                                                                              |
| [**GetProcessTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes)                               | Recupera le informazioni di intervallo relative al processo specificato.                                                                                                                                 |
| [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion)                           | Recupera i numeri di versione principale e secondaria del sistema in cui si prevede di eseguire il processo specificato.                                                                                    |
| [**GetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize)             | Recupera le dimensioni minime e massime working set dimensioni del processo specificato.                                                                                                                 |
| [**GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex)         | Recupera le dimensioni minime e massime working set dimensioni del processo specificato.                                                                                                                 |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)       | Recupera il tempo di ciclo impiegato da ogni processore nel gruppo specificato per l'esecuzione di chiamate di procedura posticipate e l'interruzione delle routine di servizio (ISR).                                         |
| [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow)                                 | Recupera il contenuto della struttura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) specificata al momento della creazione del processo chiamante.                                                       |
| [**IsImmersiveProcess**](/windows/desktop/api/Winuser/nf-winuser-isimmersiveprocess)                         | Determina se il processo appartiene a un'app di Windows Store.                                                                                                                                |
| [**NeedCurrentDirectoryForExePath**](/windows/win32/api/processenv/nf-processenv-needcurrentdirectoryforexepatha) | Determina se la directory corrente deve essere inclusa nel percorso di ricerca per l'eseguibile specificato.                                                                                  |
| [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)                                       | Apre un oggetto processo locale esistente.                                                                                                                                                       |
| [**QueryFullProcessImageName**](/windows/desktop/api/WinBase/nf-winbase-queryfullprocessimagenamea)           | Recupera il nome completo dell'immagine eseguibile per il processo specificato.                                                                                                                    |
| [**QueryProcessAffinityUpdateMode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprocessaffinityupdatemode) | Recupera la modalità di aggiornamento dell'affinità del processo specificato.                                                                                                                                  |
| [**QueryProcessCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryprocesscycletime)                   | Recupera la somma del tempo di ciclo di tutti i thread del processo specificato.                                                                                                                  |
| [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable)                 | Imposta il valore di una variabile di ambiente per il processo corrente.                                                                                                                            |
| [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass)                             | Imposta la classe di priorità per il processo specificato.                                                                                                                                            |
| [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask)                 | Imposta una maschera di affinità del processore per i thread di un processo specificato.                                                                                                                        |
| [**SetProcessAffinityUpdateMode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessaffinityupdatemode)     | Imposta la modalità di aggiornamento dell'affinità del processo specificato.                                                                                                                                       |
| [**SetProcessInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessinformation)                   | Imposta le informazioni per il processo specificato.                                                                                                                                                   |
| [**SetProcessMitigationPolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy)         | Imposta i criteri di mitigazione per il processo chiamante.                                                                                                                                           |
| [**SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost)               | Disabilita la possibilità del sistema di aumentare temporaneamente la priorità dei thread del processo specificato.                                                                                 |
| [**SetProcessRestrictionExemption**](/windows/desktop/api/Winuser/nf-winuser-setprocessrestrictionexemption) | Esenta il processo chiamante dalle restrizioni che impediscono ai processi desktop di interagire con l'ambiente app di Windows Store. Questa funzione viene usata dagli strumenti di sviluppo e debug. |
| [**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)     | Imposta i parametri di arresto per il processo attualmente chiamante.                                                                                                                                   |
| [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize)             | Imposta le dimensioni minime e massime working set per il processo specificato.                                                                                                                     |
| [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex)         | Imposta le dimensioni minime e massime working set per il processo specificato.                                                                                                                     |
| [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)                             | Termina il processo specificato e tutti i relativi thread.                                                                                                                                      |



 

## <a name="process-enumeration-functions"></a>Funzioni di enumerazione dei processi

Le funzioni seguenti vengono usate per enumerare i processi.



| Funzione                                                    | Descrizione                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Recupera l'identificatore di processo per ogni oggetto processo nel sistema.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Recupera informazioni sul primo processo rilevato in uno snapshot di sistema.    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Recupera informazioni sul processo successivo registrato in uno snapshot di sistema.        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Recupera informazioni sui processi attivi nel server terminal specificato. |



 

## <a name="policy-functions"></a>Funzioni dei criteri

Le funzioni seguenti vengono usate con i criteri a livello di processo.



|  Funzione                                                    |  Descrizione                                                     |
|------------------------------------------------------|-------------------------------------------------------|
| [**QueryProtectedPolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprotectedpolicy) | Esegue una query sul valore associato a un criterio protetto. |
| [**SetProtectedPolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprotectedpolicy)     | Imposta un criterio protetto.                              |



 

## <a name="thread-functions"></a>Funzioni thread

Le funzioni seguenti vengono usate con [i thread](multiple-threads.md).



| Funzione                                                           | Descrizione                                                                                                                                               |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput)                     | Collega il meccanismo di elaborazione dell'input di un thread a quello di un altro thread.                                                                          |
| [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)                   | Crea un thread che viene eseguito nello spazio degli indirizzi virtuali di un altro processo.                                                                               |
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)               | Crea un thread che viene eseguito nello spazio degli indirizzi virtuali di un altro processo e, facoltativamente, specifica attributi estesi, ad esempio affinità del gruppo di processori. |
| [**Createthread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)                               | Crea un thread da eseguire all'interno dello spazio degli indirizzi virtuali del processo chiamante.                                                                      |
| [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)                                   | Termina il thread chiamante.                                                                                                                                  |
| [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread)                       | Recupera uno pseudo handle per il thread corrente.                                                                                                         |
| [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid)                   | Recupera l'identificatore di thread del thread chiamante.                                                                                                    |
| [**GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread)                     | Recupera lo stato di terminazione del thread specificato.                                                                                                 |
| [**GetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-getthreaddescription)               | Recupera la descrizione assegnata a un thread chiamando [**SetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription).                                  |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)           | Recupera l'affinità del gruppo di processori del thread specificato.                                                                                           |
| [**GetThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadid)                                 | Recupera l'identificatore di thread del thread specificato.                                                                                                  |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)     | Recupera il numero del processore ideale per il thread specificato.                                                                           |
| [**GetThreadInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadinformation)               | Recupera informazioni sul thread specificato.                                                                                                         |
| [**GetThreadIOPendingFlag**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadiopendingflag)           | Determina se un thread specificato dispone di richieste di I/O in sospeso.                                                                                       |
| [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority)                     | Recupera il valore di priorità per il thread specificato.                                                                                                    |
| [**GetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost)           | Recupera lo stato priority boost controllo del thread specificato.                                                                                       |
| [**GetThreadTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadtimes)                           | Recupera le informazioni di intervallo per il thread specificato.                                                                                                    |
| [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)                                   | Apre un oggetto thread esistente.                                                                                                                          |
| [**QueryIdleProcessorCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime) | Recupera il tempo di ciclo per il thread inattivo di ogni processore nel sistema.                                                                             |
| [**QueryThreadCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-querythreadcycletime)               | Recupera il tempo di ciclo per il thread specificato.                                                                                                        |
| [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)                               | Decrementa il conteggio di sospensione di un thread.                                                                                                                      |
| [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask)             | Imposta una maschera di affinità del processore per il thread specificato.                                                                                                  |
| [**SetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription)               | Assegna una descrizione a un thread.                                                                                                                        |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)           | Imposta l'affinità del gruppo di processori per il thread specificato.                                                                                               |
| [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor)         | Specifica un processore preferito per un thread.                                                                                                             |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)     | Imposta il processore ideale per il thread specificato e recupera facoltativamente il processore ideale precedente.                                                  |
| [**SetThreadInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation)               | Imposta le informazioni per il thread specificato.                                                                                                                |
| [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)                     | Imposta il valore di priorità per il thread specificato.                                                                                                         |
| [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost)           | Disabilita la possibilità del sistema di aumentare temporaneamente la priorità di un thread.                                                                         |
| [**SetThreadStackGuarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee)         | Imposta la garanzia dello stack per il thread chiamante.                                                                                                          |
| [**Sospendi**](/windows/win32/api/synchapi/nf-synchapi-sleep)                                             | Sospende l'esecuzione del thread corrente per un intervallo specificato.                                                                                    |
| [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)                                         | Sospende il thread corrente finché non viene soddisfatta la condizione specificata.                                                                                         |
| [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread)                             | Sospende il thread specificato.                                                                                                                            |
| [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)                           | Determina che il thread chiamante ceda l'esecuzione a un altro thread pronto per l'esecuzione sul processore corrente.                                             |
| [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)                         | Termina un thread.                                                                                                                                      |
| [**Threadproc**](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))                                   | Funzione definita dall'applicazione che funge da indirizzo iniziale per un thread.                                                                         |
| [**Tlsalloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc)                                       | Alloca un indice tls (Thread Local Storage).                                                                                                             |
| [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree)                                         | Rilascia un indice TLS.                                                                                                                                     |
| [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue)                                 | Recupera il valore nello slot TLS del thread chiamante per un indice TLS specificato.                                                                           |
| [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue)                                 | Archivia un valore nello slot TLS del thread chiamante per un indice TLS specificato.                                                                                |
| [**WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle)                       | Attende fino a quando il processo specificato è in attesa dell'input dell'utente senza input in sospeso o fino a quando non è trascorso l'intervallo di timeout.                            |



 

## <a name="process-and-thread-extended-attribute-functions"></a>Funzioni degli attributi estesi di processo e thread

Le funzioni seguenti vengono usate per impostare attributi estesi per la creazione di processi e thread.



| Funzione                                                                       | Descrizione                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DeleteProcThreadAttributeList**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-deleteprocthreadattributelist)         | Elimina l'elenco specificato di attributi per la creazione di processi e thread.                            |
| [**InitializeProcThreadAttributeList**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist) | Inizializza l'elenco specificato di attributi per la creazione di processi e thread.                        |
| [**UpdateProcThreadAttribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute)                 | Aggiorna l'attributo specificato nell'elenco specificato di attributi per la creazione di processi e thread. |



 

## <a name="wow64-functions"></a>Funzioni WOW64

Le funzioni seguenti vengono usate con [WOW64.](../winprog64/running-32-bit-applications.md)



| Funzione                                         | Descrizione                                                                                                                            |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**IsWow64Message**](/windows/desktop/api/Winuser/nf-winuser-iswow64message)         | Determina se l'ultimo messaggio letto dalla coda del thread corrente ha avuto origine da un processo WOW64.                              |
| [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)         | Determina se il processo specificato è in esecuzione in WOW64.                                                                       |
| [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2)       | Determina se il processo specificato è in esecuzione in WOW64; restituisce anche informazioni aggiuntive sul processo e sull'architettura del computer. |
| [**Wow64SuspendThread**](/windows/desktop/api/WinBase/nf-winbase-wow64suspendthread) | Sospende il thread WOW64 specificato.                                                                                                   |



 

## <a name="job-object-functions"></a>Funzioni degli oggetti processo

Le funzioni seguenti vengono usate con gli [oggetti processo](job-objects.md).



| Funzione                                                       | Descrizione                                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject)   | Associa un processo a un oggetto processo esistente.                                                    |
| [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)                     | Crea o apre un oggetto processo.                                                                       |
| [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)                       | Determina se il processo è in esecuzione nel processo specificato.                                      |
| [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta)                         | Apre un oggetto processo esistente.                                                                        |
| [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) | Recupera le informazioni sui limiti e sullo stato del processo dall'oggetto processo.                                       |
| [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)     | Impostare i limiti per un oggetto processo.                                                                         |
| [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject)               | Termina tutti i processi attualmente associati al processo.                                          |
| [**UserHandleGrantAccess**](/windows/desktop/api/Winuser/nf-winuser-userhandlegrantaccess)         | Concede o nega l'accesso a un handle a un oggetto User a un processo con una restrizione dell'interfaccia utente. |



 

## <a name="thread-pool-functions"></a>Funzioni del pool di thread

Le funzioni seguenti vengono usate con i [pool di thread](thread-pools.md).



| Funzione                                                                                   | Descrizione                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallbackMayRunLong**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-callbackmayrunlong)                                           | Indica che il callback potrebbe non restituire rapidamente.                                                                                                                                                                                                 |
| [**CancelThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio)                                           | Annulla la notifica dalla [**funzione StartThreadpoolIo.**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio)                                                                                                                                                          |
| [**CloseThreadpool**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool)                                                 | Chiude il pool di thread specificato.                                                                                                                                                                                                                   |
| [**CloseThreadpoolCleanupGroup**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup)                         | Chiude il gruppo di pulizia specificato.                                                                                                                                                                                                                 |
| [**Closethreadpoolcleanupgroupmembers**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers)           | Rilascia i membri del gruppo di pulizia specificato, attende il completamento di tutte le funzioni di callback e facoltativamente annulla tutte le funzioni di callback in sospeso.                                                                                       |
| [**CloseThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolio)                                             | Rilascia l'oggetto di completamento I/O specificato.                                                                                                                                                                                                       |
| [**CloseThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer)                                       | Rilascia l'oggetto timer specificato.                                                                                                                                                                                                                |
| [**CloseThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait)                                         | Rilascia l'oggetto wait specificato.                                                                                                                                                                                                                 |
| [**CloseThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork)                                         | Rilascia l'oggetto lavoro specificato.                                                                                                                                                                                                                 |
| [**CreateThreadpool**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool)                                               | Alloca un nuovo pool di thread per eseguire i callback.                                                                                                                                                                                               |
| [**CreateThreadpoolCleanupGroup**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup)                       | Crea un gruppo di pulizia che le applicazioni possono usare per tenere traccia di uno o più callback del pool di thread.                                                                                                                                                       |
| [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio)                                           | Crea un nuovo oggetto di completamento I/O.                                                                                                                                                                                                                |
| [**CreateThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer)                                     | Crea un nuovo oggetto timer.                                                                                                                                                                                                                         |
| [**CreateThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait)                                       | Crea un nuovo oggetto wait.                                                                                                                                                                                                                          |
| [**CreateThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork)                                       | Crea un nuovo oggetto di lavoro.                                                                                                                                                                                                                          |
| [**DestroyThreadpoolEnvironment**](/windows/desktop/api/WinBase/nf-winbase-destroythreadpoolenvironment)                       | Elimina l'ambiente di callback specificato. Chiamare questa funzione quando l'ambiente di callback non è più necessario per la creazione di nuovi oggetti pool di thread.                                                                                              |
| [**DisassociateCurrentThreadFromCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-disassociatecurrentthreadfromcallback)     | Rimuove l'associazione tra la funzione di callback attualmente in esecuzione e l'oggetto che ha avviato il callback. Il thread corrente non verrà più conteggiato come l'esecuzione di un callback per conto dell'oggetto .                                      |
| [**FreeLibraryWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns)                   | Specifica la DLL che verrà scaricata dal pool di thread al completamento del callback corrente.                                                                                                                                                             |
| [**InitializeThreadpoolEnvironment**](/windows/desktop/api/WinBase/nf-winbase-initializethreadpoolenvironment)                 | Inizializza un ambiente di callback.                                                                                                                                                                                                                 |
| [**IsThreadpoolTimerSet**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-isthreadpooltimerset)                                       | Determina se l'oggetto timer specificato è attualmente impostato.                                                                                                                                                                                     |
| [**LeaveCriticalSectionWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-leavecriticalsectionwhencallbackreturns) | Specifica la sezione critica che il pool di thread rilascerà al completamento del callback corrente.                                                                                                                                               |
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)                 | Recupera le dimensioni di riserva e commit dello stack per i thread nel pool di thread specificato.                                                                                                                                                              |
| [**ReleaseMutexWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasemutexwhencallbackreturns)                 | Specifica il mutex che il pool di thread rilascerà al completamento del callback corrente.                                                                                                                                                          |
| [**ReleaseSemaphoreWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasesemaphorewhencallbackreturns)         | Specifica il semaforo che il pool di thread rilascerà al completamento del callback corrente.                                                                                                                                                      |
| [**SetEventWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-seteventwhencallbackreturns)                         | Specifica l'evento che verrà impostato dal pool di thread al completamento del callback corrente.                                                                                                                                                              |
| [**SetThreadpoolCallbackCleanupGroup**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackcleanupgroup)             | Associa il gruppo di pulizia specificato all'ambiente di callback specificato.                                                                                                                                                                     |
| [**SetThreadpoolCallbackLibrary**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbacklibrary)                       | Assicura che la DLL specificata rimanga caricata finché sono presenti callback in sospeso.                                                                                                                                                           |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)                 | Specifica che il callback deve essere eseguito in un thread persistente.                                                                                                                                                                                      |
| [**SetThreadpoolCallbackPool**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpool)                             | Imposta il pool di thread da utilizzare durante la generazione di callback.                                                                                                                                                                                          |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)                     | Specifica la priorità di una funzione di callback rispetto ad altri elementi di lavoro nello stesso pool di thread.                                                                                                                                                 |
| [**SetThreadpoolCallbackRunsLong**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackrunslong)                     | Indica che i callback associati a questo ambiente di callback potrebbero non restituire rapidamente risultati.                                                                                                                                                          |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)                     | Imposta le dimensioni di riserva e commit dello stack per i nuovi thread nel pool di thread specificato.                                                                                                                                                               |
| [**SetThreadpoolThreadMaximum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum)                           | Imposta il numero massimo di thread che il pool di thread specificato può allocare per elaborare i callback.                                                                                                                                                |
| [**SetThreadpoolThreadMinimum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum)                           | Imposta il numero minimo di thread che il pool di thread specificato deve rendere disponibile per elaborare i callback.                                                                                                                                         |
| [**SetThreadpoolTimerEx**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimerex)                                       | Imposta l'oggetto timer. Un thread di lavoro chiama il callback dell'oggetto timer dopo la scadenza del timeout specificato.                                                                                                                                       |
| [**SetThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer)                                           | Imposta l'oggetto timer. Un thread di lavoro chiama il callback dell'oggetto timer dopo la scadenza del timeout specificato.                                                                                                                                       |
| [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait)                                             | Imposta l'oggetto wait. Un thread di lavoro chiama la funzione di callback dell'oggetto di attesa dopo che l'handle viene segnalato o dopo la scadenza del timeout specificato.                                                                                           |
| [**SetThreadpoolWaitEx**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwaitex)                                         | Imposta l'oggetto wait. Un thread di lavoro chiama la funzione di callback dell'oggetto di attesa dopo che l'handle viene segnalato o dopo la scadenza del timeout specificato.                                                                                           |
| [**StartThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio)                                             | Notifica al pool di thread che le operazioni di I/O possono iniziare per l'oggetto di completamento I/O specificato. Un thread di lavoro chiama la funzione di callback dell'oggetto di completamento I/O dopo il completamento dell'operazione sull'handle di file associato a questo oggetto. |
| [**SubmitThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork)                                       | Invia un oggetto di lavoro al pool di thread. Un thread di lavoro chiama la funzione di callback dell'oggetto di lavoro.                                                                                                                                                  |
| [**TpInitializeCallbackEnviron**](/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron)                         | Inizializza un ambiente di callback per il pool di thread.                                                                                                                                                                                             |
| [**TpDestroyCallbackEnviron**](/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron)                               | Elimina l'ambiente di callback specificato. Chiamare questa funzione quando l'ambiente di callback non è più necessario per la creazione di nuovi oggetti pool di thread.                                                                                              |
| [**TpSetCallbackActivationContext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext)                   | Assegna un contesto di attivazione all'ambiente di callback.                                                                                                                                                                                          |
| [**TpSetCallbackCleanupGroup**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup)                             | Associa il gruppo di pulizia specificato all'ambiente di callback specificato.                                                                                                                                                                     |
| [**TpSetCallbackFinalizationCallback**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback)             | Indica una funzione da chiamare quando l'ambiente di callback è finalizzato.                                                                                                                                                                            |
| [**TpSetCallbackLongFunction**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction)                             | Indica che i callback associati a questo ambiente di callback potrebbero non restituire rapidamente risultati.                                                                                                                                                          |
| [**TpSetCallbackNoActivationContext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext)               | Indica che l'ambiente di callback non ha un contesto di attivazione.                                                                                                                                                                                  |
| [**TpSetCallbackPersistent**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent)                                 | Specifica che il callback deve essere eseguito in un thread persistente.                                                                                                                                                                                      |
| [**TpSetCallbackPriority**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority)                                     | Specifica la priorità di una funzione di callback rispetto ad altri elementi di lavoro nello stesso pool di thread.                                                                                                                                                 |
| [**TpSetCallbackRaceWithDll**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll)                               | Assicura che la DLL specificata rimanga caricata finché sono presenti callback in sospeso.                                                                                                                                                           |
| [**TpSetCallbackThreadpool**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool)                                 | Assegna un pool di thread a un ambiente di callback.                                                                                                                                                                                                    |
| [**TrySubmitThreadpoolCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-trysubmitthreadpoolcallback)                         | Richiede che un thread di lavoro del pool di thread chiami la funzione di callback specificata.                                                                                                                                                                     |
| [**WaitForThreadpoolIoCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooliocallbacks)                       | Attende il completamento dei callback di completamento I/O in sospeso e facoltativamente annulla i callback in sospeso che non sono ancora stati avviati per l'esecuzione.                                                                                                           |
| [**WaitForThreadpoolTimerCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks)                 | Attende il completamento dei callback del timer in sospeso e facoltativamente annulla i callback in sospeso che non sono ancora stati avviati per l'esecuzione.                                                                                                                    |
| [**WaitForThreadpoolWaitCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks)                   | Attende il completamento dei callback di attesa in sospeso e facoltativamente annulla i callback in sospeso che non sono ancora stati avviati per l'esecuzione.                                                                                                                     |
| [**WaitForThreadpoolWorkCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolworkcallbacks)                   | Attende il completamento dei callback di lavoro in sospeso e facoltativamente annulla i callback in sospeso che non sono ancora stati avviati per l'esecuzione.                                                                                                                     |



 

Le funzioni seguenti fanno parte dell'API di [pooling di thread](thread-pooling.md) originale.



| Funzione                                                            | Descrizione                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)        | Associa la porta di completamento I/O di proprietà del pool di thread all'handle di file specificato. Al completamento di una richiesta di I/O che interessa questo file, un thread di lavoro non di I/O eseguirà la funzione di callback specificata. |
| [**Queueuserworkitem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                      | Accoda un elemento di lavoro a un thread di lavoro nel pool di thread.                                                                                                                                                              |
| [**Registerwaitforsingleobject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) | Indica a un thread di attesa nel pool di thread di attendere l'oggetto .                                                                                                                                                        |
| [**UnregisterWaitEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-unregisterwaitex)                       | Attende che uno o tutti gli oggetti specificati siano nello stato segnalato o che sia trascorso l'intervallo di timeout.                                                                                                            |



 

## <a name="thread-ordering-service-functions"></a>Funzioni del servizio di ordinamento dei thread

Le funzioni seguenti vengono usate con il [servizio di ordinamento dei thread](thread-ordering-service.md).



| Funzione                                                                   | Descrizione                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**AvQuerySystemResponsiveness**](/windows/desktop/api/Avrt/nf-avrt-avquerysystemresponsiveness)         | Recupera l'impostazione di velocità di risposta del sistema utilizzata dal servizio di pianificazione delle classi multimediali. |
| [**AvRtCreateThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup)     | Crea un gruppo di ordinamento dei thread.                                                            |
| [**AvRtCreateThreadOrderingGroupEx**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroupexa) | Crea un gruppo di ordinamento dei thread e associa il thread del server a un'attività.               |
| [**AvRtDeleteThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup)     | Elimina il gruppo di ordinamento dei thread specificato creato dal chiamante.                          |
| [**AvRtJoinThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup)         | Unisce i thread client a un gruppo di ordinamento dei thread.                                            |
| [**AvRtLeaveThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup)       | Consente ai thread client di uscire da un gruppo di ordinamento dei thread.                                    |
| [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup)     | Consente ai thread client di un gruppo di ordinamento di thread di attendere l'esecuzione.        |



 

## <a name="multimedia-class-scheduler-service-functions"></a>Funzioni del servizio Utilità di pianificazione classi multimediali

Le funzioni seguenti vengono usate con il servizio [utilità di pianificazione della classe multimediale](multimedia-class-scheduler-service.md).



| Funzione                                                                   | Descrizione                                                                                           |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**AvRevertMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avrevertmmthreadcharacteristics) | Indica che un thread non esegue più il lavoro associato all'attività specificata.              |
| [**AvSetMmMaxThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) | Associa il thread chiamante alle attività specificate.                                               |
| [**AvSetMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa)       | Associa il thread chiamante all'attività specificata.                                                |
| [**AvSetMmThreadPriority**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority)                     | Regola la priorità del thread chiamante rispetto ad altri thread che eseguono la stessa attività. |



 

## <a name="fiber-functions"></a>Funzioni fiber

Le funzioni seguenti vengono usate con [fiber .](fibers.md)



| Funzione                                                 | Descrizione                                                                                                  |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**ConvertFiberToThread**](/windows/desktop/api/WinBase/nf-winbase-convertfibertothread)     | Converte il fiber corrente in un thread.                                                                    |
| [**ConvertThreadToFiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber)     | Converte il thread corrente in un fiber.                                                                    |
| [**ConvertThreadToFiberEx**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiberex) | Converte il thread corrente in un fiber.                                                                    |
| [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber)                       | Alloca un oggetto fiber, gli assegna uno stack e imposta l'esecuzione in modo che inizi dall'indirizzo iniziale specificato. |
| [**CreateFiberEx**](/windows/desktop/api/WinBase/nf-winbase-createfiberex)                   | Alloca un oggetto fiber, gli assegna uno stack e imposta l'esecuzione in modo che inizi dall'indirizzo iniziale specificato. |
| [**DeleteFiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber)                       | Elimina un fiber esistente.                                                                                   |
| [**FiberProc**](/windows/win32/api/winbase/nc-winbase-pfiber_start_routine)                           | Funzione definita dall'applicazione usata con la [**funzione CreateFiber.**](/windows/desktop/api/WinBase/nf-winbase-createfiber)                   |
| [**FlsAlloc**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc)                             | Alloca un indice di archiviazione fiber local (FLS).                                                                 |
| [**FlsFree**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree)                               | Rilascia un indice FLS.                                                                                       |
| [**FlsGetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)                       | Recupera il valore nello slot FLS del fiber chiamante per un indice FLS specificato.                               |
| [**FlsSetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)                       | Archivia un valore nello slot FLS del fiber chiamante per un indice FLS specificato.                                    |
| [**IsThreadAFiber**](/windows/win32/api/fibersapi/nf-fibersapi-isthreadafiber)                 | Determina se il thread corrente è un fiber.                                                            |
| [**SwitchToFiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber)                   | Pianifica un fiber.                                                                                           |



 

## <a name="numa-support-functions"></a>Funzioni di supporto NUMA

Le funzioni seguenti forniscono il [supporto NUMA](numa-support.md).



| Funzione                                                                 | Descrizione                                                                                                                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)  | Riserva o esegue il commit di un'area di memoria all'interno dello spazio degli indirizzi virtuali del processo specificato e specifica il nodo NUMA per la memoria fisica. |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Recupera informazioni sui processori logici e sull'hardware correlato.                                                                                   |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)         | Recupera la quantità di memoria disponibile nel nodo specificato.                                                                                        |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)     | Recupera la quantità di memoria disponibile nel nodo specificato come valore USHORT.                                                              |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)             | Recupera il nodo con il numero più alto.                                                                                              |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)       | Recupera il nodo NUMA associato al dispositivo sottostante per un handle di file.                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)             | Recupera la maschera del processore per il nodo specificato.                                                                                                   |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)         | Recupera la maschera del processore per il nodo NUMA specificato come valore USHORT.                                                                            |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                     | Recupera il numero di nodo per il processore specificato.                                                                                                 |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                 | Recupera il numero di nodo del processore logico specificato come valore USHORT.                                                                        |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                     | Recupera il numero di nodo per l'identificatore di prossimità specificato.                                                                                      |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                 | Recupera il numero di nodo come valore USHORT per l'identificatore di prossimità specificato.                                                                    |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                        | Riserva o esegue il commit di un'area di memoria all'interno dello spazio degli indirizzi virtuali del processo specificato e specifica il nodo NUMA per la memoria fisica. |



 

## <a name="processor-functions"></a>Funzioni del processore

Le funzioni seguenti vengono usate con i processori logici e i [gruppi di processori](processor-groups.md).



| Funzione                                                                     | Descrizione                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)                   | Restituisce il numero di processori attivi in un gruppo di processori o nel sistema.                                       |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)         | Restituisce il numero di gruppi di processori attivi nel sistema.                                                         |
| [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)               | Recupera il numero del processore su cui era in esecuzione il thread corrente durante la chiamata a questa funzione.            |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)           | Recupera il gruppo di processori e il numero del processore logico in cui è in esecuzione il thread chiamante.            |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Recupera informazioni sui processori logici e sull'hardware correlato.                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Recupera informazioni sulle relazioni dei processori logici e dell'hardware correlato.                            |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)                 | Restituisce il numero massimo di processori logici che un gruppo di processori o il sistema può avere.                      |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)       | Restituisce il numero massimo di gruppi di processori che il sistema può avere.                                             |
| [**QueryIdleProcessorCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime)           | Recupera il tempo di ciclo per il thread inattivo di ogni processore nel sistema.                                        |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)       | Recupera il tempo di ciclo accumulato per il thread inattivo in ogni processore logico nel gruppo di processori specificato. |



 

## <a name="user-mode-scheduling-functions"></a>User-Mode funzioni di pianificazione

Le funzioni seguenti vengono usate con la pianificazione in modalità utente (UMS).



| Funzione                                                               | Descrizione                                                                                               |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)             | Crea un elenco di completamento UMS.                                                                            |
| [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)               | Crea un contesto di thread UMS per rappresentare un thread di lavoro UMS.                                            |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)             | Elimina l'elenco di completamento UMS specificato. L'elenco deve essere vuoto.                                        |
| [**DeleteUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)               | Elimina il contesto del thread UMS specificato. Il thread deve essere terminato.                                  |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) | Recupera i thread di lavoro UMS dall'elenco di completamento UMS specificato.                                      |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)               | Converte il thread chiamante in un thread dell'utilità di pianificazione UMS.                                                  |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)                           | Esegue il thread di lavoro UMS specificato.                                                                     |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)                     | Restituisce il contesto del thread UMS chiamante.                                                 |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)                       | Restituisce il contesto del thread UMS successivo in un elenco di contesti di thread UMS.                                     |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)         | Recupera un handle per l'evento associato all'elenco di completamento UMS specificato.                        |
| [**GetUmsSystemThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-getumssystemthreadinformation) | Esegue una query se il thread specificato è un thread dell'utilità di pianificazione UMS, un thread di lavoro UMS o un thread non UMS. |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)         | Recupera informazioni sul thread di lavoro UMS specificato.                                              |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)             | Imposta informazioni di contesto specifiche dell'applicazione per il thread di lavoro UMS specificato.                        |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)                             | Funzione del punto di ingresso dell'utilità di pianificazione UMS definita dall'applicazione associata a un elenco di completamento UMS.         |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)                               | Cede il controllo al thread dell'utilità di pianificazione UMS in cui è in esecuzione il thread di lavoro UMS chiamante.             |



 

## <a name="obsolete-functions"></a>Funzioni obsolete

-   [**NtGetCurrentProcessorNumber**](ntgetcurrentprocessornumber.md)
-   [**NtQueryInformationProcess**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationprocess)
-   [**NtQueryInformationThread**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationthread)
-   [**WinExec**](/windows/desktop/api/WinBase/nf-winbase-winexec)
-   [**ZwQueryInformationProcess**](zwqueryinformationprocess.md)

 

 
