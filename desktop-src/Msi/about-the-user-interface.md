---
description: Windows Installer contiene funzionalità che consentono agli sviluppatori di pacchetti di installazione di creare un'interfaccia utente grafica (GUI) che viene visualizzata all'utente finale durante l'installazione.
ms.assetid: 58ef0043-fb30-4f64-9291-e703d7a28bb5
title: Informazioni sull'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8639a19c5ec045d77cb90648323388d5cb6e452
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881174"
---
# <a name="about-the-user-interface"></a>Informazioni sull'interfaccia utente

Windows Installer contiene funzionalità che consentono agli sviluppatori di pacchetti di installazione di creare un'interfaccia utente grafica (GUI) che viene visualizzata all'utente finale durante l'installazione. Questa interfaccia utente può presentare il [comportamento della procedura guidata dell'interfaccia utente](user-interface-wizard-behavior.md), visualizzare le finestre di dialogo e i tabelloni e presentare controlli interattivi agli utenti durante l'installazione.

L'interfaccia utente interna del programma di installazione viene gestita e controllata tramite un set di tabelle di database all'interno Windows Installer stesso. Il programma di installazione fornisce solo un piccolo set di finestre di dialogo predefinite destinate alla gestione dei messaggi di errore e informazioni. Tutte le finestre di dialogo personalizzate devono essere create dall'autore del pacchetto.

Non sono disponibili API Windows Installer specifiche per consentire a un autore di pacchetti di creare un'interfaccia utente a livello di codice. Per creare un'interfaccia utente a livello di codice, è possibile usare l'API di Microsoft Windows. Tuttavia, è consigliabile che gli autori dei pacchetti usino l'interfaccia utente interna fornita.

Gli autori dei pacchetti di installazione creano finestre di dialogo personalizzate immettendo il nome della finestra di dialogo personalizzata nella \_ colonna "finestra di dialogo" della tabella della finestra di dialogo e specificando le dimensioni, la posizione e altri attributi usando le colonne rimanenti.

Windows Installer implementa inoltre una serie di controlli standard che un autore di pacchetti può inserire nelle finestre di dialogo. Non tutti i controlli standard di Microsoft Windows sono disponibili e non è possibile creare controlli personalizzati per l'uso con l'interfaccia utente del programma di installazione.

I controlli vengono creati in una finestra di dialogo specifica immettendo il nome della finestra di dialogo, la chiave primaria per la voce della finestra di dialogo nella tabella della finestra di dialogo, nel secondo campo della tabella di controllo e specificando le dimensioni, la posizione e altri attributi del controllo utilizzando le colonne rimanenti.

Per consentire l'interazione dell'utente con l'installazione di, è necessario che i controlli attivi siano collegati a un ControlEvent nella [tabella ControlEvent](controlevent-table.md) . I controlli passivi che ricevono e visualizzano le informazioni devono essere sottoscritti a un ControlEvent appropriato nella [tabella EventMapping](eventmapping-table.md).

Per altre informazioni su ControlEvents, vedere [Panoramica di ControlEvent](controlevent-overview.md). Si noti che un controllo pubblica un ControlEvent se elencato nella tabella ControlEvent e sottoscrive un evento se elencato nella tabella EventMapping.

La visualizzazione dell'interfaccia utente del programma di installazione viene gestita tramite le tabelle di sequenza dell'interfaccia utente: [InstallUISequence Table](installuisequence-table.md)e [AdminUISequence Table](adminuisequence-table.md). Una di queste tabelle di sequenza viene eseguita a seconda dell'azione di primo livello che ha avviato l'installazione: [Install](install-action.md), [admin](admin-action.md)o [advertise](advertise-action.md).

Per ulteriori informazioni sull'implementazione di un'interfaccia utente in Windows Installer, vedere [utilizzo dell'interfaccia utente](using-the-user-interface.md), [dello schema dell'interfaccia utente](user-interface-schema.md), nonché dei singoli argomenti per le finestre di dialogo e i controlli.

 

 



