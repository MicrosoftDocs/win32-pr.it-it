---
description: La funzione SetPrinterDataEx imposta i dati di configurazione per una stampante o un server di stampa. La funzione archivia i dati di configurazione nella chiave del registro di sistema Printers.
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: Funzione SetPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterDataEx
- SetPrinterDataExA
- SetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9f384c9c9d6f0d956264b45ec8b52043ad20e897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233343"
---
# <a name="setprinterdataex-function"></a>SetPrinterDataEx (funzione)

La funzione **SetPrinterDataEx** imposta i dati di configurazione per una stampante o un server di stampa. La funzione archivia i dati di configurazione sotto la chiave del registro di sistema della stampante.

## <a name="syntax"></a>Sintassi


```C++
DWORD SetPrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName,
  _In_ DWORD   Type,
  _In_ LPBYTE  pData,
  _In_ DWORD   cbData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante o il server di stampa per il quale la funzione imposta i dati di configurazione. Utilizzare la funzione [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*pKeyName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica la chiave contenente il valore da impostare. Se la chiave o le sottochiavi specificate non esistono, la funzione le crea.

Per archiviare i dati di configurazione che possono essere pubblicati nel servizio directory (DS), specificare una delle seguenti chiavi del registro di sistema predefinite.



| Valore                                                                                                                                                                      | Significato                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <dt>**SPLDS_DRIVER_KEY**</dt> </dl>    | I driver della stampante utilizzano questa chiave per archiviare le proprietà del driver.<br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <dt>**SPLDS_SPOOLER_KEY**</dt> </dl> | Riservato. Utilizzato solo dallo spooler di stampa per archiviare le proprietà dello spooler interno.<br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <dt>**SPLDS_USER_KEY**</dt> </dl>          | Le applicazioni utilizzano questa chiave per archiviare le proprietà della stampante, ad esempio i numeri degli asset della stampante.<br/> |



 

I valori archiviati con la chiave di SPLDS_USER_KEY vengono pubblicati nel servizio directory solo se nello schema è presente una proprietà corrispondente. Un amministratore di dominio deve creare la proprietà, se non esiste già. Per pubblicare una proprietà definita dall'utente dopo aver usato **SetPrinterDataEx** per aggiungere o modificare un valore, chiamare [**seprinter**](setprinter.md) con *Level* = 7 e con il membro **dwAction** di [**PRINTER_INFO_7**](printer-info-7.md) impostato su **DSPRINT_UPDATE**.

È possibile specificare altre chiavi per archiviare i dati di configurazione non DS. Usare il carattere barra rovesciata ( \\ ) come delimitatore per specificare un percorso con una o più sottochiavi.

Se *hPrinter* è un handle per una stampante e *pKeyName* è **null** o una stringa vuota, **SetPrinterDataEx** restituisce **ERROR_INVALID_PARAMETER**.

Se *hPrinter* è un handle per un server di stampa, *pKeyName* viene ignorato.

Non utilizzare **SPLDS_SPOOLER_KEY**. Per modificare le proprietà della stampante dello spooler, usare [**Seprinter**](setprinter.md) con *Level* = 2.

</dd> <dt>

*pValueName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica i dati da impostare.

Per le stampanti, questa stringa specifica il nome di un valore nella chiave *pKeyName* .

Per i server di stampa, questa stringa è una delle stringhe predefinite elencate nella sezione Osservazioni riportata di seguito.

</dd> <dt>

*Tipo* \[ di in\]
</dt> <dd>

Codice che indica il tipo di dati a cui punta il parametro *pData* . Per un elenco dei possibili codici di tipo, vedere [tipi di valore del registro di sistema](/windows/desktop/SysInfo/registry-value-types).

Se *pKeyName* specifica una delle chiavi del servizio directory predefinite, il *tipo* deve essere **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD** o **REG_BINARY**. Se si utilizza **REG_BINARY** , *cbData* deve essere uguale a 1 e il servizio directory considera i dati come un valore booleano.

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Puntatore a un buffer che contiene i dati di configurazione della stampante.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Dimensione, in byte, della matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito viene **ERROR_SUCCESS**.

Se la funzione ha esito negativo, il valore restituito è un valore di errore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Per recuperare i dati di configurazione esistenti per una stampante o uno spooler di stampa, chiamare la funzione [**GetPrinterDataEx**](getprinterdataex.md) .

La chiamata di **SetPrinterDataEx** con il parametro *pKeyName* impostato su "PrinterDriverData" equivale alla chiamata alla funzione [**SetPrinterData**](setprinterdata.md) .

Se *hPrinter* è un handle per un server di stampa, *pValueName* può specificare uno dei seguenti valori predefiniti.



| valore                                                               | Commenti                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_ALLOW_USER_MANAGEFORMS**                                | Windows XP con Service Pack 2 (SP2) e versioni successive<br/> Windows Server 2003 con Service Pack 1 (SP1) e versioni successive<br/>                                                                                                    |
| **SPLREG_BEEP_ENABLED**                                           |                                                                                                                                                                                                                                 |
| **SPLREG_DEFAULT_SPOOL_DIRECTORY**                               |                                                                                                                                                                                                                                 |
| **SPLREG_EVENT_LOG**                                              |                                                                                                                                                                                                                                 |
| **SPLREG_NET_POPUP**                                              | Non supportato in Windows Server 2003 e versioni successive<br/>                                                                                                                                                                       |
| **SPLREG_PORT_THREAD_PRIORITY_DEFAULT**                         |                                                                                                                                                                                                                                 |
| **SPLREG_PORT_THREAD_PRIORITY**                                  |                                                                                                                                                                                                                                 |
| **SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**                        | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**         | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE** | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**                 | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**             | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**              | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **SPLREG_RETRY_POPUP**                                            | In caso di esito positivo, *pData* contiene 1 se il server è impostato per ritentare le finestre popup per tutti i processi oppure 0 se il server non ritenta le finestre popup per tutti i processi.<br/> Non supportato in Windows Server 2003 e versioni successive<br/> |
| **SPLREG_SCHEDULER_THREAD_PRIORITY**                             |                                                                                                                                                                                                                                 |
| **SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**                    |                                                                                                                                                                                                                                 |
| **SPLREG_WEBSHAREMGMT**                                            | Windows Server 2003 e versioni successive<br/>                                                                                                                                                                                        |



 

Se si passa uno dei seguenti valori predefiniti come *pValueName* , viene impostato il comportamento di stampa del pool quando si verifica un errore.



| valore                                       | Commenti                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_RESTART_JOB_ON_POOL_ERROR**   | Il valore di *pData* indica il tempo, in secondi, in cui un processo viene riavviato in un'altra porta dopo che si è verificato un errore. Questa impostazione viene utilizzata con **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.<br/> |
| **SPLREG_RESTART_JOB_ON_POOL_ENABLED** | Un valore diverso da zero in *pData* indica che **SPLREG_RESTART_JOB_ON_POOL_ERROR** è abilitato.<br/>                                                                                            |



 

Il tempo specificato in **SPLREG_RESTART_JOB_ON_POOL_ERROR** è il tempo minimo. Il tempo effettivo può essere più lungo, a seconda delle impostazioni di monitoraggio porta seguenti, che sono valori del registro di sistema in questa chiave del registro di sistema:

**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *MonitorName* > \\ porte**

Chiamare la funzione [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) per impostare questi valori.



| Impostazione di monitoraggio porta     | Tipo di dati      | Significato                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG_DWORD** | Se un valore diverso da zero, Abilita il monitoraggio della porta per aggiornare lo spooler con lo stato della porta.<br/>            |
| **StatusUpdateInterval** | **REG_DWORD** | Specifica l'intervallo, in minuti, quando il monitoraggio porta aggiorna lo spooler con lo stato della porta.<br/> |



 

Per assicurarsi che lo spooler reindirizza i processi alla successiva stampante disponibile nel pool (quando il processo di stampa non viene stampato entro l'intervallo di tempo impostato), il monitor porta deve supportare SNMP e le porte di rete nel pool devono essere configurate come "stato SNMP abilitato". Il monitoraggio porta che supporta SNMP è il monitor porta TCP/IP standard.

In Windows 7 e versioni successive di Windows, per impostazione predefinita viene eseguito il rendering dei processi di stampa inviati a un server di stampa nel client. Il rendering lato client dei processi di stampa può essere configurato impostando *pKeyName* su "PrinterDriverData" e *pValueName* sul valore dell'impostazione nella tabella seguente.



| Impostazione                      | Tipo di dati      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG_DWORD** | Il valore 0, o se questo valore non è presente nel registro di sistema, Abilita il rendering predefinito lato client dei processi di stampa.<br/> Il valore 1 disabilita il rendering lato client dei processi di stampa.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG_DWORD** | Il valore 0, o se questo valore non è presente nel registro di sistema, provocherà il rendering dei processi di stampa nel client. Se non è possibile eseguire il rendering di un processo di stampa sul client, ne verrà eseguito il rendering nel server. Se non è possibile eseguire il rendering di un processo di stampa sul server, l'operazione avrà esito negativo.<br/> Il valore 1 eseguirà il rendering dei processi di stampa nel client. Se non è possibile eseguire il rendering di un processo di stampa sul client, l'operazione avrà esito negativo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **SetPrinterDataExW** (Unicode) e **SetPrinterDataExA** (ANSI)<br/>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**PRINTER_INFO_7**](printer-info-7.md)
</dt> </dl>

 

