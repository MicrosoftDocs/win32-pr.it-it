---
description: Windows 7 e Windows Server 2008 R2 includono i nuovi elementi di programmazione seguenti per processi e thread.
ms.assetid: 69cd8713-b40c-4fec-a256-9c2ee3d73da5
title: Novità di processi e thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe8b53349f5c6f19dd9beda1ffe6b933fbff63533988a40937453194df57295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792959"
---
# <a name="whats-new-in-processes-and-threads"></a>Novità di processi e thread

Windows 7 e Windows Server 2008 R2 includono i nuovi elementi di programmazione seguenti per processi e thread.

## <a name="new-capabilities"></a>Nuove funzionalità

Le versioni a 64 bit di Windows 7 e Windows Server 2008 R2 supportano più di 64 processori logici in un singolo computer. Per altre informazioni, vedere [Gruppi di processori.](processor-groups.md)

La pianificazione in modalità utente è un meccanismo leggero che le applicazioni possono usare per pianificare i propri thread. Per altre informazioni, vedere [Pianificazione in modalità utente.](user-mode-scheduling.md)

## <a name="new-functions"></a>Funzioni nuove

Le nuove funzioni seguenti vengono usate con processori e gruppi di processori.



| Funzione                                                                                | Descrizione                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)<br/>                         | Crea un thread che viene eseguito nello spazio di indirizzi virtuali di un altro processo e, facoltativamente, specifica gli attributi estesi, ad esempio l'affinità del gruppo di processori.<br/> |
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)<br/>                   | Restituisce il numero di processori attivi in un gruppo di processori o nel sistema.<br/>                                                                            |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)<br/>         | Restituisce il numero di gruppi di processori attivi nel sistema.<br/>                                                                                              |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)<br/>           | Recupera il gruppo di processori e il numero del processore logico in cui è in esecuzione il thread chiamante.<br/>                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex)<br/> | Recupera informazioni sulle relazioni dei processori logici e dell'hardware correlato.<br/>                                                                 |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)<br/>                 | Restituisce il numero massimo di processori logici che un gruppo di processori o il sistema può avere.<br/>                                                           |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)<br/>       | Restituisce il numero massimo di gruppi di processori che il sistema può avere. <br/>                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)<br/>         | Recupera la quantità di memoria disponibile nel nodo specificato come valore USHORT.<br/>                                                                 |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)<br/>           | Recupera il nodo NUMA associato al dispositivo sottostante per un handle di file.<br/>                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)<br/>             | Recupera la maschera del processore per il nodo NUMA specificato come valore USHORT.<br/>                                                                               |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)<br/>                     | Recupera il numero di nodo del processore logico specificato come valore USHORT.<br/>                                                                           |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)<br/>                     | Recupera il numero di nodo come valore USHORT per l'identificatore di prossimità specificato.<br/>                                                                       |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)<br/>                   | Recupera l'affinità del gruppo di processori del processo specificato.<br/>                                                                                          |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)<br/>           | Recupera il tempo di ciclo impiegato da ogni processore nel gruppo specificato per l'esecuzione di chiamate di routine posticipate (DPC) e di routine del servizio di interrupt (ISR).<br/>     |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)<br/>                     | Recupera l'affinità del gruppo di processori del thread specificato.<br/>                                                                                           |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)<br/>               | Recupera il numero del processore ideale per il thread specificato.<br/>                                                                           |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)<br/>       | Recupera il tempo di ciclo accumulato per il thread inattivo in ogni processore logico nel gruppo di processori specificato. <br/>                                     |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)<br/>                     | Imposta l'affinità del gruppo di processori per il thread specificato.<br/>                                                                                               |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)<br/>               | Imposta il processore ideale per il thread specificato e, facoltativamente, recupera il processore ideale precedente.<br/>                                                  |



 

Le nuove funzioni seguenti vengono usate con i pool di thread.



| Funzione                                                                              | Descrizione                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)<br/> | Recupera le dimensioni di riserva e commit dello stack per i thread nel pool di thread specificato.<br/>              |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)<br/> | Specifica che il callback deve essere eseguito in un thread persistente.<br/>                                      |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)<br/>     | Specifica la priorità di una funzione di callback rispetto ad altri elementi di lavoro nello stesso pool di thread.<br/> |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)<br/>     | Imposta le dimensioni di riserva e commit dello stack per i nuovi thread nel pool di thread specificato. <br/>              |



 

Le nuove funzioni seguenti vengono usate con UMS.



| Funzione                                                                          | Descrizione                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)<br/>             | Crea un elenco di completamento UMS.<br/>                                                                     |
| [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)<br/>               | Crea un contesto di thread UMS per rappresentare un thread di lavoro UMS.<br/>                                     |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)<br/>             | Elimina l'elenco di completamento UMS specificato. L'elenco deve essere vuoto.<br/>                                 |
| [**DeleteUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)<br/>               | Elimina il contesto del thread UMS specificato. Il thread deve essere terminato.<br/>                           |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems)<br/> | Recupera i thread di lavoro UMS dall'elenco di completamento UMS specificato.<br/>                               |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)<br/>               | Converte il thread chiamante in un thread dell'utilità di pianificazione UMS.<br/>                                           |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)<br/>                           | Esegue il thread di lavoro UMS specificato.<br/>                                                              |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)<br/>                     | Restituisce il contesto del thread UMS chiamante.<br/>                                          |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)<br/>                       | Restituisce il contesto del thread UMS successivo in un elenco di contesti di thread UMS.<br/>                              |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)<br/>         | Recupera un handle per l'evento associato all'elenco di completamento UMS specificato.<br/>                 |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)<br/>         | Recupera informazioni sul thread di lavoro UMS specificato.<br/>                                       |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)<br/>             | Imposta informazioni di contesto specifiche dell'applicazione per il thread di lavoro UMS specificato.<br/>                 |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)<br/>                             | Funzione del punto di ingresso dell'utilità di pianificazione UMS definita dall'applicazione associata a un elenco di completamento UMS. <br/> |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)<br/>                               | Cede il controllo al thread dell'utilità di pianificazione UMS in cui è in esecuzione il thread di lavoro UMS chiamante.<br/>      |



 

## <a name="new-structures"></a>Nuove strutture



| Struttura                                                                                                 | Descrizione                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**RELAZIONE \_ CACHE**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)<br/>                                              | Descrive gli attributi della cache. <br/>                                                             |
| [**AFFINITÀ \_ DI GRUPPO**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)<br/>                                                      | Contiene un'affinità specifica del gruppo di processori, ad esempio l'affinità di un thread.<br/>          |
| [**RELAZIONE \_ DI GRUPPO**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)<br/>                                              | Contiene informazioni sui gruppi di processori. <br/>                                            |
| [**RELAZIONE TRA NODI NUMA \_ \_**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)<br/>                                     | Contiene informazioni su un nodo NUMA in un gruppo di processori. <br/>                            |
| [**INFORMAZIONI SUL \_ GRUPPO DI \_ PROCESSORI**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)<br/>                                         | Contiene il numero e l'affinità dei processori in un gruppo di processori.<br/>                     |
| [**NUMERO \_ PROCESSORE**](/windows/desktop/api/WinNT/ns-winnt-processor_number)<br/>                                                  | Rappresenta un processore logico in un gruppo di processori.<br/>                                     |
| [**RELAZIONE \_ PROCESSORE**](/windows/desktop/api/WinNT/ns-winnt-processor_relationship)<br/>                                      | Contiene informazioni sull'affinità all'interno di un gruppo di processori.<br/>                            |
| [**INFORMAZIONI \_ SUL \_ PROCESSORE LOGICO DI SISTEMA \_ \_ EX**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)<br/> | Contiene informazioni sulle relazioni dei processori logici e dell'hardware correlato.<br/> |
| [**ATTRIBUTI DI \_ CREAZIONE \_ THREAD UMS \_**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)<br/>                        | Specifica gli attributi per un thread di lavoro UMS. <br/>                                           |
| [**INFORMAZIONI DI AVVIO \_ DELL'UTILITÀ \_ DI PIANIFICAZIONE UMS \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)<br/>                            | Specifica gli attributi per un thread dell'utilità di pianificazione UMS<br/>                                          |



 

 

 
