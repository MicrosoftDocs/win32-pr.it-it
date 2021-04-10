---
description: La tabella Condition può essere utilizzata per modificare lo stato di selezione di qualsiasi voce nella tabella feature basata su un'espressione condizionale.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Tabella Condition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d9a3c27d43b7d71bc8e5b0593771bc86a3ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966491"
---
# <a name="condition-table"></a>Tabella Condition

La tabella Condition può essere utilizzata per modificare lo stato di selezione di qualsiasi voce nella [tabella Feature](feature-table.md) basata su un'espressione condizionale.

La tabella Condition contiene le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Funzionalità\_ | [Identificatore](identifier.md) | S   | N        |
| Level     | [Integer](integer.md)       | S   | N        |
| Condizione | [Condition](condition.md)   | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave esterna nella colonna uno della tabella delle funzionalità.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Livello
</dt> <dd>

Livello di installazione condizionale per la funzionalità nella \_ colonna feature della tabella. Il programma di installazione imposta il livello di installazione della funzionalità sul livello specificato in questa colonna se l'espressione nella colonna condizione restituisce TRUE.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Se questa espressione condizionale restituisce TRUE, la colonna Level della tabella Feature viene impostata sul livello di installazione condizionale.

L'espressione nella colonna condizione non deve contenere riferimenti allo stato di installazione di una funzionalità o di un componente. Ciò è dovuto al fatto che le espressioni nella colonna condition vengono valutate prima che il programma di installazione valuti gli stati installati delle funzionalità e dei componenti. Qualsiasi espressione nella tabella della condizione che tenta di verificare lo stato installato di una funzionalità o di un componente restituisce sempre false.

Per informazioni sulla sintassi delle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Una funzionalità può essere disabilitata in modo permanente impostando la colonna livello su 0.

Il livello può essere impostato in base a qualsiasi istruzione condizionale, ad esempio un test per la piattaforma, il sistema operativo o una particolare impostazione della proprietà.

È necessario scegliere attentamente le condizioni in modo che una funzionalità non sia abilitata durante l'installazione e quindi disabilitata durante la disinstallazione. La funzionalità verrà orfana e il prodotto non potrà essere disinstallato.

Questa tabella viene definita quando viene eseguita l' [azione CostFinalize secondo](costfinalize-action.md) .

Se la proprietà [**preselezionata**](preselected.md) è stata impostata su 1, il programma di installazione non valuta la tabella della condizione. La tabella della condizione influiscono solo sull'installazione delle funzionalità quando non è stata impostata nessuna delle proprietà seguenti:

<dl>

[**ADDLOCAL**](addlocal.md)  
[**RIMUOVERE**](remove.md)  
[**ADDSOURCE**](addsource.md)  
[**ADDDEFAULT**](adddefault.md)  
[**REINSTALL**](reinstall.md)  
[**PUBBLICIZZARE**](advertise.md)  
[**COMPADDLOCAL**](compaddlocal.md)  
[**COMPADDSOURCE**](compaddsource.md)  
[**COMPADDDEFAULT**](compadddefault.md)  
[**FILEADDLOCAL**](fileaddlocal.md)  
[**FILEADDSOURCE**](fileaddsource.md)  
[**FILEADDDEFAULT**](fileadddefault.md)  
</dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



