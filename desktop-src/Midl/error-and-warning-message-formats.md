---
title: Formati di messaggio di errore e di avviso
description: Elenco dei formati dei messaggi di errore e di avviso MIDL.
ms.assetid: 8eb0f46f-e494-430a-8bb4-b8a21524b62e
keywords:
- errori MIDL, formati di messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42552b8106b72d82b2b13b69a7cba7ac2e99e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396774"
---
# <a name="error-and-warning-message-formats"></a>Formati di messaggio di errore e di avviso

Gli errori della riga di comando vengono visualizzati nel formato seguente:

``` syntax
Command line error : MIDLnnnn: <error text> 
[<additional error information>]
```

Il campo informazioni aggiuntive sull'errore fornisce informazioni specifiche del contesto a seconda del messaggio di errore. Ad esempio, quando si verifica un errore di dichiarazione di tipo non risolto, nel campo informazioni aggiuntive sull'errore viene visualizzato il nome del tipo che non è stato possibile risolvere.

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

Le informazioni di contesto facoltative fanno riferimento al contesto in cui si è verificato l'errore. Viene generato quando il compilatore MIDL individua un errore durante l'analisi semantica delle firme di tipi e procedure. Il compilatore MIDL segnala queste informazioni per facilitare l'individuazione rapida dell'errore nel file IDL.

I messaggi di errore di sistema vengono visualizzati nel formato seguente:

``` syntax
<FileName>(line#) : MIDL error 0xnnnn: 
"Unexpected internal compiler problem. Try to find a workaround."
```

Questo messaggio viene generato da un errore imprevisto. Il numero di errore esadecimale è un identificatore di errore di sistema di Windows XP, Windows 2000, Windows NT, Windows 98 o Windows 95. È possibile trovare informazioni aggiuntive in Winerror. h o NTSTATUS. h. Per ulteriori informazioni sull'utilizzo delle condizioni che hanno causato questo errore, vedere il testo dell'errore per l' [errore del compilatore](compiler-errors.md) MIDL9008.

 

 




