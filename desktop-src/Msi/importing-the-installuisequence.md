---
description: La sequenza dell'interfaccia utente viene importata nel database di esempio.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importazione del InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232441"
---
# <a name="importing-the-installuisequence"></a>Importazione del InstallUISequence

Nella [tabella InstallUISequence](installuisequence-table.md) sono elencate le azioni che vengono eseguite quando viene eseguita l' [azione di installazione](install-action.md) di livello superiore e il livello dell'interfaccia utente interna è impostato sull'interfaccia utente completa o sull'interfaccia utente ridotta. Il programma di installazione ignora le azioni in questa tabella se il livello dell'interfaccia utente è impostato sull'interfaccia utente di base o su nessuna interfaccia utente. Vedere livelli di [interfaccia utente e](user-interface.md) [interfaccia utente](user-interface-levels.md). Vedere il [gruppo di tabelle delle procedure di installazione](installation-procedure-tables-group.md), [usando una tabella di sequenza](using-a-sequence-table.md)e l' [esempio dettagliato della tabella di sequenza](sequence-table-detailed-example.md).

Se nella sezione [importazione di un database vuoto](importing-a-blank-database.md) utilizzato uisample.msi da Windows Installer SDK, le tabelle di sequenza nella copia di MNP2000.msi contengono già le sequenze di azioni suggerite descritte in [utilizzo di una tabella di sequenza](using-a-sequence-table.md). Per creare il pacchetto di installazione del blocco note non è necessario apportare modifiche a tali sequenze.

Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella InstallUISequence.

[Tabella InstallUISequence](installuisequence-table.md)



| Azione                | Condizione                                    | Sequenza |
|-----------------------|----------------------------------------------|----------|
| AppSearch             |                                              | 400      |
| CCPSearch             | NON installato                                | 500      |
| CostFinalize secondo          |                                              | 1000     |
| CostInitialize        |                                              | 800      |
| ExecuteAction         |                                              | 1300     |
| ExitDlg               |                                              | -1       |
| FatalErrorDlg         |                                              | -3       |
| Filecost              |                                              | 900      |
| LaunchConditions      |                                              | 100      |
| MaintenanceWelcomeDlg | Installato e non ripreso e non preselezionato | 1250     |
| PrepareDlg            |                                              | 140      |
| ProgressDlg           |                                              | 1280     |
| ResumeDlg             | Installato e (ripresa o preselezione)        | 1240     |
| RMCCPSearch           | NON installato                                | 600      |
| UserExitDlg           |                                              | -2       |
| WelcomeDlg            | NON installato                                | 1230     |
| MigrateFeatureStates  |                                              | 1200     |
| FindRelatedProducts   |                                              | 200      |



 

[Continua](importing-the-adminexecutesequence.md)

 

 



