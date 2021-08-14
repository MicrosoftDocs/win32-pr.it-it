---
description: Questo set di argomenti illustra come implementare i gestori di estensioni che consentono di modificare un'ampia gamma di azioni della shell.
ms.assetid: 794b6369-665f-49a9-a263-7c736c5ce8ac
title: Uso delle estensioni della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 804b121ccf633b44574ae956b367143eebdaf7a2a3a8a9cc8400995522b4cbef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452849"
---
# <a name="working-with-shell-extensions"></a>Uso delle estensioni della shell

Le funzionalità della shell possono essere estese con voci del Registro di sistema e .ini file. Sebbene questo approccio all'estensione della shell sia semplice e adeguato per molti scopi, è limitato. Ad esempio, se si usa il Registro di sistema per specificare un'icona personalizzata per un tipo di file, verrà visualizzata la stessa icona per ogni file di quel tipo. L'estensione della shell con il Registro di sistema non consente di variare l'icona per i diversi membri del tipo di file. Altri aspetti della shell, ad  esempio la finestra delle proprietà Proprietà che può essere visualizzata quando si fa clic con il pulsante destro del mouse su un file, non possono essere modificati con il Registro di sistema.

Un approccio più potente e flessibile per estendere la shell consiste nell'implementare i *gestori di estensioni della shell*. Questi gestori possono essere implementati per un'ampia gamma di azioni che la shell può eseguire. Prima di eseguire l'azione, la shell esegue una query sul gestore dell'estensione, offrendo la possibilità di modificare l'azione. Un esempio comune è un gestore di estensione del menu di scelta rapida. Se ne viene implementato uno per un tipo di file, verrà eseguita una query ogni volta che si fa clic con il pulsante destro del mouse su uno dei file. Il gestore può quindi specificare voci di menu aggiuntive file per file, anziché avere lo stesso set per tutti i file di quel tipo di file.

Questo set di argomenti illustra come implementare i gestori di estensioni che consentono di modificare un'ampia gamma di azioni della shell. I gestori seguenti sono associati a un particolare tipo di file e consentono di specificare file per file.



| Gestore                                               | Descrizione                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestore del menu di scelta rapida](context-menu-handlers.md)    | Chiamato prima che venga visualizzato il menu di scelta rapida di un file. Consente di aggiungere voci al menu di scelta rapida file per file.                                               |
| [Gestore dati](how-to-create-data-handlers.md)       | Chiamato quando viene eseguita un'operazione di trascinamento della selezione sugli oggetti della shell. Consente di fornire formati di Appunti aggiuntivi all'obiettivo di rilascio.                            |
| [Gestore di eliminazione](how-to-create-drop-handlers.md)       | Chiamato quando un oggetto dati viene trascinato su un file. Consente di convertire un file in un obiettivo di rilascio.                                                          |
| [Gestore dell'icona](how-to-create-icon-handlers.md)       | Chiamato prima che venga visualizzata l'icona di un file. Consente di sostituire l'icona predefinita del file con un'icona personalizzata per ogni file.                                    |
| [Gestore della finestra delle proprietà](propsheet-handlers.md)      | Chiamato prima che venga visualizzata la **finestra delle** proprietà Proprietà di un oggetto. Consente di aggiungere o sostituire pagine.                                                              |
| [**Gestore dell'immagine di anteprima**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Fornisce un'immagine per rappresentare l'elemento.                                                                                                                                   |
| [**Gestore della finestra popup**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Fornisce testo popup quando l'utente passa il puntatore del mouse sull'oggetto .                                                                                               |
| [**Gestore di metadati**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)       | Fornisce accesso in lettura e scrittura ai metadati (proprietà) archiviati in un file. Può essere usato per estendere la visualizzazione Dettagli, le descrizioni comandi, la pagina delle proprietà e le funzionalità di raggruppamento. |



 

Altri non sono associati a un particolare tipo di file, ma vengono chiamati prima di alcune operazioni della shell.



| Gestore                                                            | Descrizione                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestore delle colonne](../lwef/column-handlers.md)                             | Chiamato da Windows Explorer prima di visualizzare la visualizzazione Dettagli di una cartella. Consente di aggiungere colonne personalizzate alla visualizzazione Dettagli.        |
| [Gestore hook di copia](how-to-create-copy-hook-handlers.md)          | Chiamato quando una cartella o un oggetto stampante sta per essere spostato, copiato, eliminato o rinominato. Consente di approvare o veto l'operazione.   |
| [Gestore di trascinamento della selezione](context-menu-handlers.md)                 | Chiamato quando un file viene trascinato con il pulsante destro del mouse. Consente di modificare il menu di scelta rapida visualizzato.                     |
| [Gestore di sovrimpressione dell'icona](how-to-implement-icon-overlay-handlers.md) | Chiamato prima che venga visualizzata l'icona di un file. Consente di specificare una sovrimpressione per l'icona del file.                                          |
| [Gestore della ricerca](../lwef/search-handlers.md)                             | Chiamato per avviare un motore di ricerca. Consente di implementare un motore di ricerca personalizzato accessibile dal menu **Start** o Windows Explorer. |



 

I dettagli su come implementare gestori di estensioni specifici sono descritti nelle sezioni elencate in precedenza. Per discussioni sui problemi di implementazione comuni a tutti i gestori di estensioni della shell, vedere questi argomenti:

-   [Inizializzazione dei gestori di estensioni della shell](int-shell-exts.md)
-   [Registrazione dei gestori di estensioni della shell](reg-shell-exts.md)

 

 
