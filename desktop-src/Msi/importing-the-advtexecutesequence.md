---
description: La tabella AdvtExecuteSequence elenca le azioni chiamate dal programma di installazione quando esegue l'azione ADVERTISE di primo livello. Vedere Installation Procedure Tables Group, Using a Sequence Table (Gruppo di tabelle delle procedure di installazione), Using a Sequence Table (Uso di una tabella di sequenza) e Sequence Table Detailed Example (Esempio dettagliato della tabella sequence).
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importazione di AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518adfa315b5705806ba65caf09691316894ab664c32485dd3f4b6ce894be1a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043671"
---
# <a name="importing-the-advtexecutesequence"></a>Importazione di AdvtExecuteSequence

La [tabella AdvtExecuteSequence](advtexecutesequence-table.md) elenca le azioni chiamate dal programma di installazione quando esegue l'azione [ADVERTISE di primo livello.](advertise-action.md) Vedere [Installation Procedure Tables Group](installation-procedure-tables-group.md), Using a Sequence [Table](using-a-sequence-table.md)e Sequence [Table Detailed Example](sequence-table-detailed-example.md).

Se nella sezione Importazione di un [database](importing-a-blank-database.md) vuoto è stato usato uisample.msi da Windows Installer SDK, le tabelle di sequenza nella copia di MNP2000.msi contengono già le sequenze di azione suggerite descritte in [Uso](using-a-sequence-table.md)di una tabella sequence . Non è necessario apportare modifiche a queste sequenze per creare il Blocco note di installazione di esempio.

Usare l'editor di database per MNP2000.msi e immettere i dati seguenti nella [tabella AdvtExecuteSequence](advtexecutesequence-table.md).

[Tabella AdvtExecuteSequence](advtexecutesequence-table.md)



| Azione                | Condition | Sequenza |
|-----------------------|-----------|----------|
| CostFinalize          |           | 1000     |
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



 

La [tabella AdvtUISequence](advtuisequence-table.md) non viene usata dal programma di installazione. Questa tabella non deve esistere o essere lasciata vuota nel database di installazione.

[Continua](adding-summary-information.md)

 

 



