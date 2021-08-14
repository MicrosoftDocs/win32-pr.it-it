---
title: Formati dei messaggi di errore e di avviso
description: Elenco dei formati dei messaggi di errore MIDL e dei messaggi di avviso.
ms.assetid: 8eb0f46f-e494-430a-8bb4-b8a21524b62e
keywords:
- errori MIDL, formati di messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cbe6e32109bbe8e4d40b7715c6463e16cd0c27fc77492f5044ce32a7fe57436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384417"
---
# <a name="error-and-warning-message-formats"></a>Formati dei messaggi di errore e di avviso

Gli errori della riga di comando vengono visualizzati nel formato seguente:

``` syntax
Command line error : MIDLnnnn: <error text> 
[<additional error information>]
```

Il campo aggiuntivo error-information fornisce informazioni specifiche del contesto a seconda del messaggio di errore. Ad esempio, quando si verifica un errore di dichiarazione di tipo non risolto, il campo delle informazioni sull'errore aggiuntivo visualizza il nome del tipo che non è stato possibile risolvere.

Gli avvisi in fase di compilazione vengono visualizzati nel formato seguente:

``` syntax
<FileName>(line#) : warning MIDLnnnn: 
<warning text>
[optional context information]:
```

Gli errori in fase di compilazione vengono visualizzati nel formato seguente:

``` syntax
<FileName>(line#) : error MIDLnnnn: 
<error text>
[optional context information] :
```

Le informazioni di contesto facoltative si riferiscono al contesto in cui si è verificato l'errore. Viene generato quando il compilatore MIDL individua un errore durante l'analisi semantica delle firme di tipo e routine. Il compilatore MIDL segnala queste informazioni per individuare rapidamente l'errore nel file IDL.

I messaggi di errore di sistema vengono visualizzati nel formato seguente:

``` syntax
<FileName>(line#) : MIDL error 0xnnnn: 
"Unexpected internal compiler problem. Try to find a workaround."
```

Questo messaggio viene generato da un errore imprevisto. Il numero di errore esadecimale è un identificatore di errore di sistema Windows XP, Windows 2000, Windows NT, Windows 98 o Windows 95. È possibile trovare informazioni aggiuntive in Winerror.h o Ntstatus.h. Per altre informazioni su come risolvere le condizioni che hanno causato questo errore, vedere il testo dell'errore del [compilatore](compiler-errors.md) MIDL9008.

 

 




