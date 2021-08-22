---
description: La funzione di callback CPlApplet elabora tutti i messaggi inviati a un Pannello di controllo elemento Windows. I messaggi inviati alla funzione sono in un ordine specifico. Con lo stesso token, l.cpl elemento richiede che i messaggi vengano elaborati in modo specifico.
ms.assetid: 70302698-f9d5-4de4-a662-4815002eea52
title: Pannello di controllo di messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e697c603b69790d17c4d6771666a1111fa6f968eb97a30256696921f133530d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719952"
---
# <a name="control-panel-message-processing"></a>Pannello di controllo di messaggi

La funzione di callback [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora tutti i messaggi inviati a un Pannello di controllo elemento Windows. I messaggi inviati alla funzione sono in un ordine specifico. Con lo stesso token, l.cpl elemento richiede che i messaggi vengano elaborati in modo specifico.

In primo luogo, [**la funzione CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) riceve il messaggio \_ CPL INIT Windows prima carica l'Pannello di controllo elemento. La funzione deve eseguire qualsiasi inizializzazione, ad esempio l'allocazione di memoria, e restituire un valore diverso da zero. Se **CPlApplet non** riesce a completare l'inizializzazione, deve restituire zero, indicando Windows per terminare la comunicazione e rilasciare la DLL.

Successivamente, se il messaggio CPL INIT ha avuto esito \_ positivo, Windows il messaggio \_ GETCOUNT CPL. La funzione deve quindi restituire il numero di Pannello di controllo supportati dal file .dll dati.

La [**funzione CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) riceve quindi un messaggio CPL INQUIRE e un messaggio \_ CPL NEWINQUIRE per ogni elemento Pannello di controllo supportato dal \_ file .dll. La funzione compila una struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) con informazioni sull'elemento, ad esempio il nome, l'icona e una stringa descrittiva. La maggior parte delle applicazioni deve elaborare il messaggio \_ CPL INQUIRE e ignorare il messaggio CPL \_ NEWINQUIRE. Il messaggio CPL INQUIRE fornisce informazioni in un formato che Windows memorizzare nella cache, con prestazioni \_ molto migliori. Il messaggio CPL NEWINQUIRE viene usato solo se è necessario modificare l'icona dell'elemento o visualizzare le stringhe in base allo \_ stato del computer. Pannello di controllo elementi che usano CPL NEWINQUIRE non possono essere trovati da una ricerca nel menu Start in Windows Vista perché si basa \_ sulla memorizzazione nella cache. 

La [**funzione CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) riceve quindi un messaggio DBLCLK CPL come notifica che l'utente ha scelto l'icona che rappresenta l'Pannello di controllo \_ elemento. La funzione potrebbe ricevere questo messaggio per un numero qualsiasi di volte. Il messaggio include l'identificatore dell'elemento e il puntatore **lpData** restituito nella struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) nella chiamata a [**CPL \_ INQUIRE**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE**](cpl-newinquire.md). La funzione deve visualizzare la finestra di dialogo corrispondente ed elaborare l'input utente successivo.

Oltre a CPL DBLCLK, il messaggio \_ STARTWPARMS CPL può essere inviato se un elemento Pannello di controllo viene richiamato con parametri di input, ad esempio da un prompt dei comandi o da un altro \_ programma. Il messaggio include l'identificatore dell'elemento insieme alla stringa di parametro aggiuntiva.

Prima che l'applicazione di controllo termini, [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) riceve il messaggio STOP CPL una volta per ogni Pannello di controllo elemento supportato dal \_ file .dll. Il messaggio include l'identificatore per l'elemento Pannello di controllo e il puntatore **lpData** restituito nella struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) nella chiamata a [**CPL \_ INQUIRE**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE**](cpl-newinquire.md). La funzione deve liberare la memoria allocata per la finestra di dialogo specificata.

Dopo l'ultimo messaggio CPL \_ STOP, [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) riceve un messaggio EXIT \_ CPL. La funzione deve liberare tutta la memoria allocata rimanente e annullare la registrazione di tutte le classi di finestre private che potrebbe aver registrato. Immediatamente dopo che la funzione viene restituita da questo messaggio, Windows rilascia l'Pannello di controllo chiamando la [**funzione FreeLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pannello di controllo elementi](control-panel-applications.md)
</dt> <dt>

[Linee guida sull'esperienza utente](user-experience-guidelines.md)
</dt> <dt>

[Registrazione di Pannello di controllo elementi](registering-control-panel-items.md)
</dt> <dt>

[Uso di CPLApplet](using-cplapplet.md)
</dt> <dt>

[Esecuzione di Pannello di controllo elementi](executing-control-panel-items.md)
</dt> <dt>

[Estensione degli elementi Pannello di controllo sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Assegnazione di Pannello di controllo categorie](assigning-control-panel-categories.md)
</dt> <dt>

[Creazione di collegamenti di attività ricercabili per un Pannello di controllo ricerca](creating-searchable-task-links.md)
</dt> <dt>

[Accesso al Pannello di controllo in Cassaforte in Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
