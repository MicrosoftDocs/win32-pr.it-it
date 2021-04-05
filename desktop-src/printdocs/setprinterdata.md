---
description: La funzione SetPrinterData imposta i dati di configurazione per una stampante o un server di stampa.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: Funzione SetPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterData
- SetPrinterDataA
- SetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 36af84fe665d68fd7996a0b81fbbf291314cc69e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881394"
---
# <a name="setprinterdata-function"></a>SetPrinterData (funzione)

La funzione **SetPrinterData** imposta i dati di configurazione per una stampante o un server di stampa.

Per specificare la chiave del registro di sistema in cui archiviare i dati, chiamare la funzione [**SetPrinterDataEx**](setprinterdataex.md) . La chiamata a **SetPrinterData** equivale alla chiamata della funzione **SetPrinterDataEx** con il parametro *pKeyName* impostato su "PrinterDriverData".

## <a name="syntax"></a>Sintassi


```C++
DWORD SetPrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName,
  _In_ DWORD  Type,
  _In_ LPBYTE pData,
  _In_ DWORD  cbData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante o il server di stampa per il quale la funzione imposta i dati di configurazione. Utilizzare la funzione [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*pValueName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica i dati da impostare.

Per le stampanti, questa stringa è il nome di un valore del registro di sistema nella chiave "PrinterDriverData" della stampante nel registro di sistema.

Per i server di stampa, questa stringa è una delle stringhe predefinite elencate nella sezione Osservazioni riportata di seguito.

</dd> <dt>

*Tipo* \[ di in\]
</dt> <dd>

Codice che indica il tipo di dati a cui punta il parametro *pData* . Per un elenco dei possibili codici di tipo, vedere [tipi di valore del registro di sistema](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Puntatore a una matrice di byte che contiene i dati di configurazione della stampante.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Dimensione, in byte, della matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **Error \_ Success**.

Se la funzione ha esito negativo, il valore restituito è un valore di errore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Per recuperare i dati di configurazione esistenti per una stampante, chiamare la funzione [**GetPrinterDataEx**](getprinterdataex.md) o [**GetPrinterData**](getprinterdata.md) .

Se *hPrinter* è un handle per un server di stampa, *pValueName* può specificare uno dei seguenti valori predefiniti.



| valore                                                               | Commenti                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ consentire all' \_ utente \_ MANAGEFORMS**                                | Windows XP con Service Pack 2 (SP2) e versioni successive<br/> Windows Server 2003 con Service Pack 1 (SP1) e versioni successive<br/>                                                                                                    |
| **\_bip SPLREG \_ abilitato**                                           |                                                                                                                                                                                                                                 |
| **SPLREG \_ directory predefinita dello \_ spooling \_**                               |                                                                                                                                                                                                                                 |
| **\_registro eventi di SPLREG \_**                                              |                                                                                                                                                                                                                                 |
| **\_popup NET \_ SPLREG**                                              | Non supportato in Windows Server 2003 e versioni successive<br/>                                                                                                                                                                       |
| **\_ \_ \_ impostazione predefinita priorità thread porta SPLREG \_**                         |                                                                                                                                                                                                                                 |
| **\_ \_ priorità thread della porta SPLREG \_**                                  |                                                                                                                                                                                                                                 |
| **\_gruppi di \_ isolamento del driver di stampa SPLREG \_ \_**                        | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **SPLREG \_ tempo di isolamento del driver di stampa \_ prima del \_ \_ \_ \_ riciclo**         | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **\_numero massimo di oggetti di isolamento del driver di stampa SPLREG \_ \_ prima del \_ \_ \_ \_ riciclo** | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **\_timeout di \_ \_ \_ inattività isolamento driver di \_ stampa SPLREG**                 | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **\_criteri di \_ \_ esecuzione isolamento \_ driver \_ di stampa SPLREG**             | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **\_criteri di \_ \_ sostituzione isolamento \_ driver \_ di stampa SPLREG**              | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **\_popup nuovo tentativo SPLREG \_**                                            | In caso di esito positivo, *pData* contiene 1 se il server è impostato per ritentare le finestre popup per tutti i processi oppure 0 se il server non ritenta le finestre popup per tutti i processi.<br/> Non supportato in Windows Server 2003 e versioni successive<br/> |
| **\_priorità thread dell'utilità di pianificazione SPLREG \_ \_**                             |                                                                                                                                                                                                                                 |
| **\_ \_ \_ impostazione predefinita priorità thread dell'utilità di pianificazione SPLREG \_**                    |                                                                                                                                                                                                                                 |
| **\_WEBSHAREMGMT SPLREG**                                            | Windows Server 2003 e versioni successive<br/>                                                                                                                                                                                        |



 

I valori seguenti di *pValueName* determinano il comportamento di stampa del pool quando si verifica un errore.



| valore                                       | Commenti                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ errore di riavvio del processo di SPLREG nel \_ pool \_**   | Il valore di *pData* indica il tempo, in secondi, in cui un processo viene riavviato in un'altra porta dopo che si è verificato un errore. Questa impostazione viene usata con **\_ \_ il processo di riavvio del SPLREG \_ nel \_ pool \_ abilitato**.<br/> |
| **SPLREG \_ riavvio \_ \_ del processo nel \_ pool \_ abilitato** | Un valore diverso da zero in *pData* indica che è abilitato il **processo di riavvio SPLREG \_ \_ \_ sull' \_ \_ errore del pool** .<br/>                                                                                            |



 

Il tempo specificato nel **processo di riavvio del SPLREG \_ \_ per l' \_ \_ \_ errore del pool** è minimo. Il tempo effettivo può essere più lungo, a seconda delle impostazioni di monitoraggio porta seguenti, che sono valori del registro di sistema in questa chiave del registro di sistema:

**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *MonitorName* > \\ porte**

Chiamare la funzione [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) per impostare questi valori.



| Impostazione di monitoraggio porta     | Tipo di dati      | Significato                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG \_ DWORD** | Se un valore diverso da zero, Abilita il monitoraggio della porta per aggiornare lo spooler con lo stato della porta.<br/>            |
| **StatusUpdateInterval** | **REG \_ DWORD** | Specifica l'intervallo, in minuti, quando il monitoraggio porta aggiorna lo spooler con lo stato della porta.<br/> |



 

In Windows 7 e versioni successive di Windows, per impostazione predefinita viene eseguito il rendering dei processi di stampa inviati a un server di stampa nel client. Il rendering lato client di un processo di stampa può essere configurato per ogni stampante impostando i valori seguenti in *pValueName*.



| Impostazione                      | Tipo di dati      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | Il valore 0, o se questo valore non è presente nel registro di sistema, Abilita il rendering predefinito lato client dei processi di stampa.<br/> Il valore 1 disabilita il rendering lato client dei processi di stampa.<br/>                                                                                                                                                                                                      |
| **ForceClientSideRendering** | **REG \_ DWORD** | Il valore 0, o se questo valore non è presente nel registro di sistema, causa il rendering dei processi di stampa nel client. Se non è possibile eseguire il rendering di un processo di stampa sul client, ne verrà eseguito il rendering nel server. Se non è possibile eseguire il rendering di un processo di stampa sul server, l'operazione avrà esito negativo.<br/> Il valore 1 eseguirà il rendering dei processi di stampa nel client. Se non è possibile eseguire il rendering di un processo di stampa sul client, l'operazione avrà esito negativo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **SetPrinterDataW** (Unicode) e **SetPrinterDataA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

