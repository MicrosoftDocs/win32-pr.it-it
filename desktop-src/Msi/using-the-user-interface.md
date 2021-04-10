---
description: Questa sezione riguarda principalmente il modo in cui gli sviluppatori di pacchetti di installazione creano un'interfaccia utente di installazione usando il database del programma di installazione e l'interfaccia utente interna.
ms.assetid: c04e32ba-08a9-49fe-9a4a-db258767f0b3
title: Utilizzo dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714d41ab6b91bb0f3ce519887f7004f919c5c6b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231534"
---
# <a name="using-the-user-interface"></a>Utilizzo dell'interfaccia utente

Questa sezione riguarda principalmente il modo in cui gli sviluppatori di pacchetti di installazione creano un'interfaccia utente di installazione usando il database del programma di installazione e l'interfaccia utente interna. Per ulteriori informazioni sulla differenza tra un'interfaccia utente interna ed esterna, vedere [informazioni sull'interfaccia utente](about-the-user-interface.md).

Per visualizzare una sequenza o un Billboard della finestra di dialogo durante l'installazione, è necessario immettere il nome della finestra di dialogo nella colonna azione della tabella delle sequenze di azione appropriata. Il nome della finestra di dialogo deve essere visualizzato nella [tabella](adminuisequence-table.md) [InstallUISequence](installuisequence-table.md) o AdminUISequence a seconda che l'interfaccia utente sia pianificata per l'esecuzione con l'azione di [installazione](install-action.md), [annuncio](advertise-action.md)o [Amministrazione](admin-action.md).

Sebbene il programma di installazione supporti la creazione di finestre di dialogo e cartelloni personalizzati, è anche possibile fare un certo numero di nomi riservati per determinate sequenze della finestra di dialogo. Poiché il programma di installazione utilizza questi nomi durante l'esecuzione di determinate azioni, questi nomi devono essere utilizzati solo con i tipi di finestre di dialogo per cui sono riservati. Nelle [finestre di dialogo](dialog-boxes.md)viene fornito un elenco di questi nomi riservati e una descrizione di ogni sequenza di finestra di dialogo speciale.

Le proprietà di ogni finestra di dialogo o Billboard nell'interfaccia utente devono essere specificate rispettivamente nelle tabelle [Dialog](dialog-table.md) e [Billboard](billboard-table.md) . Lo stile di ogni finestra di dialogo deve essere specificato anche nella tabella della finestra di dialogo impostando il flag di [bit dello stile della finestra](dialog-style-bits.md) di dialogo.

È necessario aggiungere i controlli e il testo alla finestra di dialogo, che devono essere associati a [ControlEvents](controlevent-overview.md), per consentire all'utente di interagire con il processo di installazione. Per ulteriori informazioni su come aggiungere controlli a una finestra di dialogo, vedere [aggiunta di controlli e testo](adding-controls-and-text.md) .

Windows Installer gestore dell'interfaccia utente interno può visualizzare o nascondere in modo selettivo le finestre di dialogo per controllare il livello di interattività dell'utente finale durante l'installazione. Questi livelli di interattività dell'utente finale sono detti full, Reduced, Basic e None. Vedere [livelli di interfaccia utente](user-interface-levels.md). per una descrizione completa di questi UIlevels.

Sono disponibili due metodi per impostare il livello dell'interfaccia utente. Il livello di interfaccia utente può essere impostato a livello di codice con una chiamata a [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)e il primo parametro di **MsiSetInternalUI** specifica il livello dell'interfaccia utente. Gli sviluppatori di pacchetti possono inoltre impostare il livello di interfaccia utente utilizzando l' [opzione della riga di comando](command-line-options.md) "/q".

Il comportamento di ogni livello dell'interfaccia utente è determinato dalla creazione del file con estensione msi da parte dello sviluppatore del pacchetto. L'autore di un'interfaccia utente interna dispone di flessibilità nel modo in cui questi livelli si comportano per un pacchetto. La disponibilità di questi livelli dipende dalla creazione del pacchetto di installazione. L'autore deve specificare ogni finestra di dialogo e il controllo nell'interfaccia utente nelle tabelle Dialog e Control.

-   Un'interfaccia utente completa in genere presenta il [comportamento della procedura guidata dell'interfaccia utente](user-interface-wizard-behavior.md), ad esempio ogni finestra di dialogo in una sequenza contenente un pulsante **>>successivo** . Questa forma di interfaccia utente è familiare a molti utenti ed è il tipo più comune di interfaccia utente che può essere creato da un autore. Il programma di installazione presenta una sequenza logica di finestre di dialogo e chiede all'utente di interagire con i controlli disponibili in ogni finestra di dialogo.
-   Un'interfaccia utente ridotta in genere disattiva la visualizzazione del comportamento della procedura guidata.
-   Un'interfaccia utente di base in genere Visualizza solo i messaggi di stato per l'utente.
-   Un livello dell'interfaccia utente None indica un'installazione invisibile all'utente.

Windows Installer fornisce un indicatore di stato univoco nel [controllo ProgressBar](progressbar-control.md) che visualizza all'utente una stima del tempo totale rimanente fino al completamento dell'installazione. Per ulteriori informazioni sull'indicatore di stato, vedere la pagina relativa alla [creazione di un controllo ProgressBar](authoring-a-progressbar-control.md).

Gli autori dell'interfaccia utente devono facilitare l'accessibilità dell'applicazione o del prodotto per tutti gli utenti. Per ulteriori informazioni su Active Accessibility e Windows Installer, vedere [accessibilità](accessibility.md).

Per ulteriori informazioni sulla creazione di un'interfaccia utente, vedere [aggiunta di controlli e testo](adding-controls-and-text.md), [creazione di un controllo ProgressBar](authoring-a-progressbar-control.md), [creazione di messaggi di richiesta del disco](authoring-disk-prompt-messages.md), [creazione di un condizionale "attendere..." MessageBox](authoring-a-conditional-please-wait-------message-box.md)e [anteprima dell'interfaccia utente](previewing-the-user-interface.md). Per ulteriori informazioni sui manifesti dell'autore, vedere [visualizzazione di manifesti in una finestra di dialogo non modale](displaying-billboards-on-a-modeless-dialog.md)

A partire da Windows Installer 4,5 un'interfaccia utente personalizzata può essere incorporata all'interno del pacchetto di Windows Installer. Per un esempio di un'interfaccia utente personalizzata incorporata, vedere [uso di un'interfaccia utente incorporata](using-an-embedded-ui.md).

 

 



