---
description: La funzione OpenPrinter recupera un handle per la stampante o il server di stampa specificato o per altri tipi di handle nel sottosistema di stampa.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: Funzione OpenPrinter (winspool. h)
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
ms.openlocfilehash: 02cd6f6b5d56eec525bd00e2feef50f4d5f07734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313023"
---
# <a name="openprinter-function"></a>OpenPrinter (funzione)

La funzione **OpenPrinter** recupera un handle per la stampante o il server di stampa specificato o per altri tipi di handle nel sottosistema di stampa.

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

*pPrinterName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome della stampante o del server di stampa, l'oggetto Printer, XcvMonitor o XcvPort.

Per un oggetto Printer, utilizzare: PrinterName, job xxxx. Per un XcvMonitor, usare: ServerName, XcvMonitor MonitorName. Per un XcvPort, usare: ServerName, XcvPort Portaname.

Se è **null**, indica il server di stampa locale.

</dd> <dt>

*phPrinter* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve un handle (non thread-safe) per l'oggetto della stampante o del server di stampa aperto.

Il parametro *phPrinter* può restituire un handle XCV per l'utilizzo con la funzione XcvData. Per ulteriori informazioni su XcvData, vedere DDK.

</dd> <dt>

*pDefault* \[ in\]
</dt> <dd>

Un puntatore a una struttura di [**\_ impostazioni predefinite della stampante**](printer-defaults.md) . Questo valore può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Non chiamare questo metodo in [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Un handle ottenuto per una stampante remota mediante una chiamata a **OpenPrinter** per una stampante remota accede alla stampante tramite una cache locale nel servizio spooler di stampa. Questa cache non è precisa in tempo reale. Per ottenere dati accurati, sostituire la chiamata OpenPrinter con [**OpenPrinter2**](openprinter2.md) con POptions. dwFlags impostato sull' \_ opzione Printer \_ No \_ cache. Si noti che solo OpenPrinter2W è funzionante. La funzione restituisce un handle della stampante che usa altre chiamate API di stampa e ignora la cache locale. Questo metodo si blocca durante l'attesa della comunicazione di rete con la stampante remota, quindi potrebbe non essere restituito immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione dell'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

> [!Note]  
> Un handle ottenuto da una chiamata a **OpenPrinter** per una stampante remota effettuerà l'accesso alla stampante tramite una cache locale nel servizio spooler di stampa. Questa cache è, in base alla progettazione, non accurata in tempo reale. Se è necessario ottenere dati accurati, sostituire la chiamata **OpenPrinter** con [**OpenPrinter2**](openprinter2.md) con *pOptions. dwFlags* impostato sull' [**\_ opzione Printer \_ No \_ cache**](printer-options.md). Si noti che solo **OpenPrinter2W** è funzionante. In questo modo la funzione restituisce un handle della stampante che esegue altre chiamate API di stampa per ignorare la cache locale. Si noti che questo approccio si bloccherà durante l'attesa della comunicazione di rete di andata e ritorno alla stampante remota, quindi potrebbe non essere immediatamente reimpostata. La velocità con cui questa funzione restituisce dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e l'implementazione di driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe quindi far sembrare che l'applicazione non risponda.

 

L'handle a cui fa riferimento *phPrinter* non è thread-safe. Se i chiamanti devono utilizzarlo contemporaneamente su più thread, devono fornire l'accesso di sincronizzazione personalizzato all'handle della stampante utilizzando le [funzioni di sincronizzazione](/windows/desktop/Sync/synchronization-functions). Per evitare di scrivere codice personalizzato, l'applicazione può aprire un handle della stampante in ogni thread, in base alle esigenze.

Il parametro *pDefault* consente di specificare il tipo di dati e i valori della modalità dispositivo usati per la stampa dei documenti inviati dalla funzione [**StartDocPrinter**](startdocprinter.md) . È tuttavia possibile eseguire l'override di questi valori utilizzando la funzione [**SetJob**](setjob.md) dopo l'avvio di un documento.

Le [**Impostazioni DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) definite nella struttura delle impostazioni [**\_ predefinite della stampante**](printer-defaults.md) del parametro *pDefault* non vengono utilizzate quando il valore del membro *pDatatype* della struttura [**doc \_ info \_ 1**](doc-info-1.md) passato nel parametro *pDocInfo* della chiamata [**StartDocPrinter**](startdocprinter.md) è "Raw". Quando un documento di alto livello (ad esempio un file Adobe PDF o Microsoft Word) o altri dati della stampante (ad esempio, PCL, PS o HPGL) vengono inviati direttamente a una stampante con *pDatatype* impostato su "Raw", il documento deve descrivere completamente le impostazioni del processo di stampa in stile **DEVMODE** nella lingua compresa nell'hardware.

È possibile chiamare la funzione **OpenPrinter** per aprire un handle per un server di stampa o per determinare i diritti di accesso di un client a un server di stampa. A tale scopo, specificare il nome del server di stampa nel parametro *pPrinterName* , impostare i membri **pDatatype** e **pDevMode** della struttura [**Printer \_ defaults**](printer-defaults.md) su **null** e impostare il membro **desiredAccess** per specificare un valore della maschera di accesso al server, ad esempio server \_ All \_ Access. Al termine dell'handle, passarlo alla funzione [**ClosePrinter**](closeprinter.md) per chiuderla.

Utilizzare il membro **desiredAccess** della struttura [**Printer \_ defaults**](printer-defaults.md) per specificare i diritti di accesso necessari per la stampante. I diritti di accesso possono essere uno dei seguenti. Se *pDefault* è **null**, i diritti di accesso sono Printer \_ usare l'accesso \_ .)



| Valore di accesso desiderato                        | Significato                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_amministrazione dell'accesso alla stampante \_                 | Per eseguire attività amministrative, ad esempio quelle fornite da [**Seprinter**](setprinter.md).                                                                                                 |
| \_uso dell'accesso alla stampante \_                        | Per eseguire operazioni di stampa di base.                                                                                                                                                        |
| \_tutti gli \_ accessi alla stampante                        | Per eseguire tutte le attività amministrative e le operazioni di stampa di base, ad eccezione della sincronizzazione (vedere [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights).                                     |
| \_gestione dell'accesso alla stampante \_ \_ limitata            | Per eseguire attività amministrative, ad esempio quelle fornite da [**Seprinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md). Questo valore è disponibile a partire da Windows 8.1. |
| valori di sicurezza generici, ad esempio WRITE \_ DAC | Per consentire diritti di accesso di controllo specifici. Vedere [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

Se un utente non dispone dell'autorizzazione per aprire una stampante o un server di stampa specificato con l'accesso desiderato, la chiamata a **OpenPrinter** avrà esito negativo con un valore restituito pari a zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il valore Error \_ Access \_ negato.

## <a name="examples"></a>Esempio

Per un programma di esempio che usa questa funzione, vedere [procedura: stampare con l'API di stampa GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
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

[**\_impostazioni predefinite stampanti**](printer-defaults.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

