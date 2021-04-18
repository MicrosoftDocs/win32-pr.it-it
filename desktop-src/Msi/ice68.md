---
description: ICE68 verifica che tutti i tipi di azione personalizzati necessari per un'installazione siano validi.
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318667"
---
# <a name="ice68"></a>ICE68

ICE68 verifica che tutti i tipi di azione personalizzati necessari per un'installazione siano validi. Se si verifica un errore durante la correzione dell'errore segnalato da ICE68, un'installazione che tenta di eseguire l'azione avrà esito negativo. ICE68 genera un avviso se l'attributo **msidbCustomActionTypeNoImpersonate** è impostato senza impostare anche l'attributo **msidbCustomActionTypeInScript** .

## <a name="result"></a>Risultato

ICE68 restituisce un errore se un tipo di azione necessario per un'installazione non è valido.

## <a name="example"></a>Esempio

ICE68 invia l'avviso seguente se un'azione personalizzata ha il bit **msidbCustomActionTypeNoImpersonate** impostato nel campo Type della tabella CustomAction senza impostare anche **msidbCustomActionTypeInScript** .

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

Per correggere il problema, includere **msidbCustomActionTypeInScript** (0x400) se l'azione personalizzata include **msidbCustomActionTypeNoImpersonate** (0x800). In caso contrario, il programma di installazione ignora l'attributo **msidbCustomActionTypeNoImpersonate** . Per altre informazioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).

ICE68 segnala l'errore seguente per l'esempio illustrato:

``` syntax
Invalid custom action type for action 'Action1'.
```

1027 non è un tipo di azione valido.

Per correggere l'errore, scegliere un tipo di azione personalizzata valido.

[Tabella CustomAction](customaction-table.md) (parziale)



| Azione  | Tipo | Source (Sorgente)   | Destinazione     |
|---------|------|----------|------------|
| Action1 | 1027 | Argomento | Component1 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



