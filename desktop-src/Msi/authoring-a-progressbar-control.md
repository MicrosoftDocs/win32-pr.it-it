---
description: Windows Installer contiene la funzionalità per visualizzare un indicatore di stato in una finestra di dialogo di visualizzazione dell'azione.
ms.assetid: cfc2d974-4f2d-4f52-9835-eab1dc091c9b
title: Creazione di un controllo ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b872ed2dd36fb8ed04ee48fd69e4680fce002a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881102"
---
# <a name="authoring-a-progressbar-control"></a>Creazione di un controllo ProgressBar

Windows Installer contiene la funzionalità per visualizzare un indicatore di stato in una finestra di dialogo di visualizzazione dell'azione. Il [controllo ProgressBar](progressbar-control.md) rappresenta graficamente l'installazione di singoli componenti e segnala il tempo totale trascorso in relazione al tempo rimanente o al tempo totale approssimativo rimanente fino al completamento dell'installazione.

Per determinare il tempo totale previsto per l'installazione, il programma di installazione tiene traccia dei cicli di avanzamento totali previsti da ogni azione durante la generazione dello script di esecuzione. Al termine della generazione dello script, il totale del segno di avanzamento viene archiviato e viene avviata l'installazione.

I messaggi di stato che descrivono in dettaglio il numero trascorso di cicli di avanzamento vengono inviati al gestore di messaggi attivi quando ogni azione nello script viene eseguita. In ogni messaggio di stato, il programma di installazione trasmette un [ControlEvent di avanzamento](setprogress-controlevent.md) alla finestra di dialogo attualmente attiva. La sequenza dell'interfaccia utente deve essere creata per creare la finestra di dialogo visualizzazione azione durante l'esecuzione dello script per ricevere i messaggi di ControlEvent di stato dal programma di installazione.

Quando la finestra di dialogo visualizzazione azione riceve un ControlEvent di avanzamento, verifica la [tabella EventMapping](eventmapping-table.md) per tutti i controlli che sottoscrivono ControlEvent. Il controllo ProgressBar nella finestra di dialogo visualizzazione azione è stato sottoscritto con l'attributo di controllo progress specificato nella colonna attributi. L'attributo di controllo progress specifica che al controllo ProgressBar verranno passati i valori "ticksSoFar" e "totalTicks" insieme al ControlEvent di avanzamento. Il controllo indicatore di stato USA queste informazioni per far avanzare la barra grafica da sinistra a destra per un'installazione e da destra a sinistra per un'operazione di [rollback](rollback-installation.md) .

Inoltre, il programma di installazione trasmette un [ControlEvent TimeRemaining](timeremaining-controlevent.md) a ogni messaggio di stato. Il tempo totale rimanente per l'installazione viene determinato calcolando prima la velocità di esecuzione, ovvero il numero totale di cicli trascorsi per il tempo totale trascorso dall'inizio dell'installazione. Il totale dei cicli rimanenti divisi per la velocità di esecuzione indica il tempo di permanenza approssimativo.

Quando la finestra di dialogo visualizzazione azione riceve il ControlEvent TimeRemaining, Cerca nuovamente nella tabella EventMapping i controlli sottoscritti. Per visualizzare il tempo rimanente, è necessario che un [controllo di testo](text-control.md) abbia sottoscritto il ControlEvent TimeRemaining con l' [attributo di controllo TimeRemaining](timeremaining-control-attribute.md) specificato nella colonna attributi.

Il controllo testo sottoscritto esegue una query sulla [tabella UIText](uitext-table.md) per una stringa di modello con parametri denominata "TimeRemaining". Questa stringa ha due parametri, \[ 1 \] per i minuti e \[ 2 \] per i secondi. Il controllo testo converte ogni valore in minuti e secondi, valuta la stringa del modello TimeRemaining e aggiorna il controllo di testo con le nuove informazioni.

Se il livello di visualizzazione dell'interfaccia utente è impostato su di base o inferiore, il programma di installazione visualizza una finestra di dialogo predefinita contenente un indicatore di stato e un campo di testo TimeRemaining. Per ulteriori informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

 

 



