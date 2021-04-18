---
description: Nella tabella AdminUISequence sono elencate le azioni chiamate dal programma di installazione quando viene eseguita l'azione di amministrazione di livello superiore e il livello dell'interfaccia utente interna è impostato su interfaccia utente completa o interfaccia utente ridotta.
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: Importazione del AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314783"
---
# <a name="importing-the-adminuisequence"></a>Importazione del AdminUISequence

Nella [tabella AdminUISequence](adminuisequence-table.md) sono elencate le azioni chiamate dal programma di installazione quando viene eseguita l' [azione di amministrazione](admin-action.md) di livello superiore e il livello dell'interfaccia utente interna è impostato su interfaccia utente completa o interfaccia utente ridotta. Il programma di installazione ignora le azioni in questa tabella se il livello dell'interfaccia utente è impostato su interfaccia utente di base o nessuna interfaccia utente. Vedere livelli di [interfaccia utente e](user-interface.md) [interfaccia utente](user-interface-levels.md). Vedere il [gruppo di tabelle delle procedure di installazione](installation-procedure-tables-group.md), [usando una tabella di sequenza](using-a-sequence-table.md)e l' [esempio dettagliato della tabella di sequenza](sequence-table-detailed-example.md).

Se nella sezione [importazione di un database vuoto](importing-a-blank-database.md) utilizzato uisample.msi da Windows Installer SDK, le tabelle di sequenza nella copia di MNP2000.msi contengono già le sequenze di azioni suggerite descritte in [utilizzo di una tabella di sequenza](using-a-sequence-table.md). Non è necessario apportare modifiche a queste sequenze per installare l'esempio del blocco note.

Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella AdminExecuteSequence.

[Tabella AdminUISequence](adminuisequence-table.md)



| Azione          | Condizione | Sequenza |
|-----------------|-----------|----------|
| AdminWelcomeDlg |           | 1230     |
| CostFinalize secondo    |           | 1000     |
| CostInitialize  |           | 800      |
| ExecuteAction   |           | 1300     |
| ExitDlg         |           | -1       |
| FatalErrorDlg   |           | -3       |
| Filecost        |           | 900      |
| PrepareDlg      |           | 140      |
| ProgressDlg     |           | 1280     |
| UserExitDlg     |           | -2       |



 

[Continua](importing-the-advtexecutesequence.md)

 

 



