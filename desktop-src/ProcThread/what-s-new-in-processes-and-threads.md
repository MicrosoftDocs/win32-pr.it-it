---
description: Windows 7 e Windows Server 2008 R2 includono i nuovi elementi di programmazione seguenti per i processi e i thread.
ms.assetid: 69cd8713-b40c-4fec-a256-9c2ee3d73da5
title: Novità di processi e thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7dfb708a2890bab1fcd3fd66385f74bd8513b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881689"
---
# <a name="whats-new-in-processes-and-threads"></a>Novità di processi e thread

Windows 7 e Windows Server 2008 R2 includono i nuovi elementi di programmazione seguenti per i processi e i thread.

## <a name="new-capabilities"></a>Nuove funzionalità

Le versioni a 64 bit di Windows 7 e Windows Server 2008 R2 supportano più di 64 processori logici in un singolo computer. Per ulteriori informazioni, vedere [gruppi di processori](processor-groups.md).

La pianificazione in modalità utente è un meccanismo leggero che le applicazioni possono utilizzare per pianificare i propri thread. Per ulteriori informazioni, vedere [pianificazione in modalità utente](user-mode-scheduling.md).

## <a name="new-functions"></a>Funzioni nuove

Con i processori e i gruppi di processori vengono utilizzate le nuove funzioni seguenti.



| Funzione                                                                                | Descrizione                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)<br/>                         | Crea un thread che viene eseguito nello spazio degli indirizzi virtuali di un altro processo e, facoltativamente, specifica gli attributi estesi, ad esempio l'affinità del gruppo di processori.<br/> |
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)<br/>                   | Restituisce il numero di processori attivi in un gruppo di processori o nel sistema.<br/>                                                                            |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)<br/>         | Restituisce il numero di gruppi di processori attivi nel sistema.<br/>                                                                                              |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)<br/>           | Recupera il gruppo di processori e il numero del processore logico in cui è in esecuzione il thread chiamante.<br/>                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex)<br/> | Recupera le informazioni sulle relazioni tra i processori logici e i componenti hardware correlati.<br/>                                                                 |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)<br/>                 | Restituisce il numero massimo di processori logici che possono essere presenti in un gruppo di processori o nel sistema.<br/>                                                           |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)<br/>       | Restituisce il numero massimo di gruppi di processori che possono essere presenti nel sistema. <br/>                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)<br/>         | Recupera la quantità di memoria disponibile nel nodo specificato come valore USHORT.<br/>                                                                 |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)<br/>           | Recupera il nodo NUMA associato al dispositivo sottostante per un handle di file.<br/>                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)<br/>             | Recupera la maschera del processore per il nodo NUMA specificato come valore USHORT.<br/>                                                                               |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)<br/>                     | Recupera il numero di nodo del processore logico specificato come valore USHORT.<br/>                                                                           |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)<br/>                     | Recupera il numero di nodo come valore USHORT per l'identificatore di prossimità specificato.<br/>                                                                       |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)<br/>                   | Recupera l'affinità del gruppo di processori del processo specificato.<br/>                                                                                          |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)<br/>           | Recupera la durata del ciclo di ogni processore del gruppo specificato durante l'esecuzione delle chiamate di procedura posticipate (DPC) e delle routine del servizio di interrupt (ISRs).<br/>     |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)<br/>                     | Recupera l'affinità del gruppo di processori del thread specificato.<br/>                                                                                           |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)<br/>               | Recupera il numero del processore ideale per il thread specificato.<br/>                                                                           |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)<br/>       | Recupera il tempo di ciclo accumulato per il thread inattivo in ogni processore logico del gruppo di processori specificato. <br/>                                     |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)<br/>                     | Imposta l'affinità del gruppo di processori per il thread specificato.<br/>                                                                                               |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)<br/>               | Imposta il processore ideale per il thread specificato e, facoltativamente, recupera il processore ideale precedente.<br/>                                                  |



 

Con i pool di thread vengono utilizzate le nuove funzioni seguenti.



| Funzione                                                                              | Descrizione                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)<br/> | Recupera le dimensioni della riserva dello stack e del commit per i thread nel pool di thread specificato.<br/>              |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)<br/> | Specifica che il callback deve essere eseguito su un thread permanente.<br/>                                      |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)<br/>     | Specifica la priorità di una funzione di callback rispetto ad altri elementi di lavoro nello stesso pool di thread.<br/> |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)<br/>     | Imposta le dimensioni della riserva dello stack e del commit per i nuovi thread nel pool di thread specificato. <br/>              |



 

Con UMS vengono usate le nuove funzioni seguenti.



| Funzione                                                                          | Descrizione                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)<br/>             | Crea un elenco di completamento UMS.<br/>                                                                     |
| [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)<br/>               | Crea un contesto del thread UMS per rappresentare un thread di lavoro UMS.<br/>                                     |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)<br/>             | Elimina l'elenco di completamento UMS specificato. L'elenco deve essere vuoto.<br/>                                 |
| [**DeleteUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)<br/>               | Elimina il contesto del thread UMS specificato. Il thread deve terminare.<br/>                           |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems)<br/> | Recupera i thread di lavoro UMS dall'elenco di completamento UMS specificato.<br/>                               |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)<br/>               | Converte il thread chiamante in un thread dell'utilità di pianificazione UMS.<br/>                                           |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)<br/>                           | Esegue il thread di lavoro UMS specificato.<br/>                                                              |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)<br/>                     | Restituisce il contesto del thread UMS del thread UMS chiamante.<br/>                                          |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)<br/>                       | Restituisce il contesto del thread UMS successivo in un elenco di contesti di thread UMS.<br/>                              |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)<br/>         | Recupera un handle per l'evento associato all'elenco di completamento UMS specificato.<br/>                 |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)<br/>         | Recupera le informazioni sul thread di lavoro UMS specificato.<br/>                                       |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)<br/>             | Imposta le informazioni sul contesto specifiche dell'applicazione per il thread di lavoro UMS specificato.<br/>                 |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)<br/>                             | Funzione del punto di ingresso dell'utilità di pianificazione UMS definita dall'applicazione associata a un elenco di completamento UMS. <br/> |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)<br/>                               | Restituisce il controllo al thread dell'utilità di pianificazione UMS su cui è in esecuzione il thread di lavoro UMS chiamante.<br/>      |



 

## <a name="new-structures"></a>Nuove strutture



| Struttura                                                                                                 | Descrizione                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**\_relazione cache**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)<br/>                                              | Vengono descritti gli attributi della cache. <br/>                                                             |
| [**\_affinità gruppo**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)<br/>                                                      | Contiene un'affinità specifica del gruppo di processori, ad esempio l'affinità di un thread.<br/>          |
| [**\_relazione tra gruppi**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)<br/>                                              | Contiene informazioni sui gruppi di processori. <br/>                                            |
| [**\_relazione nodo \_ NUMA**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)<br/>                                     | Contiene informazioni su un nodo NUMA in un gruppo di processori. <br/>                            |
| [**\_informazioni gruppo \_ processore**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)<br/>                                         | Contiene il numero e l'affinità dei processori in un gruppo di processori.<br/>                     |
| [**\_numero processore**](/windows/desktop/api/WinNT/ns-winnt-processor_number)<br/>                                                  | Rappresenta un processore logico in un gruppo di processori.<br/>                                     |
| [**\_relazione processore**](/windows/desktop/api/WinNT/ns-winnt-processor_relationship)<br/>                                      | Contiene informazioni sull'affinità all'interno di un gruppo di processori.<br/>                            |
| [**\_ \_ informazioni sul processore logico di sistema, ad \_ \_ esempio**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)<br/> | Contiene informazioni sulle relazioni tra i processori logici e l'hardware correlato.<br/> |
| [**\_attributi di \_ thread \_ creati da UMS**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)<br/>                        | Specifica gli attributi per un thread di lavoro UMS. <br/>                                           |
| [**\_informazioni di avvio dell'utilità di pianificazione UMS \_ \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)<br/>                            | Specifica gli attributi per un thread dell'utilità di pianificazione UMS<br/>                                          |



 

 

 
