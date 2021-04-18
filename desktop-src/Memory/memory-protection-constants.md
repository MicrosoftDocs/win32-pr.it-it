---
Description: Di seguito sono riportate le opzioni di protezione della memoria. Quando si alloca o si protegge una pagina in memoria, è necessario specificare uno dei valori seguenti. Gli attributi di protezione non possono essere assegnati a una parte di una pagina; possono essere assegnati solo a una pagina intera.
ms.assetid: 09839db7-2118-4a7d-a707-a08c92bd600c
title: Costanti di protezione della memoria (WinNT. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 641fab68024d9db96f50327f7c78d51f3f9bca01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325468"
---
# <a name="memory-protection-constants"></a>Costanti di protezione della memoria

Di seguito sono riportate le opzioni di protezione della memoria. Quando si alloca o si protegge una pagina in memoria, è necessario specificare uno dei valori seguenti. Gli attributi di protezione non possono essere assegnati a una parte di una pagina; possono essere assegnati solo a una pagina intera.

## <a name="example"></a>Esempio

```cpp
STDMETHODIMP CExtBuffer::FInit
    (
    ULONG cItemMax,     //@parm IN | Maximum number of items ever
    ULONG cbItem,       //@parm IN | Size of each item, in bytes
    ULONG cbPage        //@parm IN | Size of system page size (from SysInfo)
    )
{
    BYTE  *pb;

    m_cbReserved = ((cbItem *cItemMax) / cbPage + 1) *cbPage;
    m_rgItem = (BYTE *) VirtualAlloc( NULL, m_cbReserved, MEM_RESERVE, PAGE_READWRITE );

    if (m_rgItem == NULL)
        return ResultFromScode( E_OUTOFMEMORY );

    m_cbItem  = cbItem;
    m_dbAlloc = (cbItem / cbPage + 1) *cbPage;
    pb = (BYTE *) VirtualAlloc( m_rgItem, m_dbAlloc, MEM_COMMIT, PAGE_READWRITE );
    if (pb == NULL)
        {
        VirtualFree((VOID *) m_rgItem, 0, MEM_RELEASE );
        m_rgItem = NULL;
        return ResultFromScode( E_OUTOFMEMORY );
        }

    m_cbAlloc = m_dbAlloc;
    return ResultFromScode( S_OK );
}
```
Esempio da [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/dataaccess/oledb/sampprov/extbuff.cpp) in GitHub.

## <a name="constants"></a>Costanti


| Costante/valore                                                                                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_EXECUTE"></span><span id="page_execute"></span><dl> <dt>**Pagina \_ di Esegui**</dt> <dt>0x10</dt> </dl>                                       | Consente l'accesso Execute all'area di pagine di cui è stato eseguito il commit. Un tentativo di scrittura nell'area di cui è stato eseguito il commit comporta una violazione di accesso.<br/> Questo flag non è supportato dalla funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="PAGE_EXECUTE_READ"></span><span id="page_execute_read"></span><dl> <dt>**Pagina \_ di Esegui \_ lettura**</dt> <dt>0x20</dt> </dl>                       | Consente l'accesso di esecuzione o di sola lettura all'area di cui è stato eseguito il commit delle pagine. Un tentativo di scrittura nell'area di cui è stato eseguito il commit comporta una violazione di accesso.<br/> **Windows Server 2003 e Windows XP:** Questo attributo non è supportato dalla funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) fino a Windows XP con SP2 e windows Server 2003 con SP1.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="PAGE_EXECUTE_READWRITE"></span><span id="page_execute_readwrite"></span><dl> <dt>**Pagina \_ di ESEGUIRE \_ ReadWrite**</dt> <dt>0x40</dt> </dl>        | Consente l'accesso in lettura/scrittura o in lettura/scrittura all'area di cui è stato eseguito il commit delle pagine.<br/> **Windows Server 2003 e Windows XP:** Questo attributo non è supportato dalla funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) fino a Windows XP con SP2 e windows Server 2003 con SP1.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="PAGE_EXECUTE_WRITECOPY"></span><span id="page_execute_writecopy"></span><dl> <dt>**Pagina \_ di ESEGUIRE \_ WRITECOPY**</dt> <dt>0x80</dt> </dl>        | Consente l'accesso Execute, read-only o copy-on-write a una visualizzazione mappata di un oggetto mapping di file. Un tentativo di scrittura in una pagina copia in scrittura di cui è stato eseguito il commit genera una copia privata della pagina eseguita per il processo. La pagina privata è contrassegnata come **pagina \_ Execute \_ ReadWrite** e la modifica viene scritta nella nuova pagina.<br/> Questo flag non è supportato dalle funzioni [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) . **Windows Vista, Windows Server 2003 e Windows XP:** Questo attributo non è supportato dalla funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) fino a Windows Vista con SP1 e windows Server 2008.<br/> <br/> |
| <span id="PAGE_NOACCESS"></span><span id="page_noaccess"></span><dl> <dt>**Pagina \_ di NoAccess**</dt> <dt>0x01</dt> </dl>                                    | Disabilita tutti gli accessi all'area di pagine di cui è stato eseguito il commit. Un tentativo di leggere, scrivere o eseguire l'area di cui è stato eseguito il commit comporta una violazione di accesso.<br/> Questo flag non è supportato dalla funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="PAGE_READONLY"></span><span id="page_readonly"></span><dl> <dt>**Pagina \_ di**</dt> <dt>0x02</dt> di sola lettura </dl>                                    | Consente l'accesso in sola lettura all'area di cui è stato eseguito il commit delle pagine. Un tentativo di scrittura nell'area di cui è stato eseguito il commit comporta una violazione di accesso. Se la [prevenzione dell'esecuzione dei dati](data-execution-prevention.md) è abilitata, un tentativo di eseguire codice nell'area di cui è stato eseguito il commit comporta una violazione di accesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="PAGE_READWRITE"></span><span id="page_readwrite"></span><dl> <dt>**Pagina \_ di**</dt> <dt>0x04</dt> ReadWrite </dl>                                 | Consente l'accesso in sola lettura o in lettura/scrittura all'area di pagine di cui è stato eseguito il commit. Se la [prevenzione dell'esecuzione dei dati](data-execution-prevention.md) è abilitata, il tentativo di eseguire codice nell'area di cui è stato eseguito il commit comporta una violazione di accesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="PAGE_WRITECOPY"></span><span id="page_writecopy"></span><dl> <dt>**Pagina \_ di**</dt> <dt>0x08</dt> WRITECOPY </dl>                                 | Consente l'accesso in sola lettura o copy-on-write a una visualizzazione mappata di un oggetto mapping di file. Un tentativo di scrittura in una pagina copia in scrittura di cui è stato eseguito il commit genera una copia privata della pagina eseguita per il processo. La pagina privata è contrassegnata come **pagina \_ ReadWrite** e la modifica viene scritta nella nuova pagina. Se la [prevenzione dell'esecuzione dei dati](data-execution-prevention.md) è abilitata, il tentativo di eseguire codice nell'area di cui è stato eseguito il commit comporta una violazione di accesso.<br/> Questo flag non è supportato dalle funzioni [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) .<br/>                                                                               |
| <span id="PAGE_TARGETS_INVALID"></span><span id="page_targets_invalid"></span><dl> <dt>**Pagina \_ di DESTINAZIONI \_ 0x40000000 non valide**</dt> <dt></dt> </dl>        | Imposta tutte le posizioni nelle pagine come destinazioni non valide per la CFG. Utilizzato insieme a qualsiasi protezione della pagina di esecuzione, ad esempio **\_ esecuzione pagina**, **\_ \_ lettura pagina esecuzione**, pagina **\_ esecuzione \_ ReadWrite** e **pagina \_ esecuzione \_ WRITECOPY**. Tutte le chiamate indirette a posizioni in tali pagine avranno esito negativo per i controlli CFG e il processo verrà terminato. Il comportamento predefinito per le pagine eseguibili allocate deve essere contrassegnato come destinazioni di chiamata valide per CFG.<br/> Questo flag non è supportato dalle funzioni [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) o [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                              |
| <span id="PAGE_TARGETS_NO_UPDATE"></span><span id="page_targets_no_update"></span><dl> <dt>**Pagina \_ di DESTINAZIONI \_ senza \_ aggiornamento**</dt> <dt>0x40000000</dt> </dl> | Le pagine dell'area non avranno aggiornato le informazioni di CFG mentre la protezione viene modificata per [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect). Se, ad esempio, le pagine dell'area sono state allocate usando le **destinazioni della pagina \_ \_ non valide**, le informazioni non valide verranno mantenute mentre la protezione della pagina viene modificata. Questo flag è valido solo quando la protezione viene modificata in un tipo eseguibile, ad esempio **pagina \_ esecuzione**, **pagina \_ esecuzione \_ lettura**, **pagina \_ esecuzione \_ ReadWrite** e **pagina \_ esecuzione \_ WRITECOPY**. Il comportamento predefinito per la modifica della protezione **VirtualProtect** in eseguibile consiste nel contrassegnare tutti i percorsi come destinazioni di chiamata valide per cfg. <br/>                                           |



Di seguito sono riportati i modificatori che possono essere usati in aggiunta alle opzioni fornite nella tabella precedente, ad eccezione di quanto indicato.



| Costante/valore                                                                                                                                                                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_GUARD"></span><span id="page_guard"></span><dl> <dt>**Pagina \_ di GUARD**</dt> <dt>0x100</dt> </dl>                      | Le pagine dell'area diventano pagine di Guard. Se si tenta di accedere a una pagina di protezione, il sistema genera un'eccezione di **\_ violazione della \_ pagina \_ status Guard** e disattiva lo stato della pagina Guard. Le pagine Guard funzionano quindi come un allarme di accesso monouso. Per altre informazioni, vedere [Creating Guard Pages](creating-guard-pages.md) (Creazione di guard page).<br/> Quando un tentativo di accesso induce il sistema a disattivare lo stato della pagina di protezione, assume la protezione della pagina sottostante.<br/> Se si verifica un'eccezione della pagina Guard durante un servizio di sistema, in genere il servizio restituisce un indicatore di stato di errore.<br/> Questo valore non può essere utilizzato con la **pagina \_ NoAccess**.<br/> Questo flag non è supportato dalla funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                                                                                              |
| <span id="PAGE_NOCACHE"></span><span id="page_nocache"></span><dl> <dt>**Pagina \_ di NoCache**</dt> <dt>0x200</dt> </dl>                | Imposta tutte le pagine come non memorizzabili nella cache. Le applicazioni non devono usare questo attributo tranne quando richiesto in modo esplicito per un dispositivo. L'utilizzo delle funzioni Interlocked con memoria mappata con **sec \_ NoCache** può causare un'eccezione **di \_ \_ istruzione non valida** .<br/> Impossibile utilizzare il flag di **pagina \_ NoCache** con i flag Page **\_ Guard**, **pagina \_ NoAccess** o **Page \_ WRITECOMBINE** .<br/> Il flag della **pagina \_ NoCache** può essere utilizzato solo quando si alloca una memoria privata con le funzioni [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)o [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) . Per abilitare l'accesso alla memoria non memorizzato nella cache per la memoria condivisa, specificare il flag **sec \_ NoCache** quando si chiama la funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/>                                                                                                                                                   |
| <span id="PAGE_WRITECOMBINE"></span><span id="page_writecombine"></span><dl> <dt>**Pagina \_ di**</dt> <dt>0x400</dt> WRITECOMBINE </dl> | Imposta tutte le pagine come combinate in scrittura. <br/> Le applicazioni non devono usare questo attributo tranne quando richiesto in modo esplicito per un dispositivo. L'utilizzo delle funzioni Interlocked con memoria mappata come scrittura combinata può generare un'eccezione di **\_ \_ istruzione non valida** . <br/> Impossibile specificare il flag **Page \_ WRITECOMBINE** con i flag di pagina **\_ NoAccess**, **Page \_ Guard** e **Page \_ NoCache** . <br/> Il **flag \_ WRITECOMBINE della pagina** può essere utilizzato solo quando si alloca la memoria privata con le funzioni [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)o [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) . Per abilitare l'accesso in scrittura alla memoria condivisa per la memoria condivisa, specificare il flag **sec \_ WRITECOMBINE** quando si chiama la funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) .<br/> **Windows Server 2003 e Windows XP:** Questo flag non è supportato fino a Windows Server 2003 con SP1.<br/> |



Le costanti seguenti possono essere usate solo con la funzione [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) quando si specifica un'enclave con l'architettura di Intel Software Guard Extensions (SGX).



| Costante                                                                                                                                                                                                  | Descrizione                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_ENCLAVE_THREAD_CONTROL"></span><span id="page_enclave_thread_control"></span><dl> <dt>**\_controllo thread enclave pagina \_ \_**</dt> </dl> | La pagina contiene una struttura di controllo dei thread (TCS).<br/>                                                                              |
| <span id="PAGE_ENCLAVE_UNVALIDATED"></span><span id="page_enclave_unvalidated"></span><dl> <dt>**enclave della pagina non \_ \_ convalidato**</dt> </dl>           | Il contenuto della pagina fornito viene escluso dalla misurazione con l'istruzione EEXTEND del modello di programmazione Intel SGX.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>WinNT. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)
</dt> <dt>

[Protezione della memoria](memory-protection.md)
</dt> <dt>

[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
</dt> <dt>

[**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)
</dt> <dt>

[**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)
</dt> </dl>

 

 
