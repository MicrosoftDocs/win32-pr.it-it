---
description: Ogni origine evento deve registrare i file di messaggio contenenti stringhe di descrizione per ogni identificatore di evento, categoria di eventi e parametro.
ms.assetid: 0c251a45-1414-4855-a6f5-86ebdfab2693
title: File di messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44de0c91a098ab1b916a73d99a02d0d31a8b5b7690936322166e65baef4bd13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951410"
---
# <a name="message-files"></a>File di messaggio

Ogni [origine evento deve](event-sources.md) registrare file di messaggio contenenti stringhe di descrizione per ogni [identificatore](event-identifiers.md)di evento, categoria [di eventi](event-categories.md)e [parametro](event-identifiers.md). Registrare questi file nei valori del Registro di sistema **EventMessageFile**, **CategoryMessageFile** e **ParameterMessageFile** per l'origine evento.

È possibile creare un file di messaggio contenente descrizioni per gli identificatori di evento, le categorie e i parametri oppure creare tre file di messaggio separati. Gli identificatori di messaggio per tutti i messaggi devono essere univoci indipendentemente dal fatto che si specificano i messaggi in uno o tre file. Diverse applicazioni possono condividere lo stesso file di messaggio. Per altre informazioni sui file di messaggio, vedere [**Message Compiler.**](/windows/desktop/WES/message-compiler--mc-exe-) Per informazioni dettagliate sulla sintassi di un file di messaggio, vedere [File di testo dei messaggi.](message-text-files.md)

## <a name="example-message-file"></a>File di messaggio di esempio

Di seguito è riportato un file di messaggio di esempio.

``` syntax
; /* --------------------------------------------------------
; HEADER SECTION
;*/
SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
               Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
               Warning=0x2:STATUS_SEVERITY_WARNING
               Error=0x3:STATUS_SEVERITY_ERROR
              )
;
;
FacilityNames=(System=0x0:FACILITY_SYSTEM
               Runtime=0x2:FACILITY_RUNTIME
               Stubs=0x3:FACILITY_STUBS
               Io=0x4:FACILITY_IO_ERROR_CODE
              )
;
;/* ------------------------------------------------------------------
; MESSAGE DEFINITION SECTION
;*/

MessageIdTypedef=WORD

MessageId=0x1
SymbolicName=CAT_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CAT_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CAT_3
Language=English
Category 3
.

MessageIdTypedef=DWORD

MessageId=0x100
Severity=Error
Facility=Runtime
SymbolicName=MSG_COMMAND_ERR
Language=English
The command is incorrect. 
.

MessageId=0x101
Severity=Success
Facility=System
SymbolicName=MSG_STRIKE_ANY_KEY
Language=English
Press any key to continue . . . %0
.

MessageId=0x102
Severity=Error
Facility=System
SymbolicName=MSG_FILE_BAD_CONTENTS
Language=English
File %1 contains %2, which is in error
.

MessageId=0x103
Severity=Warning
Facility=System
SymbolicName=MSG_RETRYS
Language=English
There have been %1 retrys with %2 success! Disconnect from
the server and retry later.
.

MessageId=0x104
Severity=Informational
Facility=System
SymbolicName=MSG_INSERT_DISK
Language=English
Insert %%1000 in %%1001 and hit any key when ready... 
.

;/* Insert string parameters */
;

MessageId=1000
Severity=Success
Facility=System
SymbolicName=DISK
Language=English
disk%0
.

MessageId=1001
Severity=Success
Facility=System
SymbolicName=DRIVE
Language=English
drive%0
.
```

L'applicazione di visualizzazione degli eventi può utilizzare la procedura seguente per ottenere l'accesso alle stringhe [di messaggio](event-identifiers.md) nella DLL del messaggio.

**Per ottenere stringhe di descrizione**

1.  Chiamare la [**funzione RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) per aprire l'origine evento.
2.  Chiamare la [**funzione RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) per ottenere il contenuto del valore **EventMessageFile** per l'origine evento, ovvero il nome della DLL del messaggio.
3.  Chiamare la [**funzione LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) per caricare la DLL del messaggio determinata dal passaggio 2.
4.  Chiamare la [**funzione FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) con l'identificatore del messaggio per ottenere la descrizione dalla DLL. Si noti che gli identificatori dei messaggi sono definiti in . File H generato dal compilatore di messaggi. La **funzione FormatMessage** sostituirà le stringhe di inserimento usando i valori degli argomenti passati, ma non sostituirà le stringhe di inserimento dei parametri. È necessario sostituire manualmente le stringhe di inserimento dei parametri prima di visualizzare la stringa.

 

 
