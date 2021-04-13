---
description: Ogni origine evento deve registrare i file di messaggio contenenti stringhe di descrizione per ogni identificatore evento, categoria di eventi e parametro.
ms.assetid: 0c251a45-1414-4855-a6f5-86ebdfab2693
title: File di messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb20d5919c75f06bfd7b6db9b47216566ab6ac8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528746"
---
# <a name="message-files"></a>File di messaggio

Ogni [origine evento](event-sources.md) deve registrare i file di messaggio contenenti stringhe di descrizione per ogni [identificatore evento](event-identifiers.md), [categoria di eventi](event-categories.md)e [parametro](event-identifiers.md). Registrare questi file nei valori del registro di sistema **EventMessageFile**, **CategoryMessageFile** e **ParameterMessageFile** per l'origine evento.

È possibile creare un file di messaggio contenente le descrizioni per gli identificatori, le categorie e i parametri degli eventi oppure creare tre file di messaggio distinti. Gli identificatori di messaggio per tutti i messaggi devono essere univoci se si specificano i messaggi in un file o in tre file. Diverse applicazioni possono condividere lo stesso file di messaggio. Per ulteriori informazioni sui file dei messaggi, vedere [**compilatore di messaggi**](/windows/desktop/WES/message-compiler--mc-exe-). Per informazioni dettagliate sulla sintassi di un file di messaggio, vedere [file di testo del messaggio](message-text-files.md).

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

L'applicazione per la visualizzazione degli eventi può utilizzare la procedura seguente per ottenere l'accesso alle [stringhe di messaggio](event-identifiers.md) nella dll del messaggio.

**Per ottenere le stringhe di descrizione**

1.  Chiamare la funzione [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) per aprire l'origine evento.
2.  Chiamare la funzione [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) per ottenere il contenuto del valore **EventMessageFile** per l'origine evento, ovvero il nome della dll del messaggio.
3.  Chiamare la funzione [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) per caricare la dll del messaggio determinata dal passaggio 2.
4.  Chiamare la funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) con l'identificatore del messaggio per ottenere la descrizione dalla dll. Si noti che gli identificatori dei messaggi sono definiti in. File H generato dal compilatore di messaggi. La funzione **FormatMessage** sostituisce le stringhe di inserimento usando i valori degli argomenti passati, ma non sostituisce le stringhe di inserimento dei parametri. prima di visualizzare la stringa, è necessario sostituire le stringhe di inserimento dei parametri.

 

 
