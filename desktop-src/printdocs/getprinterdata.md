---
description: La funzione GetPrinterData recupera i dati di configurazione per la stampante o il server di stampa specificato.
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: Funzione GetPrinterData (Winspool.h)
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
ms.openlocfilehash: d4cf7d1d1b668974f792c6535f1667f127c78541f4786b32201209553e452c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948791"
---
# <a name="getprinterdata-function"></a>Funzione GetPrinterData

La **funzione GetPrinterData** recupera i dati di configurazione per la stampante o il server di stampa specificato.

In Windows 2000 e versioni successive di Windows, chiamare **GetPrinterData** equivale a chiamare [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) con il *parametro pKeyName* impostato su "PrinterDriverData".

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

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante o il server di stampa per cui la funzione recupera i dati di configurazione. Usare la [**funzione OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*pValueName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica i dati da recuperare.

Per le stampanti, questa stringa è il nome di un valore del Registro di sistema nella chiave "PrinterDriverData" della stampante nel Registro di sistema.

Per i server di stampa, questa stringa è una delle stringhe predefinite elencate nella sezione Osservazioni seguente.

</dd> <dt>

*pType* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve un valore che indica il tipo di dati recuperati in *pData*. La funzione restituisce il tipo specificato nella [**chiamata SetPrinterData**](setprinterdata.md) o [**SetPrinterDataEx**](setprinterdataex.md) che ha archiviato i dati. Impostare questo parametro **su NULL** se il tipo di dati non è necessario.

</dd> <dt>

*pData* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve i dati di configurazione.

</dd> <dt>

*nSize* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer a cui *punta pData.*

</dd> <dt>

*pcbNeeded* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati di configurazione. Se le dimensioni del buffer specificate da *nSize* sono troppo piccole, la funzione restituisce **ERROR MORE \_ \_ DATA** e *pcbNeeded* indica le dimensioni del buffer richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **ERROR \_ SUCCESS**. Se la funzione ha esito negativo, il valore restituito è un valore di errore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

**GetPrinterData** recupera i dati di configurazione della stampante impostati dalla [**funzione SetPrinterDataEx**](setprinterdataex.md) o [**SetPrinterData.**](setprinterdata.md)

**GetPrinterData potrebbe** attivare una Windows chiamata a [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), che potrebbe scrivere nel Registro di sistema. In caso contrario, possono verificarsi effetti collaterali, ad esempio l'attivazione di un aggiornamento o l'aggiornamento dell'ID evento della stampante 20 nel client, se la stampante è condivisa in una rete.

Se *hPrinter* è un handle per un server di stampa, *pValueName* può specificare uno dei valori predefiniti seguenti.



| valore                                                               | Commenti                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ ALLOW \_ USER \_ MANAGEFORMS**                                | Windows XP con Service Pack 2 (SP2) e versioni successive<br/> Windows Server 2003 con Service Pack 1 (SP1) e versioni successive<br/>                                                                                                    |
| **ARCHITETTURA \_ SPLREG**                                            |                                                                                                                                                                                                                                 |
| **SEGNALE ACUSTICO SPLREG \_ \_ ABILITATO**                                           |                                                                                                                                                                                                                                 |
| **\_ \_ DIRECTORY SPOOL PREDEFINITA SPLREG \_**                               |                                                                                                                                                                                                                                 |
| **NOME COMPUTER \_ DNS \_ SPLREG \_**                                      |                                                                                                                                                                                                                                 |
| **SPLREG \_ DS \_ PRESENT**                                             | In caso di esito positivo, *pData* contiene 0x0001 se il computer si trova in un dominio DS, 0 in caso contrario.<br/>                                                                                                                         |
| **SPLREG \_ DS \_ PRESENTE PER \_ \_ L'UTENTE**                                  | In caso di esito positivo, *pData* contiene 0x0001 se l'utente è connesso a un dominio DS, 0 in caso contrario.<br/>                                                                                                                   |
| **REGISTRO EVENTI \_ \_ SPLREG**                                              |                                                                                                                                                                                                                                 |
| **VERSIONE PRINCIPALE DI \_ \_ SPLREG**                                          |                                                                                                                                                                                                                                 |
| **VERSIONE SECONDARIA DI \_ \_ SPLREG**                                          |                                                                                                                                                                                                                                 |
| **POPUP DI RETE SPLREG \_ \_**                                              | Non supportato in Windows Server 2003 e versioni successive<br/>                                                                                                                                                                       |
| **POPUP DI RETE SPLREG \_ \_ AL \_ \_ COMPUTER**                                | In caso di esito positivo, *pData* contiene 1 se le notifiche del processo devono essere inviate al computer client oppure 0 se le notifiche del processo devono essere inviate all'utente.<br/> Non supportato in Windows Server 2003 e versioni successive<br/> |
| **VERSIONE DEL SISTEMA \_ OPERATIVO SPLREG \_**                                             | Windows XP e versioni successive<br/>                                                                                                                                                                                                 |
| **SPLREG \_ OS \_ VERSIONEX**                                           |                                                                                                                                                                                                                                 |
| **IMPOSTAZIONE PREDEFINITA PRIORITÀ THREAD PORTA SPLREG \_ \_ \_ \_**                         |                                                                                                                                                                                                                                 |
| **PRIORITÀ DEL THREAD DELLA PORTA SPLREG \_ \_ \_**                                  |                                                                                                                                                                                                                                 |
| **GRUPPI DI ISOLAMENTO DEL DRIVER DI STAMPA SPLREG \_ \_ \_ \_**                        | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **TEMPO DI ISOLAMENTO DEL DRIVER DI STAMPA SPLREG \_ \_ PRIMA DEL \_ \_ \_ \_ RICICLO**         | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **SPLREG PRINT DRIVER ISOLATION MAX OBJECTS BEFORE RECYCLE (NUMERO MASSIMO DI OGGETTI DI ISOLAMENTO DEL DRIVER DI STAMPA SPLREG \_ \_ PRIMA DEL \_ \_ \_ \_ \_ RICICLO)** | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **TIMEOUT DI INATTIVITÀ ISOLAMENTO DRIVER DI \_ \_ \_ \_ \_ STAMPA SPLREG**                 | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **CRITERI DI ESECUZIONE DELL'ISOLAMENTO \_ \_ DEL DRIVER DI \_ \_ \_ STAMPA SPLREG**             | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **CRITERI DI OVERRIDE DELL'ISOLAMENTO DEL DRIVER DI \_ \_ \_ \_ \_ STAMPA SPLREG**              | Windows 7 e versioni successive<br/>                                                                                                                                                                                                  |
| **SPLREG \_ REMOTE \_ FAX**                                             | In caso di esito positivo, *pData* contiene 0x0001 se il servizio FAX supporta i client remoti, 0 in caso contrario.<br/>                                                                                                               |
| **POPUP DI RIPETIZIONE DEI TENTATIVI SPLREG \_ \_**                                            | In caso di esito positivo, *pData* contiene 1 se il server è impostato per ripetere la ripetizione delle finestre popup per tutti i processi oppure 0 se il server non ritenta le finestre popup per tutti i processi.<br/> Non supportato in Windows Server 2003 e versioni successive<br/> |
| **PRIORITÀ DEL THREAD DELL'UTILITÀ DI PIANIFICAZIONE SPLREG \_ \_ \_**                             |                                                                                                                                                                                                                                 |
| **IMPOSTAZIONE PREDEFINITA PRIORITÀ \_ THREAD UTILITÀ \_ DI \_ \_ PIANIFICAZIONE SPLREG**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows Server 2003 e versioni successive<br/>                                                                                                                                                                                        |



 

I valori seguenti di *pValueName indicano* il comportamento di stampa del pool quando si verifica un errore.



| valore                                       | Commenti                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ERRORE DEL PROCESSO DI \_ \_ RIAVVIO SPLREG \_ NEL \_ \_ POOL**   | Il valore *pData* indica il tempo, in secondi, in cui un processo viene riavviato su un'altra porta dopo che si è verificato un errore. Questa impostazione viene usata con **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ENABLED**.<br/> |
| **PROCESSO DI RIAVVIO SPLREG \_ \_ NEL POOL \_ \_ \_ ABILITATO** | Un valore diverso da zero in *pData* indica che **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ERROR** è abilitato.<br/>                                                                                            |



 

Il tempo specificato in **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ERROR** è un tempo minimo. Il tempo effettivo può essere più lungo, a seconda delle impostazioni di monitoraggio delle porte seguenti, che sono valori del Registro di sistema in questa chiave del Registro di sistema:

**HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *MonitorName* > \\ Ports**

Chiamare la [**funzione RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) per eseguire query su questi valori.



| Impostazione di Monitoraggio porte     | Tipo di dati      | Significato                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG \_ DWORD** | Se un valore diverso da zero, consente al monitoraggio delle porte di aggiornare lo spooler con lo stato della porta.<br/>            |
| **StatusUpdateInterval** | **REG \_ DWORD** | Specifica l'intervallo, in minuti, quando il monitoraggio delle porte aggiorna lo spooler con lo stato della porta.<br/> |



 

Per Windows 7 e versioni successive di Windows, il rendering dei processi di stampa inviati a un server di stampa viene eseguito sul client per impostazione predefinita. I valori seguenti configurano il rendering lato client di un processo di stampa e possono essere letti se si impostano i valori seguenti in *pValueName*.



| Impostazione                      | Tipo di dati      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | Il valore 0 o se questo valore non è presente nel Registro di sistema abilita il rendering lato client predefinito dei processi di stampa.<br/> Il valore 1 disabilita il rendering lato client dei processi di stampa.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG \_ DWORD** | Il valore 0 o se questo valore non è presente nel Registro di sistema causerà il rendering dei processi di stampa nel client. Se non è possibile eseguire il rendering di un processo di stampa nel client, ne verrà eseguito il rendering nel server. Se non è possibile eseguire il rendering di un processo di stampa nel server, avrà esito negativo.<br/> Il valore 1 eseguirà il rendering dei processi di stampa nel client. Se non è possibile eseguire il rendering di un processo di stampa nel client, avrà esito negativo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
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

[**Setprinter**](setprinter.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> <dt>

[**PRINTPROCESSOR \_ CAPS \_ 1**](printprocessor-caps-1.md)
</dt> </dl>

 

