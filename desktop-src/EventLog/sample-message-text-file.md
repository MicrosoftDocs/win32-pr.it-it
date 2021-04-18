---
description: Nel file di messaggio di esempio seguente viene illustrato come creare e utilizzare un file di testo del messaggio che definisce i messaggi in più lingue.
ms.assetid: 403eaccc-07a3-4368-a39a-18c706c65537
title: File di testo del messaggio di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e4247b1e39ef94c006262f282d8d830af11851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310810"
---
# <a name="sample-message-text-file"></a><span data-ttu-id="f0133-103">File di testo del messaggio di esempio</span><span class="sxs-lookup"><span data-stu-id="f0133-103">Sample Message Text File</span></span>

<span data-ttu-id="f0133-104">Nel file di messaggio di esempio seguente viene illustrato come creare e utilizzare un file di testo del messaggio che definisce i messaggi in più lingue.</span><span class="sxs-lookup"><span data-stu-id="f0133-104">The following sample message file shows how to create and use a message text file that defines messages in multiple languages.</span></span>

## <a name="sample-message-file"></a><span data-ttu-id="f0133-105">File di messaggio di esempio</span><span class="sxs-lookup"><span data-stu-id="f0133-105">Sample Message File</span></span>

<span data-ttu-id="f0133-106">Questo file di messaggio di esempio, Sample.mc, contiene un blocco di commento, seguito da una sezione di intestazione, seguito da messaggi in due lingue.</span><span class="sxs-lookup"><span data-stu-id="f0133-106">This sample message file, Sample.mc, contains a comment block, followed by a header section, followed by messages in two languages.</span></span> <span data-ttu-id="f0133-107">È necessario utilizzare un editor compatibile con Unicode per supportare contemporaneamente i caratteri utilizzati in linguaggi scritti differenti.</span><span class="sxs-lookup"><span data-stu-id="f0133-107">You must use a Unicode-compatible editor to simultaneously support the characters used in different written languages.</span></span> <span data-ttu-id="f0133-108">Per ulteriori informazioni e una descrizione dettagliata della sintassi dei file con estensione MC, vedere [file di testo del messaggio](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="f0133-108">For more information and a detailed description of the syntax of .mc files, see [Message Text Files](message-text-files.md).</span></span>

``` syntax
; // ***** Sample.mc *****
; // This is the header section.

MessageIdTypedef=DWORD

SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
Warning=0x2:STATUS_SEVERITY_WARNING
Error=0x3:STATUS_SEVERITY_ERROR
)

FacilityNames=(System=0x0:FACILITY_SYSTEM
Runtime=0x2:FACILITY_RUNTIME
Stubs=0x3:FACILITY_STUBS
Io=0x4:FACILITY_IO_ERROR_CODE
)

LanguageNames=(English=0x409:MSG00409)
LanguageNames=(Japanese=0x411:MSG00411)

; // The following are message definitions.

MessageId=0x1
Severity=Error
Facility=Runtime
SymbolicName=MSG_BAD_COMMAND
Language=English
You have chosen an incorrect command.
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x2
Severity=Warning
Facility=Io
SymbolicName=MSG_BAD_PARM1
Language=English
Cannot reconnect to the server.
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x3
Severity=Success
Facility=System
SymbolicName=MSG_STRIKE_ANY_KEY
Language=English
Press any key to continue . . . %0
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2 which is in error.
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x5
Severity=Informational
Facility=System
SymbolicName=MSG_RETRYS
Language=English
There have been %1!d! attempts with %2!d!%% success%! Disconnect from 
the server and try again later.
.

Language=Japanese
<Japanese message string goes here>
.
```

 

 



