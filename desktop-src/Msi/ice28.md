---
description: ICE28 viene in genere usato per verificare che l'azione ForceReboot venga posizionata prima o dopo e mai all'interno di un gruppo specifico di azioni nelle tabelle della sequenza di azione. Vedere l'argomento azione ForceReboot per determinare le azioni che compongono questo gruppo.
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65878bdc3db4f9b79ba95b4a170b694a4728ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750130"
---
# <a name="ice28"></a>ICE28

ICE28 viene in genere usato per verificare che l'azione ForceReboot venga posizionata prima o dopo e mai all'interno di un gruppo specifico di azioni nelle tabelle della sequenza di azione. Vedere l'argomento [azione ForceReboot](forcereboot-action.md) per determinare le azioni che compongono questo gruppo.

ICE28 convalida le azioni nelle tabelle di sequenza seguenti:

[Tabella AdminUISequence](adminuisequence-table.md)

[Tabella AdminExecuteSequence](adminexecutesequence-table.md)

[Tabella InstallUISequence](installuisequence-table.md)

[Tabella InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Risultato

ICE28 Invia un messaggio di errore se ForceReboot viene sequenziato all'interno del gruppo di azioni specificato.

## <a name="example"></a>Esempio

Per l'esempio illustrato, ICE28 invia il messaggio di errore seguente:

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[Tabella InstallExecuteSequence](installexecutesequence-table.md)



| Azione             | Sequenza |
|--------------------|----------|
| ForceReboot        | 10       |
| RegisterMIMEInfo   |   5      |
| RegisterProgIdInfo | 15       |



 

Il numero di sequenza di 10 specificato per le interruzioni ForceReboot genera l'errore, perché è incluso tra i numeri di sequenza di RegisterMIMEInfo e RegisterProgIdInfo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



