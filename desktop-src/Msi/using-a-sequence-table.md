---
description: La creazione di tabelle di sequenza è una parte essenziale dello sviluppo di un pacchetto di installazione, in quanto queste tabelle specificano l'ordine di esecuzione per le azioni standard che controllano il processo di installazione e visualizzano le finestre di dialogo dell'interfaccia utente.
ms.assetid: db9a9cae-2a66-4e0d-a981-8de66d7c2a13
title: Utilizzo di una tabella di sequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0be10082aba05429a63df69444ed28bea350aa5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882117"
---
# <a name="using-a-sequence-table"></a>Utilizzo di una tabella di sequenza

La creazione di tabelle di sequenza è una parte essenziale dello sviluppo di un pacchetto di installazione, in quanto queste tabelle specificano l'ordine di esecuzione per le [azioni standard](standard-actions.md) che controllano il processo di installazione e visualizzano le finestre di dialogo dell'interfaccia utente.

Sono disponibili tre modalità di installazione e due tipi di tabelle di sequenza per ogni modalità.

Le tre modalità di installazione separate attualmente supportate dal programma di installazione sono:

-   Installazione semplice
-   Installazione amministrativa
-   Installazione annuncio

Ogni tabella di sequenza presenta tre campi: azione, condizione e sequenza. Il campo azione denomina un'azione standard o personalizzata oppure una finestra di dialogo o una sequenza definita dall'utente in cui viene eseguito il programma di installazione. Il campo condizione consente all'autore di specificare un'espressione logica che controlla se un'azione o una finestra di dialogo definita dall'utente viene eseguita o visualizzata. Se il campo condizione è vuoto o contiene un'espressione che restituisce true, l'azione o la finestra di dialogo viene eseguita o visualizzata. L'azione o la finestra di dialogo viene ignorata se l'espressione restituisce false. Il campo sequenza specifica l'ordine di esecuzione di ogni azione o finestra di dialogo definita dall'utente nella tabella.

Ognuna di queste modalità di installazione elabora le tabelle di sequenza dell'interfaccia utente e le tabelle di sequenza di esecuzione. Le tabelle di sequenza dell'interfaccia utente vengono elaborate solo se il programma di installazione è stato inizializzato con il livello di visualizzazione dell'interfaccia utente impostato su ridotto o completo. Per ulteriori informazioni sui livelli di visualizzazione dell'interfaccia utente, vedere la Guida di riferimento a [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .

Le tabelle di sequenza dell'interfaccia utente contengono in genere azioni standard correlate alla raccolta di informazioni di sistema visualizzate dall'utente tramite l'interfaccia utente. L'interfaccia utente viene visualizzata registrando le chiavi esterne nei nomi delle finestre di dialogo della [tabella della finestra di dialogo](dialog-table.md) nel campo azione della tabella sequenza dell'interfaccia utente. L'utente ha quindi la possibilità di modificare o accettare le informazioni di sistema e di iniziare l'installazione, che si verifica quando viene elaborata la tabella di esecuzione della sequenza.

Durante un'installazione semplice, viene eseguita l'azione di primo livello [Install](install-action.md) che elabora a sua volta la [tabella InstallUISequence](installuisequence-table.md) e la [tabella InstallExecuteSequence](installexecutesequence-table.md).

Un'installazione amministrativa viene in genere avviata da un amministratore di rete per assegnare e installare le applicazioni per singoli utenti e gruppi di utenti. Durante questo tipo di installazione, viene eseguita l'azione di primo livello [amministratore](admin-action.md) che elabora la [tabella AdminUISequence](adminuisequence-table.md) e la [tabella AdminExecuteSequence](adminexecutesequence-table.md).

Per [annunciare](advertisement.md) un'applicazione o una funzionalità, è necessario avviare il programma di installazione con l'azione [annuncia](advertise-action.md) . Durante questo tipo di installazione viene elaborata la [tabella AdvtExecuteSequence](advtexecutesequence-table.md) .

Quando si crea una tabella di sequenza, è consigliabile usare il numero di sequenza per le azioni standard delle sequenze suggerite negli argomenti seguenti. Per le azioni standard che non hanno una posizione standard nella tabella di sequenza, ad esempio [ForceReboot](forcereboot-action.md), [ValidateProductID](validateproductid-action.md)e [InstallExecute](installexecute-action.md), usare un numero di sequenza che corrisponde a un multiplo di dieci per identificare l'azione come azione standard. Per le azioni personalizzate, usare un numero di sequenza che non sia un multiplo di dieci per distinguerlo dalle azioni standard nella tabella di sequenza.

Per le sequenze di azioni consigliate per ogni tabella di sequenza, vedere gli argomenti seguenti:

-   [InstallUISequence suggerito](suggested-installuisequence.md)
-   [InstallExecuteSequence suggerito](suggested-installexecutesequence.md)
-   [AdminUISequence suggerito](suggested-adminuisequence.md)
-   [AdminExecuteSequence suggerito](suggested-adminexecutesequence.md)
-   [AdvtUISequence suggerito](suggested-advtuisequence.md)
-   [AdvtExecuteSequence suggerito](suggested-advtexecutesequence.md)

Per una descrizione dettagliata delle tabelle di sequenza e del modo in cui vengono eseguite le azioni standard, vedere l' [esempio dettagliato della tabella Sequence](sequence-table-detailed-example.md).

* * Windows Installer 3,0 e versioni successive: * *

A partire da Windows Installer 3,0, un pacchetto di patch può contenere la [tabella MsiPatchSequence](msipatchsequence-table.md). Questa tabella contiene tutte le informazioni necessarie per il programma di installazione per determinare la sequenza dell'applicazione di una patch di aggiornamento ridotta rispetto a tutte le altre patch. Per ulteriori informazioni, vedere applicazione di [patch e aggiornamenti](patching-and-upgrades.md).

> [!Note]
>
> I [moduli merge](merge-modules.md) possono contenere [tabelle di database del modulo merge](merge-module-database-tables.md) che modificano le tabelle di sequenza delle azioni del file con estensione msi di destinazione. L'Unione del modulo in un database consente di modificare le informazioni nella tabella di sequenza, ma non di aggiungere tali tabelle al file con estensione msi. Per ulteriori informazioni, vedere [creazione di tabelle di sequenza dei moduli merge](authoring-merge-module-sequence-tables.md).

 

 

 



