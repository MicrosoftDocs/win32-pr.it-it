---
description: Il modello tradizionale per il supporto multiprocessore è Symmetric Multiprocessor (SMP). In questo modello ogni processore ha accesso uguale a memoria e I/O. Con l'aggiunta di più processori, il bus di processore diventa una limitazione per le prestazioni del sistema.
ms.assetid: a1263968-2b26-45cc-bdd7-6aa354821a5a
title: Supporto NUMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559df7d4e13571953f2826188bd80ccbc472b2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311978"
---
# <a name="numa-support"></a>Supporto NUMA

Il modello tradizionale per il supporto multiprocessore è Symmetric Multiprocessor (SMP). In questo modello ogni processore ha accesso uguale a memoria e I/O. Con l'aggiunta di più processori, il bus di processore diventa una limitazione per le prestazioni del sistema.

I progettisti di sistema utilizzano l'accesso non uniforme alla memoria (NUMA) per aumentare la velocità del processore senza aumentare il carico sul bus del processore. L'architettura è non uniforme perché ogni processore è vicino ad alcune parti della memoria e più lontano da altre parti della memoria. Il processore ottiene rapidamente l'accesso alla memoria a cui si avvicina, mentre può richiedere più tempo per ottenere l'accesso alla memoria più lontana.

In un sistema NUMA le CPU sono disposte in sistemi più piccoli chiamati *nodi*. Ogni nodo dispone di processori e memoria propri ed è connesso al sistema più grande tramite un bus di interconnessione coerente con la cache.

Il sistema tenta di migliorare le prestazioni pianificando i thread nei processori che si trovano nello stesso nodo della memoria utilizzata. Tenta di soddisfare le richieste di allocazione della memoria all'interno del nodo, ma alloca memoria da altri nodi, se necessario. Fornisce inoltre un'API per rendere la topologia del sistema disponibile per le applicazioni. È possibile migliorare le prestazioni delle applicazioni usando le funzioni NUMA per ottimizzare la pianificazione e l'utilizzo della memoria.

Prima di tutto, sarà necessario determinare il layout dei nodi nel sistema. Per recuperare il nodo con il numero più alto nel sistema, usare la funzione [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber) . Si noti che questo numero non è garantito uguale al numero totale di nodi nel sistema. Inoltre, non è garantito che i nodi con numeri sequenziali siano vicini tra loro. Per recuperare l'elenco di processori nel sistema, utilizzare la funzione [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) . È possibile determinare il nodo per ogni processore nell'elenco usando la funzione [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode) . In alternativa, per recuperare un elenco di tutti i processori in un nodo, utilizzare la funzione [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask) .

Dopo aver determinato i processori che appartengono ai nodi, è possibile ottimizzare le prestazioni dell'applicazione. Per assicurarsi che tutti i thread per il processo vengano eseguiti nello stesso nodo, usare la funzione [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) con una maschera di affinità di processo che specifica i processori nello stesso nodo. Ciò consente di aumentare l'efficienza delle applicazioni i cui thread devono accedere alla stessa memoria. In alternativa, per limitare il numero di thread in ogni nodo, utilizzare la funzione [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) .

Le applicazioni con utilizzo intensivo della memoria dovranno ottimizzare l'utilizzo della memoria. Per recuperare la quantità di memoria libera disponibile per un nodo, utilizzare la funzione [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode) . La funzione [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) consente all'applicazione di specificare un nodo preferito per l'allocazione di memoria. **VirtualAllocExNuma** non alloca alcuna pagina fisica, quindi avrà esito positivo se le pagine sono disponibili o meno in tale nodo o in un'altra posizione nel sistema. Le pagine fisiche vengono allocate su richiesta. Se il nodo preferito esaurisce le pagine, il gestore della memoria utilizzerà le pagine di altri nodi. Se viene eseguito il paging della memoria, viene usato lo stesso processo quando viene riportato in.

### <a name="numa-support-on-systems-with-more-than-64-logical-processors"></a>Supporto NUMA su sistemi con più di 64 processori logici

Nei sistemi con più di 64 processori logici, i nodi vengono assegnati ai [gruppi di processori](processor-groups.md) in base alla capacità dei nodi. La capacità di un nodo è il numero di processori presenti quando il sistema viene avviato insieme a tutti i processori logici aggiuntivi che è possibile aggiungere mentre il sistema è in esecuzione.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** I gruppi di processori non sono supportati.

Ogni nodo deve essere completamente contenuto all'interno di un gruppo. Se le capacità dei nodi sono relativamente ridotte, il sistema assegna più di un nodo allo stesso gruppo, scegliendo nodi fisicamente vicini a un altro per ottenere prestazioni migliori. Se la capacità di un nodo supera il numero massimo di processori in un gruppo, il sistema suddivide il nodo in più nodi più piccoli, ciascuno sufficientemente piccolo da adattarsi a un gruppo.

È possibile richiedere un nodo NUMA ideale per un nuovo processo usando l'attributo Extended [**\_ \_ \_ \_ node preferenziale dell'attributo proc thread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) durante la creazione del processo. Come un processore ideale per thread, il nodo ideale è un suggerimento per l'utilità di pianificazione, che assegna il nuovo processo al gruppo che contiene il nodo richiesto, se possibile.

Le funzioni NUMA estese [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex), [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex), [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)e [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex) sono diverse dalle controparti non estese, in quanto il numero di nodo è un valore **ushort** anziché un **UCHAR**, per contenere il numero potenzialmente maggiore di nodi in un sistema con più di 64 processori logici. Inoltre, il processore specificato con o recuperato dalle funzioni estese include il gruppo di processori. il processore specificato con o recuperato dalle funzioni non estese è relativo al gruppo. Per informazioni dettagliate, vedere gli argomenti di riferimento per le singole funzioni.

Un'applicazione compatibile con i gruppi può assegnare tutti i thread a un nodo specifico in modo analogo a quanto descritto in precedenza in questo argomento, usando le corrispondenti funzioni NUMA estese. L'applicazione usa [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) per ottenere l'elenco di tutti i processori nel sistema. Si noti che l'applicazione non è in grado di impostare la maschera di affinità del processo a meno che il processo non sia assegnato a un singolo gruppo e il nodo previsto si trovi in tale gruppo. In genere, l'applicazione deve chiamare [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity) per limitare i thread al nodo previsto.

## <a name="numa-api"></a>API NUMA

La tabella seguente descrive l'API NUMA.



| Funzione                                                                     | Descrizione                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)      | Alloca le pagine di memoria fisica da mappare e non mappare all'interno di qualsiasi area AWE ( [Address Windowing Extensions](../memory/address-windowing-extensions.md) ) di un processo specificato e specifica il nodo NUMA per la memoria fisica. |
| [**CreateFileMappingNuma**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingnumaw)                      | Crea o apre un oggetto mapping di file denominato o senza nome per un file specificato e specifica il nodo NUMA per la memoria fisica.                                                                                              |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Recupera le informazioni sui processori logici e sull'hardware correlato.                                                                                                                                                            |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Recupera le informazioni sulle relazioni tra i processori logici e i componenti hardware correlati.                                                                                                                                       |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)             | Recupera la quantità di memoria disponibile nel nodo specificato.                                                                                                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)         | Recupera la quantità di memoria disponibile in un nodo specificato come valore **ushort** .                                                                                                                                             |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)                 | Recupera il nodo che dispone attualmente del numero più alto.                                                                                                                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)                 | Recupera la maschera del processore per il nodo specificato.                                                                                                                                                                            |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)             | Recupera la maschera del processore per un nodo specificato come valore **ushort** .                                                                                                                                                        |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                         | Recupera il numero di nodo per il processore specificato.                                                                                                                                                                          |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                     | Recupera il numero di nodo come valore **ushort** per il processore specificato.                                                                                                                                                    |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                         | Recupera il numero di nodo per l'identificatore di prossimità specificato.                                                                                                                                                               |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                     | Recupera il numero di nodo come valore **ushort** per l'identificatore di prossimità specificato.                                                                                                                                         |
| [**MapViewOfFileExNuma**](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)                          | Esegue il mapping di una visualizzazione di un mapping di file nello spazio degli indirizzi di un processo chiamante e specifica il nodo NUMA per la memoria fisica.                                                                                                 |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                            | Consente di riservare o eseguire il commit di un'area di memoria nello spazio degli indirizzi virtuali del processo specificato e di specificare il nodo NUMA per la memoria fisica.                                                                          |



 

La funzione [**QueryWorkingSetEx**](/windows/win32/api/psapi/nf-psapi-queryworkingsetex) può essere utilizzata per recuperare il nodo NUMA in cui è allocata una pagina. Per un esempio, vedere [allocazione di memoria da un nodo NUMA](../memory/allocating-memory-from-a-numa-node.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Allocazione della memoria da un nodo NUMA](../memory/allocating-memory-from-a-numa-node.md)
</dt> <dt>

[Processori multipli](multiple-processors.md)
</dt> <dt>

[Gruppi di processori](processor-groups.md)
</dt> </dl>

 

 
