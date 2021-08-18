---
description: Questa sezione riguarda principalmente il modo in cui gli sviluppatori di pacchetti di installazione creano un'interfaccia utente di installazione usando il database del programma di installazione e l'interfaccia utente interna.
ms.assetid: c04e32ba-08a9-49fe-9a4a-db258767f0b3
title: Utilizzo dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2303ddcdf589b69abb819ab1cdee9060f4918c1bd238e161677da7987300bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995991"
---
# <a name="using-the-user-interface"></a>Utilizzo dell'interfaccia utente

Questa sezione riguarda principalmente il modo in cui gli sviluppatori di pacchetti di installazione creano un'interfaccia utente di installazione usando il database del programma di installazione e l'interfaccia utente interna. Per altre informazioni sulla differenza tra un'interfaccia utente interna ed esterna, [vedere About the Interfaccia utente](about-the-user-interface.md).

Per visualizzare una sequenza di finestre di dialogo o un manifesto durante l'installazione, è necessario immettere il nome della finestra di dialogo nella colonna Azione della tabella della sequenza di azioni appropriata. Il nome della finestra di dialogo deve essere visualizzato nella tabella [InstallUISequence](installuisequence-table.md) o [AdminUISequence](adminuisequence-table.md) a seconda che l'interfaccia utente sia pianificata per l'esecuzione con l'azione [INSTALL](install-action.md), [ADVERTISE](advertise-action.md)o [ADMIN](admin-action.md).

Anche se il programma di installazione supporta la creazione di finestre di dialogo personalizzate e manifesti, esistono anche diversi nomi riservati per determinate sequenze di finestre di dialogo. Poiché il programma di installazione usa questi nomi quando si eseguono determinate azioni, questi nomi devono essere usati solo con i tipi di finestre di dialogo per cui sono riservate. Un elenco di questi nomi riservati e una descrizione di ognuna delle sequenze di finestre di dialogo speciali è disponibile in [Finestre di dialogo](dialog-boxes.md).

Le proprietà di ogni finestra di dialogo o manifesto nell'interfaccia utente devono essere specificate rispettivamente nelle tabelle [Dialog](dialog-table.md) e [BillBoard.](billboard-table.md) Lo stile di ogni finestra di dialogo deve essere specificato anche nella tabella Finestra di dialogo impostando il flag di [bit di stile della](dialog-style-bits.md) finestra di dialogo.

I controlli e il testo devono essere aggiunti alla finestra di dialogo e devono essere associati a [ControlEvents](controlevent-overview.md)per consentire all'utente di interagire con il processo di installazione. Per [altre informazioni su come](adding-controls-and-text.md) aggiungere controlli a una finestra di dialogo, vedere Aggiunta di controlli e testo.

Windows Il gestore interno dell'interfaccia utente del programma di installazione può mostrare o nascondere in modo selettivo le finestre di dialogo per controllare il livello di interattività dell'utente finale durante l'installazione. Questi livelli di interattività dell'utente finale vengono definiti completi, ridotti, di base e nessuno. Vedere [Interfaccia utente livelli .](user-interface-levels.md) per una descrizione completa di questi livelli UI.

Esistono due metodi per impostare il livello dell'interfaccia utente. Il livello dell'interfaccia utente può essere impostato a livello di codice con una chiamata a [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)e il primo parametro di **MsiSetInternalUI** specifica il livello dell'interfaccia utente. Gli sviluppatori di pacchetti possono anche impostare il livello dell'interfaccia utente usando l'opzione della [riga di comando](command-line-options.md) "/q".

Il comportamento di ogni livello dell'interfaccia utente è determinato dalla creazione del file .msi dallo sviluppatore del pacchetto. L'autore di un'interfaccia utente interna ha flessibilità nel comportamento di questi livelli per un pacchetto. La disponibilità di questi livelli dipende dalla creazione del pacchetto di installazione. L'autore deve specificare ogni finestra di dialogo e controllo nell'interfaccia utente nelle tabelle Dialog e Control.

-   Un'interfaccia utente completa presenta in genere il [comportamento](user-interface-wizard-behavior.md)della procedura guidata dell'interfaccia utente, ad esempio ogni finestra di dialogo in una sequenza contenente un **pulsante**>>successivo. Questa forma di interfaccia utente è familiare a molti utenti ed è il tipo più comune di interfaccia utente che un autore può creare. Il programma di installazione presenta una sequenza logica di finestre di dialogo e richiede all'utente di interagire con i controlli presenti in ogni finestra di dialogo.
-   Un'interfaccia utente ridotta in genere elimina la visualizzazione del comportamento della procedura guidata.
-   Un'interfaccia utente di base visualizza in genere solo i messaggi di stato per l'utente.
-   Un livello di interfaccia utente None indica un'installazione invisibile all'utente.

Windows Il programma di installazione fornisce un indicatore univoco dell'indicatore di stato nel controllo [ProgressBar](progressbar-control.md) che visualizza all'utente una stima del tempo totale rimanente fino al completamento dell'installazione. Per altre informazioni sull'indicatore di stato, vedere [Creazione di un controllo ProgressBar](authoring-a-progressbar-control.md).

Gli autori dell'interfaccia utente devono facilitare l'accessibilità dell'applicazione o del prodotto per tutti gli utenti. Per altre informazioni sul programma di Active Accessibility e Windows, vedere [Accessibilità](accessibility.md).

Per altre informazioni sulla creazione di un'interfaccia utente, vedere Aggiunta di controlli e [testo,](adding-controls-and-text.md)Creazione di un controllo [ProgressBar,](authoring-a-progressbar-control.md) [Creazione](authoring-disk-prompt-messages.md)di messaggi di richiesta su disco, Creazione di un ['attesa condizionale' . . . Finestra di messaggio](authoring-a-conditional-please-wait-------message-box.md)e [anteprima dell'Interfaccia utente](previewing-the-user-interface.md). Per altre informazioni sugli autori di manifesti, vedere [Visualizzazione di manifesti in un dialogo non modali](displaying-billboards-on-a-modeless-dialog.md)

A partire da Windows Installer 4.5, un'interfaccia utente personalizzata può essere incorporata nel pacchetto Windows Installer. Per un esempio di un'interfaccia utente personalizzata incorporata, vedere [Uso di un'interfaccia utente incorporata.](using-an-embedded-ui.md)

 

 



