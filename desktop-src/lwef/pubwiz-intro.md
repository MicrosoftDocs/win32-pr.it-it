---
title: Introduzione alla pubblicazione delle procedure guidate
description: In Windows XP sono stati introdotti la pubblicazione guidata sul Web e l'ordinamento guidato stampa online.
ms.assetid: da3adc24-5b37-48b5-b055-d5bfa572defd
keywords:
- procedure guidate di pubblicazione, informazioni
- Pubblicazione guidata sul Web, informazioni
- Procedura guidata per l'ordine di stampa online, informazioni
- pubblicazione guidata, pubblicazione guidata sul Web
- procedure guidate di pubblicazione, ordinamento guidato stampa online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b4e6d3c515edae23d0e74f550e000bdfdfacf03
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472798"
---
# <a name="publishing-wizards-introduction"></a>Introduzione alla pubblicazione delle procedure guidate

In Windows XP sono stati introdotti la pubblicazione guidata sul Web e l'ordinamento guidato stampa online. In base allo stesso Framework, queste procedure guidate forniscono all'utente un meccanismo semplice per la pubblicazione di contenuto in un sito Web o per l'ordinamento di stampe effettuate da file di immagine digitali. Il vantaggio di queste procedure guidate risiede nella capacità di ospitare contenuto HTML da provider diversi nelle pagine della procedura guidata, in modo che l'aspetto, la procedura e le opzioni utente disponibili siano completamente controllati dal provider e possano essere modificati in qualsiasi momento senza influire sulla procedura guidata client che li ospita. Sebbene queste procedure guidate esistenti siano state create con la creazione di immagini digitali, è possibile usare il Framework e i concetti per molti altri scopi, ad esempio un servizio di stampa di documenti o come metodo di condivisione di immagini con amici e parenti.

-   [Come funziona?](#how-does-it-work)
-   [Documentazione della pubblicazione guidata](#publishing-wizard-documentation)

## <a name="how-does-it-work"></a>Come funziona?

L'esperienza utente per la pubblicazione guidata sul Web e l'ordinamento guidato di stampa online è simile, ma il punto di ingresso per ogni procedura guidata è diverso. Per la pubblicazione guidata sul Web, un'attività denominata **pubblica questa cartella sul Web** è disponibile dall'elenco **attività file e cartelle** a sinistra della maggior parte delle visualizzazioni cartella. Il testo per l'attività varia in base al contenuto selezionato. Se, ad esempio, si seleziona un file, l'attività legge la **pubblicazione del file sul Web** , come illustrato nell'esempio seguente.

![attività di file e cartelle](images/shell-pubwiz-tasks.png)

L'utente fa clic sull'attività per avviare la procedura guidata. Continuando con la procedura guidata, all'utente viene visualizzato un elenco di provider, come illustrato nell'esempio seguente. I provider di servizi Internet (ISP) possono sviluppare e registrare le proprie pagine del provider da visualizzare in questo elenco.

![elenco dei provider della procedura guidata di pubblicazione](images/shell-pubwiz-provs.png)

Una volta scelto un provider, la procedura guidata si connette al sito e la prima pagina HTML viene scaricata per la visualizzazione nella procedura guidata. Se gli utenti non dispongono di un account con il provider selezionato, avranno la possibilità di configurarne uno.

All'interno di una singola pagina della procedura guidata sono contenute più pagine HTML. in altre parole, l'handle della pagina della procedura guidata che ospita il processo di pagine HTML rimane costante. Le pagine HTML sono esposte nel riquadro centrale come con qualsiasi pagina della procedura guidata standard. Il sito del provider fornisce i metodi per controllare la posizione in cui vengono visualizzati i pulsanti **indietro**, **Avanti** e **Annulla** quando vengono visualizzate le pagine HTML. All'interno di queste pagine HTML, agli utenti potrebbe essere richiesto di specificare una cartella in cui è possibile copiare i file o salvare il nome di un sito Web che si desidera creare. Dopo che un utente ha completato tutti i passaggi necessari, il sito chiama un metodo per avviare il caricamento, restituendo il controllo alla procedura guidata. La procedura guidata gestisce il caricamento e gli eventuali elementi grafici di supervisore, ad esempio un indicatore di stato. Al termine del caricamento, il sito del provider può specificare un URL in cui l'utente può passare dopo la chiusura della procedura guidata.

Nella procedura guidata per l'ordine di stampa online, l'ordine delle attività **stampa online** viene visualizzato solo in cartelle immagini, ad esempio immagini personali, mostrate nell'esempio seguente. Tuttavia, il processo è molto simile alla pubblicazione guidata sul Web. Il sito del provider richiede agli utenti opzioni quali la selezione delle immagini, le dimensioni di stampa, il numero di copie e le informazioni di pagamento.

![attività immagine](images/shell-pubwiz-pix.png)

## <a name="publishing-wizard-documentation"></a>Documentazione della pubblicazione guidata

La pubblicazione guidata sul Web e l'ordinamento guidato stampa online sono descritti in dettaglio nei documenti seguenti. Sono inoltre illustrate le istruzioni per lo sviluppo di applicazioni da ospitare.

-   [Progettazione lato client](pubwiz-client.md)
-   [Progettazione lato server](pubwiz-server.md)
-   [Registrazione di un servizio](pubwiz-reg.md)
-   [Utilizzo del manifesto di trasferimento](pubwiz-manifest.md)
-   [Trasferimento dello schema del manifesto](/windows/desktop/shell/interfaces)

 

 