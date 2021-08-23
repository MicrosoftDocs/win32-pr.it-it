---
description: La tabella AdminExecuteSequence elenca le azioni eseguite dal programma di installazione quando chiama l'azione ADMIN di primo livello. Vedere Installation Procedure Tables Group, Using a Sequence Table (Gruppo di tabelle delle procedure di installazione), Using a Sequence Table (Uso di una tabella di sequenza) e Sequence Table Detailed Example (Esempio dettagliato della tabella sequence).
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Importazione di AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de646049fed05f881b61c4b635af3bc9d2caed09512a1ec89853066b0ba99c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787381"
---
# <a name="importing-the-adminexecutesequence"></a>Importazione di AdminExecuteSequence

La [tabella AdminExecuteSequence](adminexecutesequence-table.md) elenca le azioni eseguite dal programma di installazione quando chiama l'azione [ADMIN di primo livello.](admin-action.md) Vedere [Installation Procedure Tables Group](installation-procedure-tables-group.md), Using a Sequence [Table](using-a-sequence-table.md)e Sequence [Table Detailed Example](sequence-table-detailed-example.md).

Se nella sezione Importazione di un [database](importing-a-blank-database.md) vuoto è stato usato uisample.msi da Windows Installer SDK, le tabelle di sequenza nella copia di MNP2000.msi contengono già le sequenze di azione suggerite descritte in [Uso](using-a-sequence-table.md)di una tabella di sequenza . Non è necessario apportare modifiche a queste sequenze per creare il Blocco note di installazione di esempio.

Usare l'editor di database per MNP2000.msi e immettere i dati seguenti nella tabella AdminExecuteSequence.

[Tabella AdminExecuteSequence](adminexecutesequence-table.md)



| Azione              | Condition | Sequenza |
|---------------------|-----------|----------|
| CostFinalize        |           | 1000     |
| CostInitialize      |           | 800      |
| FileCost            |           | 900      |
| InstallAdminPackage |           | 3900     |
| InstallFiles        |           | 4000     |
| InstallFinalize     |           | 6600     |
| InstallInitialize   |           | 1500     |
| InstallValidate     |           | 1400     |



 

[Continua](importing-the-adminuisequence.md)

 

 



