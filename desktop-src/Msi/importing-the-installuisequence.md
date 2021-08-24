---
description: La sequenza dell'interfaccia utente viene importata nel database di esempio.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importazione di InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c559f9c4ad2cbd766447d27c879246f0fbf6af1ff78e1e02dece17b362ad2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580661"
---
# <a name="importing-the-installuisequence"></a>Importazione di InstallUISequence

La [tabella InstallUISequence](installuisequence-table.md) elenca le azioni eseguite quando viene eseguita l'azione [INSTALL](install-action.md) di primo livello e il livello dell'interfaccia utente interno è impostato su interfaccia utente completa o ridotta. Il programma di installazione ignora le azioni in questa tabella se il livello dell'interfaccia utente è impostato sull'interfaccia utente di base o su nessuna interfaccia utente. Vedere [Interfaccia utente](user-interface.md) e [Interfaccia utente livelli .](user-interface-levels.md) Vedere [Installation Procedure Tables Group](installation-procedure-tables-group.md), Using a Sequence [Table](using-a-sequence-table.md)e Sequence [Table Detailed Example](sequence-table-detailed-example.md).

Se nella sezione Importazione di un [database](importing-a-blank-database.md) vuoto è stato usato uisample.msi da Windows Installer SDK, le tabelle di sequenza nella copia di MNP2000.msi contengono già le sequenze di azione suggerite descritte in [Uso](using-a-sequence-table.md)di una tabella di sequenza . Non è necessario apportare modifiche a queste sequenze per creare il Blocco note di installazione.

Usare l'editor di database per MNP2000.msi e immettere i dati seguenti nella tabella InstallUISequence.

[Tabella InstallUISequence](installuisequence-table.md)



| Azione                | Condition                                    | Sequenza |
|-----------------------|----------------------------------------------|----------|
| Appsearch             |                                              | 400      |
| CCPSearch             | NON installato                                | 500      |
| CostFinalize          |                                              | 1000     |
| CostInitialize        |                                              | 800      |
| ExecuteAction         |                                              | 1300     |
| ExitDlg               |                                              | -1       |
| FatalErrorDlg         |                                              | -3       |
| FileCost              |                                              | 900      |
| LaunchConditions      |                                              | 100      |
| ManutenzioneWelcomeDlg | Installato E NON RIPRESO E NON preselezionato | 1250     |
| PrepareDlg            |                                              | 140      |
| ProgressDlg           |                                              | 1280     |
| ResumeDlg             | INSTALLATO AND (RESUME O preselezionato)        | 1240     |
| RMCCPSearch           | NON installato                                | 600      |
| UserExitDlg           |                                              | -2       |
| WelcomeDlg            | NON installato                                | 1230     |
| MigrateFeatureStates  |                                              | 1200     |
| FindRelatedProducts   |                                              | 200      |



 

[Continua](importing-the-adminexecutesequence.md)

 

 



