---
description: Windows Il programma di installazione contiene funzionalità per visualizzare un indicatore di stato in una finestra di dialogo di visualizzazione delle azioni.
ms.assetid: cfc2d974-4f2d-4f52-9835-eab1dc091c9b
title: Creazione di un controllo ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1074744220bde8734fe0cd1f65aa1037ff1f0cb26763a11845a7ea7f1b58e507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066161"
---
# <a name="authoring-a-progressbar-control"></a>Creazione di un controllo ProgressBar

Windows Il programma di installazione contiene funzionalità per visualizzare un indicatore di stato in una finestra di dialogo di visualizzazione delle azioni. Il [controllo ProgressBar](progressbar-control.md) rappresenta graficamente l'installazione di singoli componenti e segnala il tempo totale trascorso rispetto al tempo rimanente o il tempo totale approssimativo rimanente fino al completamento dell'installazione.

Per determinare il tempo totale previsto per l'installazione, il programma di installazione tiene traccia dei tick di avanzamento totali previsti da ogni azione durante la generazione dello script di esecuzione. Al termine della generazione dello script, viene archiviato il totale dei tick di avanzamento e viene avviata l'installazione.

I messaggi di stato che specificano il numero di tick di avanzamento trascorso vengono inviati al gestore di messaggi attivo durante l'esecuzione di ogni azione nello script. In ogni messaggio di stato, il programma di installazione trasmette [un oggetto SetProgress ControlEvent](setprogress-controlevent.md) alla finestra di dialogo attualmente attiva. La sequenza dell'interfaccia utente deve essere creata per creare la finestra di dialogo di visualizzazione dell'azione durante l'esecuzione dello script per ricevere i messaggi SetProgress ControlEvent dal programma di installazione.

Quando la finestra di dialogo di visualizzazione dell'azione riceve un oggetto SetProgress ControlEvent, controlla la tabella [EventMapping](eventmapping-table.md) per tutti i controlli che sottoscriveno ControlEvent. Il controllo ProgressBar nella finestra di dialogo di visualizzazione delle azioni viene sottoscritto con l'attributo del controllo Progress specificato nella colonna Attributi . L'attributo Progress Control specifica che al controllo ProgressBar verranno passati i valori "ticksSoFar" e "totalTicks" insieme a SetProgress ControlEvent. Il controllo indicatore di stato usa queste informazioni per far avanzare la barra grafica da sinistra a destra per un'installazione e da destra a sinistra per un'operazione [di rollback.](rollback-installation.md)

Inoltre, il programma di installazione trasmette un [Evento di controllo TimeRemaining](timeremaining-controlevent.md) su ogni messaggio di stato. Il tempo totale rimanente per l'installazione viene determinato calcolando innanzitutto la velocità di esecuzione, ovvero il numero totale di tick trascorsi diviso per il tempo totale dall'inizio dell'installazione. Il totale dei tick rimanenti diviso per la frequenza di esecuzione indica il tempo rimanente approssimativo.

Quando la finestra di dialogo di visualizzazione dell'azione riceve l'evento ControlEvent TimeRemaining, cerca di nuovo nella tabella EventMapping tutti i controlli sottoscritti. Per visualizzare il tempo rimanente, è necessario sottoscrivere un controllo Text per TimeRemaining ControlEvent con l'attributo di controllo [TimeRemaining](timeremaining-control-attribute.md) specificato nella colonna Attributi. [](text-control.md)

Il controllo Text sottoscritto esegue una query [nella tabella UIText](uitext-table.md) per una stringa di modello con parametri denominata "TimeRemaining". Questa stringa ha due parametri, \[ 1 \] per i minuti e \[ 2 per i \] secondi. Il controllo Text converte ogni valore in minuti e secondi, valuta la stringa del modello TimeRemaining e aggiorna il controllo di testo con le nuove informazioni.

Se il livello di visualizzazione dell'interfaccia utente è impostato su base o inferiore, il programma di installazione visualizza una finestra di dialogo predefinita contenente un indicatore di stato e un campo di testo TimeRemaining. Per altre informazioni, vedere [Interfaccia utente Levels.](user-interface-levels.md)

 

 



