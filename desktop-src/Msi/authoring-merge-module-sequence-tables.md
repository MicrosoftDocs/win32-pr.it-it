---
description: Includere le tabelle MergeModuleSequence nel file con estensione MSM se il modulo merge deve modificare le tabelle di sequenza delle azioni del file con estensione msi di destinazione. Il merge non aggiunge queste tabelle al file con estensione msi. Queste tabelle si verificano solo nei moduli unione.
ms.assetid: 9efb75d2-43f9-404c-8e7f-918d056190cf
title: Creazione di tabelle di sequenza del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b21780601e626c006967cefa0dcff5700bdec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967266"
---
# <a name="authoring-merge-module-sequence-tables"></a>Creazione di tabelle di sequenza del modulo merge

Includere le tabelle MergeModuleSequence nel file con estensione MSM se il modulo merge deve modificare le [*tabelle di sequenza*](s-gly.md) delle azioni del file con estensione msi di destinazione. Il merge non aggiunge queste tabelle al file con estensione msi. Queste tabelle si verificano solo nei moduli unione.

Se una delle tabelle ModuleSequence è presente in un file con estensione MSM, è necessario creare anche una copia vuota della tabella di sequenza del programma di installazione corrispondente nel modulo merge. Se, ad esempio, un modulo merge contiene una tabella ModuleAdminExecuteSequence, anche il modulo merge deve includere una tabella AdminExecuteSequence vuota. Durante un'operazione di merge, queste tabelle vuote forniscono lo strumento di merge con le linee guida necessarie per lo schema.

Quando si utilizzano [azioni standard](standard-actions.md) nelle tabelle di sequenza dei moduli di merge, il valore nella colonna sequenza deve essere il numero di sequenza di azione consigliato per l'azione standard. Vedere le sequenze di azioni suggerite indicate di seguito per i numeri di sequenza consigliati in ogni tabella di sequenza. Se il numero di sequenza nella tabella di sequenza dei moduli unione è diverso dal numero di sequenza per la stessa azione nel file con estensione msi, lo strumento di merge utilizzerà il numero di sequenza nel file con estensione MSI durante il merge.



| Tabella MergeModuleSequence                                                    | Sequenze di azioni consigliate                                             |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)                     | [AdminUISequence suggerito](suggested-adminuisequence.md)               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)           | [AdminExecuteSequence suggerito](suggested-adminexecutesequence.md)     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                       | [AdvtUISequence suggerito](suggested-advtuisequence.md)                 |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)             | [AdvtExecuteSequence suggerito](suggested-advtexecutesequence.md)       |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)                 | [InstallUISequence suggerito](suggested-installuisequence.md)           |
| [Tabella ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) | [InstallExecuteSequence suggerito](suggested-installexecutesequence.md) |



 

Se nella colonna Action di una tabella di sequenza di un modulo merge viene utilizzata un' [azione standard](standard-actions.md) , le colonne BaseAction e After del record devono essere null.

Se una finestra di dialogo o un'azione personalizzata viene immessa nella colonna azione, la colonna sequenza deve essere null.

Se nella colonna Action viene immessa un'azione che restituisce un flag di terminazione, la colonna Sequence deve contenere il valore negativo per tale flag e le colonne BaseAction e After del record devono essere null. I valori negativi seguenti indicano che l'azione viene chiamata se il programma di installazione restituisce il flag di terminazione.



| Flag di terminazione          | Valore | Descrizione              |
|---------------------------|-------|--------------------------|
| msiDoActionStatusSuccess  | -1    | Operazione completata.   |
| msiDoActionStatusUserExit | -2    | L'utente termina l'installazione. |
| msiDoActionStatusFailure  | -3    | Terminazione irreversibile.   |
| msiDoActionStatusSuspend  | -4    | L'installazione è stata sospesa.    |



 

La colonna BaseAction può contenere un'azione standard, un'azione personalizzata specificata nella tabella delle azioni personalizzata del modulo merge o una finestra di dialogo specificata nella tabella delle finestre di dialogo del modulo. La colonna BaseAction è una chiave nella colonna Action della tabella. Non può essere una chiave esterna in un'altra tabella o tabella di merge nel file con estensione msi. Ciò significa che ogni azione standard, azione personalizzata o finestra di dialogo elencata nella colonna BaseAction deve essere elencata anche nella colonna azione di un altro record in questa tabella.

 

 



