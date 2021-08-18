---
description: La funzione SetPrinterDataEx imposta i dati di configurazione per una stampante o un server di stampa. La funzione archivia i dati di configurazione nella chiave del Registro di sistema printers.
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: Funzione SetPrinterDataEx (Winspool.h)
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
ms.openlocfilehash: 6d2904c853510efeb379c9d590852c8f082a4644315560c4dfa5a7f51daca6ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460351"
---
# <a name="setprinterdataex-function"></a>Funzione SetPrinterDataEx

La **funzione SetPrinterDataEx** imposta i dati di configurazione per una stampante o un server di stampa. La funzione archivia i dati di configurazione nella chiave del Registro di sistema della stampante.

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

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante o il server di stampa per il quale la funzione imposta i dati di configurazione. Usare la [**funzione OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*pKeyName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica la chiave contenente il valore da impostare. Se la chiave o le sottochiavi specificate non esistono, la funzione le crea.

Per archiviare i dati di configurazione che possono essere pubblicati nel servizio directory, specificare una delle chiavi del Registro di sistema predefinite seguenti.



| Valore                                                                                                                                                                      | Significato                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <dt>**SPLDS_DRIVER_KEY**</dt> </dl>    | I driver della stampante usano questa chiave per archiviare le proprietà dei driver.<br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <dt>**SPLDS_SPOOLER_KEY**</dt> </dl> | Riservato. Utilizzato solo dallo spooler di stampa per archiviare le proprietà interne dello spooler.<br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <dt>**SPLDS_USER_KEY**</dt> </dl>          | Le applicazioni usano questa chiave per archiviare le proprietà della stampante, ad esempio i numeri di asset della stampante.<br/> |



 

I valori archiviati nella chiave SPLDS_USER_KEY vengono pubblicati nel servizio directory solo se nello schema è presente una proprietà corrispondente. Se non esiste già, un amministratore di dominio deve creare la proprietà . Per pubblicare una proprietà definita dall'utente dopo aver utilizzato **SetPrinterDataEx** per aggiungere o modificare un valore, chiamare [**SetPrinter**](setprinter.md) con *Level* = 7 e con il membro **dwAction** di [**PRINTER_INFO_7**](printer-info-7.md) impostato su **DSPRINT_UPDATE**.

È possibile specificare altre chiavi per archiviare i dati di configurazione non DS. Usare il carattere barra rovesciata ( ) come delimitatore per specificare un percorso \\ con una o più sottochiavi.

Se *hPrinter è* un handle per una stampante e *pKeyName* è **NULL** o una stringa vuota, **SetPrinterDataEx** restituisce **ERROR_INVALID_PARAMETER**.

Se *hPrinter è* un handle per un server di stampa, *pKeyName viene* ignorato.

Non usare **SPLDS_SPOOLER_KEY**. Per modificare le proprietà della stampante dello spooler, usare [**SetPrinter**](setprinter.md) con *Livello* = 2.

</dd> <dt>

*pValueName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica i dati da impostare.

Per le stampanti, questa stringa specifica il nome di un valore nella *chiave pKeyName.*

Per i server di stampa, questa stringa è una delle stringhe predefinite elencate nella sezione Osservazioni seguente.

</dd> <dt>

*Tipo* \[ Pollici\]
</dt> <dd>

Codice che indica il tipo di dati a cui punta il *parametro pData.* Per un elenco dei codici di tipo possibili, vedere Tipi [di valori del Registro di sistema.](/windows/desktop/SysInfo/registry-value-types)

Se *pKeyName* specifica una delle chiavi del servizio directory predefinite, *type* deve essere REG_SZ **,** **REG_MULTI_SZ**, **REG_DWORD** o **REG_BINARY**. Se **REG_BINARY** viene usato , *cbData* deve essere uguale a 1 e il servizio directory considera i dati come un valore booleano.

</dd> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer che contiene i dati di configurazione della stampante.

</dd> <dt>

*cbData* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, della matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito viene **ERROR_SUCCESS**.

Se la funzione ha esito negativo, il valore restituito è un valore di errore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Per recuperare i dati di configurazione esistenti per una stampante o uno spooler di stampa, chiamare la [**funzione GetPrinterDataEx.**](getprinterdataex.md)

Chiamare **SetPrinterDataEx con** il *parametro pKeyName* impostato su "PrinterDriverData" equivale a chiamare la [**funzione SetPrinterData.**](setprinterdata.md)

Se *hPrinter* è un handle per un server di stampa, *pValueName* può specificare uno dei valori predefiniti seguenti.



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
| **SPLREG_RETRY_POPUP**                                            | In caso di esito positivo, *pData* contiene 1 se il server è impostato per ripetere la ripetizione delle finestre popup per tutti i processi oppure 0 se il server non ritenta la ripetizione delle finestre popup per tutti i processi.<br/> Non supportato in Windows Server 2003 e versioni successive<br/> |
| **SPLREG_SCHEDULER_THREAD_PRIORITY**                             |                                                                                                                                                                                                                                 |
| **SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**                    |                                                                                                                                                                                                                                 |
| **SPLREG_WEBSHAREMGMT**                                            | Windows Server 2003 e versioni successive<br/>                                                                                                                                                                                        |



 

Il passaggio di uno dei valori predefiniti seguenti come *pValueName* imposta il comportamento di stampa del pool quando si verifica un errore.



| valore                                       | Commenti                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_RESTART_JOB_ON_POOL_ERROR**   | Il valore *di pData* indica il tempo, in secondi, in cui un processo viene riavviato su un'altra porta dopo che si è verificato un errore. Questa impostazione viene usata con **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.<br/> |
| **SPLREG_RESTART_JOB_ON_POOL_ENABLED** | Un valore diverso da zero in *pData* indica che SPLREG_RESTART_JOB_ON_POOL_ERROR **è** abilitato.<br/>                                                                                            |



 

Il tempo specificato in **SPLREG_RESTART_JOB_ON_POOL_ERROR** è un tempo minimo. Il tempo effettivo può essere più lungo, a seconda delle impostazioni di monitoraggio delle porte seguenti, che sono valori del Registro di sistema in questa chiave del Registro di sistema:

**Controllo HKLM \\ SYSTEM \\ CurrentControlSet \\ Monitor \\ \\ monitora \\ < *monitoraggiNome* > \\ porte**

Chiamare la [**funzione RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) per impostare questi valori.



| Impostazione del monitoraggio delle porte     | Tipo di dati      | Significato                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG_DWORD** | Se un valore diverso da zero, consente al monitoraggio delle porte di aggiornare lo spooler con lo stato della porta.<br/>            |
| **StatusUpdateInterval** | **REG_DWORD** | Specifica l'intervallo, in minuti, in cui il monitoraggio delle porte aggiorna lo spooler con lo stato della porta.<br/> |



 

Per assicurarsi che lo spooler reindirizza i processi alla successiva stampante disponibile nel pool (quando il processo di stampa non viene stampato entro il tempo impostato), il monitoraggio delle porte deve supportare SNMP e le porte di rete nel pool devono essere configurate come "Stato SNMP abilitato". Il monitor di porta che supporta SNMP è il monitor di porta TCP/IP Standard.

In Windows 7 e versioni successive di Windows, il rendering dei processi di stampa inviati a un server di stampa viene eseguito nel client per impostazione predefinita. Il rendering lato client dei processi di stampa può essere configurato impostando *pKeyName* su "PrinterDriverData" e *pValueName* sul valore dell'impostazione nella tabella seguente.



| Impostazione                      | Tipo di dati      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG_DWORD** | Il valore 0, o se questo valore non è presente nel Registro di sistema, abilita il rendering lato client predefinito dei processi di stampa.<br/> Il valore 1 disabilita il rendering lato client dei processi di stampa.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG_DWORD** | Il valore 0 o se questo valore non è presente nel Registro di sistema causerà il rendering dei processi di stampa nel client. Se non è possibile eseguire il rendering di un processo di stampa nel client, ne verrà eseguito il rendering nel server. Se non è possibile eseguire il rendering di un processo di stampa nel server, l'esecuzione avrà esito negativo.<br/> Il valore 1 eseguirà il rendering dei processi di stampa nel client. Se non è possibile eseguire il rendering di un processo di stampa nel client, l'esecuzione avrà esito negativo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
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

[**Setprinter**](setprinter.md)
</dt> <dt>

[**PRINTER_INFO_7**](printer-info-7.md)
</dt> </dl>

 

