---
description: La funzione di callback CPlApplet elabora tutti i messaggi inviati a un elemento del pannello di controllo da Windows. I messaggi inviati alla funzione sono in un ordine specifico. Per lo stesso token, l'elemento. cpl richiede che i messaggi vengano elaborati in modo specifico.
ms.assetid: 70302698-f9d5-4de4-a662-4815002eea52
title: Elaborazione del messaggio del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8b43c6e265030279a6644547f41e3630208325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968043"
---
# <a name="control-panel-message-processing"></a>Elaborazione del messaggio del pannello di controllo

La funzione di callback [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) elabora tutti i messaggi inviati a un elemento del pannello di controllo da Windows. I messaggi inviati alla funzione sono in un ordine specifico. Per lo stesso token, l'elemento. cpl richiede che i messaggi vengano elaborati in modo specifico.

Prima di tutto, la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) riceve il \_ messaggio cpl init quando Windows carica l'elemento del pannello di controllo. La funzione deve eseguire qualsiasi inizializzazione, ad esempio l'allocazione della memoria e restituire un valore diverso da zero. Se **CPlApplet** non è in grado di completare l'inizializzazione, deve restituire zero, indirizzando le finestre per terminare la comunicazione e rilasciare la dll.

Successivamente, se il \_ messaggio cpl init ha avuto esito positivo, Windows invierà il \_ messaggio cpl GetCount. La funzione deve quindi restituire il numero di elementi del pannello di controllo supportati dal file con estensione dll.

La funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) riceve quindi un \_ messaggio di richiesta cpl e un messaggio cpl \_ NEWINQUIRE per ogni elemento del pannello di controllo supportato dal file con estensione dll. La funzione compila una struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) con le informazioni sull'elemento, ad esempio il nome, l'icona e una stringa descrittiva. La maggior parte delle applicazioni deve elaborare il \_ messaggio cpl Inquirer e ignorare il \_ messaggio cpl NEWINQUIRE. Il \_ messaggio di richiesta cpl fornisce informazioni in un modulo che può essere memorizzato nella cache di Windows, con un conseguente miglioramento delle prestazioni. Il \_ messaggio cpl NEWINQUIRE viene usato solo se è necessario modificare l'icona dell'elemento o visualizzare le stringhe in base allo stato del computer. Gli elementi del pannello di controllo che usano CPL \_ NEWINQUIRE non sono stati trovati da una ricerca del menu **Start** in Windows Vista perché si basa sulla memorizzazione nella cache.

La funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) successivamente riceve un \_ messaggio cpl DBLCLK come notifica che l'utente ha scelto l'icona che rappresenta l'elemento del pannello di controllo. La funzione può ricevere questo messaggio un numero qualsiasi di volte. Il messaggio include l'identificatore dell'elemento e il puntatore **lpData** restituito nella struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) nella chiamata a [**cpl \_ Inquirer**](cpl-inquire.md) o [**cpl \_ NEWINQUIRE**](cpl-newinquire.md). La funzione dovrebbe visualizzare la finestra di dialogo corrispondente ed elaborare l'input dell'utente successivo.

Oltre a CPL \_ DblClk, \_ è possibile inviare il messaggio cpl STARTWPARMS se viene richiamato un elemento del pannello di controllo con parametri di input, ad esempio da un prompt dei comandi o da un altro programma. Il messaggio include l'identificatore dell'elemento insieme alla stringa di parametro aggiuntiva.

Prima di terminare l'applicazione di controllo, [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) riceve il \_ messaggio di arresto cpl una volta per ogni elemento del pannello di controllo supportato dal file con estensione dll. Il messaggio include l'identificatore per l'elemento del pannello di controllo e il puntatore **lpData** restituito nella struttura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) nella chiamata a [**cpl \_ Inquirer**](cpl-inquire.md) o [**cpl \_ NEWINQUIRE**](cpl-newinquire.md). La funzione deve liberare la memoria allocata per la finestra di dialogo specificata.

Dopo l'ultimo \_ messaggio di arresto cpl, [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) riceve un \_ messaggio di uscita cpl. La funzione deve liberare tutta la memoria allocata rimanente e annullare la registrazione di tutte le classi della finestra privata che potrebbero essere state registrate. Subito dopo la restituzione della funzione da questo messaggio, Windows rilascia l'elemento del pannello di controllo chiamando la funzione [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi del pannello di controllo](control-panel-applications.md)
</dt> <dt>

[Linee guida sull'esperienza utente](user-experience-guidelines.md)
</dt> <dt>

[Registrazione degli elementi del pannello di controllo](registering-control-panel-items.md)
</dt> <dt>

[Uso di CPLApplet](using-cplapplet.md)
</dt> <dt>

[Esecuzione degli elementi del pannello di controllo](executing-control-panel-items.md)
</dt> <dt>

[Estensione degli elementi del pannello di controllo di sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Assegnazione delle categorie del pannello di controllo](assigning-control-panel-categories.md)
</dt> <dt>

[Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo](creating-searchable-task-links.md)
</dt> <dt>

[Accesso al pannello di controllo in modalità provvisoria in Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
