---
description: ICE72 verifica che le azioni personalizzate non incorporate non siano usate nella tabella AdvtExecuteSequence.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f931e705dbca734348f62ba4b1ca106b43bb80a52c50f0e94ecab7139c624da2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946578"
---
# <a name="ice72"></a>ICE72

ICE72 verifica che le azioni personalizzate non incorporate non siano usate nella [tabella AdvtExecuteSequence](advtexecutesequence-table.md). In particolare, nella tabella AdvtExecuteSequence sono consentiti solo i tipi 19, 35 e 51 azioni personalizzate. Se vengono usate altre azioni personalizzate, l'annuncio potrebbe non comportarsi come previsto.

## <a name="result"></a>Risultato

ICE72 restituisce un errore se la tabella AdvExecuteSequence usa azioni personalizzate diverse dal tipo 35, dal tipo 51 e dal tipo 19.

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



 

## <a name="tables-used-during-execution"></a>Tabelle usate durante l'esecuzione

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

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



