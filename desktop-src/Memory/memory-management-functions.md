---
description: 'In questo argomento vengono descritte le funzioni di gestione della memoria:'
ms.assetid: 5a2a7a62-0bda-4a0d-93d2-25b4898871fd
title: Funzioni di gestione della memoria
ms.topic: article
ms.date: 11/06/2018
ms.openlocfilehash: a203583016a127a550f609068df8e86da384fa34
ms.sourcegitcommit: 43aef65e6563a56f35c019c5202827ab65772186
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/23/2020
ms.locfileid: "103734775"
---
# <a name="memory-management-functions"></a>Funzioni di gestione della memoria

- [Funzioni di memoria generale](#general-memory-functions)
- [Funzioni di prevenzione dell'esecuzione dei dati](#data-execution-prevention-functions)
- [Funzioni di mapping dei file](#file-mapping-functions)
- [Funzioni AWE](#awe-functions)
- [Funzioni heap](#heap-functions)
- [Funzioni di memoria virtuale](#virtual-memory-functions)
- [Funzioni globali e locali](#global-and-local-functions)
- [Funzioni di memoria non valide](#bad-memory-functions)
- [Funzioni enclave](#enclave-functions)
- [Funzioni thunk ATL](#atl-thunk-functions)
- [Funzioni obsolete](#obsolete-functions)

## <a name="general-memory-functions"></a>Funzioni di memoria generale

| Funzione | Descrizione |
|-|-|
| [**AddSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) | Registra una funzione di callback da chiamare quando viene liberato un intervallo di memoria protetto o se vengono modificate le protezioni. |
| [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) | Copia un blocco di memoria da una posizione a un'altra. |
| [**CreateMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) | Crea un oggetto di notifica delle risorse di memoria. |
| [**FillMemory**](/previous-versions/windows/desktop/legacy/aa366561(v=vs.85)) | Riempie un blocco di memoria con un valore specificato. |
| [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) | Recupera la dimensione minima di una pagina di grandi dimensioni. |
| [**GetPhysicallyInstalledSystemMemory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getphysicallyinstalledsystemmemory) | Recupera la quantità di RAM installata fisicamente nel computer. |
| [**GetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-getsystemfilecachesize) | Recupera i limiti delle dimensioni correnti per il working set della cache di sistema. |
| [**GetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-getwritewatch) | Recupera gli indirizzi delle pagine in cui sono stati scritti in un'area della memoria virtuale. |
| [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) | Ottiene informazioni sull'utilizzo corrente del sistema della memoria fisica e virtuale. |
| [**MoveMemory**](/previous-versions/windows/desktop/legacy/aa366788(v=vs.85)) | Sposta un blocco di memoria da una posizione a un'altra. |
| [**QueryMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-querymemoryresourcenotification) | Recupera lo stato dell'oggetto risorsa di memoria specificato. |
| [**RemoveSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-removesecurememorycachecallback) | Annulla la registrazione di una funzione di callback precedentemente registrata con la funzione [**AddSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) . |
| [**ResetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-resetwritewatch) | Reimposta lo stato di rilevamento in scrittura per un'area della memoria virtuale. |
| [**SecureMemoryCacheCallback**](/windows/desktop/api/WinNT/nc-winnt-psecure_memory_cache_callback) | Funzione definita dall'applicazione che viene chiamata quando viene liberato un intervallo di memoria protetto o la relativa protezione viene modificata. |
| [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) | Riempie un blocco di memoria con zeri. |
| [**SetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-setsystemfilecachesize) | Limita le dimensioni del working set per la cache file system. |
| [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) | Riempie un blocco di memoria con zeri. |

## <a name="data-execution-prevention-functions"></a>Funzioni di prevenzione dell'esecuzione dei dati

Queste funzioni vengono utilizzate con la [prevenzione esecuzione](data-execution-prevention.md) programmi (DEP).

| Funzione | Descrizione |
|-|-|
| [**GetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getprocessdeppolicy) | Recupera le impostazioni DEP per un processo. |
| [**GetSystemDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) | Recupera le impostazioni DEP per il sistema. |
| [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) | Modifica le impostazioni DEP per un processo. |

## <a name="file-mapping-functions"></a>Funzioni di mapping dei file

Queste funzioni vengono usate nel [mapping di file](file-mapping.md).

| Funzione | Descrizione |
|-|-|
| [**CreateFileMappingA**](/windows/win32/api/winbase/nf-winbase-createfilemappinga) | Crea o apre un oggetto mapping di file denominato o senza nome per un file specificato. |
| [**CreateFileMappingW**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingw) | Crea o apre un oggetto mapping di file denominato o senza nome per un file specificato. |
| [**CreateFileMapping2**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemapping2) | Crea o apre un oggetto mapping di file denominato o senza nome per un file specificato. È possibile specificare un nodo NUMA preferito per la memoria fisica come parametro esteso; vedere il parametro *ExtendedParameters* . |
| [**CreateFileMappingFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-createfilemappingfromapp) | Crea o apre un oggetto mapping di file denominato o senza nome per un file specificato da un'app di Windows Store. |
| [**CreateFileMappingNuma**](/windows/desktop/api/WinBase/nf-winbase-createfilemappingnumaa) | Crea o apre un oggetto mapping di file denominato o senza nome per un file specificato e specifica il nodo NUMA per la memoria fisica. |
| [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) | Scrive nel disco un intervallo di byte all'interno di una visualizzazione mappata di un file. |
| [**GetMappedFileName**](/windows/win32/api/psapi/nf-psapi-getmappedfilenamea) | Verifica se l'indirizzo specificato si trova all'interno di un file mappato alla memoria nello spazio degli indirizzi del processo specificato. In tal caso, la funzione restituisce il nome del file mappato alla memoria. |
| [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) | Esegue il mapping di una visualizzazione di un mapping di file nello spazio degli indirizzi di un processo chiamante. |
| [**MapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile2) | Esegue il mapping di una visualizzazione di un file o di una sezione di cui è stato eseguito il paging nello spazio degli indirizzi del processo specificato. |
| [**MapViewOfFile3**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3) | Esegue il mapping di una visualizzazione di un file o di una sezione di cui è stato eseguito il paging nello spazio degli indirizzi del processo specificato. |
| [**MapViewOfFile3FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3fromapp) | Esegue il mapping di una visualizzazione di un mapping di file nello spazio degli indirizzi di un processo chiamante da un'app di Windows Store. |
| [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) | Esegue il mapping di una visualizzazione di un mapping di file nello spazio degli indirizzi di un processo chiamante. Un chiamante può facoltativamente specificare un indirizzo di memoria suggerito per la visualizzazione. |
| [**MapViewOfFileExNuma**](/windows/desktop/api/WinBase/nf-winbase-mapviewoffileexnuma) | Esegue il mapping di una visualizzazione di un mapping di file nello spazio degli indirizzi di un processo chiamante e specifica il nodo NUMA per la memoria fisica. |
| [**MapViewOfFileFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffilefromapp) | Esegue il mapping di una visualizzazione di un mapping di file nello spazio degli indirizzi di un processo chiamante da un'app di Windows Store. |
| [**MapViewOfFileNuma2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffilenuma2) | Esegue il mapping di una visualizzazione di un file o di una sezione di cui è stato eseguito il paging nello spazio degli indirizzi del processo specificato. |
| [**OpenFileMapping**](/windows/win32/api/winbase/nf-winbase-openfilemappinga) | Apre un oggetto mapping di file denominato. |
| [**OpenFileMappingFromApp**](/windows/win32/api/winbase/nf-winbase-openfilemappingafromapp) | Apre un oggetto mapping di file denominato. |
| [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) | Esegue l'unmapping di una visualizzazione mappata di un file dallo spazio degli indirizzi del processo chiamante. |
| [**UnmapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile2) | Rimuove il mapping di una visualizzazione mappata in precedenza di un file o di una sezione di cui è stato eseguito il paging. |
| [**UnmapViewOfFileEx**](/windows/desktop/api/MemoryApi/nf-memoryapi-unmapviewoffileex) | Rimuove il mapping di una visualizzazione mappata in precedenza di un file o di una sezione di cui è stato eseguito il paging. |

## <a name="awe-functions"></a>Funzioni AWE

Si tratta delle [funzioni AWE](address-windowing-extensions.md).

| Funzione | Descrizione |
|-|-|
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages) | Alloca le pagine di memoria fisica da mappare e non mappare all'interno di un'area AWE del processo. |
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma) | Alloca le pagine di memoria fisica da mappare e non mappare all'interno di un'area AWE del processo e specifica il nodo NUMA per la memoria fisica. |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages) | Libera le pagine di memoria fisica precedentemente allocate con [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages). |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages) | Esegue il mapping delle pagine di memoria fisica allocate in precedenza all'indirizzo specificato all'interno di un'area AWE. |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter) | Esegue il mapping delle pagine di memoria fisica allocate in precedenza all'indirizzo specificato all'interno di un'area AWE. |

## <a name="heap-functions"></a>Funzioni heap

Si tratta delle [funzioni dell'heap](heap-functions.md).

| Funzione | Descrizione |
|-|-|
| [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) | Ottiene un handle per l'heap del processo chiamante. |
| [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) | Ottiene gli handle per tutti gli heap validi per il processo chiamante. |
| [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) | Alloca un blocco di memoria da un heap. |
| [**HeapCompact**](/windows/desktop/api/HeapApi/nf-heapapi-heapcompact) | Unisce i blocchi di memoria liberi adiacenti in un heap. |
| [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) | Crea un oggetto heap. |
| [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) | Elimina definitivamente l'oggetto heap specificato. |
| [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) | Libera un blocco di memoria allocato da un heap. |
| [**HeapLock**](/windows/desktop/api/HeapApi/nf-heapapi-heaplock) | Tenta di acquisire il blocco associato a un heap specificato. |
| [**HeapQueryInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapqueryinformation) | Recupera le informazioni sull'heap specificato. |
| [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) | Rialloca un blocco di memoria da un heap. |
| [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) | Imposta le informazioni sull'heap per l'heap specificato. |
| [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) | Recupera la dimensione di un blocco di memoria allocato da un heap. |
| [**HeapUnlock**](/windows/desktop/api/HeapApi/nf-heapapi-heapunlock) | Rilascia la proprietà del blocco associato a un heap specificato. |
| [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) | Tenta di convalidare un heap specificato. |
| [**HeapWalk**](/windows/desktop/api/HeapApi/nf-heapapi-heapwalk) | Enumera i blocchi di memoria in un heap specificato. |

## <a name="virtual-memory-functions"></a>Funzioni di memoria virtuale

Queste sono le [funzioni di memoria virtuale](virtual-memory-functions.md).

| Funzione | Descrizione |
|-|-|
| [**DiscardVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-discardvirtualmemory) | Elimina il contenuto della memoria di un intervallo di pagine di memoria senza eseguire il commit della memoria. Il contenuto della memoria scartata non è definito e deve essere riscritto dall'applicazione. |
| [**OfferVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory) | Indica che i dati contenuti in un intervallo di pagine di memoria non sono più necessari per l'applicazione e possono essere rimossi dal sistema, se necessario. |
| [**PrefetchVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-prefetchvirtualmemory) | Recupera gli intervalli di indirizzi virtuali nella memoria fisica. |
| [**QueryVirtualMemoryInformation**](/windows/desktop/api/MemoryApi/nf-memoryapi-queryvirtualmemoryinformation) | Restituisce informazioni su una pagina o un set di pagine nello spazio degli indirizzi virtuali del processo specificato. |
| [**ReclaimVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-reclaimvirtualmemory) | Recupera un intervallo di pagine di memoria offerte al sistema con [**OfferVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory). |
| [**SetProcessValidCallTargets**](/windows/desktop/api/MemoryApi/nf-memoryapi-setprocessvalidcalltargets) | Fornisce il CFG con un elenco di destinazioni di chiamata indiretta valide e specifica se devono essere contrassegnate come valide o meno. |
| [**VirtualAlloc**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc) | Riserva o conferma un'area di pagine nello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualAlloc2**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc2) | Riserva, commit o modifica lo stato di un'area di memoria nello spazio degli indirizzi virtuali di un processo specificato. La funzione Inizializza la memoria allocata a zero. |
| [**VirtualAlloc2FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Riserva, commit o modifica lo stato di un'area di pagine nello spazio degli indirizzi virtuali del processo chiamante. La memoria allocata da questa funzione viene automaticamente inizializzata su zero. |
| [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Riserva o conferma un'area di pagine nello spazio degli indirizzi virtuali del processo specificato. |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) | Consente di riservare o eseguire il commit di un'area di memoria nello spazio degli indirizzi virtuali del processo specificato e di specificare il nodo NUMA per la memoria fisica. |
| [**VirtualAllocFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Riserva, commit o modifica lo stato di un'area di pagine nello spazio degli indirizzi virtuali del processo chiamante. La memoria allocata da questa funzione viene automaticamente inizializzata su zero. |
| [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) | Rilascia o decommit un'area di pagine all'interno dello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) | Rilascia o Elimina un commit di un'area di memoria nello spazio degli indirizzi virtuali di un processo specificato. |
| [**VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) | Blocca la regione specificata dello spazio degli indirizzi virtuali del processo nella memoria fisica. |
| [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) | Modifica la protezione dell'accesso in un'area di pagine di cui è stato eseguito il commit nello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) | Modifica la protezione dell'accesso in un'area di pagine di cui è stato eseguito il commit nello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualProtectFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualprotectfromapp) | Modifica la protezione in un'area di pagine di cui è stato eseguito il commit nello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) | Fornisce informazioni su un intervallo di pagine nello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) | Fornisce informazioni su un intervallo di pagine nello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) | Sblocca un intervallo specificato di pagine nello spazio degli indirizzi virtuali di un processo. |

## <a name="global-and-local-functions"></a>Funzioni globali e locali

Vedere anche [funzioni globali e locali](global-and-local-functions.md). Queste funzioni vengono fornite per la compatibilità con Windows a 16 bit e vengono utilizzate con Dynamic Data Exchange (DDE), le funzioni degli Appunti e gli oggetti dati OLE. A meno che la documentazione non riferisca specificamente che è necessario utilizzare una funzione globale o locale, le nuove applicazioni devono utilizzare la [funzione heap](heap-functions.md) corrispondente con l'handle restituito da [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap). Per la funzionalità equivalente per la funzione globale o locale, impostare il parametro *dwFlags* della funzione heap su 0.

| Funzione | Descrizione | Funzione heap corrispondente |
|-|-|-|
| [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [ **LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) | Alloca il numero specificato di byte dall'heap. | [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) |
| [**GlobalDiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard), [ **LocalDiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) | Elimina il blocco di memoria globale specificato. | Non applicabile. |
| [**GlobalFlags**](/windows/desktop/api/WinBase/nf-winbase-globalflags), [ **LocalFlags**](/windows/desktop/api/WinBase/nf-winbase-localflags) | Restituisce informazioni sull'oggetto memoria globale specificato. | Non applicabile. Usare [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) per convalidare l'heap. |
| [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree), [ **LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) | Libera l'oggetto memoria globale specificato. | [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) |
| [**GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle), [ **LocalHandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) | Recupera l'handle associato al puntatore specificato a un blocco di memoria globale. Questa funzione deve essere utilizzata solo con le funzioni OLE e appunti che lo richiedono. | Non applicabile. |
| [**Funzione GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock), [ **LocalLock**](/windows/desktop/api/WinBase/nf-winbase-locallock) | Blocca un oggetto memoria globale e restituisce un puntatore al primo byte del blocco di memoria dell'oggetto. | Non applicabile. |
| [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc), [ **LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) | Modifica la dimensione o gli attributi di un oggetto memoria globale specificato. | [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) |
| [**GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize), [ **LocalSize**](/windows/desktop/api/WinBase/nf-winbase-localsize) | Recupera le dimensioni correnti dell'oggetto memoria globale specificato. | [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) |
| [**Funzione GlobalUnlock**](/windows/desktop/api/WinBase/nf-winbase-globalunlock), [ **LocalUnlock**](/windows/desktop/api/WinBase/nf-winbase-localunlock) | Decrementa il conteggio dei blocchi associato a un oggetto Memory. Questa funzione deve essere utilizzata solo con le funzioni OLE e appunti che lo richiedono. | Non applicabile. |

## <a name="bad-memory-functions"></a>Funzioni di memoria non valide

| Funzione | Descrizione |
|-|-|
| [**BadMemoryCallbackRoutine**](/previous-versions/windows/desktop/legacy/hh691011(v=vs.85)) | Funzione definita dall'applicazione registrata con la funzione [**RegisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) che viene chiamata quando vengono rilevate una o più pagine di memoria non valida. |
| [**GetMemoryErrorHandlingCapabilities**](/windows/win32/api/memoryapi/nf-memoryapi-getmemoryerrorhandlingcapabilities) | Ottiene le funzionalità di gestione degli errori di memoria del sistema. |
| [**RegisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) | Registra una notifica di memoria non valida che viene chiamata quando vengono rilevate una o più pagine di memoria non valida. |
| [**UnregisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-unregisterbadmemorynotification) | Chiude l'handle di notifica della memoria non valida specificato. |

## <a name="enclave-functions"></a>Funzioni enclave

| Funzione | Descrizione |
|-|-|
| [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave) | Crea una nuova enclave non inizializzata. Un enclave è un'area isolata del codice e dei dati all'interno dello spazio di indirizzi per un'applicazione. Solo il codice eseguito all'interno dell'enclave può accedere ai dati all'interno della stessa enclave. |
| [**InitializeEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave) | Inizializza un enclave creato e caricato con i dati. |
| [**IsEnclaveTypeSupported**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported) | Recupera un valore che indica se il tipo di enclave specificato è supportato. |
| [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) | Carica i dati in un'enclave non inizializzata creata chiamando [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave). |

## <a name="atl-thunk-functions"></a>Funzioni thunk ATL

| Funzione | Descrizione |
|-|-|
| [**AtlThunk_AllocateData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_allocatedata) | Alloca spazio in memoria per un thunk ATL. |
| [**AtlThunk_DataToCode**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_datatocode) | Restituisce una funzione eseguibile corrispondente al parametro AtlThunkData_t. |
| [**AtlThunk_FreeData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_freedata) | Libera la memoria associata a un thunk ATL. |
| [**AtlThunk_InitData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_initdata) | Inizializza un thunk ATL. |

## <a name="obsolete-functions"></a>Funzioni obsolete

Queste funzioni vengono fornite solo per la compatibilità con le versioni di Windows a 16 bit:

- [**IsBadCodePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadcodeptr)
- [**IsBadReadPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadreadptr)
- [**IsBadStringPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadstringptra)
- [**IsBadWritePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadwriteptr)

La funzione seguente può restituire informazioni non corrette e non deve essere utilizzata. Usare invece la funzione [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) .

- [**GlobalMemoryStatus**](/windows/desktop/api/WinBase/nf-winbase-globalmemorystatus)