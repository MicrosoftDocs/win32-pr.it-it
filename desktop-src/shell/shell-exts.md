---
description: In questo set di argomenti viene illustrato come implementare i gestori di estensione che consentono di modificare un'ampia gamma di azioni della shell.
ms.assetid: 794b6369-665f-49a9-a263-7c736c5ce8ac
title: Uso delle estensioni della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbb696f4536cdb0fb6869be073771d431bd8d2de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980650"
---
# <a name="working-with-shell-extensions"></a>Uso delle estensioni della shell

Le funzionalità della shell possono essere estese con le voci del registro di sistema e i file ini. Sebbene questo approccio per estendere la shell sia semplice e appropriato per molti scopi, è limitato. Se ad esempio si usa il registro di sistema per specificare un'icona personalizzata per un tipo di file, verrà visualizzata la stessa icona per ogni file di quel tipo. L'estensione della shell con il registro di sistema non consente di variare l'icona per membri diversi del tipo di file. Altri aspetti della shell, ad esempio la finestra delle proprietà **delle proprietà che** può essere visualizzata quando si fa clic con il pulsante destro del mouse su un file, non possono essere modificati nel registro di sistema.

Un approccio più potente e flessibile per estendere la Shell consiste nell'implementare i *gestori di estensioni della shell*. Questi gestori possono essere implementati per un'ampia gamma di azioni che la shell può eseguire. Prima di eseguire l'azione, la shell esegue una query sul gestore dell'estensione, offrendo la possibilità di modificare l'azione. Un esempio comune è un gestore di estensione del menu di scelta rapida. Se ne viene implementato uno per un tipo di file, verrà eseguita una query ogni volta che viene fatto clic con il pulsante destro del mouse su uno dei file. Il gestore può quindi specificare voci di menu aggiuntive in base al file, anziché avere lo stesso set per tutti i file di quel tipo di file.

In questo set di argomenti viene illustrato come implementare i gestori di estensione che consentono di modificare un'ampia gamma di azioni della shell. I gestori seguenti sono associati a un tipo di file specifico e consentono di specificare in base al file.



| Gestore                                               | Descrizione                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestore del menu di scelta rapida](context-menu-handlers.md)    | Chiamato prima che venga visualizzato il menu di scelta rapida di un file. Consente di aggiungere elementi al menu di scelta rapida in base al file.                                               |
| [Gestore dati](how-to-create-data-handlers.md)       | Chiamato quando viene eseguita un'operazione di trascinamento e rilascio sugli oggetti della shell. Consente di fornire altri formati degli Appunti all'obiettivo di rilascio.                            |
| [Gestore di trascinamento](how-to-create-drop-handlers.md)       | Chiamato quando un oggetto dati viene trascinato o rilasciato in un file. Consente di creare un file in un obiettivo di rilascio.                                                          |
| [Gestore icone](how-to-create-icon-handlers.md)       | Chiamato prima che venga visualizzata l'icona di un file. Consente di sostituire l'icona predefinita del file con un'icona personalizzata in base al file.                                    |
| [Gestore della finestra delle proprietà](propsheet-handlers.md)      | Chiamato prima della visualizzazione della finestra delle proprietà **delle proprietà di** un oggetto. Consente di aggiungere o sostituire pagine.                                                              |
| [**Gestore immagini di anteprima**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Fornisce un'immagine per rappresentare l'elemento.                                                                                                                                   |
| [**Gestore della finestra popup**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Fornisce il testo popup quando l'utente posiziona il puntatore del mouse sull'oggetto.                                                                                               |
| [**Gestore di metadati**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)       | Fornisce l'accesso in lettura e scrittura ai metadati (proprietà) archiviati in un file. Questa operazione può essere utilizzata per estendere la visualizzazione dettagli, infotip, la pagina delle proprietà e le funzionalità di raggruppamento. |



 

Altri non sono associati a un tipo di file specifico, ma vengono chiamati prima di alcune operazioni della shell.



| Gestore                                                            | Descrizione                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestore delle colonne](../lwef/column-handlers.md)                             | Chiamato da Esplora risorse prima di visualizzare la visualizzazione dettagli di una cartella. Consente di aggiungere colonne personalizzate alla visualizzazione dettagli.        |
| [Gestore hook di copia](how-to-create-copy-hook-handlers.md)          | Chiamato quando un oggetto Folder o Printer sta per essere spostato, copiato, eliminato o rinominato. Consente di approvare o porre il veto sull'operazione.   |
| [Gestore di trascinamento della selezione](context-menu-handlers.md)                 | Chiamato quando un file viene trascinato con il pulsante destro del mouse. Consente di modificare il menu di scelta rapida visualizzato.                     |
| [Gestore sovrimpressione icone](how-to-implement-icon-overlay-handlers.md) | Chiamato prima che venga visualizzata l'icona di un file. Consente di specificare una sovrapposizione per l'icona del file.                                          |
| [Gestore ricerche](../lwef/search-handlers.md)                             | Chiamato per avviare un motore di ricerca. Consente di implementare un motore di ricerca personalizzato accessibile dal menu **Start** o da Esplora risorse. |



 

I dettagli relativi all'implementazione di gestori di estensioni specifici sono descritti nelle sezioni elencate in precedenza. Per le discussioni sui problemi di implementazione comuni a tutti i gestori di estensioni della shell, vedere gli argomenti seguenti:

-   [Inizializzazione di gestori estensioni della shell](int-shell-exts.md)
-   [Registrazione di gestori estensioni della shell](reg-shell-exts.md)

 

 
