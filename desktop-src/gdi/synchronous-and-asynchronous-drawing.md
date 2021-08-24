---
description: La maggior parte dei disegni eseguiti durante l'elaborazione del messaggio WM PAINT è asincrona, ad esempio si verifica un ritardo tra il momento in cui una parte della finestra viene invalidata e il momento in cui WM PAINT viene \_ \_ inviato.
ms.assetid: c4eac615-6526-4ca6-854b-b4a598da13a4
title: Disegno sincrono e asincrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e22b49a61d021c886da6253a2575c0e7f1c7a8c01eb2c3b550e04acda5daf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613391"
---
# <a name="synchronous-and-asynchronous-drawing"></a>Disegno sincrono e asincrono

La maggior parte dei disegni eseguiti durante l'elaborazione del messaggio [**WM \_ PAINT**](wm-paint.md) è asincrona, ad esempio si verifica un ritardo tra il momento in cui una parte della finestra viene invalidata e il momento in cui WM PAINT viene \_ inviato. Durante il ritardo, l'applicazione recupera in genere i messaggi dalla coda ed esegue altre attività. Il motivo del ritardo è che il sistema considera in genere il disegno in una finestra come un'operazione con priorità bassa e funziona come se i messaggi di input dell'utente e i messaggi che potrebbero influire sulla posizione o sulle dimensioni di una finestra vengano elaborati prima di WM \_ PAINT.

In alcuni casi, è necessario che un'applicazione esere disegna in modo sincrono nella finestra immediatamente dopo l'invalidazione di una parte della finestra. Un'applicazione tipica disegna la finestra principale immediatamente dopo la creazione della finestra per segnalare all'utente che l'applicazione è stata avviata correttamente. Il sistema disegna alcune finestre di controllo in modo sincrono, ad esempio i pulsanti, perché tali finestre fungono da stato attivo per l'input dell'utente. Anche se qualsiasi finestra con una routine di disegno semplice può essere disegnata in modo sincrono, tutto questo disegno deve essere eseguito rapidamente e non deve interferire con la capacità dell'applicazione di rispondere all'input dell'utente.

Le [**funzioni UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) [**e RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) consentono il disegno sincrono. **UpdateWindow** invia un [**messaggio WM \_ PAINT**](wm-paint.md) direttamente alla finestra se l'area di aggiornamento non è vuota. **RedrawWindow** invia anche un messaggio **WM \_ PAINT,** ma offre all'applicazione un maggiore controllo su come disegnare la finestra, ad esempio se disegnare l'area non client e lo sfondo della finestra o se inviare il messaggio indipendentemente dal fatto che l'area di aggiornamento sia vuota. Queste funzioni inviano **il \_ messaggio WM PAINT** direttamente alla finestra, indipendentemente dal numero di altri messaggi nella coda di messaggi dell'applicazione.

Qualsiasi finestra che richiede operazioni di disegno dispendiose in termini di tempo deve essere disegnata in modo asincrono per impedire il blocco dei messaggi in sospeso durante il disegno della finestra. Qualsiasi applicazione che invalida spesso piccole parti di una finestra deve inoltre consentire il consolidamento di queste parti non valide in un singolo messaggio [**WM \_ PAINT**](wm-paint.md) asincrono, anziché in una serie di messaggi **WM \_ PAINT sincroni.**

 

 



