---
title: Informazioni sui Carrier
description: Questo argomento illustra le carriere.
ms.assetid: 4487c93c-9a0f-467c-86b1-969f664d5526
keywords:
- risorse, punto di inserimento
- carenze, rimozione
- righe lampeggianti
- blocchi lampeggianti
- bitmap intermittenti
- carriere, visibilità
- intermittenza, tempi di inattenzione
- lampeggi volte
- punti di inserimento, posizioni
- rimozione di carriere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a19eb3895ada13297f090a09529b2bcb7c75dee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299758"
---
# <a name="about-carets"></a>Informazioni sui Carrier

Il sistema fornisce un cursore per ogni coda di messaggi. Una finestra deve creare un accento circonflesso solo quando ha lo stato attivo della tastiera o è attivo. La finestra deve eliminare il cursore prima di perdere lo stato attivo della tastiera o diventare inattivo. Per ulteriori informazioni sull'input da tastiera, vedere [input da tastiera](/windows/desktop/inputdev/keyboard-input).

Utilizzare la funzione [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) per specificare i parametri per un accento circonflesso. Il sistema forma un cursore invertendo il colore del pixel all'interno del rettangolo specificato dalla posizione, dalla larghezza e dall'altezza del cursore. La larghezza e l'altezza sono specificate in unità logiche. Pertanto, l'aspetto di un accento circonflesso è soggetto alla modalità di mapping della finestra.

In questa sezione vengono descritti gli argomenti seguenti.

-   [Visibilità del cursore](#caret-visibility)
-   [Tempo di intermittenza del punto di inserimento](#caret-blink-time)
-   [Posizione del punto di inserimento](#caret-position)
-   [Rimozione di un punto di inserimento](#removing-a-caret)

## <a name="caret-visibility"></a>Visibilità del cursore

Dopo aver definito il cursore, utilizzare la funzione [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) per rendere visibile il cursore. Quando viene visualizzato il punto di inserimento, inizia automaticamente a lampeggiare. Per visualizzare un cursore a tinta unita, il sistema inverte ogni pixel nel rettangolo. per visualizzare un cursore grigio, il sistema inverte tutti gli altri pixel; per visualizzare un cursore bitmap, il sistema inverte solo i bit vuoti della bitmap.

## <a name="caret-blink-time"></a>Tempo di intermittenza del punto di inserimento

Il tempo trascorso, in millisecondi, necessario per invertire il punto di inserimento è denominato *tempo di lampeggio*. Il punto di inserimento lampeggerà finché il thread proprietario della coda di messaggi avrà un message pump che elabora i messaggi.

L'utente può impostare il tempo di indisponibilità del cursore usando il pannello di controllo e le applicazioni devono rispettare le impostazioni scelte dall'utente. Un'applicazione può determinare il tempo di indisponibilità del cursore utilizzando la funzione [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) . Se si sta scrivendo un'applicazione che consente all'utente di modificare il tempo di indisponibilità, ad esempio un'applet del pannello di controllo, usare la funzione [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) per impostare la frequenza del lampeggio su un numero specificato di millisecondi.

Il tempo di *Flash* è il tempo trascorso, in millisecondi, necessario per visualizzare, invertire e ripristinare la visualizzazione del cursore. Il tempo di insufficiente del cursore è due volte maggiore del tempo di lampeggio.

## <a name="caret-position"></a>Posizione del punto di inserimento

È possibile determinare la posizione del punto di inserimento usando la funzione [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos) . La posizione, in coordinate client, viene copiata in una struttura specificata da un parametro in **GetCaretPos**. Un'applicazione può spostare un punto di inserimento in una finestra usando la funzione [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) . Una finestra può spostare un punto di inserimento solo se è già proprietario del punto di inserimento. **SetCaretPos** può spostare il punto di inserimento se è visibile o meno.

## <a name="removing-a-caret"></a>Rimozione di un punto di inserimento

È possibile rimuovere temporaneamente un cursore nascondendo il cursore oppure è possibile rimuoverlo definitivamente. Per nascondere il cursore, usare la funzione [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) . Questa operazione è utile quando l'applicazione deve ricreare lo schermo durante l'elaborazione di un messaggio, ma deve evitare il punto di inserimento. Al termine del disegno, l'applicazione può visualizzare di nuovo il cursore usando la funzione [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) . Nascondendo il punto di inserimento non si elimina la forma o non si invalida il punto di inserimento. Nascondere il punto di inserimento è cumulativo. ovvero, se l'applicazione chiama **HideCaret** cinque volte, deve chiamare anche **ShowCaret** cinque volte prima che il punto di inserimento venga nuovamente visualizzato.

Per rimuovere il punto di inserimento dalla schermata ed eliminarne la forma, utilizzare l'utilizzo della funzione [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) . **DestroyCaret** Elimina il punto di inserimento solo se la finestra occupata dall'attività corrente è proprietaria del cursore.

 

 