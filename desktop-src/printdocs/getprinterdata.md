---
description: La funzione GetPrinterData recupera i dati di configurazione per la stampante o il server di stampa specificato.
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: Funzione GetPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterData
- GetPrinterDataA
- GetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: cb18936d6d3c1d82f4a52a874883cdcdfaae4815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314995"
---
# <a name="getprinterdata-function"></a>GetPrinterData (funzione)

La funzione **GetPrinterData** recupera i dati di configurazione per la stampante o il server di stampa specificato.

In Windows 2000 e versioni successive di Windows, la chiamata di **GetPrinterData** equivale alla chiamata di [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) con il parametro *pKeyName* impostato su "PrinterDriverData".

## <a name="syntax"></a>Sintassi


```C++
DWORD GetPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pValueName,
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

*pValueName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica i dati da recuperare.

Per le stampanti, questa stringa è il nome di un valore del registro di sistema nella chiave "PrinterDriverData" della stampante nel registro di sistema.

Per i server di stampa, questa stringa è una delle stringhe predefinite elencate nella sezione Osservazioni riportata di seguito.

</dd> <dt>

*pType* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve un valore che indica il tipo di dati recuperati in *pData*. La funzione restituisce il tipo specificato nella chiamata a [**SetPrinterData**](setprinterdata.md) o [**SetPrinterDataEx**](setprinterdataex.md) in cui sono archiviati i dati. Se non è necessario il tipo di dati, impostare questo parametro su **null** .

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve i dati di configurazione.

</dd> <dt>

*nSize* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pData* .

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati di configurazione. Se la dimensione del buffer specificata da *nSize* è troppo piccola, la funzione restituisce l' **errore \_ più \_ dati** e *pcbNeeded* indica le dimensioni del buffer richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **Error \_ Success**. Se la funzione ha esito negativo, il valore restituito è un valore di errore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

**GetPrinterData** recupera i dati di configurazione della stampante impostati dalla funzione [**SetPrinterDataEx**](setprinterdataex.md) o [**SetPrinterData**](setprinterdata.md) .

**GetPrinterData** potrebbe attivare una chiamata di Windows a [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), che potrebbe scrivere nel registro di sistema. In tal caso, è possibile che si verifichino effetti collaterali, ad esempio l'attivazione di un evento di aggiornamento o di aggiornamento della stampante con ID 20 nel client, se la stampante è condivisa in una rete.

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



 

In Windows 7 e versioni successive di Windows, per impostazione predefinita viene eseguito il rendering dei processi di stampa inviati a un server di stampa nel client. I valori seguenti configurano il rendering lato client di un processo di stampa e possono essere letti se si impostano i valori seguenti in *pValueName*.



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
| Nomi Unicode e ANSI<br/>   | **GetPrinterDataW** (Unicode) e **GetPrinterDataA** (ANSI)<br/>                                   |



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

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> <dt>

[**PRINTPROCESSOR \_ Caps \_ 1**](printprocessor-caps-1.md)
</dt> </dl>

 

