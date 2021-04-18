---
description: L'ordine di esecuzione delle azioni è determinato dalla sequenza di azioni che sono state create nelle tabelle di sequenza e dall'ordine in cui il programma di installazione esegue le tabelle di sequenza.
ms.assetid: f4666f49-4ea1-42fb-b32d-ce77de79b212
title: Ordine di esecuzione delle azioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954c44f6e2525deb3375cb9ea72d0320df3a5f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311092"
---
# <a name="action-execution-order"></a>Ordine di esecuzione delle azioni

L'ordine di esecuzione delle azioni è determinato dalla sequenza di azioni che sono state create nelle tabelle di [*sequenza*](s-gly.md) e dall'ordine in cui il programma di installazione esegue le tabelle di sequenza. Per informazioni dettagliate, vedere le sequenze di azioni suggerite in [uso di una tabella di sequenza](using-a-sequence-table.md).

Il programma di installazione esegue tabelle di sequenza in risposta a una richiesta di installazione, [annuncio](advertisement.md)o un' [installazione amministrativa](administrative-installation.md). Ad esempio, in risposta all'utilizzo delle [Opzioni della riga di comando](command-line-options.md)/I,/J o/a, le azioni di [installazione](install-action.md), [annuncio](advertise-action.md)e [Amministrazione](admin-action.md) non vengono chiamate dall'interno della sequenza di azione. Queste azioni di alto livello vengono invece passate al programma di installazione quando viene inizializzato il programma di installazione.

Se al programma di installazione viene passata l'azione di installazione e il pacchetto di installazione è stato creato con un'interfaccia utente, il programma di installazione esegue prima le azioni nella [tabella InstallUISequence](installuisequence-table.md) , quindi esegue le azioni nella [tabella InstallExecuteSequence](installexecutesequence-table.md) in ordine. Se il pacchetto non dispone di un'interfaccia utente, il programma di installazione esegue le azioni nella tabella InstallExecuteSequence in ordine.

Se al programma di installazione viene passata l'azione di amministrazione e il pacchetto di installazione è stato creato con un'interfaccia utente, il programma di installazione esegue innanzitutto la [tabella AdminUISequence](adminuisequence-table.md) e quindi esegue la [tabella AdminExecuteSequence](adminexecutesequence-table.md). Se il pacchetto non dispone di un'interfaccia utente, il programma di installazione esegue la tabella AdminExecute.

Se al programma di installazione viene passata l'azione annuncia, il programma di installazione esegue la tabella [AdvtExecuteSequence](advtexecutesequence-table.md) .

> [!Note]  
> Il programma di installazione non usa la tabella [AdvtUISequence](advtuisequence-table.md) . La tabella AdvtUISequence non deve esistere nel database di installazione oppure deve essere lasciata vuota.

 

Quando il programma di installazione esegue una tabella di sequenza, esegue le azioni nell'ordine dei numeri di sequenza elencati nella colonna sequenza. L'ordine di azione è sempre lineare senza branching o loop. Gli sviluppatori di pacchetti possono impedire in modo condizionale l'esecuzione di una determinata azione mediante la creazione di un'espressione logica nella colonna condizione. Il programma di installazione ignora l'azione ogni volta che la condizione restituisce false. Vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md) e di una [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).

Tutte le tabelle di sequenza hanno le colonne seguenti.



| Colonna    | Descrizione                                                                                                                                                                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azione    | Chiave primaria per la tabella. il nome dell'azione deve essere univoco.                                                                                                                                                                                |
| Condizione | Espressione booleana utilizzata per determinare se eseguire l'azione. L'azione viene eseguita se il campo è vuoto o contiene un'espressione che restituisce true. L'azione non viene eseguita se l'espressione restituisce false. |
| Sequenza  | Numero di sequenza relativo utilizzato per determinare l'ordine in cui vengono eseguite le azioni.                                                                                                                                                         |



 

 

 



