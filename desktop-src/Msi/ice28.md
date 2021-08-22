---
description: ICE28 viene comunemente usato per verificare che l'azione ForceReboot sia posizionata prima o dopo e mai all'interno di un gruppo specifico di azioni nelle tabelle della sequenza di azioni. Vedere l'argomento Azione ForceReboot per determinare le azioni che costituiscono questo gruppo.
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cda8676a072ebed21a16653dca9af67464f35699530eb3c08ae05d3cd9574b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528781"
---
# <a name="ice28"></a>ICE28

ICE28 viene comunemente usato per verificare che l'azione ForceReboot sia posizionata prima o dopo e mai all'interno di un gruppo specifico di azioni nelle tabelle della sequenza di azioni. Vedere [l'argomento Azione ForceReboot](forcereboot-action.md) per determinare le azioni che costituiscono questo gruppo.

ICE28 convalida le azioni nelle tabelle di sequenza seguenti:

[Tabella AdminUISequence](adminuisequence-table.md)

[Tabella AdminExecuteSequence](adminexecutesequence-table.md)

[Tabella InstallUISequence](installuisequence-table.md)

[Tabella InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Risultato

ICE28 invia un messaggio di errore se ForceReboot è sequenziato all'interno del gruppo di azioni specificato.

## <a name="example"></a>Esempio

Per l'esempio illustrato, ICE28 pubblica il messaggio di errore seguente:

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[Tabella InstallExecuteSequence](installexecutesequence-table.md)



| Azione             | Sequenza |
|--------------------|----------|
| ForceReboot        | 10       |
| RegisterMIMEInfo   |   5      |
| RegisterProgIdInfo | 15       |



 

Il numero di sequenza 10 assegnato alle interruzioni ForceReboot genera l'errore, perché è compreso tra i numeri di sequenza di RegisterMIMEInfo e RegisterProgIdInfo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



