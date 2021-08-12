---
title: Introduzione alle procedure guidate di pubblicazione
description: Windows XP introduce la Pubblicazione guidata sul Web e l'Ordinazione guidata stampa online.
ms.assetid: da3adc24-5b37-48b5-b055-d5bfa572defd
keywords:
- pubblicazione guidata, informazioni
- Pubblicazione guidata sul Web, informazioni
- Online Print Ordering Wizard,about
- pubblicazione guidata, Pubblicazione guidata sul Web
- pubblicazione guidata, Online Print Ordering Wizard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d576d04579847d2e65bbc59399d11689259f8e64823a3c3068cafad912ff8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246685"
---
# <a name="publishing-wizards-introduction"></a>Introduzione alle procedure guidate di pubblicazione

Windows XP introduce la Pubblicazione guidata sul Web e l'Ordinazione guidata stampa online. In base allo stesso framework, queste procedure guidate forniscono all'utente un semplice meccanismo per la pubblicazione di contenuto in un sito Web o per l'ordinamento delle stampe effettuate da file di immagine digitale. Il vantaggio di queste procedure guidate consiste nella possibilità di ospitare contenuto HTML da provider diversi all'interno delle pagine della procedura guidata, in modo che l'aspetto, la procedura e le opzioni utente disponibili siano completamente controllati dal provider e possano essere modificati in qualsiasi momento senza influire sulla procedura guidata client che li ospita. Anche se queste procedure guidate esistenti sono state create tenendo in considerazione la creazione dell'immagine digitale, il framework e i concetti possono essere usati per molti altri scopi, ad esempio un servizio di stampa di documenti o come metodo per condividere immagini con amici e famiglia.

-   [Come funziona?](#how-does-it-work)
-   [Documentazione della Pubblicazione guidata](#publishing-wizard-documentation)

## <a name="how-does-it-work"></a>Come funziona?

L'esperienza utente per la Pubblicazione guidata sul Web e l'Ordinamento guidato stampa online è simile, ma il punto di ingresso per ogni procedura guidata è diverso. Per la Pubblicazione guidata sul Web, un'attività intitolata Pubblica questa cartella sul **Web** è disponibile nell'elenco **Attività** file e cartelle a sinistra della maggior parte delle visualizzazioni cartella. Il testo dell'attività varia in base al contenuto selezionato. Ad esempio, se è selezionato un file, l'attività legge **Pubblica questo file** sul Web come illustrato nell'esempio seguente.

![Attività relative a file e cartelle](images/shell-pubwiz-tasks.png)

L'utente fa clic sull'attività per avviare la procedura guidata. Procedendo con la procedura guidata, all'utente viene visualizzato un elenco di provider, come illustrato nell'esempio seguente. I provider di servizi Internet (ISP) possono sviluppare e registrare le proprie pagine del provider da visualizzare in questo elenco.

![elenco di provider della pubblicazione guidata](images/shell-pubwiz-provs.png)

Dopo aver scelto un provider, la procedura guidata si connette al sito e la prima pagina HTML viene scaricata per la visualizzazione nella procedura guidata. Se gli utenti non hanno un account con il provider selezionato, hanno la possibilità di configurarne uno.

Più pagine HTML sono contenute all'interno di una singola pagina della procedura guidata. in altre parole, l'handle della pagina della procedura guidata che ospita le pagine HTML rimane costante. Le pagine HTML vengono esposte nel riquadro centrale come per qualsiasi pagina standard della procedura guidata. Il sito del provider fornisce metodi per controllare la  posizione dei pulsanti **Indietro** **,** Avanti e Annulla della procedura guidata durante la visualizzazione delle pagine HTML. All'interno di tali pagine HTML, agli utenti potrebbe essere richiesto di specificare una cartella in cui copiare i file o salvare il nome di un sito Web da creare. Dopo che un utente ha completato tutti i passaggi necessari, il sito chiama un metodo per avviare il caricamento e restituire il controllo alla procedura guidata. La procedura guidata gestisce il caricamento ed eventuali elementi grafici di grande disposizione, ad esempio un indicatore di stato. Al termine del caricamento, il sito del provider può specificare un URL a cui l'utente può accedere dopo la chiusura della procedura guidata.

Nell'Ordinamento guidato stampa online l'attività Ordine stampa **online** viene visualizzata solo nelle cartelle immagini, ad esempio Immagini, come illustrato nell'esempio seguente. Il processo, tuttavia, è molto simile alla Pubblicazione guidata sul Web. Il sito del provider richiede agli utenti opzioni quali la selezione di immagini, le dimensioni di stampa, il numero di copie e le informazioni di pagamento.

![attività immagine](images/shell-pubwiz-pix.png)

## <a name="publishing-wizard-documentation"></a>Documentazione della Pubblicazione guidata

La Pubblicazione guidata sul Web e l'Ordinamento guidato stampa online sono descritti in dettaglio nei documenti seguenti. Vengono inoltre illustrate le istruzioni per lo sviluppo di applicazioni che devono essere ospitate da esse.

-   [Progettazione lato client](pubwiz-client.md)
-   [Progettazione lato server](pubwiz-server.md)
-   [Registrazione di un servizio](pubwiz-reg.md)
-   [Uso del manifesto di trasferimento](pubwiz-manifest.md)
-   [Trasferire lo schema del manifesto](/windows/desktop/shell/interfaces)

 

 