---
description: Questo esempio illustra come usare azioni personalizzate per creare account utente in un computer locale durante l'installazione di un componente.
ms.assetid: fc06dd7b-46d7-45a0-85b3-26f808c64f89
title: Uso di un'azione personalizzata per creare account utente in un computer locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd3bf002c0fa1d661c6bfebb6d1a18cbc4b0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346576"
---
# <a name="using-a-custom-action-to-create-user-accounts-on-a-local-computer"></a>Uso di un'azione personalizzata per creare account utente in un computer locale

Questo esempio illustra come usare azioni personalizzate per creare account utente in un computer locale durante l'installazione di un componente. La rimozione di un componente consente di rimuovere gli account utente locali creati dall'azione personalizzata. Vengono illustrate diverse azioni personalizzate, incluse le [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md) e le [azioni personalizzate di rollback](rollback-custom-actions.md).

L'esempio soddisfa le specifiche seguenti.

-   L'installazione crea gli account utente solo se si esegue Windows 2000.
-   L'installazione crea gli account utente solo se il componente viene installato per l'esecuzione in locale. Ciò impedisce la creazione di account utente durante la riparazione o la reinstallazione del componente.
-   Il programma di installazione rimuove gli account quando il componente viene rimosso.
-   Le informazioni sull'account utente vengono lette da una tabella personalizzata nel database di installazione e non sono hardcoded nel codice dell'azione personalizzata.
-   Poiché la creazione o la rimozione di account utente richiede privilegi elevati, alcune delle azioni personalizzate devono essere in grado di apportare modifiche al sistema che richiedono privilegi elevati. Queste azioni personalizzate devono essere azioni personalizzate posticipate che vengono eseguite quando nello script di esecuzione.
-   Ogni account ha un'azione di rollback personalizzata per assicurarsi che l'account venga rimosso durante il rollback dell'installazione del componente. Questa operazione non include il rollback di un'eliminazione dell'account durante la rimozione di un componente.
-   Le azioni personalizzate inviano messaggi ActionData per ogni account creato o rimosso. Questa operazione non include la fornitura di messaggi di stato per il ProgressBar.
-   Le azioni personalizzate segnalano un errore se non è possibile creare un account.
-   La password per l'account viene ottenuta tramite l'interazione dell'utente con l'interfaccia utente o, nel caso di un'installazione nell'interfaccia utente di base o in nessuno dei [livelli dell'interfaccia utente](user-interface-levels.md), come proprietà passata nella riga di comando.
-   I dati sensibili sono nascosti dal file di log.

Nell'esempio è incluso un ipotetico componente denominato TestAccount. Nelle sezioni seguenti si presuppone che siano già state create le risorse richieste da TestAccount e che siano state create le tabelle [feature](feature-table.md), [Component](component-table.md), [file](file-table.md), [directory](directory-table.md)e [FeatureComponents](featurecomponents-table.md) del database di esempio necessarie per installare questo componente. Per ulteriori informazioni, vedere [un esempio di installazione](an-installation-example.md).

Negli argomenti seguenti sono contenute informazioni su come creare azioni personalizzate obbligatorie e aggiungerle a un pacchetto di installazione.

-   [Creazione di azioni personalizzate](authoring-the-custom-actions.md)
-   [Aggiunta di una tabella CustomUserAccounts personalizzata](adding-a-custom-customuseraccounts-table.md)
-   [Creazione della tabella CustomAction](authoring-the-customaction-table.md)
-   [Creazione di tabelle ActionText e Error](authoring-the-actiontext-and-error-tables.md)
-   [Creazione della tabella InstallExecuteSequence](authoring-the-installexecutesequence-table.md)
-   [Creazione dell'interfaccia utente per l'input della password](authoring-the-user-interface-for-password-input.md)
-   [Sicurezza dell'installazione](securing-the-installation.md)

 

 



