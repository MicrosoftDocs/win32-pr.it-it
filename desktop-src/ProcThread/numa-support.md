---
description: Il modello tradizionale per il supporto multiprocessore è SMP (Symmetric MultiProcessor). In questo modello, ogni processore ha uguale accesso alla memoria e all'I/O. Con l'aggiunta di più processori, il bus del processore diventa una limitazione per le prestazioni del sistema.
ms.assetid: a1263968-2b26-45cc-bdd7-6aa354821a5a
title: Supporto NUMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178f53c6b55b6ae291cd5cdcf99386515a441094
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549806"
---
# <a name="numa-support"></a>Supporto NUMA

Il modello tradizionale per il supporto multiprocessore è SMP (Symmetric MultiProcessor). In questo modello, ogni processore ha uguale accesso alla memoria e all'I/O. Con l'aggiunta di più processori, il bus del processore diventa una limitazione per le prestazioni del sistema.

I progettisti di sistema usano l'accesso alla memoria non uniforme (NUMA) per aumentare la velocità del processore senza aumentare il carico sul bus del processore. L'architettura non è uniforme perché ogni processore è vicino ad alcune parti della memoria e più lontano da altre parti della memoria. Il processore ottiene rapidamente l'accesso alla memoria a cui è vicina, mentre può richiedere più tempo per ottenere l'accesso alla memoria più lontana.

In un sistema NUMA le CPU sono disposte in sistemi più piccoli denominati *nodi*. Ogni nodo ha i propri processori e memoria ed è connesso al sistema più grande tramite un bus di interconnessione coerente con la cache.

Il sistema tenta di migliorare le prestazioni pianificando i thread nei processori che si trovare nello stesso nodo della memoria in uso. Tenta di soddisfare le richieste di allocazione di memoria dall'interno del nodo, ma alloca la memoria da altri nodi, se necessario. Fornisce anche un'API per rendere disponibile la topologia del sistema alle applicazioni. È possibile migliorare le prestazioni delle applicazioni usando le funzioni NUMA per ottimizzare la pianificazione e l'utilizzo della memoria.

Prima di tutto, è necessario determinare il layout dei nodi nel sistema. Per recuperare il nodo con il numero più alto nel sistema, usare la [**funzione GetNumaHighestNodeNumber.**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber) Si noti che non è garantito che questo numero sia uguale al numero totale di nodi nel sistema. Inoltre, non è garantito che i nodi con numeri sequenziali siano vicini. Per recuperare l'elenco dei processori nel sistema, usare la [**funzione GetProcessAffinityMask.**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) È possibile determinare il nodo per ogni processore nell'elenco usando la [**funzione GetNumaProcessorNode.**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode) In alternativa, per recuperare un elenco di tutti i processori in un nodo, usare la [**funzione GetNumaNodeProcessorMask.**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)

Dopo aver determinato quali processori appartengono a quali nodi, è possibile ottimizzare le prestazioni dell'applicazione. Per assicurarsi che tutti i thread per il processo siano eseguiti nello stesso nodo, usare la [**funzione SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) con una maschera di affinità di processo che specifica i processori nello stesso nodo. Ciò aumenta l'efficienza delle applicazioni i cui thread devono accedere alla stessa memoria. In alternativa, per limitare il numero di thread in ogni nodo, usare la [**funzione SetThreadAffinityMask.**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask)

Le applicazioni a elevato utilizzo di memoria dovranno ottimizzare l'utilizzo della memoria. Per recuperare la quantità di memoria disponibile per un nodo, usare la [**funzione GetNumaAvailableMemoryNode.**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode) La [**funzione VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) consente all'applicazione di specificare un nodo preferito per l'allocazione di memoria. **VirtualAllocExNuma** non alloca pagine fisiche, pertanto avrà esito positivo indipendentemente dal fatto che le pagine siano disponibili in tale nodo o in un'altra posizione nel sistema. Le pagine fisiche vengono allocate su richiesta. Se il nodo preferito esauriva le pagine, il gestore della memoria userà le pagine di altri nodi. Se si esegue il page out della memoria, viene usato lo stesso processo quando viene riesezione.

### <a name="numa-support-on-systems-with-more-than-64-logical-processors"></a>Supporto NUMA nei sistemi con più di 64 processori logici

Nei sistemi con più di 64 processori logici, i nodi vengono assegnati ai gruppi [di processori](processor-groups.md) in base alla capacità dei nodi. La capacità di un nodo è il numero di processori presenti quando il sistema viene avviato insieme a eventuali processori logici aggiuntivi che possono essere aggiunti mentre il sistema è in esecuzione.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** I gruppi di processori non sono supportati.

Ogni nodo deve essere completamente contenuto all'interno di un gruppo. Se le capacità dei nodi sono relativamente piccole, il sistema assegna più nodi allo stesso gruppo, scegliendo nodi fisicamente vicini tra loro per ottenere prestazioni migliori. Se la capacità di un nodo supera il numero massimo di processori in un gruppo, il sistema suddivide il nodo in più nodi più piccoli, ognuno sufficientemente piccolo da rientrare in un gruppo.

Un nodo NUMA ideale per un nuovo processo può essere richiesto usando l'attributo esteso [**PROC THREAD ATTRIBUTE PREFERRED \_ \_ \_ \_ NODE**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) al momento della creazione del processo. Analogamente a un processore ideale per thread, il nodo ideale è un hint all'utilità di pianificazione, che assegna il nuovo processo al gruppo che contiene il nodo richiesto, se possibile.

Le funzioni NUMA estese [**GetNumaAvailableMemoryNodeEx,**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex) [**GetNumaNodeProcessorMaskEx,**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex) [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)e [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex) differiscono dalle controparti non estese in quanto il numero di nodo è un valore **USHORT** anziché **UCHAR,** per supportare il numero potenzialmente maggiore di nodi in un sistema con più di 64 processori logici. Inoltre, il processore specificato con o recuperato dalle funzioni estese include il gruppo di processori. il processore specificato con o recuperato dalle funzioni non estense è relativo al gruppo. Per informazioni dettagliate, vedere gli argomenti di riferimento sulle singole funzioni.

Un'applicazione in grado di riconoscere i gruppi può assegnare tutti i relativi thread a un nodo specifico in modo simile a quello descritto in precedenza in questo argomento, usando le funzioni NUMA estese corrispondenti. L'applicazione [**usa GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) per ottenere l'elenco di tutti i processori nel sistema. Si noti che l'applicazione non può impostare la maschera di affinità del processo a meno che il processo non sia assegnato a un singolo gruppo e il nodo desiderato non si trovi in tale gruppo. In genere l'applicazione deve [**chiamare SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity) per limitare i thread al nodo desiderato.


### <a name="behavior-starting-with-windows-10-build-20348"></a>Comportamento a partire Windows 10 build 20348 

> [!NOTE]
> A partire Windows 10 build 20348, il comportamento di questa e di altre funzioni NUMA è stato modificato per supportare meglio i sistemi con nodi contenenti più di 64 processori.

La creazione di nodi "falsi" per supportare un mapping 1:1 tra gruppi e nodi ha comportato comportamenti confusi in cui viene segnalato un numero imprevisto di nodi NUMA e quindi, a partire da Windows 10 Build 20348, il sistema operativo è stato modificato per consentire l'associazione di più gruppi a un nodo e quindi ora è possibile segnalarne la vera topologia NUMA del sistema.  

Come parte di queste modifiche al sistema operativo, diverse API NUMA sono state modificate per supportare la segnalazione di più gruppi che ora possono essere associati a un singolo nodo NUMA. Le API aggiornate e nuove sono etichettate nella tabella nella sezione **API NUMA riportata** di seguito.

Poiché la rimozione della suddivisione dei nodi può potenzialmente influire sulle applicazioni esistenti, è disponibile un valore del Registro di sistema per consentire il rifiuto esplicito del comportamento di suddivisione dei nodi legacy. La suddivisione dei nodi può  essere ri abilitata creando un valore REG_DWORD denominato "SplitLargeNodes" con il valore 1 sotto HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\NUMA. Le modifiche apportate a questa impostazione richiedono un riavvio per avere effetto.

```powershell
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\NUMA" /v SplitLargeNumaNodes /t REG_DWORD /v 1
```

> [!NOTE]
> Le applicazioni aggiornate per l'uso della nuova funzionalità API che segnala la vera topologia NUMA continueranno a funzionare correttamente nei sistemi in cui la suddivisione di nodi di grandi dimensioni è stata ri abilitata con questa chiave del Registro di sistema.

L'esempio seguente illustra prima di tutto potenziali problemi con le tabelle di compilazione che esemplizzano il mapping dei processori ai nodi NUMA usando le API di affinità legacy, che non forniscono più una copertura completa di tutti i processori nel sistema. Ciò può comportare una tabella incompleta. Le implicazioni di tale incompletezza dipendono dal contenuto della tabella. Se la tabella archivia semplicemente il numero di nodo corrispondente, probabilmente si tratta solo di un problema di prestazioni con i processori scoperti che vengono lasciati come parte del nodo 0. Tuttavia, se la tabella contiene puntatori a una struttura di contesto per nodo, ciò può comportare dereferenziazione NULL in fase di esecuzione.

L'esempio di codice illustra quindi due soluzioni alternative per il problema. Il primo è eseguire la migrazione alle API di affinità dei nodi a più gruppi (modalità utente e modalità kernel). Il secondo è usare **KeQueryLogicalProcessorRelationship** per eseguire direttamente una query sul nodo NUMA associato a un determinato numero di processore.

```cpp

//
// Problematic implementation using KeQueryNodeActiveAffinity.
//

USHORT CurrentNode;
USHORT HighestNodeNumber;
GROUP_AFFINITY NodeAffinity;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    KeQueryNodeActiveAffinity(CurrentNode, &NodeAffinity, NULL);
    while (NodeAffinity.Mask != 0) {

        ProcessorNumber.Group = NodeAffinity.Group;
        BitScanForward(&ProcessorNumber.Number, NodeAffinity.Mask);

        ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

        ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode;]

        NodeAffinity.Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
    }
}

//
// Resolution using KeQueryNodeActiveAffinity2.
//

USHORT CurrentIndex;
USHORT CurrentNode;
USHORT CurrentNodeAffinityCount;
USHORT HighestNodeNumber;
ULONG MaximumGroupCount;
PGROUP_AFFINITY NodeAffinityMasks;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

MaximumGroupCount = KeQueryMaximumGroupCount();
NodeAffinityMasks = ExAllocatePool2(POOL_FLAG_PAGED,
                                    sizeof(GROUP_AFFINITY) * MaximumGroupCount,
                                    'tseT');

if (NodeAffinityMasks == NULL) {
    return STATUS_NO_MEMORY;
}

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    Status = KeQueryNodeActiveAffinity2(CurrentNode,
                                        NodeAffinityMasks,
                                        MaximumGroupCount,
                                        &CurrentNodeAffinityCount);
    NT_ASSERT(NT_SUCCESS(Status));

    for (CurrentIndex = 0; CurrentIndex < CurrentNodeAffinityCount; CurrentIndex += 1) {

        CurrentAffinity = &NodeAffinityMasks[CurrentIndex];

        while (CurrentAffinity->Mask != 0) {

            ProcessorNumber.Group = CurrentAffinity.Group;
            BitScanForward(&ProcessorNumber.Number, CurrentAffinity->Mask);

            ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

            ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode];

            CurrentAffinity->Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
        }
    }
}

//
// Resolution using KeQueryLogicalProcessorRelationship.
//

ULONG ProcessorCount;
ULONG ProcessorIndex;
SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX ProcessorInformation;
ULONG ProcessorInformationSize;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

ProcessorCount = KeQueryActiveProcessorCountEx(ALL_PROCESSOR_GROUPS);

for (ProcessorIndex = 0; ProcessorIndex < ProcessorCount; ProcessorIndex += 1) {

    Status = KeGetProcessorNumberFromIndex(ProcessorIndex, &ProcessorNumber);
    NT_ASSERT(NT_SUCCESS(Status));

    ProcessorInformationSize = sizeof(ProcessorInformation);
    Status = KeQueryLogicalProcessorRelationship(&ProcessorNumber,
                                                    RelationNumaNode,
                                                    &ProcessorInformation,
                                                    &ProcesorInformationSize);
    NT_ASSERT(NT_SUCCESS(Status));

    NodeNumber = ProcessorInformation.NumaNode.NodeNumber;

    ProcessorNodeContexts[ProcessorIndex] = NodeContexts[NodeNumber];
}
```

## <a name="numa-api"></a>NUMA API

La tabella seguente descrive l'API NUMA.



| Funzione                                                                     | Descrizione                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)      | Alloca le pagine di memoria fisica da mappare e annullare il mapping all'interno di qualsiasi area AWE [(Address Windowing Extensions)](../memory/address-windowing-extensions.md) di un processo specificato e specifica il nodo NUMA per la memoria fisica. |
| [**CreateFileMappingNuma**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingnumaw)                      | Crea o apre un oggetto mapping di file denominato o senza nome per un file specificato e specifica il nodo NUMA per la memoria fisica.                                                                                              |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Aggiornamento in Windows 10 Build 20348. Recupera informazioni sui processori logici e sull'hardware correlato.                                                                                                                                                            |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Aggiornamento in Windows 10 Build 20348. Recupera informazioni sulle relazioni dei processori logici e dell'hardware correlato.                                                                                                                                       |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)             | Recupera la quantità di memoria disponibile nel nodo specificato.                                                                                                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)         | Recupera la quantità di memoria disponibile in un nodo specificato come valore **USHORT.**                                                                                                                                             |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)                 | Recupera il nodo con il numero più alto.                                                                                                                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)                 | Aggiornamento in Windows 10 build 20348. Recupera la maschera del processore per il nodo specificato.                                                                                                                                                                            |
| [**GetNumaNodeProcessorMask2**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormask2)                         | Novità di Windows 10 build 20348. Recupera la maschera del processore multi-gruppo del nodo specificato.                                                                                                                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)             | Aggiornamento in Windows 10 build 20348. Recupera la maschera del processore per un nodo specificato come **valore USHORT.**                                                                                                                                                        |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                         | Recupera il numero di nodo per il processore specificato.                                                                                                                                                                          |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                     | Recupera il numero di nodo come valore **USHORT** per il processore specificato.                                                                                                                                                    |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                         | Recupera il numero di nodo per l'identificatore di prossimità specificato.                                                                                                                                                               |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                     | Recupera il numero di nodo come valore **USHORT** per l'identificatore di prossimità specificato.                                                                                                                                         |
| [**GetProcessDefaultCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessdefaultcpusetmasks)                     | Novità di Windows 10 build 20348. Recupera l'elenco di set di CPU nel set predefinito del processo impostato da SetProcessDefaultCpuSetMasks o SetProcessDefaultCpuSets.                                                                                                                                         |
| [**GetThreadSelectedCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadselectedcpusetmasks)                     | Novità di Windows 10 build 20348. Imposta l'assegnazione dei set di CPU selezionati per il thread specificato. Questa assegnazione esegue l'override dell'assegnazione predefinita del processo, se impostata.                                                                                                                                          |
| [**MapViewOfFileExNuma**](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)                          | Esegue il mapping di una visualizzazione di un mapping di file nello spazio degli indirizzi di un processo chiamante e specifica il nodo NUMA per la memoria fisica.                                                                                                 |
| [**SetProcessDefaultCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessdefaultcpusetmasks)                     | Novità di Windows 10 build 20348. Imposta l'assegnazione predefinita dei set di CPU per i thread nel processo specificato.                                                                                                                                          |
| [**SetThreadSelectedCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadselectedcpusetmasks)                     | Novità di Windows 10 build 20348. Imposta l'assegnazione dei set di CPU selezionati per il thread specificato. Questa assegnazione esegue l'override dell'assegnazione predefinita del processo, se impostata.                                                                                                                                          |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                            | Riserva o esegue il commit di un'area di memoria all'interno dello spazio degli indirizzi virtuali del processo specificato e specifica il nodo NUMA per la memoria fisica.                                                                          |



 

La [**funzione QueryWorkingSetEx**](/windows/win32/api/psapi/nf-psapi-queryworkingsetex) può essere usata per recuperare il nodo NUMA in cui viene allocata una pagina. Per un esempio, vedere [Allocazione di memoria da un nodo NUMA](../memory/allocating-memory-from-a-numa-node.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Allocazione di memoria da un nodo NUMA](../memory/allocating-memory-from-a-numa-node.md)
</dt> <dt>

[Processori multipli](multiple-processors.md)
</dt> <dt>

[Gruppi di processori](processor-groups.md)
</dt> </dl>

 

 
