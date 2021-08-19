---
description: La funzione OpenPrinter recupera un handle per la stampante o il server di stampa specificato o altri tipi di handle nel sottosistema di stampa.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: Funzione OpenPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 48f25f9c8aec314b997a4600335e22bea2f0bbd8eefa78235ddbb25192f556f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868603"
---
# <a name="openprinter-function"></a>Funzione OpenPrinter

La **funzione OpenPrinter** recupera un handle per la stampante o il server di stampa specificato o altri tipi di handle nel sottosistema di stampa.

## <a name="syntax"></a>Sintassi


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPrinterName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome della stampante o del server di stampa, l'oggetto stampante, XcvMonitor o XcvPort.

Per un oggetto stampante usare: PrinterName, Job xxxx. Per un oggetto XcvMonitor, usare: ServerName, XcvMonitor MonitorName. Per un oggetto XcvPort, usare: ServerName, XcvPort PortName.

Se **NULL,** indica il server di stampa locale.

</dd> <dt>

*phPrinter* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve un handle (non thread-safe) per la stampante aperta o l'oggetto server di stampa.

Il *parametro phPrinter* può restituire un handle Xcv da usare con la funzione XcvData. Per altre informazioni su XcvData, vedere DDK.

</dd> <dt>

*pDefault* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura PRINTER \_ DEFAULTS.**](printer-defaults.md) Questo valore può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Non chiamare questo metodo in [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Un handle ottenuto per una stampante remota da una chiamata a **OpenPrinter** per una stampante remota accede alla stampante tramite una cache locale nel servizio spooler di stampa. Questa cache non è accurata in tempo reale. Per ottenere dati accurati, sostituire la chiamata OpenPrinter con [**OpenPrinter2**](openprinter2.md) con pOptions.dwFlags impostato su PRINTER \_ OPTION NO \_ \_ CACHE. Si noti che solo OpenPrinter2W è funzionale. La funzione restituisce un handle della stampante che usa altre chiamate all'API di stampa e ignora la cache locale. Questo metodo si blocca durante l'attesa della comunicazione di rete con la stampante remota, pertanto potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. Chiamando questa funzione da un thread che gestisce l'interazione dell'interfaccia utente, l'applicazione potrebbe non rispondere.

 

> [!Note]  
> Un handle ottenuto da una chiamata a **OpenPrinter** per una stampante remota accederà alla stampante tramite una cache locale nel servizio spooler di stampa. Per impostazione predefinita, questa cache non è accurata in tempo reale. Se è necessario ottenere dati accurati, sostituire la chiamata **OpenPrinter** con [**OpenPrinter2**](openprinter2.md) con *pOptions.dwFlags* impostato su [**PRINTER OPTION NO \_ \_ \_ CACHE**](printer-options.md). Si noti che **solo OpenPrinter2W** è funzionale. In questo modo la funzione restituisce un handle della stampante che esegue altre chiamate all'API di stampa per ignorare la cache locale. Si noti che questo approccio si blocca durante l'attesa della comunicazione di rete round trip con la stampante remota, quindi potrebbe non restituire immediatamente. La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e l'implementazione del driver della stampante, fattori difficili da prevedere durante la scrittura di un'applicazione. Pertanto, chiamando questa funzione da un thread che gestisce l'interazione con l'interfaccia utente, l'applicazione potrebbe non rispondere.

 

L'handle a cui punta *phPrinter* non è thread-safe. Se i chiamanti devono usarlo contemporaneamente su più thread, devono fornire l'accesso di sincronizzazione personalizzato all'handle della stampante usando le funzioni [di sincronizzazione](/windows/desktop/Sync/synchronization-functions). Per evitare di scrivere codice personalizzato, l'applicazione può aprire un handle della stampante in ogni thread, in base alle esigenze.

Il *parametro pDefault* consente di specificare il tipo di dati e i valori della modalità dispositivo usati per la stampa di documenti inviati dalla [**funzione StartDocPrinter.**](startdocprinter.md) È tuttavia possibile eseguire l'override di questi valori usando la [**funzione SetJob**](setjob.md) dopo l'avvio di un documento.

Le impostazioni [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) definite nella struttura [**PRINTER \_ DEFAULTS**](printer-defaults.md) del parametro *pDefault* non vengono usate quando il valore del membro *pDatatype* della struttura [**DOC INFO \_ \_ 1**](doc-info-1.md) passato nel *parametro pDocInfo* della [**chiamata StartDocPrinter**](startdocprinter.md) è "RAW". Quando un documento di alto livello (ad esempio un file Adobe PDF o Microsoft Word) o altri dati della stampante (ad esempio PCL, PS o HPGL) viene inviato direttamente a una stampante con *pDatatype* impostato su "RAW", il documento deve descrivere completamente le impostazioni del processo di stampa in stile **DEVMODE** nella lingua compresa dall'hardware.

È possibile chiamare la **funzione OpenPrinter** per aprire un handle per un server di stampa o per determinare i diritti di accesso di un client a un server di stampa. A tale scopo, specificare il nome del server di stampa nel *parametro pPrinterName,* impostare i membri **pDatatype** e **pDevMode** della struttura [**PRINTER \_ DEFAULTS**](printer-defaults.md) su **NULL** e impostare il membro **DesiredAccess** per specificare un valore della maschera di accesso al server, ad esempio SERVER \_ ALL \_ ACCESS. Al termine dell'operazione, passarlo alla [**funzione ClosePrinter**](closeprinter.md) per chiuderlo.

Usare il **membro DesiredAccess** della struttura [**PRINTER \_ DEFAULTS**](printer-defaults.md) per specificare i diritti di accesso necessari per la stampante. I diritti di accesso possono essere uno dei seguenti. Se *pDefault è* **NULL,** i diritti di accesso sono PRINTER \_ ACCESS \_ USE.)



| Valore di Accesso desiderato                        | Significato                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AMMINISTRAZIONE \_ DELL'ACCESSO ALLA \_ STAMPANTE                 | Per eseguire attività amministrative, ad esempio quelle fornite da [**SetPrinter**](setprinter.md).                                                                                                 |
| USO \_ DELL'ACCESSO ALLA \_ STAMPANTE                        | Per eseguire operazioni di stampa di base.                                                                                                                                                        |
| ACCESSO A PRINTER \_ ALL \_                        | Per eseguire tutte le attività amministrative e le operazioni di stampa di base ad eccezione di SYNCHRONIZE (vedere [Diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights).                                     |
| GESTIONE LIMITATA \_ \_ DELL'ACCESSO ALLA \_ STAMPANTE            | Per eseguire attività amministrative, ad esempio quelle fornite da [**SetPrinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md). Questo valore è disponibile a partire da Windows 8.1. |
| valori di sicurezza generici, ad esempio l'applicazione livello dati WRITE \_ | Per consentire diritti di accesso di controllo specifici. Vedere [Diritti di accesso standard.](/windows/desktop/SecAuthZ/standard-access-rights)                                                                                      |



 

Se un utente non dispone dell'autorizzazione per aprire una stampante o un server di stampa specificato con l'accesso desiderato, la chiamata **OpenPrinter** avrà esito negativo con un valore restituito pari a zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il valore ERROR \_ ACCESS \_ DENIED.

## <a name="examples"></a>Esempio

Per un programma di esempio che usa questa funzione, vedere [Procedura: Stampare usando l'API di stampa GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **OpenPrinterW** (Unicode) e **OpenPrinterA** (ANSI)<br/>                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**IMPOSTAZIONI \_ PREDEFINITE DELLA STAMPANTE**](printer-defaults.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

