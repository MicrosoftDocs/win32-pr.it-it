---
description: Questo esempio illustra come usare azioni personalizzate per creare account utente in un computer locale durante l'installazione di un componente.
ms.assetid: fc06dd7b-46d7-45a0-85b3-26f808c64f89
title: Uso di un'azione personalizzata per creare account utente in un computer locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 408c80a5fbf32d9da758322bd6c5ebc881da73501d2b241c39f64cdd779d239d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499581"
---
# <a name="using-a-custom-action-to-create-user-accounts-on-a-local-computer"></a>Uso di un'azione personalizzata per creare account utente in un computer locale

Questo esempio illustra come usare azioni personalizzate per creare account utente in un computer locale durante l'installazione di un componente. La rimozione di un componente rimuove gli account utente locali creati dall'azione personalizzata. Vengono illustrate diverse azioni personalizzate, tra cui azioni personalizzate di [esecuzione posticipata](deferred-execution-custom-actions.md) e [azioni personalizzate di rollback.](rollback-custom-actions.md)

L'esempio soddisfa le specifiche seguenti.

-   L'installazione crea gli account utente solo se Windows 2000.
-   L'installazione crea account utente solo se il componente viene installato per l'esecuzione in locale. Questo preclude la creazione di account utente durante il ripristino o la reinstallazione del componente.
-   Il programma di installazione rimuove gli account quando il componente viene rimosso.
-   Le informazioni sull'account utente vengono lette da una tabella personalizzata nel database di installazione e non sono hard coded nel codice dell'azione personalizzata.
-   Poiché la creazione o la rimozione di account utente richiede privilegi elevati, alcune azioni personalizzate devono essere in grado di apportare modifiche al sistema che richiedono privilegi elevati. Queste azioni personalizzate devono essere azioni personalizzate posticipate che vengono eseguite nello script di esecuzione.
-   Ogni account ha un'azione personalizzata di rollback per assicurarsi che l'account venga rimosso al rollback dell'installazione del componente. Questo non include il rollback di un'eliminazione di account durante la rimozione di un componente.
-   Le azioni personalizzate inviano messaggi ActionData per ogni account creato o rimosso. Ciò non include l'invio di messaggi di stato per ProgressBar.
-   Le azioni personalizzate segnalano un errore se non è possibile creare un account.
-   La password per l'account viene ottenuta tramite l'interazione dell'utente con l'interfaccia utente o nel caso di un'installazione all'interfaccia utente di base o a nessuno dei livelli [Interfaccia utente](user-interface-levels.md), come proprietà passata nella riga di comando.
-   I dati sensibili vengono nascosti dal file di log.

L'esempio include un componente ipotetico denominato TestAccount. La discussione nelle sezioni seguenti presuppone che siano già state create le risorse richieste da TestAccount e che siano state create le tabelle [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md)e [FeatureComponents](featurecomponents-table.md) nel database di esempio necessarie per installare questo componente. Per altre informazioni, vedere [An Installation Example](an-installation-example.md).

Gli argomenti seguenti contengono informazioni su come creare le azioni personalizzate necessarie e aggiungerle a un pacchetto di installazione.

-   [Creazione di azioni personalizzate](authoring-the-custom-actions.md)
-   [Aggiunta di una tabella CustomUserAccounts personalizzata](adding-a-custom-customuseraccounts-table.md)
-   [Creazione della tabella CustomAction](authoring-the-customaction-table.md)
-   [Creazione delle tabelle ActionText ed Error](authoring-the-actiontext-and-error-tables.md)
-   [Creazione della tabella InstallExecuteSequence](authoring-the-installexecutesequence-table.md)
-   [Creazione del Interfaccia utente per l'input della password](authoring-the-user-interface-for-password-input.md)
-   [Protezione dell'installazione](securing-the-installation.md)

 

 



