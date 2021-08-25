---
description: L'ordine di esecuzione dell'azione è determinato dalla sequenza di azioni che sono state scritte nelle tabelle di sequenza e dall'ordine in cui il programma di installazione esegue le tabelle di sequenza.
ms.assetid: f4666f49-4ea1-42fb-b32d-ce77de79b212
title: Ordine di esecuzione dell'azione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28244d46ae5556d1b68cc3b7258297c69e11a8d526f3e7ca31a184e64c424e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381841"
---
# <a name="action-execution-order"></a>Ordine di esecuzione dell'azione

L'ordine di esecuzione dell'azione è determinato dalla sequenza [](s-gly.md) di azioni che sono state scritte nelle tabelle di sequenza e dall'ordine in cui il programma di installazione esegue le tabelle di sequenza. Per informazioni dettagliate, vedere le sequenze di azioni suggerite in [Uso di una tabella di sequenza](using-a-sequence-table.md).

Il programma di installazione esegue le tabelle di sequenza in risposta a una richiesta per un'installazione, [un annuncio](advertisement.md)o un'installazione [amministrativa.](administrative-installation.md) Ad esempio, in risposta all'uso delle opzioni della riga di comando /I, /J o [/A](command-line-options.md), le azioni [INSTALL](install-action.md), [ADVERTISE](advertise-action.md)e [ADMIN](admin-action.md) non vengono chiamate dall'interno della sequenza di azioni. Queste azioni di alto livello vengono invece passate al programma di installazione quando il programma di installazione viene inizializzato.

Se al programma di installazione viene passata l'azione INSTALL e il pacchetto di installazione è stato creato con un'interfaccia utente, il programma di installazione esegue prima le azioni nella tabella [InstallUISequence](installuisequence-table.md) e quindi esegue le azioni nella [tabella InstallExecuteSequence](installexecutesequence-table.md) nell'ordine indicato. Se il pacchetto non ha un'interfaccia utente, il programma di installazione esegue le azioni nella tabella InstallExecuteSequence nell'ordine indicato.

Se al programma di installazione viene passata l'azione ADMIN e il pacchetto di installazione è stato creato con un'interfaccia utente, il programma di installazione esegue prima la tabella [AdminUISequence](adminuisequence-table.md) e quindi la tabella [AdminExecuteSequence](adminexecutesequence-table.md). Se il pacchetto non ha un'interfaccia utente, il programma di installazione esegue la tabella AdminExecute.

Se al programma di installazione viene passata l'azione ADVERTISE, il programma di installazione esegue la [tabella AdvtExecuteSequence.](advtexecutesequence-table.md)

> [!Note]  
> Il programma di installazione non usa la [tabella AdvtUISequence.](advtuisequence-table.md) La tabella AdvtUISequence non deve esistere nel database di installazione o deve essere lasciata vuota.

 

Quando il programma di installazione esegue una tabella di sequenza, esegue azioni nell'ordine dei numeri di sequenza elencati nella colonna Sequenza. L'ordine delle azioni è sempre lineare senza diramazioni o cicli. Gli sviluppatori di pacchetti possono impedire in modo condizionale l'esecuzione di una determinata azione tramite la creazione di un'espressione logica nella colonna Condizione. Il programma di installazione ignora l'azione ogni volta che la condizione restituisce False. Vedere [Uso di una tabella di sequenza e](using-a-sequence-table.md) della [sintassi di istruzioni condizionali](conditional-statement-syntax.md).

Tutte le tabelle di sequenza hanno le colonne seguenti.



| Colonna    | Descrizione                                                                                                                                                                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azione    | Chiave primaria per la tabella. Il nome dell'azione deve essere univoco.                                                                                                                                                                                |
| Condition | Espressione booleana utilizzata per determinare se eseguire l'azione. L'azione viene eseguita se questo campo è vuoto o contiene un'espressione che restituisce True. L'azione non viene eseguita se l'espressione restituisce False. |
| Sequenza  | Numero di sequenza relativo utilizzato per determinare l'ordine di esecuzione delle azioni.                                                                                                                                                         |



 

 

 



