---
description: Recupera un handle per la stampante, il server di stampa o altri tipi di handle specificati nel sottosistema di stampa, durante l'impostazione di alcune opzioni della stampante.
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: Funzione OpenPrinter2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter2
- OpenPrinter2A
- OpenPrinter2W
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 46788d7ad810ef623cd77793a72ab6c046b73590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882513"
---
# <a name="openprinter2-function"></a>OpenPrinter2 (funzione)

Recupera un handle per la stampante, il server di stampa o altri tipi di handle specificati nel sottosistema di stampa, durante l'impostazione di alcune opzioni della stampante.

## <a name="syntax"></a>Sintassi


```C++
BOOL OpenPrinter2(
  _In_  LPCTSTR            pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault,
  _In_  PPRINTER_OPTIONS   pOptions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPrinterName* \[ in\]
</dt> <dd>

Puntatore a una stringa costante con terminazione null che specifica il nome della stampante o del server di stampa, l'oggetto Printer, XcvMonitor o XcvPort.

Per un oggetto Printer, utilizzare: PrinterName, job xxxx. Per un XcvMonitor, usare: ServerName, XcvMonitor MonitorName. Per un XcvPort, usare: ServerName, XcvPort Portaname.

**Windows Vista:** Se è **null**, indica il server di stampa locale.

</dd> <dt>

*phPrinter* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve un handle per l'oggetto Open Printer o Print Server.

</dd> <dt>

*pDefault* \[ in\]
</dt> <dd>

Un puntatore a una struttura di [**\_ impostazioni predefinite della stampante**](printer-defaults.md) . Questo valore può essere **null**.

</dd> <dt>

*pOptions* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ Opzioni della stampante**](printer-options.md) . Questo valore può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero. Per informazioni estese sugli errori, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

Non chiamare questo metodo in [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

La versione ANSI di questa funzione non è implementata e restituisce l'errore \_ non \_ supportato.

Il parametro *pDefault* consente di specificare il tipo di dati e i valori della modalità dispositivo usati per la stampa dei documenti inviati dalla funzione [**StartDocPrinter**](startdocprinter.md) . È tuttavia possibile eseguire l'override di questi valori utilizzando la funzione [**SetJob**](setjob.md) dopo l'avvio di un documento.

È possibile chiamare la funzione **OpenPrinter2** per aprire un handle per un server di stampa o per determinare i diritti di accesso client a un server di stampa. A tale scopo, specificare il nome del server di stampa nel parametro *pPrinterName* , impostare i membri **pDatatype** e **pDevMode** della struttura [**Printer \_ defaults**](printer-defaults.md) su **null** e impostare il membro **desiredAccess** per specificare un valore della maschera di accesso al server, ad esempio server \_ All \_ Access. Al termine dell'handle, passarlo alla funzione [**ClosePrinter**](closeprinter.md) per chiuderlo.

Utilizzare il membro **desiredAccess** della struttura [**Printer \_ defaults**](printer-defaults.md) per specificare i diritti di accesso necessari. I diritti di accesso possono essere uno dei seguenti.



| Valore di accesso desiderato                        | Significato                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_amministrazione dell'accesso alla stampante \_                 | Per eseguire attività amministrative, ad esempio quelle fornite da [**Seprinter**](setprinter.md).                                                                                                 |
| \_uso dell'accesso alla stampante \_                        | Per eseguire operazioni di stampa di base.                                                                                                                                                        |
| \_tutti gli \_ accessi alla stampante                        | Per eseguire tutte le attività amministrative e le operazioni di stampa di base, ad eccezione della sincronizzazione. Vedere [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights).                                         |
| \_gestione dell'accesso alla stampante \_ \_ limitata            | Per eseguire attività amministrative, ad esempio quelle fornite da [**Seprinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md). Questo valore è disponibile a partire da Windows 8.1. |
| valori di sicurezza generici, ad esempio WRITE \_ DAC | Per consentire diritti di accesso di controllo specifici. Vedere [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

Se un utente non dispone dell'autorizzazione per aprire una stampante o un server di stampa specificato con l'accesso desiderato, la chiamata a **OpenPrinter2** avrà esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il valore Error \_ Access \_ denied.

Quando *pPrinterName* è una stampante locale, **OpenPrinter2** ignora tutti i valori di **dwFlags** a cui la struttura [**delle \_ Opzioni della stampante**](printer-options.md) ha puntato usando *pOptions*, ad eccezione del client dell' \_ opzione Printer \_ \_ . Se quest'ultimo viene passato, **OpenPrinter2** restituirà un errore di \_ accesso \_ negato. Di conseguenza, quando si apre una stampante locale, **OpenPrinter2** non offre alcun vantaggio rispetto a [**OpenPrinter**](openprinter.md).

**Windows Vista:** I dati della stampante restituiti da **OpenPrinter2** vengono recuperati da una cache locale, a meno che non sia stata impostata l' **\_ opzione stampante nessun flag \_ \_ della cache** nel campo **dwFlags** della struttura delle [**\_ Opzioni stampante**](printer-options.md) a cui fa riferimento *pOptions*.

## <a name="examples"></a>Esempio

In questo esempio, **OpenPrinter2** ha esito negativo quando \_ \_ la gestione dell'accesso alla stampante \_ limitata viene passata alla struttura delle [**\_ impostazioni predefinite della stampante**](printer-defaults.md) e l'utente non dispone dell'autorizzazione appropriata.


```C++
// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L QueueWithNoAdminRights , // Queue name
                     &printer,                  // Printer handle
                     &defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
```



Per un programma di esempio che illustra come usare questa funzione, vedere [procedura: stampare con l'API di stampa GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomi Unicode e ANSI<br/>   | **OpenPrinter2W** (Unicode) e **OpenPrinter2A** (ANSI)<br/>                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**\_impostazioni predefinite stampanti**](printer-defaults.md)
</dt> <dt>

[**\_Opzioni stampante**](printer-options.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

