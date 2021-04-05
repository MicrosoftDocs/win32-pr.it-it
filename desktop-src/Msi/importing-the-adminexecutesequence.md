---
description: Nella tabella AdminExecuteSequence sono elencate le azioni eseguite dal programma di installazione quando viene chiamata l'azione di amministrazione di primo livello. Vedere il gruppo di tabelle delle procedure di installazione, usando una tabella di sequenza e l'esempio dettagliato della tabella di sequenza.
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Importazione del AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cfef89ada780d9ce647f45667fdc34cc5b01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752783"
---
# <a name="importing-the-adminexecutesequence"></a>Importazione del AdminExecuteSequence

Nella [tabella AdminExecuteSequence](adminexecutesequence-table.md) sono elencate le azioni eseguite dal programma di installazione quando viene chiamata l' [azione di amministrazione](admin-action.md)di primo livello. Vedere il [gruppo di tabelle delle procedure di installazione](installation-procedure-tables-group.md), [usando una tabella di sequenza](using-a-sequence-table.md)e l' [esempio dettagliato della tabella di sequenza](sequence-table-detailed-example.md).

Se nella sezione [importazione di un database vuoto](importing-a-blank-database.md) utilizzato uisample.msi da Windows Installer SDK, le tabelle di sequenza nella copia di MNP2000.msi contengono già le sequenze di azioni suggerite descritte in [utilizzo di una tabella di sequenza](using-a-sequence-table.md). Non è necessario apportare modifiche a queste sequenze per creare il pacchetto di installazione di esempio del blocco note.

Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella AdminExecuteSequence.

[Tabella AdminExecuteSequence](adminexecutesequence-table.md)



| Azione              | Condizione | Sequenza |
|---------------------|-----------|----------|
| CostFinalize secondo        |           | 1000     |
| CostInitialize      |           | 800      |
| Filecost            |           | 900      |
| InstallAdminPackage |           | 3900     |
| InstallFiles        |           | 4000     |
| InstallFinalize     |           | 6600     |
| InstallInitialize   |           | 1500     |
| InstallValidate     |           | 1400     |



 

[Continua](importing-the-adminuisequence.md)

 

 



