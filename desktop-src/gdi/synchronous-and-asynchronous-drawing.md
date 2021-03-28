---
description: La maggior parte del disegno eseguita durante l'elaborazione del messaggio di disegno WM \_ è asincrona, ovvero si verifica un ritardo tra il momento in cui una parte della finestra viene invalidata e l'ora di invio del disegno WM \_ .
ms.assetid: c4eac615-6526-4ca6-854b-b4a598da13a4
title: Disegno sincrono e asincrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80dd5d5d63cbe10d19ec98e9f5dc9ae9163c18a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968344"
---
# <a name="synchronous-and-asynchronous-drawing"></a>Disegno sincrono e asincrono

La maggior parte del disegno eseguita durante l'elaborazione del messaggio di disegno [**WM \_**](wm-paint.md) è asincrona, ovvero si verifica un ritardo tra il momento in cui una parte della finestra viene invalidata e l'ora di invio del disegno WM \_ . Durante il ritardo, l'applicazione in genere recupera i messaggi dalla coda ed esegue altre attività. Il motivo del ritardo è che il sistema tratta in genere il disegno in una finestra come operazione con priorità bassa e funziona come se i messaggi e i messaggi di input dell'utente che potrebbero influire sulla posizione o le dimensioni di una finestra verranno elaborati prima di WM \_ Paint.

In alcuni casi, è necessario che un'applicazione venga creata in modo sincrono, in modo da creare la finestra immediatamente dopo aver invalidato una parte della finestra. Un'applicazione tipica disegna la finestra principale immediatamente dopo la creazione della finestra per segnalare all'utente che l'applicazione è stata avviata correttamente. Il sistema disegna alcune finestre di controllo in modo sincrono, ad esempio i pulsanti, perché tale finestra funge da stato attivo per l'input dell'utente. Sebbene qualsiasi finestra con una semplice routine di disegno possa essere disegnata in modo sincrono, tutto questo disegno dovrebbe essere eseguito rapidamente e non dovrebbe interferire con la capacità dell'applicazione di rispondere all'input dell'utente.

Le funzioni [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) e [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) consentono il disegno sincrono. **UpdateWindow** Invia un messaggio di [**\_ disegno WM**](wm-paint.md) direttamente alla finestra se l'area di aggiornamento non è vuota. **RedrawWindow** invia anche un messaggio di **\_ disegno WM** , ma fornisce all'applicazione un maggiore controllo sulla modalità di disegno della finestra, ad esempio se disegnare l'area non client e lo sfondo della finestra o se inviare il messaggio indipendentemente dal fatto che l'area di aggiornamento sia vuota o meno. Queste funzioni inviano il messaggio di **\_ disegno WM** direttamente alla finestra, indipendentemente dal numero di altri messaggi nella coda di messaggi dell'applicazione.

Qualsiasi finestra che richiede lunghe operazioni di disegno deve essere disegnata in modo asincrono per impedire che i messaggi in sospeso vengano bloccati quando viene disegnata la finestra. Inoltre, qualsiasi applicazione che invalida spesso piccole parti di una finestra deve consentire il consolidamento di queste parti non valide in un singolo messaggio [**di \_ disegno WM**](wm-paint.md) asincrono, anziché una serie di messaggi **di \_ disegno WM** sincroni.

 

 



