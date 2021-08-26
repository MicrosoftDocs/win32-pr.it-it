---
description: Windows Il programma di installazione contiene funzionalità che consentono agli sviluppatori di pacchetti di installazione di creare un'interfaccia utente grafica (GUI) che viene visualizzata all'utente finale durante l'installazione.
ms.assetid: 58ef0043-fb30-4f64-9291-e703d7a28bb5
title: Informazioni sul Interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff4613e82bc25a0a9555904a6bab276b31e16642186401bbb5cc0caff58e973
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996981"
---
# <a name="about-the-user-interface"></a>Informazioni sul Interfaccia utente

Windows Il programma di installazione contiene funzionalità che consentono agli sviluppatori di pacchetti di installazione di creare un'interfaccia utente grafica (GUI) che viene visualizzata all'utente finale durante l'installazione. Questa interfaccia utente può presentare il [comportamento della procedura guidata](user-interface-wizard-behavior.md)dell'interfaccia utente, visualizzare finestre di dialogo e finestre di dialogo e presentare controlli interattivi agli utenti durante l'installazione.

L'interfaccia utente interna del programma di installazione viene gestita e controllata tramite un set di tabelle di database all Windows installer stesso. Il programma di installazione fornisce solo un piccolo set di finestre di dialogo predefinite destinate alla gestione dei messaggi di errore e informativi. Tutte le finestre di dialogo personalizzate devono essere create dall'autore del pacchetto.

Non esiste un'API Windows Installer specifica per consentire a un autore di pacchetti di creare un'interfaccia utente a livello di codice. È possibile usare l'API microsoft Windows per creare un'interfaccia utente a livello di codice. Tuttavia, è consigliabile che gli autori di pacchetti usino l'interfaccia utente interna fornita.

Gli autori di pacchetti del programma di installazione creano finestre di dialogo personalizzate immettendo il nome della finestra di dialogo personalizzata nella colonna "Dialog" della tabella della finestra di dialogo e specificando le dimensioni, la posizione e altri attributi usando le \_ colonne rimanenti.

Windows Il programma di installazione implementa anche una serie di controlli standard che l'autore di un pacchetto può inserire nelle finestre di dialogo. Non tutti i controlli Windows Microsoft standard sono disponibili e non è possibile creare controlli personalizzati per l'uso con l'interfaccia utente del programma di installazione.

I controlli vengono creati in una finestra di dialogo specifica immettendo il nome della finestra di dialogo, la chiave primaria per la voce della finestra di dialogo nella tabella della finestra di dialogo, nel secondo campo della tabella dei controlli e specificando le dimensioni, la posizione e altri attributi del controllo usando le colonne rimanenti.

I controlli attivi devono essere collegati a un ControlEvent nella tabella [ControlEvent](controlevent-table.md) per consentire l'interazione dell'utente con l'installazione. I controlli passivi che ricevono e visualizzano informazioni devono essere sottoscritti a un ControlEvent appropriato nella [tabella EventMapping](eventmapping-table.md).

Per altre informazioni su ControlEvents, vedere [Cenni preliminari su ControlEvent.](controlevent-overview.md) Si noti che un controllo pubblica un ControlEvent se elencato nella tabella ControlEvent e sottoscrive un evento se elencato nella tabella EventMapping.

La visualizzazione dell'interfaccia utente del programma di installazione durante l'installazione viene gestita tramite le tabelle delle sequenze dell'interfaccia utente: [Tabella InstallUISequence](installuisequence-table.md)e [Tabella AdminUISequence](adminuisequence-table.md). Una di queste tabelle di sequenza viene eseguita a seconda dell'azione di primo livello che ha avviato l'installazione: [INSTALL,](install-action.md) [ADMIN](admin-action.md)o [ADVERTISE.](advertise-action.md)

Per altre informazioni sull'implementazione di un'interfaccia utente nel programma di installazione di [Windows,](using-the-user-interface.md)vedere Uso di Interfaccia utente , [schema di Interfaccia utente](user-interface-schema.md), nonché i singoli argomenti per le finestre di dialogo e i controlli.

 

 



