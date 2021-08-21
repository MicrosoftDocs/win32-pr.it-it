---
description: La creazione delle tabelle di sequenza è una parte essenziale dello sviluppo di un pacchetto del programma di installazione perché queste tabelle specificano l'ordine di esecuzione per le azioni standard che controllano il processo di installazione e visualizzano le finestre di dialogo dell'interfaccia utente.
ms.assetid: db9a9cae-2a66-4e0d-a981-8de66d7c2a13
title: Uso di una tabella di sequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16adf47a554bf70298b0efc893847f84eafd6e97313b09ba9ea3182398cdd97d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809011"
---
# <a name="using-a-sequence-table"></a>Uso di una tabella di sequenza

La creazione delle tabelle di sequenza è una parte essenziale dello sviluppo di un pacchetto del programma di installazione perché queste tabelle specificano l'ordine di esecuzione per le azioni [standard](standard-actions.md) che controllano il processo di installazione e visualizzano le finestre di dialogo dell'interfaccia utente.

Esistono tre modalità di installazione e due tipi di tabelle di sequenza per ogni modalità.

Le tre modalità di installazione separate attualmente supportate dal programma di installazione sono:

-   Installazione semplice
-   Installazione amministrativa
-   Installazione di annunci

Ognuna delle tabelle di sequenza ha tre campi: Azione, Condizione e Sequenza. Il campo Azione indica un'azione standard o personalizzata oppure una finestra di dialogo o una sequenza definita dall'utente eseguita dal programma di installazione. Il campo Condizione consente all'autore di specificare un'espressione logica che controlla se un'azione o una finestra di dialogo definita dall'utente viene eseguita o visualizzata. Se il campo Condizione è vuoto o contiene un'espressione che restituisce True, l'azione o la finestra di dialogo viene eseguita o visualizzata. L'azione o la finestra di dialogo viene ignorata se l'espressione restituisce False. Il campo Sequenza specifica l'ordine di esecuzione di ogni azione o finestra di dialogo definita dall'utente nella tabella.

Ognuna di queste modalità di installazione elabora le tabelle di sequenza dell'interfaccia utente e le tabelle di sequenza di esecuzione. Le tabelle di sequenza dell'interfaccia utente vengono elaborate solo se il programma di installazione è stato inizializzato con il livello di visualizzazione dell'interfaccia utente impostato su Ridotto o Completo. Per altre informazioni sui livelli di visualizzazione dell'interfaccia utente, vedere le informazioni di riferimento su [**MsiSetInternalUI.**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

Le tabelle di sequenza dell'interfaccia utente contengono in genere azioni standard correlate alla raccolta di informazioni di sistema visualizzate all'utente tramite l'interfaccia utente. L'interfaccia utente viene visualizzata registrando le chiavi esterne [](dialog-table.md) nei nomi delle finestre di dialogo nella tabella della finestra di dialogo nel campo Azione della tabella della sequenza dell'interfaccia utente. L'utente ha quindi la possibilità di modificare o accettare le informazioni di sistema e iniziare l'installazione, che si verifica quando viene elaborata la tabella della sequenza di esecuzione.

Durante un'installazione semplice, viene eseguita l'azione di primo livello [INSTALL](install-action.md) che a sua volta elabora la tabella [InstallUISequence](installuisequence-table.md) e [la tabella InstallExecuteSequence](installexecutesequence-table.md).

Un'installazione amministrativa viene in genere avviata da un amministratore di rete per assegnare e installare applicazioni per singoli utenti e gruppi di utenti. Durante questo tipo di installazione, viene eseguita l'azione di primo livello [ADMIN](admin-action.md) che elabora la tabella [AdminUISequence](adminuisequence-table.md) e la [tabella AdminExecuteSequence](adminexecutesequence-table.md).

Per [annunciare](advertisement.md) un'applicazione o una funzionalità, il programma di installazione deve essere avviato con [l'azione ADVERTISE.](advertise-action.md) Durante questo tipo di installazione viene elaborata la tabella [AdvtExecuteSequence.](advtexecutesequence-table.md)

Quando si crea una tabella di sequenze, è consigliabile usare il numero di sequenza per le azioni standard dalle sequenze suggerite negli argomenti seguenti. Per le azioni standard che non hanno una posizione standard nella tabella di sequenza, ad esempio [ForceReboot,](forcereboot-action.md) [ValidateProductID](validateproductid-action.md)e [InstallExecute,](installexecute-action.md)usare un numero di sequenza multiplo di dieci per identificare l'azione come azione standard. Per le azioni personalizzate, usare un numero di sequenza che non sia un multiplo di dieci per differenziarlo dalle azioni standard nella tabella di sequenza.

Per le sequenze di azioni suggerite per ogni tabella di sequenza, vedere gli argomenti seguenti:

-   [Installazione suggeritaUISequence](suggested-installuisequence.md)
-   [Installazione suggeritaExecuteSequence](suggested-installexecutesequence.md)
-   [AdminUISequence suggerita](suggested-adminuisequence.md)
-   [Amministrazione suggeritaExecuteSequence](suggested-adminexecutesequence.md)
-   [AdvtUISequence suggerita](suggested-advtuisequence.md)
-   [Suggested AdvtExecuteSequence](suggested-advtexecutesequence.md)

Per una descrizione dettagliata delle tabelle di sequenza e della modalità di esecuzione delle azioni standard, vedere l'esempio dettagliato [della tabella di sequenza](sequence-table-detailed-example.md).

**Windows Installer 3.0 e versioni successive: **

A partire da Windows Installer 3.0, un pacchetto patch può contenere la tabella [MsiPatchSequence](msipatchsequence-table.md). Questa tabella contiene tutte le informazioni necessarie al programma di installazione per determinare la sequenza dell'applicazione di una patch di aggiornamento di piccole dimensioni rispetto a tutte le altre patch. Per altre informazioni, vedere [Applicazione di patch e aggiornamenti.](patching-and-upgrades.md)

> [!Note]
>
> [I moduli unione](merge-modules.md) possono [contenere tabelle di database del](merge-module-database-tables.md) modulo unione che modificano le tabelle della sequenza di azione del file di .msi di destinazione. L'unione del modulo in un database può modificare le informazioni nella tabella di sequenza, ma non aggiunge queste tabelle al file .msi database. Per altre informazioni, vedere [Creazione di tabelle di sequenza di moduli unione](authoring-merge-module-sequence-tables.md).

 

 

 



