---
description: ICE72 verifica che le azioni personalizzate non predefinite non vengano utilizzate nella tabella AdvtExecuteSequence.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d8e1859ffd8123cc7aa3dc801c5484d28ccb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316752"
---
# <a name="ice72"></a>ICE72

ICE72 verifica che le azioni personalizzate non predefinite non vengano utilizzate nella [tabella AdvtExecuteSequence](advtexecutesequence-table.md). In particolare, nella tabella AdvtExecuteSequence sono consentite solo le azioni personalizzate di tipo 19, tipo 35 e tipo 51. Se vengono utilizzate altre azioni personalizzate, l'annuncio potrebbe non comportarsi come previsto.

## <a name="result"></a>Risultato

ICE72 restituisce un errore se la tabella AdvExecuteSequence utilizza azioni personalizzate diverse da tipo 35, tipo 51 e tipo 19.

## <a name="example"></a>Esempio

ICE72 segnala l'errore seguente per l'esempio illustrato:

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

Per correggere l'errore, rimuovere "CA1" dalla tabella AdvtExecuteSequence.

[Tabella AdvtExecuteSequence](advtexecutesequence-table.md) (parziale)



| Azione |
|--------|
| CA1    |
| CA35   |



 

[Tabella CustomAction](customaction-table.md) (parziale)



| Azione | Tipo |
|--------|------|
| CA1    | 1    |
| CA35   | 35   |



 

## <a name="tables-used-during-execution"></a>Tabelle utilizzate durante l'esecuzione

[Tabella AdvtExecuteSequence](advtexecutesequence-table.md)

[Tabella CustomAction](customaction-table.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipo di azione personalizzata 19](custom-action-type-19.md)
</dt> <dt>

[Tipo di azione personalizzata 35](custom-action-type-35.md)
</dt> <dt>

[Tipo di azione personalizzata 51](custom-action-type-51.md)
</dt> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



