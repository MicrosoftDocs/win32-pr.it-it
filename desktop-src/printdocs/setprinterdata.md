---
description: La funzione SetPrinterData imposta i dati di configurazione per una stampante o un server di stampa.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: Funzione SetPrinterData (Winspool.h)
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
ms.openlocfilehash: 7b28c61030271b9de2e946fd59cddf5253a80cd4faec40ee66ceb2ae6cefdce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233950"
---
# <a name="setprinterdata-function"></a>Funzione SetPrinterData

La **funzione SetPrinterData** imposta i dati di configurazione per una stampante o un server di stampa.

Per specificare la chiave del Registro di sistema in cui archiviare i dati, chiamare la [**funzione SetPrinterDataEx.**](setprinterdataex.md) Chiamare **SetPrinterData** equivale a chiamare la **funzione SetPrinterDataEx** con il parametro *pKeyName* impostato su "PrinterDriverData".

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

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante o il server di stampa per il quale la funzione imposta i dati di configurazione. Usare la [**funzione OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*pValueName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica i dati da impostare.

Per le stampanti, questa stringa è il nome di un valore del Registro di sistema nella chiave "PrinterDriverData" della stampante nel Registro di sistema.

Per i server di stampa, questa stringa è una delle stringhe predefinite elencate nella sezione Osservazioni seguente.

</dd> <dt>

*Tipo* \[ Pollici\]
</dt> <dd>

Codice che indica il tipo di dati a cui punta *il parametro pData.* Per un elenco dei codici di tipo possibili, vedere Tipi [di valori del Registro di sistema.](/windows/desktop/SysInfo/registry-value-types)

</dd> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di byte che contiene i dati di configurazione della stampante.

</dd> <dt>

*cbData* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, della matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **ERROR \_ SUCCESS**.

Se la funzione ha esito negativo, il valore restituito è un valore di errore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Per recuperare i dati di configurazione esistenti per una stampante, chiamare la [**funzione GetPrinterDataEx**](getprinterdataex.md) o [**GetPrinterData.**](getprinterdata.md)

Se *hPrinter è* un handle per un server di stampa, *pValueName* può specificare uno dei valori predefiniti seguenti.



| valore                                                               | Commenti                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ ALLOW \_ USER \_ MANAGEFORMS**                                | Windows XP con Service Pack 2 (SP2) e versioni successive<br/> Windows Server 2003 con Service Pack 1 (SP1) e versioni successive<br/>                                                                                                    |
| **SPLREG \_ BEEP \_ ENABLED**                                           |                                                                                                                                                                                                                                 |
| **\_DIRECTORY SPOOL PREDEFINITA \_ SPLREG \_**                               |                                                                                                                                                                                                                                 |
| **REGISTRO EVENTI \_ SPLREG \_**                                              |                                                                                                                                                                                                                                 |
| **SPLREG \_ NET \_ POPUP**                                              | Non supportato in Windows Server 2003 e versioni successive<br/>                                                                                                                                                                       |
| **IMPOSTAZIONE PREDEFINITA PRIORITÀ THREAD PORTA SPLREG \_ \_ \_ \_**                         |                                                                                                                                                                                                                                 |
| **PRIORITÀ THREAD PORTA SPLREG \_ \_ \_**                                  |                                                                                                                                                                                                                                 |
| **GRUPPI DI ISOLAMENTO DEI DRIVER DI STAMPA SPLREG \_ \_ \_ \_**                        | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **TEMPO DI ISOLAMENTO DEL DRIVER DI STAMPA SPLREG \_ \_ PRIMA DEL \_ \_ \_ \_ RICICLO**         | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **NUMERO MASSIMO DI OGGETTI DI ISOLAMENTO DEL DRIVER DI STAMPA SPLREG \_ \_ PRIMA DEL \_ \_ \_ \_ \_ RICICLO** | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **TIMEOUT DI INATTIVITÀ ISOLAMENTO \_ \_ DRIVER DI \_ STAMPA \_ \_ SPLREG**                 | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **CRITERI DI ESECUZIONE DELL'ISOLAMENTO \_ \_ DEL DRIVER \_ DI \_ \_ STAMPA SPLREG**             | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **CRITERI DI SOSTITUZIONE \_ DELL'ISOLAMENTO DEL DRIVER DI \_ \_ STAMPA \_ \_ SPLREG**              | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **POPUP DI RIPETIZIONE \_ DEI TENTATIVI SPLREG \_**                                            | In caso di esito positivo, *pData* contiene 1 se il server è impostato per ripetere i tentativi di finestre popup per tutti i processi oppure 0 se il server non ritenta la ripetizione delle finestre popup per tutti i processi.<br/> Non supportato in Windows Server 2003 e versioni successive<br/> |
| **PRIORITÀ THREAD UTILITÀ DI PIANIFICAZIONE SPLREG \_ \_ \_**                             |                                                                                                                                                                                                                                 |
| **IMPOSTAZIONE PREDEFINITA PRIORITÀ \_ THREAD UTILITÀ \_ DI \_ PIANIFICAZIONE \_ SPLREG**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows Server 2003 e versioni successive<br/>                                                                                                                                                                                        |



 

I valori seguenti di *pValueName determinano* il comportamento di stampa del pool quando si verifica un errore.



| valore                                       | Commenti                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ERRORE DI RIAVVIO DEL PROCESSO SPLREG \_ \_ NEL \_ \_ \_ POOL**   | Il valore *di pData* indica il tempo, in secondi, in cui un processo viene riavviato su un'altra porta dopo che si è verificato un errore. Questa impostazione viene usata con **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ENABLED**.<br/> |
| **SPLREG \_ RESTART JOB ON POOL ENABLED (RIAVVIO SPLREG \_ PROCESSO NEL POOL \_ \_ \_ ABILITATO)** | Un valore diverso da zero in *pData* indica che **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ERROR** è abilitato.<br/>                                                                                            |



 

Il tempo specificato in **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ERROR** è un tempo minimo. Il tempo effettivo può essere più lungo, a seconda delle impostazioni di monitoraggio delle porte seguenti, che sono valori del Registro di sistema in questa chiave del Registro di sistema:

**Controllo HKLM \\ SYSTEM \\ CurrentControlSet \\ Monitor \\ \\ monitora \\ < *monitoraggiNome* > \\ porte**

Chiamare la [**funzione RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) per impostare questi valori.



| Impostazione del monitoraggio delle porte     | Tipo di dati      | Significato                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG \_ DWORD** | Se un valore diverso da zero, consente al monitoraggio delle porte di aggiornare lo spooler con lo stato della porta.<br/>            |
| **StatusUpdateInterval** | **REG \_ DWORD** | Specifica l'intervallo, in minuti, in cui il monitoraggio delle porte aggiorna lo spooler con lo stato della porta.<br/> |



 

In Windows 7 e versioni successive di Windows, il rendering dei processi di stampa inviati a un server di stampa viene eseguito sul client per impostazione predefinita. Il rendering lato client di un processo di stampa può essere configurato per ogni stampante impostando i valori seguenti in *pValueName*.



| Impostazione                      | Tipo di dati      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | Il valore 0, o se questo valore non è presente nel Registro di sistema, abilita il rendering lato client predefinito dei processi di stampa.<br/> Il valore 1 disabilita il rendering lato client dei processi di stampa.<br/>                                                                                                                                                                                                      |
| **ForceClientSideRendering** | **REG \_ DWORD** | Il valore 0, o se questo valore non è presente nel Registro di sistema, determina il rendering dei processi di stampa nel client. Se non è possibile eseguire il rendering di un processo di stampa nel client, ne verrà eseguito il rendering nel server. Se non è possibile eseguire il rendering di un processo di stampa nel server, l'esecuzione avrà esito negativo.<br/> Il valore 1 eseguirà il rendering dei processi di stampa nel client. Se non è possibile eseguire il rendering di un processo di stampa nel client, l'esecuzione avrà esito negativo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
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

 

