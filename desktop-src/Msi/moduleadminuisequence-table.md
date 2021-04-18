---
description: Uno strumento di merge valuta la tabella ModuleAdminUISequence e quindi inserisce le azioni calcolate nella tabella AdminUISequence con un numero di sequenza corretto.
ms.assetid: c71477e7-22bc-420a-9902-39bbf98b4ee5
title: Tabella ModuleAdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e128aebd6481c077827f4d1ba2b487eafe6132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317126"
---
# <a name="moduleadminuisequence-table"></a>Tabella ModuleAdminUISequence

Uno strumento di merge valuta la tabella ModuleAdminUISequence e quindi inserisce le azioni calcolate nella [tabella AdminUISequence](adminuisequence-table.md) con un numero di sequenza corretto.

La tabella ModuleAdminUISequence include le colonne seguenti.



| Colonna     | Tipo                         | Chiave | Nullable |
|------------|------------------------------|-----|----------|
| Azione     | [Identificatore](identifier.md) | S   | N        |
| Sequenza   | [Integer](integer.md)       |     | S        |
| BaseAction | [Identificatore](identifier.md) |     | S        |
| After      | [Integer](integer.md)       |     | S        |
| Condizione  | [Condition](condition.md)   |     | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Azione da inserire in sequenza. Fa riferimento a una delle [azioni standard](standard-actions.md)del programma di installazione o a una voce nella tabella [CustomAction](customaction-table.md) o nella tabella di [dialogo](dialog-table.md)del modulo merge.

Se nella colonna Action di una tabella di sequenza di un modulo merge viene utilizzata un' [azione standard](standard-actions.md) , le colonne BaseAction e After del record devono essere null.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Numero di sequenza di un'azione standard. Se una finestra di dialogo o un'azione personalizzata viene immessa nella colonna azione di questa riga, questo campo deve essere impostato su null.

Quando si utilizzano [azioni standard](standard-actions.md) nelle tabelle di sequenza dei moduli di merge, il valore nella colonna sequenza deve essere il numero di sequenza dell'azione consigliata. Se il numero di sequenza nel modulo merge è diverso da quello per la stessa azione nella tabella di sequenza dei file con estensione msi, lo strumento di merge utilizza il numero di sequenza del file con estensione msi. Vedere le sequenze suggerite nell' [uso di una tabella di sequenza](using-a-sequence-table.md) per i numeri di sequenza consigliati per le azioni standard.

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction
</dt> <dd>

La colonna BaseAction può contenere un'azione standard, un'azione personalizzata specificata nella tabella delle azioni personalizzata del modulo merge o una finestra di dialogo specificata nella tabella delle finestre di dialogo del modulo. La colonna BaseAction è una chiave nella colonna Action della tabella. Non può essere una chiave esterna in un'altra tabella o tabella di merge nel file con estensione msi. Ciò significa che ogni azione standard, azione personalizzata o finestra di dialogo elencata nella colonna BaseAction deve essere elencata anche nella colonna azione di un altro record in questa tabella.

</dd> <dt>

<span id="After"></span><span id="after"></span><span id="AFTER"></span>Dopo
</dt> <dd>

Valore booleano che indica se l'azione precede o dopo BaseAction.



| Valore | Significato                          |
|-------|----------------------------------|
| 0     | Azione da passare prima di BaseAction |
| 1     | Azione da eseguire dopo BaseAction  |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Istruzione condizionale che indica se l'azione viene eseguita. Null restituisce true.

</dd> </dl>

## <a name="remarks"></a>Commenti

<dl> <dt>

<span id="If_this_table_is_present_the__AdminUISequence_Table_must_also_be_present_in_the_merge_module."></span><span id="if_this_table_is_present_the__adminuisequence_table_must_also_be_present_in_the_merge_module."></span><span id="IF_THIS_TABLE_IS_PRESENT_THE__ADMINUISEQUENCE_TABLE_MUST_ALSO_BE_PRESENT_IN_THE_MERGE_MODULE."></span>Se questa tabella è presente, è necessario che la [tabella AdminUISequence](adminuisequence-table.md) sia presente anche nel modulo merge.
</dt> <dd></dd> </dl>

 

 



