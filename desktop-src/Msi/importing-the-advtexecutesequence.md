---
description: Nella tabella AdvtExecuteSequence sono elencate le azioni chiamate dal programma di installazione quando viene eseguita l'azione di annuncio di primo livello. Vedere il gruppo di tabelle delle procedure di installazione, usando una tabella di sequenza e l'esempio dettagliato della tabella di sequenza.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importazione del AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757817"
---
# <a name="importing-the-advtexecutesequence"></a>Importazione del AdvtExecuteSequence

Nella [tabella AdvtExecuteSequence](advtexecutesequence-table.md) sono elencate le azioni chiamate dal programma di installazione quando viene eseguita l' [azione di annuncio](advertise-action.md)di primo livello. Vedere il [gruppo di tabelle delle procedure di installazione](installation-procedure-tables-group.md), [usando una tabella di sequenza](using-a-sequence-table.md)e l' [esempio dettagliato della tabella di sequenza](sequence-table-detailed-example.md).

Se nella sezione [importazione di un database vuoto](importing-a-blank-database.md) utilizzato uisample.msi da Windows Installer SDK, le tabelle di sequenza nella copia di MNP2000.msi contengono già le sequenze di azioni suggerite descritte in [utilizzo di una tabella di sequenza](using-a-sequence-table.md). Non è necessario apportare modifiche a queste sequenze per creare il pacchetto di installazione di esempio del blocco note.

Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella [tabella AdvtExecuteSequence](advtexecutesequence-table.md).

[Tabella AdvtExecuteSequence](advtexecutesequence-table.md)



| Azione                | Condizione | Sequenza |
|-----------------------|-----------|----------|
| CostFinalize secondo          |           | 1000     |
| CostInitialize        |           | 800      |
| CreateShortcuts       |           | 4500     |
| InstallFinalize       |           | 6600     |
| InstallInitialize     |           | 1500     |
| InstallValidate       |           | 1400     |
| PublishComponents     |           | 6200     |
| PublishFeatures       |           | 6300     |
| PublishProduct        |           | 6400     |
| RegisterClassInfo     |           | 4600     |
| RegisterExtensionInfo |           | 4700     |
| RegisterMIMEInfo      |           | 4900     |
| RegisterProgIdInfo    |           | 4800     |



 

La [tabella AdvtUISequence](advtuisequence-table.md) non viene utilizzata dal programma di installazione. Questa tabella non deve esistere o essere lasciata vuota nel database di installazione.

[Continua](adding-summary-information.md)

 

 



