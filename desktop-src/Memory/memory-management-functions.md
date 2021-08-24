---
description: 'In questo argomento vengono descritte le funzioni di gestione della memoria:'
ms.assetid: 5a2a7a62-0bda-4a0d-93d2-25b4898871fd
title: Funzioni di gestione della memoria
ms.topic: article
ms.date: 11/06/2018
ms.openlocfilehash: 635fa59b6a5b6a549438d8bfed71781d6d9e6fa6a9d2c12524684ded28a0f3df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822191"
---
# <a name="memory-management-functions"></a>Funzioni di gestione della memoria

- [Funzioni di memoria generali](#general-memory-functions)
- [Funzioni di prevenzione dell'esecuzione dei dati](#data-execution-prevention-functions)
- [Funzioni di mapping dei file](#file-mapping-functions)
- [Funzioni AWE](#awe-functions)
- [Funzioni heap](#heap-functions)
- [Funzioni di memoria virtuale](#virtual-memory-functions)
- [Funzioni globali e locali](#global-and-local-functions)
- [Funzioni di memoria non gestite](#bad-memory-functions)
- [Funzioni dell'enclave](#enclave-functions)
- [Funzioni thunk ATL](#atl-thunk-functions)
- [Funzioni obsolete](#obsolete-functions)

## <a name="general-memory-functions"></a>Funzioni di memoria generali

| Funzione | Descrizione |
|-|-|
| [**AddSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) | Registra una funzione di callback da chiamare quando viene liberato un intervallo di memoria protetto o vengono modificate le relative protezioni. |
| [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) | Copia un blocco di memoria da una posizione a un'altra. |
| [**CreateMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) | Crea un oggetto notifica della risorsa di memoria. |
| [**Memoria di riempimento**](/previous-versions/windows/desktop/legacy/aa366561(v=vs.85)) | Riempie un blocco di memoria con un valore specificato. |
| [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) | Recupera le dimensioni minime di una pagina di grandi dimensioni. |
| [**GetPhysicallyInstalledSystemMemory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getphysicallyinstalledsystemmemory) | Recupera la quantità di RAM installata fisicamente nel computer. |
| [**GetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-getsystemfilecachesize) | Recupera i limiti di dimensione correnti per il working set della cache di sistema. |
| [**GetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-getwritewatch) | Recupera gli indirizzi delle pagine scritte in un'area della memoria virtuale. |
| [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) | Ottiene informazioni sull'utilizzo corrente della memoria fisica e virtuale da parte del sistema. |
| [**MoveMemory**](/previous-versions/windows/desktop/legacy/aa366788(v=vs.85)) | Sposta un blocco di memoria da una posizione a un'altra. |
| [**QueryMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-querymemoryresourcenotification) | Recupera lo stato dell'oggetto risorsa di memoria specificato. |
| [**RemoveSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-removesecurememorycachecallback) | Annulla la registrazione di una funzione di callback registrata in precedenza [**con la funzione AddSecureMemoryCacheCallback.**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) |
| [**ResetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-resetwritewatch) | Reimposta lo stato di rilevamento delle operazioni di scrittura per un'area della memoria virtuale. |
| [**SecureMemoryCacheCallback**](/windows/desktop/api/WinNT/nc-winnt-psecure_memory_cache_callback) | Funzione definita dall'applicazione che viene chiamata quando viene liberato un intervallo di memoria protetto o vengono modificate le relative protezioni. |
| [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) | Riempie un blocco di memoria con zeri. |
| [**SetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-setsystemfilecachesize) | Limita le dimensioni del working set per la cache file system dati. |
| [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) | Riempie un blocco di memoria con zeri. |

## <a name="data-execution-prevention-functions"></a>Funzioni di prevenzione dell'esecuzione dei dati

Queste funzioni vengono usate con [Protezione esecuzione programmi.](data-execution-prevention.md)

| Funzione | Descrizione |
|-|-|
| [**GetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getprocessdeppolicy) | Recupera le impostazioni DEP per un processo. |
| [**GetSystemDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) | Recupera le impostazioni DEP per il sistema. |
| [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) | Modifica le impostazioni DEP per un processo. |

## <a name="file-mapping-functions"></a>Funzioni di mapping dei file

Queste funzioni vengono usate nel [mapping dei file](file-mapping.md).

| Funzione | Descrizione |
|-|-|
| [**CreateFileMappingA**](/windows/win32/api/winbase/nf-winbase-createfilemappinga) | Crea o apre un oggetto mapping di file denominato o senza nome per un file specificato. |
| [**CreateFileMappingW**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingw) | Crea o apre un oggetto mapping di file denominato o senza nome per un file specificato. |
| [**CreateFileMapping2**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemapping2) | Crea o apre un oggetto mapping di file denominato o senza nome per un file specificato. È possibile specificare un nodo NUMA preferito per la memoria fisica come parametro esteso. vedere il *parametro ExtendedParameters.* |
| [**CreateFileMappingFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-createfilemappingfromapp) | Crea o apre un oggetto mapping di file denominato o senza nome per un file specificato da un'app Windows Store. |
| [**CreateFileMappingNuma**](/windows/desktop/api/WinBase/nf-winbase-createfilemappingnumaa) | Crea o apre un oggetto mapping di file denominato o senza nome per un file specificato e specifica il nodo NUMA per la memoria fisica. |
| [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) | Scrive sul disco un intervallo di byte all'interno di una visualizzazione mappata di un file. |
| [**GetMappedFileName**](/windows/win32/api/psapi/nf-psapi-getmappedfilenamea) | Controlla se l'indirizzo specificato si trova all'interno di un file mappato alla memoria nello spazio indirizzi del processo specificato. In tal caso, la funzione restituisce il nome del file mappato alla memoria. |
| [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) | Mappe una visualizzazione di un mapping di file nello spazio degli indirizzi di un processo chiamante. |
| [**MapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile2) | Mappe una visualizzazione di un file o di una sezione basata su file di paging nello spazio degli indirizzi del processo specificato. |
| [**MapViewOfFile3**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3) | Mappe una visualizzazione di un file o di una sezione basata su file di paging nello spazio degli indirizzi del processo specificato. |
| [**MapViewOfFile3FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3fromapp) | Mappe una visualizzazione di un mapping di file nello spazio degli indirizzi di un processo chiamante da un'app Windows Store. |
| [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) | Mappe una visualizzazione di un mapping di file nello spazio degli indirizzi di un processo chiamante. Un chiamante può facoltativamente specificare un indirizzo di memoria suggerito per la visualizzazione. |
| [**MapViewOfFileExNuma**](/windows/desktop/api/WinBase/nf-winbase-mapviewoffileexnuma) | Mappe una visualizzazione di un mapping di file nello spazio degli indirizzi di un processo chiamante e specifica il nodo NUMA per la memoria fisica. |
| [**MapViewOfFileFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffilefromapp) | Mappe una visualizzazione di un mapping di file nello spazio degli indirizzi di un processo chiamante da un'app Windows Store. |
| [**MapViewOfFileNuma2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffilenuma2) | Mappe una visualizzazione di un file o di una sezione basata su file di paging nello spazio degli indirizzi del processo specificato. |
| [**OpenFileMapping**](/windows/win32/api/winbase/nf-winbase-openfilemappinga) | Apre un oggetto di mapping di file denominato. |
| [**OpenFileMappingFromApp**](/windows/win32/api/winbase/nf-winbase-openfilemappingafromapp) | Apre un oggetto di mapping di file denominato. |
| [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) | Annulla il mapping di una visualizzazione mappata di un file dallo spazio degli indirizzi del processo chiamante. |
| [**UnmapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile2) | Annulla il mapping di una visualizzazione mappata in precedenza di un file o di una sezione con file di paging. |
| [**UnmapViewOfFileEx**](/windows/desktop/api/MemoryApi/nf-memoryapi-unmapviewoffileex) | Annulla il mapping di una visualizzazione mappata in precedenza di un file o di una sezione con file di paging. |

## <a name="awe-functions"></a>Funzioni AWE

Queste sono le [funzioni AWE](address-windowing-extensions.md).

| Funzione | Descrizione |
|-|-|
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages) | Alloca le pagine di memoria fisica da mappare e annullare il mapping all'interno di qualsiasi area AWE del processo. |
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma) | Alloca le pagine di memoria fisica da mappare e annullare il mapping all'interno di qualsiasi area AWE del processo e specifica il nodo NUMA per la memoria fisica. |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages) | Libera le pagine di memoria fisica precedentemente allocate [**con AllocateUserPhysicalPages.**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages) |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages) | Mappe pagine di memoria fisica precedentemente allocate all'indirizzo specificato all'interno di un'area AWE. |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter) | Mappe pagine di memoria fisica precedentemente allocate all'indirizzo specificato all'interno di un'area AWE. |

## <a name="heap-functions"></a>Funzioni heap

Queste sono le [funzioni heap](heap-functions.md).

| Funzione | Descrizione |
|-|-|
| [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) | Ottiene un handle per l'heap del processo chiamante. |
| [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) | Ottiene gli handle per tutti gli heap validi per il processo chiamante. |
| [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) | Alloca un blocco di memoria da un heap. |
| [**HeapCompact**](/windows/desktop/api/HeapApi/nf-heapapi-heapcompact) | Unesce blocchi di memoria liberi adiacenti in un heap. |
| [**HeapCrea**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) | Crea un oggetto heap. |
| [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) | Elimina l'oggetto heap specificato. |
| [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) | Libera un blocco di memoria allocato da un heap. |
| [**HeapLock**](/windows/desktop/api/HeapApi/nf-heapapi-heaplock) | Tenta di acquisire il blocco associato a un heap specificato. |
| [**HeapQueryInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapqueryinformation) | Recupera informazioni sull'heap specificato. |
| [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) | Rialloca un blocco di memoria da un heap. |
| [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) | Imposta le informazioni sull'heap per l'heap specificato. |
| [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) | Recupera le dimensioni di un blocco di memoria allocato da un heap. |
| [**HeapUnlock**](/windows/desktop/api/HeapApi/nf-heapapi-heapunlock) | Rilascia la proprietà del blocco associato a un heap specificato. |
| [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) | Tenta di convalidare un heap specificato. |
| [**HeapWalk**](/windows/desktop/api/HeapApi/nf-heapapi-heapwalk) | Enumera i blocchi di memoria in un heap specificato. |

## <a name="virtual-memory-functions"></a>Funzioni di memoria virtuale

Queste sono le [funzioni di memoria virtuale](virtual-memory-functions.md).

| Funzione | Descrizione |
|-|-|
| [**DiscardVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-discardvirtualmemory) | Rimuove il contenuto della memoria di un intervallo di pagine di memoria, senza eseguire il decommitting della memoria. Il contenuto della memoria eliminata non è definito e deve essere riscritto dall'applicazione. |
| [**OfferVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory) | Indica che i dati contenuti in un intervallo di pagine di memoria non sono più necessari per l'applicazione e possono essere eliminati dal sistema, se necessario. |
| [**PrefetchVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-prefetchvirtualmemory) | Prelettura degli intervalli di indirizzi virtuali nella memoria fisica. |
| [**QueryVirtualMemoryInformation**](/windows/desktop/api/MemoryApi/nf-memoryapi-queryvirtualmemoryinformation) | Restituisce informazioni su una pagina o un set di pagine all'interno dello spazio degli indirizzi virtuali del processo specificato. |
| [**ReclaimVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-reclaimvirtualmemory) | Recupera un intervallo di pagine di memoria offerte al sistema con [**OfferVirtualMemory.**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory) |
| [**SetProcessValidCallTargets**](/windows/desktop/api/MemoryApi/nf-memoryapi-setprocessvalidcalltargets) | Fornisce un elenco di destinazioni di chiamata indirette valide e specifica se devono essere contrassegnate come valide o meno. |
| [**Virtualalloc**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc) | Riserva o esegue il commit di un'area di pagine nello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualAlloc2**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc2) | Riserva, esegue il commit o modifica lo stato di un'area di memoria all'interno dello spazio degli indirizzi virtuali di un processo specificato. La funzione inizializza la memoria allocata a zero. |
| [**VirtualAlloc2FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Riserva, esegue il commit o modifica lo stato di un'area di pagine nello spazio degli indirizzi virtuali del processo chiamante. La memoria allocata da questa funzione viene inizializzata automaticamente su zero. |
| [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Riserva o esegue il commit di un'area di pagine nello spazio degli indirizzi virtuali del processo specificato. |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) | Riserva o esegue il commit di un'area di memoria all'interno dello spazio degli indirizzi virtuali del processo specificato e specifica il nodo NUMA per la memoria fisica. |
| [**VirtualAllocFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Riserva, esegue il commit o modifica lo stato di un'area di pagine nello spazio degli indirizzi virtuali del processo chiamante. La memoria allocata da questa funzione viene inizializzata automaticamente su zero. |
| [**Virtualfree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) | Rilascia o decommise un'area di pagine all'interno dello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) | Rilascia o decosegna un'area di memoria all'interno dello spazio degli indirizzi virtuali di un processo specificato. |
| [**VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) | Blocca l'area specificata dello spazio indirizzi virtuali del processo nella memoria fisica. |
| [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) | Modifica la protezione dell'accesso in un'area di pagine di cui è stato eseguito il commit nello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) | Modifica la protezione dell'accesso in un'area di pagine di cui è stato eseguito il commit nello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualProtectFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualprotectfromapp) | Modifica la protezione in un'area di pagine di cui è stato eseguito il commit nello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) | Fornisce informazioni su un intervallo di pagine nello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) | Fornisce informazioni su un intervallo di pagine nello spazio degli indirizzi virtuali del processo chiamante. |
| [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) | Sblocca un intervallo specificato di pagine nello spazio degli indirizzi virtuali di un processo. |

## <a name="global-and-local-functions"></a>Funzioni globali e locali

Vedere anche [funzioni globali e locali.](global-and-local-functions.md) Queste funzioni vengono fornite per la compatibilità con Windows a 16 bit e vengono usate con Dynamic Data Exchange (DDE), le funzioni degli Appunti e gli oggetti dati OLE. A meno che la documentazione non dica in modo specifico che deve essere usata una funzione globale o locale, le nuove applicazioni devono usare la funzione [heap](heap-functions.md) corrispondente con l'handle restituito da [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap). Per una funzionalità equivalente alla funzione globale o locale, impostare il parametro *dwFlags* della funzione heap su 0.

| Funzione | Descrizione | Funzione heap corrispondente |
|-|-|-|
| [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [ **LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) | Alloca il numero specificato di byte dall'heap. | [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) |
| [**GlobalDiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard), [ **LocalDiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) | Rimuove il blocco di memoria globale specificato. | Non applicabile. |
| [**GlobalFlags**](/windows/desktop/api/WinBase/nf-winbase-globalflags), [ **LocalFlags**](/windows/desktop/api/WinBase/nf-winbase-localflags) | Restituisce informazioni sull'oggetto di memoria globale specificato. | Non applicabile. Usare [**HeapValidate per**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) convalidare l'heap. |
| [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree), [ **LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) | Libera l'oggetto memoria globale specificato. | [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) |
| [**GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle), [ **LocalHandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) | Recupera l'handle associato al puntatore specificato a un blocco di memoria globale. Questa funzione deve essere usata solo con le funzioni OLE e Degli Appunti che la richiedono. | Non applicabile. |
| [**GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock), [ **LocalLock**](/windows/desktop/api/WinBase/nf-winbase-locallock) | Blocca un oggetto di memoria globale e restituisce un puntatore al primo byte del blocco di memoria dell'oggetto. | Non applicabile. |
| [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc), [ **LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) | Modifica le dimensioni o gli attributi di un oggetto di memoria globale specificato. | [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) |
| [**GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize), [ **LocalSize**](/windows/desktop/api/WinBase/nf-winbase-localsize) | Recupera le dimensioni correnti dell'oggetto memoria globale specificato. | [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) |
| [**GlobalUnlock**](/windows/desktop/api/WinBase/nf-winbase-globalunlock), [ **LocalUnlock**](/windows/desktop/api/WinBase/nf-winbase-localunlock) | Decrementa il numero di blocchi associato a un oggetto di memoria. Questa funzione deve essere usata solo con le funzioni OLE e Degli Appunti che la richiedono. | Non applicabile. |

## <a name="bad-memory-functions"></a>Funzioni di memoria non erta

| Funzione | Descrizione |
|-|-|
| [**BadMemoryCallbackRoutine**](/previous-versions/windows/desktop/legacy/hh691011(v=vs.85)) | Funzione definita dall'applicazione registrata con la [**funzione RegisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) chiamata quando vengono rilevate una o più pagine di memoria non valida. |
| [**GetMemoryErrorHandlingCapabilities**](/windows/win32/api/memoryapi/nf-memoryapi-getmemoryerrorhandlingcapabilities) | Ottiene le funzionalità di gestione degli errori di memoria del sistema. |
| [**RegisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) | Registra una notifica di memoria non valida che viene chiamata quando vengono rilevate una o più pagine di memoria non valida. |
| [**UnregisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-unregisterbadmemorynotification) | Chiude l'handle di notifica della memoria non valido specificato. |

## <a name="enclave-functions"></a>Funzioni dell'enclave

| Funzione | Descrizione |
|-|-|
| [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave) | Crea un nuovo enclave non inizializzato. Un enclave è un'area isolata di codice e dati all'interno dello spazio indirizzi per un'applicazione. Solo il codice eseguito all'interno dell'enclave può accedere ai dati all'interno dello stesso enclave. |
| [**InitializeEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave) | Inizializza un enclave creato e caricato con dati. |
| [**IsEnclaveTypeSupported**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported) | Recupera un valore che indica se il tipo di enclave specificato è supportato. |
| [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) | Carica i dati in un enclave non inizializzato creato chiamando [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave). |

## <a name="atl-thunk-functions"></a>Funzioni thunk ATL

| Funzione | Descrizione |
|-|-|
| [**AtlThunk_AllocateData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_allocatedata) | Alloca spazio in memoria per un thunk ATL. |
| [**AtlThunk_DataToCode**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_datatocode) | Restituisce una funzione eseguibile corrispondente al parametro AtlThunkData_t. |
| [**AtlThunk_FreeData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_freedata) | Libera la memoria associata a un thunk ATL. |
| [**AtlThunk_InitData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_initdata) | Inizializza un thunk ATL. |

## <a name="obsolete-functions"></a>Funzioni obsolete

Queste funzioni vengono fornite solo per la compatibilità con le versioni a 16 bit Windows:

- [**IsBadCodePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadcodeptr)
- [**IsBadReadPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadreadptr)
- [**IsBadStringPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadstringptra)
- [**IsBadWritePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadwriteptr)

La funzione seguente può restituire informazioni non corrette e non deve essere usata. Usare invece la [**funzione GlobalMemoryStatusEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex)

- [**GlobalMemoryStatus**](/windows/desktop/api/WinBase/nf-winbase-globalmemorystatus)