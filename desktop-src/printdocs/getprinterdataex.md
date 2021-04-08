---
description: La funzione GetPrinterDataEx recupera i dati di configurazione per la stampante o il server di stampa specificato.
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
title: Funzione GetPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDataEx
- GetPrinterDataExA
- GetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bdadf2e1259445ca5285e5b12bc906140a137cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759662"
---
# <a name="getprinterdataex-function"></a>GetPrinterDataEx (funzione)

La funzione **GetPrinterDataEx** recupera i dati di configurazione per la stampante o il server di stampa specificato. **GetPrinterDataEx** è in grado di recuperare i valori archiviati dalla funzione [**SetPrinterData**](setprinterdata.md) . Inoltre, **GetPrinterDataEx** è in grado di recuperare i valori che la funzione [**SetPrinterDataEx**](setprinterdataex.md) archivia con una chiave specificata.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _In_  LPCTSTR pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante o il server di stampa per il quale la funzione recupera i dati di configurazione. Utilizzare la funzione [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*pKeyName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica la chiave che contiene il valore da recuperare. Usare il carattere barra rovesciata ( \\ ) come delimitatore per specificare un percorso con una o più sottochiavi.

Se *hPrinter* è un handle per una stampante e *pKeyName* è **null** o una stringa vuota, **GetPrinterDataEx** restituisce **l' \_ errore \_ parametro non valido**.

Se *hPrinter* è un handle per un server di stampa, *pKeyName* viene ignorato.

</dd> <dt>

*pValueName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica i dati da recuperare.

Per le stampanti, questa stringa specifica il nome di un valore nella chiave *pKeyName* .

Per i server di stampa, questa stringa è una delle stringhe predefinite elencate nella sezione Osservazioni riportata di seguito.

</dd> <dt>

*pType* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il tipo di dati archiviati nel valore. La funzione restituisce il tipo specificato nella chiamata [**SetPrinterDataEx**](setprinterdataex.md) quando i dati sono stati archiviati. Questo parametro può essere **null** se non sono necessarie le informazioni. **GetPrinterDataEx** passa *pType* come parametro *lpdwType* di una chiamata di funzione [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) .

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve i dati di configurazione.

</dd> <dt>

*nSize* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pData*.

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati di configurazione. Se la dimensione del buffer specificata da *nSize* è troppo piccola, la funzione restituisce l' **errore \_ più \_ dati** e *pcbNeeded* indica le dimensioni del buffer richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **Error \_ Success**.

Se la funzione ha esito negativo, il valore restituito è un valore di errore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

**GetPrinterDataEx** recupera i dati di configurazione della stampante impostati dalle funzioni [**SetPrinterDataEx**](setprinterdataex.md) e [**SetPrinterData**](setprinterdata.md) .

La chiamata di **GetPrinterDataEx** con il parametro *pKeyName* impostato su "PrinterDriverData" equivale alla chiamata alla funzione [**GetPrinterData**](getprinterdata.md) .

Se *hPrinter* è un handle per un server di stampa, *pValueName* può specificare uno dei seguenti valori predefiniti.



| valore                                                               | Commenti                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ consentire all' \_ utente \_ MANAGEFORMS**                                | Windows XP con Service Pack 2 (SP2) e versioni successive<br/> Windows Server 2003 con Service Pack 1 (SP1) e versioni successive<br/>                                                                                                    |
| **\_architettura SPLREG**                                            |                                                                                                                                                                                                                                 |
| **\_bip SPLREG \_ abilitato**                                           |                                                                                                                                                                                                                                 |
| **SPLREG \_ directory predefinita dello \_ spooling \_**                               |                                                                                                                                                                                                                                 |
| **\_nome del \_ computer \_ DNS SPLREG**                                      |                                                                                                                                                                                                                                 |
| **SPLREG \_ DS \_ presente**                                             | In caso di esito positivo, *pData* contiene 0x0001 se il computer si trova in un dominio DS; in caso contrario, 0.<br/>                                                                                                                         |
| **SPLREG \_ DS \_ presente \_ per l' \_ utente**                                  | In caso di esito positivo, *pData* contiene 0x0001 se l'utente è connesso a un dominio DS; in caso contrario, 0.<br/>                                                                                                                   |
| **\_registro eventi di SPLREG \_**                                              |                                                                                                                                                                                                                                 |
| **\_versione principale di SPLREG \_**                                          |                                                                                                                                                                                                                                 |
| **\_versione secondaria \_ SPLREG**                                          |                                                                                                                                                                                                                                 |
| **\_popup NET \_ SPLREG**                                              | Non supportato in Windows Server 2003 e versioni successive<br/>                                                                                                                                                                       |
| **SPLREG \_ net \_ popup \_ al \_ computer**                                | In caso di esito positivo, *pData* contiene 1 se le notifiche dei processi devono essere inviate al computer client oppure 0 se le notifiche dei processi devono essere inviate all'utente.<br/> Non supportato in Windows Server 2003 e versioni successive<br/> |
| **\_versione del sistema operativo SPLREG \_**                                             | Windows XP e versioni successive<br/>                                                                                                                                                                                                 |
| **\_VERSIONEX del sistema operativo SPLREG \_**                                           |                                                                                                                                                                                                                                 |
| **\_ \_ \_ impostazione predefinita priorità thread porta SPLREG \_**                         |                                                                                                                                                                                                                                 |
| **\_ \_ priorità thread della porta SPLREG \_**                                  |                                                                                                                                                                                                                                 |
| **\_gruppi di \_ isolamento del driver di stampa SPLREG \_ \_**                        | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **SPLREG \_ tempo di isolamento del driver di stampa \_ prima del \_ \_ \_ \_ riciclo**         | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **\_numero massimo di oggetti di isolamento del driver di stampa SPLREG \_ \_ prima del \_ \_ \_ \_ riciclo** | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **\_timeout di \_ \_ \_ inattività isolamento driver di \_ stampa SPLREG**                 | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **\_criteri di \_ \_ esecuzione isolamento \_ driver \_ di stampa SPLREG**             | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **\_criteri di \_ \_ sostituzione isolamento \_ driver \_ di stampa SPLREG**              | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **\_fax remoto di SPLREG \_**                                             | In caso di esito positivo, *pData* contiene 0x0001 se il servizio fax supporta client remoti. in caso contrario, 0.<br/>                                                                                                               |
| **\_popup nuovo tentativo SPLREG \_**                                            | In caso di esito positivo, *pData* contiene 1 se il server è impostato per ritentare le finestre popup per tutti i processi oppure 0 se il server non ritenta le finestre popup per tutti i processi.<br/> Non supportato in Windows Server 2003 e versioni successive<br/> |
| **\_priorità thread dell'utilità di pianificazione SPLREG \_ \_**                             |                                                                                                                                                                                                                                 |
| **\_ \_ \_ impostazione predefinita priorità thread dell'utilità di pianificazione SPLREG \_**                    |                                                                                                                                                                                                                                 |
| **\_WEBSHAREMGMT SPLREG**                                            | Windows Server 2003 e versioni successive<br/>                                                                                                                                                                                        |



 

I valori seguenti di *pValueName* indicano il comportamento di stampa del pool quando si verifica un errore.



| valore                                       | Commenti                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ errore di riavvio del processo di SPLREG nel \_ pool \_**   | Il valore di *pData* indica il tempo, in secondi, in cui un processo viene riavviato in un'altra porta dopo che si è verificato un errore. Questa impostazione viene usata con **\_ \_ il processo di riavvio del SPLREG \_ nel \_ pool \_ abilitato**.<br/> |
| **SPLREG \_ riavvio \_ \_ del processo nel \_ pool \_ abilitato** | Un valore diverso da zero in *pData* indica che è abilitato il **processo di riavvio SPLREG \_ \_ \_ sull' \_ \_ errore del pool** .<br/>                                                                                            |



 

Il tempo specificato nel **processo di riavvio del SPLREG \_ \_ per l' \_ \_ \_ errore del pool** è minimo. Il tempo effettivo può essere più lungo, a seconda delle impostazioni di monitoraggio porta seguenti, che sono valori del registro di sistema in questa chiave del registro di sistema:

**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *MonitorName* > \\ porte**

Chiamare la funzione [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) per eseguire una query su questi valori.



| Impostazione di monitoraggio porta     | Tipo di dati      | Significato                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG \_ DWORD** | Se un valore diverso da zero, Abilita il monitoraggio della porta per aggiornare lo spooler con lo stato della porta.<br/>            |
| **StatusUpdateInterval** | **REG \_ DWORD** | Specifica l'intervallo, in minuti, quando il monitoraggio porta aggiorna lo spooler con lo stato della porta.<br/> |



 

Se *pKeyName* è una delle chiavi di servizio directory (DS) predefinite (vedere [**seprinter**](setprinter.md)) e *pValueName* contiene una virgola (','), la parte di *pValueName* prima della virgola è il nome del valore e la parte di *pValueName* a destra della virgola è l'OID della proprietà DS. Viene creata una sottochiave denominata OID e viene immesso un nuovo valore costituito dal nome del valore e dall'OID sotto la chiave OID. [**SetPrinterDataEx**](setprinterdataex.md) aggiunge anche il nome del valore e i dati sotto la chiave DS.

In Windows 7 e versioni successive di Windows, per impostazione predefinita viene eseguito il rendering dei processi di stampa inviati a un server di stampa nel client. La configurazione del rendering lato client per una stampante può essere letta impostando *pKeyName* su "PrinterDriverData" e *pValueName* sul valore dell'impostazione nella tabella seguente.



| Impostazione                      | Tipo di dati      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | Il valore 0, o se questo valore non è presente nel registro di sistema, Abilita il rendering predefinito lato client dei processi di stampa.<br/> Il valore 1 disabilita il rendering lato client dei processi di stampa.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG \_ DWORD** | Il valore 0, o se questo valore non è presente nel registro di sistema, provocherà il rendering dei processi di stampa nel client. Se non è possibile eseguire il rendering di un processo di stampa sul client, ne verrà eseguito il rendering nel server. Se non è possibile eseguire il rendering di un processo di stampa sul server, l'operazione avrà esito negativo.<br/> Il valore 1 eseguirà il rendering dei processi di stampa nel client. Se non è possibile eseguire il rendering di un processo di stampa sul client, l'operazione avrà esito negativo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **GetPrinterDataExW** (Unicode) e **GetPrinterDataExA** (ANSI)<br/>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

