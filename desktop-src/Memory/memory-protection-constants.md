---
Description: Di seguito sono riportate le opzioni di protezione della memoria. È necessario specificare uno dei valori seguenti quando si alloca o si protegge una pagina in memoria. Gli attributi di protezione non possono essere assegnati a una parte di una pagina. possono essere assegnati solo a un'intera pagina.
ms.assetid: 09839db7-2118-4a7d-a707-a08c92bd600c
title: Costanti di protezione della memoria (WinNT.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 187e8e1f4e137823451771309c9cce19db2e7fbd9c5b57597b51cfc58ca61297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067691"
---
# <a name="memory-protection-constants"></a>Costanti di protezione della memoria

Di seguito sono riportate le opzioni di protezione della memoria. È necessario specificare uno dei valori seguenti quando si alloca o si protegge una pagina in memoria. Gli attributi di protezione non possono essere assegnati a una parte di una pagina. possono essere assegnati solo a un'intera pagina.

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
Ad esempio, [Windows esempi classici](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/dataaccess/oledb/sampprov/extbuff.cpp) in GitHub.

## <a name="constants"></a>Costanti


| Costante/valore                                                                                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_EXECUTE"></span><span id="page_execute"></span><dl> <dt>**PAGINA \_ EXECUTE**</dt> <dt>0x10</dt> </dl>                                       | Abilita l'accesso in esecuzione all'area di pagine di cui è stato eseguito il commit. Un tentativo di scrittura nell'area di cui è stato eseguito il commit comporta una violazione di accesso.<br/> Questo flag non è supportato dalla [**funzione CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="PAGE_EXECUTE_READ"></span><span id="page_execute_read"></span><dl> <dt>**PAGINA \_ EXECUTE \_ READ**</dt> <dt>0x20</dt> </dl>                       | Consente l'accesso di sola lettura o di esecuzione all'area di pagine di cui è stato eseguito il commit. Un tentativo di scrittura nell'area di cui è stato eseguito il commit comporta una violazione di accesso.<br/> **Windows Server 2003 e Windows XP:** Questo attributo non è supportato dalla funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) fino Windows XP con SP2 e Windows Server 2003 con SP1.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="PAGE_EXECUTE_READWRITE"></span><span id="page_execute_readwrite"></span><dl> <dt>**PAGINA \_ ESEGUIRE \_ READWRITE**</dt> <dt>0x40</dt> </dl>        | Abilita l'accesso in esecuzione, di sola lettura o in lettura/scrittura all'area di pagine di cui è stato eseguito il commit.<br/> **Windows Server 2003 e Windows XP:** Questo attributo non è supportato dalla funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) fino Windows XP con SP2 e Windows Server 2003 con SP1.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="PAGE_EXECUTE_WRITECOPY"></span><span id="page_execute_writecopy"></span><dl> <dt>**PAGINA \_ ESEGUIRE \_ WRITECOPY**</dt> <dt>0x80</dt> </dl>        | Abilita l'accesso di esecuzione, sola lettura o copia in scrittura a una visualizzazione mappata di un oggetto di mapping di file. Un tentativo di scrittura in una pagina di copia su scrittura di cui è stato eseguito il commit comporta la creazione di una copia privata della pagina per il processo. La pagina privata è contrassegnata come **PAGE \_ EXECUTE \_ READWRITE** e la modifica viene scritta nella nuova pagina.<br/> Questo flag non è supportato dalle [**funzioni VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) [**o VirtualAllocEx.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) **Windows Vista, Windows Server 2003 e Windows XP:** Questo attributo non è supportato dalla [**funzione CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) fino Windows Vista con SP1 e Windows Server 2008.<br/> <br/> |
| <span id="PAGE_NOACCESS"></span><span id="page_noaccess"></span><dl> <dt>**PAGINA \_ NoACCESS**</dt> <dt>0x01</dt> </dl>                                    | Disabilita tutti gli accessi all'area di pagine di cui è stato eseguito il commit. Un tentativo di lettura, scrittura o esecuzione dell'area di cui è stato eseguito il commit comporta una violazione di accesso.<br/> Questo flag non è supportato dalla [**funzione CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="PAGE_READONLY"></span><span id="page_readonly"></span><dl> <dt>**PAGINA \_ READONLY**</dt> <dt>0x02</dt> </dl>                                    | Abilita l'accesso in sola lettura all'area di pagine di cui è stato eseguito il commit. Un tentativo di scrittura nell'area di cui è stato eseguito il commit comporta una violazione di accesso. Se [Prevenzione esecuzione programmi è](data-execution-prevention.md) abilitato, un tentativo di eseguire codice nell'area di cui è stato eseguito il commit comporta una violazione di accesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="PAGE_READWRITE"></span><span id="page_readwrite"></span><dl> <dt>**PAGINA \_ READWRITE**</dt> <dt>0x04</dt> </dl>                                 | Abilita l'accesso in sola lettura o in lettura/scrittura all'area di pagine di cui è stato eseguito il commit. Se [la funzionalità Protezione esecuzione programmi](data-execution-prevention.md) è abilitata, il tentativo di eseguire codice nell'area di cui è stato eseguito il commit comporta una violazione di accesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="PAGE_WRITECOPY"></span><span id="page_writecopy"></span><dl> <dt>**PAGINA \_ WRITECOPY**</dt> <dt>0x08</dt> </dl>                                 | Abilita l'accesso di sola lettura o copia in scrittura a una visualizzazione mappata di un oggetto mapping di file. Un tentativo di scrittura in una pagina di copia su scrittura di cui è stato eseguito il commit comporta la creazione di una copia privata della pagina per il processo. La pagina privata è contrassegnata come **PAGE \_ READWRITE** e la modifica viene scritta nella nuova pagina. Se [la funzionalità Protezione esecuzione programmi](data-execution-prevention.md) è abilitata, il tentativo di eseguire codice nell'area di cui è stato eseguito il commit comporta una violazione di accesso.<br/> Questo flag non è supportato dalle [**funzioni VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) [**o VirtualAllocEx.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)<br/>                                                                               |
| <span id="PAGE_TARGETS_INVALID"></span><span id="page_targets_invalid"></span><dl> <dt>**PAGINA \_ DESTINAZIONI \_ NON**</dt> <dt>0X40000000</dt> </dl>        | Imposta tutte le posizioni nelle pagine come destinazioni non valide per CFG. Usato insieme a qualsiasi protezione della pagina di esecuzione, ad esempio **PAGE \_ EXECUTE**, **PAGE EXECUTE \_ \_ READ**, **PAGE EXECUTE \_ \_ READWRITE** e **PAGE EXECUTE \_ \_ WRITECOPY**. Qualsiasi chiamata indiretta a posizioni in tali pagine avrà esito negativo nei controlli CFG e il processo verrà terminato. Il comportamento predefinito per le pagine eseguibili allocate deve essere contrassegnato come destinazioni di chiamata valide per CFG.<br/> Questo flag non è supportato dalle [**funzioni VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) [**o CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                              |
| <span id="PAGE_TARGETS_NO_UPDATE"></span><span id="page_targets_no_update"></span><dl> <dt>**PAGINA \_ DESTINAZIONI \_ NO \_ UPDATE**</dt> <dt>0x40000000</dt> </dl> | Le pagine nell'area non avranno le informazioni CFG aggiornate mentre la protezione cambia per [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect). Ad esempio, se le pagine nell'area sono state allocate usando **PAGE \_ TARGETS \_ INVALID,** le informazioni non valide verranno mantenute mentre la protezione della pagina cambia. Questo flag è valido solo quando la protezione viene modificata in un tipo di file eseguibile, ad esempio **PAGE \_ EXECUTE**, **PAGE EXECUTE \_ \_ READ**, **PAGE EXECUTE \_ \_ READWRITE** e **PAGE EXECUTE \_ \_ WRITECOPY**. Il comportamento predefinito per **la modifica della protezione VirtualProtect** in eseguibile è contrassegnare tutte le località come destinazioni di chiamata valide per CFG. <br/>                                           |



Di seguito sono riportati i modificatori che possono essere usati in aggiunta alle opzioni fornite nella tabella precedente, ad eccezione di quanto indicato.



| Costante/valore                                                                                                                                                                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_GUARD"></span><span id="page_guard"></span><dl> <dt>**PAGINA \_ GUARD**</dt> <dt>0x100</dt> </dl>                      | Le pagine nell'area diventano pagine di protezione. Qualsiasi tentativo di accedere a una pagina di protezione fa sì che il sistema genera un'eccezione **DI \_ \_ VIOLAZIONE DI PAGINA \_ DI STATUS GUARD** e disattiva lo stato della pagina di protezione. Le pagine di protezione fungono quindi da allarme di accesso una sola volta. Per altre informazioni, vedere [Creating Guard Pages](creating-guard-pages.md) (Creazione di guard page).<br/> Quando un tentativo di accesso porta il sistema a disattivare lo stato della pagina di protezione, viene attivata la protezione della pagina sottostante.<br/> Se si verifica un'eccezione di pagina di protezione durante un servizio di sistema, il servizio restituisce in genere un indicatore di stato di errore.<br/> Questo valore non può essere usato con **PAGE \_ NOACCESS.**<br/> Questo flag non è supportato dalla [**funzione CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                              |
| <span id="PAGE_NOCACHE"></span><span id="page_nocache"></span><dl> <dt>**PAGINA \_ NoCACHE**</dt> <dt>0x200</dt> </dl>                | Imposta tutte le pagine come non memorizzabili nella cache. Le applicazioni non devono usare questo attributo se non quando sono richieste in modo esplicito per un dispositivo. L'uso delle funzioni interlock con la memoria mappata con **SEC \_ NOCACHE** può generare un'eccezione **EXCEPTION ILLEGAL \_ \_ INSTRUCTION.**<br/> Il flag **PAGE \_ NOCACHE** non può essere usato con i flag **PAGE \_ GUARD,** **PAGE \_ NOACCESS** o **PAGE \_ WRITECOMBINE.**<br/> Il flag **PAGE \_ NOCACHE** può essere usato solo quando si alloca memoria privata con le [**funzioni VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)o [**VirtualAllocExNuma.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) Per abilitare l'accesso alla memoria non memorizzata nella cache per la memoria condivisa, specificare il flag **\_ SEC NOCACHE** quando si chiama la [**funzione CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                   |
| <span id="PAGE_WRITECOMBINE"></span><span id="page_writecombine"></span><dl> <dt>**PAGINA \_ WRITECOMBINE**</dt> <dt>0x400</dt> </dl> | Imposta tutte le pagine da combinare in scrittura. <br/> Le applicazioni non devono usare questo attributo se non quando sono richieste in modo esplicito per un dispositivo. L'uso delle funzioni interlock con la memoria mappata come combinazione di scrittura può generare un'eccezione **EXCEPTION \_ ILLEGAL \_ INSTRUCTION.** <br/> Il flag **PAGE \_ WRITECOMBINE** non può essere specificato con i flag **PAGE \_ NOACCESS,** **PAGE \_ GUARD** e **PAGE \_ NOCACHE.** <br/> Il flag **\_ PAGE WRITECOMBINE** può essere usato solo quando si alloca memoria privata con le [**funzioni VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)o [**VirtualAllocExNuma.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) Per abilitare l'accesso alla memoria combinata in scrittura per la memoria condivisa, specificare il flag **\_ SEC WRITECOMBINE** quando si chiama la [**funzione CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)<br/> **Windows Server 2003 e Windows XP:** Questo flag non è supportato fino Windows Server 2003 con SP1.<br/> |



Le costanti seguenti possono essere usate con la funzione [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) solo quando si specifica un enclave con l'architettura Intel Software Guard Extensions (SGX).



| Costante                                                                                                                                                                                                  | Descrizione                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_ENCLAVE_THREAD_CONTROL"></span><span id="page_enclave_thread_control"></span><dl> <dt>**CONTROLLO \_ THREAD ENCLAVE \_ DI \_ PAGINA**</dt> </dl> | La pagina contiene una struttura di controllo del thread (TCS).<br/>                                                                              |
| <span id="PAGE_ENCLAVE_UNVALIDATED"></span><span id="page_enclave_unvalidated"></span><dl> <dt>**\_ENCLAVE DI PAGINA \_ NON CONVALIDATO**</dt> </dl>           | Il contenuto della pagina fornito viene escluso dalla misurazione con l'istruzione EEXTEND del modello di programmazione Intel SGX.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>WinNT.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)
</dt> <dt>

[Protezione della memoria](memory-protection.md)
</dt> <dt>

[**Virtualalloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
</dt> <dt>

[**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)
</dt> <dt>

[**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)
</dt> </dl>

 

 
