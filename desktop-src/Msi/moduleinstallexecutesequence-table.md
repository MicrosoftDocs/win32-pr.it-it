---
description: Uno strumento di merge valuta la tabella ModuleInstallExecuteSequence e quindi inserisce le azioni calcolate nella tabella InstallExecuteSequence con un numero di sequenza corretto.
ms.assetid: 6cd04d9a-5489-4fde-951e-aa962e9bd755
title: Tabella ModuleInstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6659c8223e41307766d67a4a5138699b46e03fbf3d50b514cb452bdc870c009c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042848"
---
# <a name="moduleinstallexecutesequence-table"></a>Tabella ModuleInstallExecuteSequence

Uno strumento di merge valuta la tabella ModuleInstallExecuteSequence e quindi inserisce le azioni calcolate nella [tabella InstallExecuteSequence](installexecutesequence-table.md) con un numero di sequenza corretto.

La tabella ModuleInstallExecuteSequence contiene le colonne seguenti.



| Colonna     | Tipo                         | Chiave | Nullable |
|------------|------------------------------|-----|----------|
| Azione     | [Identificatore](identifier.md) | S   | N        |
| Sequenza   | [Integer](integer.md)       |     | S        |
| BaseAction | [Identificatore](identifier.md) |     | S        |
| After      | [Integer](integer.md)       |     | S        |
| Condition  | [Condition](condition.md)   |     | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Azione da inserire in sequenza. Fa riferimento a una delle azioni standard del [programma](standard-actions.md)di installazione o a una voce nella tabella [CustomAction](customaction-table.md)del modulo unione o nella [tabella Dialog](dialog-table.md).

Se viene [usata un'azione standard](standard-actions.md) nella colonna Azione di una tabella della sequenza del modulo unione, le colonne BaseAction e After del record devono essere Null.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Numero di sequenza di un'azione standard. Se nella colonna Azione di questa riga viene immessa un'azione o una finestra di dialogo personalizzata, questo campo deve essere impostato su Null.

Quando si [usano azioni standard](standard-actions.md) nelle tabelle di sequenza del modulo unione, il valore nella colonna Sequenza deve essere il numero di sequenza di azione consigliato. Se il numero di sequenza nel modulo unione è diverso da quello per la stessa azione nella tabella della sequenza di file .msi, lo strumento di unione usa il numero di sequenza del file .msi. Per i numeri di sequenza consigliati delle azioni standard, vedere le sequenze suggerite in [Uso](using-a-sequence-table.md) di una tabella di sequenza.

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction
</dt> <dd>

La colonna BaseAction può contenere un'azione standard, un'azione personalizzata specificata nella tabella delle azioni personalizzate del modulo unione o una finestra di dialogo specificata nella tabella della finestra di dialogo del modulo. La colonna BaseAction è una chiave nella colonna Azione di questa tabella. Non può essere una chiave esterna in un'altra tabella o tabella di merge nel file Windows Installer. Ciò significa che ogni azione standard, azione personalizzata o dialogo elencata nella colonna BaseAction deve essere elencata anche nella colonna Azione di un altro record in questa tabella.

</dd> <dt>

<span id="After"></span><span id="after"></span><span id="AFTER"></span>Dopo
</dt> <dd>

Valore booleano per indicare se Action viene prima o dopo BaseAction.



| Valore | Significato                          |
|-------|----------------------------------|
| 0     | Azione da eseguire prima di BaseAction |
| 1     | Azione da eseguire dopo BaseAction  |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Istruzione condizionale che indica se l'azione deve essere eseguita. Un valore Null restituisce true.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se la [tabella ModuleInstallExecuteSequence](installexecutesequence-table.md) è presente, la [tabella InstallExecuteSequence](installexecutesequence-table.md) deve essere presente anche nel modulo unione.

 

 



