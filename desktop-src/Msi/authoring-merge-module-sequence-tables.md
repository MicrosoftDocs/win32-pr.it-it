---
description: Includere le tabelle MergeModuleSequence nel file con estensione msm se il modulo di merge deve modificare le tabelle della sequenza di azioni del file di .msi destinazione. L'unione non aggiunge queste tabelle al file .msi. Queste tabelle si verificano solo nei moduli unione.
ms.assetid: 9efb75d2-43f9-404c-8e7f-918d056190cf
title: Creazione di tabelle di sequenza del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45e4cf86c846030854054d7ab700e34210d4e27367cd31d606c78c24f2a9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381186"
---
# <a name="authoring-merge-module-sequence-tables"></a>Creazione di tabelle di sequenza del modulo merge

Includere le tabelle MergeModuleSequence nel file con estensione msm [](s-gly.md) se il modulo di merge deve modificare le tabelle della sequenza di azioni del file .msi destinazione. L'unione non aggiunge queste tabelle al file .msi. Queste tabelle si verificano solo nei moduli unione.

Se una delle tabelle ModuleSequence è presente in un file con estensione msm, nel modulo merge deve essere creata anche una copia vuota della tabella della sequenza del programma di installazione corrispondente. Ad esempio, se un modulo di merge contiene una tabella ModuleAdminExecuteSequence, il modulo di merge deve includere anche una tabella AdminExecuteSequence vuota. Durante un'unione, queste tabelle vuote forniscono allo strumento di unione le linee guida necessarie per lo schema.

Quando si [usano azioni standard](standard-actions.md) nelle tabelle di sequenza del modulo merge, il valore nella colonna Sequenza deve essere il numero di sequenza di azione consigliato per l'azione standard. Per i numeri di sequenza consigliati in ogni tabella di sequenza, vedere le sequenze di azione suggerite riportate di seguito. Se il numero di sequenza nella tabella di sequenza del modulo di merge è diverso dal numero di sequenza per la stessa azione nel file .msi, lo strumento di unione usa il numero di sequenza nel file di .msi durante l'unione.



| Tabella MergeModuleSequence                                                    | Sequenze di azioni consigliate                                             |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)                     | [AdminUISequence suggerito](suggested-adminuisequence.md)               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)           | [Amministrazione suggeritaExecuteSequence](suggested-adminexecutesequence.md)     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                       | [Suggested AdvtUISequence](suggested-advtuisequence.md)                 |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)             | [Suggested AdvtExecuteSequence](suggested-advtexecutesequence.md)       |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)                 | [Installazione suggeritaUISequence](suggested-installuisequence.md)           |
| [Tabella ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) | [Installazione suggeritaExecuteSequence](suggested-installexecutesequence.md) |



 

Se viene [usata un'azione standard](standard-actions.md) nella colonna Action di una tabella di sequenza del modulo di merge, le colonne BaseAction e After del record devono essere Null.

Se nella colonna Azione viene immessa un'azione o una finestra di dialogo personalizzata, la colonna Sequenza deve essere Null.

Se nella colonna Azione viene immessa un'azione che restituisce un flag di terminazione, la colonna Sequenza deve contenere il valore negativo per tale flag e le colonne BaseAction e After del record devono essere Null. I valori negativi seguenti indicano che l'azione viene chiamata se il programma di installazione restituisce il flag di terminazione.



| Flag di terminazione          | Valore | Descrizione              |
|---------------------------|-------|--------------------------|
| msiDoActionStatusSuccess  | -1    | Completamento.   |
| msiDoActionStatusUserExit | -2    | L'utente termina l'installazione. |
| msiDoActionStatusFailure  | -3    | Termina l'uscita irreversibile.   |
| msiDoActionStatusSuspend  | -4    | L'installazione è sospesa.    |



 

La colonna BaseAction può contenere un'azione standard, un'azione personalizzata specificata nella tabella delle azioni personalizzate del modulo di merge o una finestra di dialogo specificata nella tabella delle finestre di dialogo del modulo. La colonna BaseAction è una chiave nella colonna Action di questa tabella. Non può essere una chiave esterna in un'altra tabella o tabella di merge nel file .msi. Ciò significa che ogni azione standard, azione personalizzata o finestra di dialogo elencata nella colonna BaseAction deve essere elencata anche nella colonna Azione di un altro record in questa tabella.

 

 



