---
title: Informazioni sui caret
description: In questo argomento vengono illustrati i caret.
ms.assetid: 4487c93c-9a0f-467c-86b1-969f664d5526
keywords:
- risorse, caret
- caret, rimozione
- righe lampeggianti
- blocchi lampeggianti
- bitmap lampeggianti
- caret, visibilità
- cursori, tempi di lampeggiamento
- blink times
- cursori, posizioni
- rimozione di caret
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ed2cbe50771b893c7a2ccc0874a882aabb23a1d0b4ba27822d7ce0ec47a18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461321"
---
# <a name="about-carets"></a>Informazioni sui caret

Il sistema fornisce un solo caret per ogni coda di messaggi. Una finestra deve creare un punto di interesse solo quando ha lo stato attivo o è attivo. La finestra deve eliminare il punto di interesse prima di perdere lo stato attivo della tastiera o diventare inattiva. Per altre informazioni sull'input da tastiera, vedere [Input da tastiera.](/windows/desktop/inputdev/keyboard-input)

Usare la [**funzione CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) per specificare i parametri per un punto di accesso. Il sistema forma un cursore invertendo il colore del pixel all'interno del rettangolo specificato dalla posizione, dalla larghezza e dall'altezza del cursore. La larghezza e l'altezza sono specificate in unità logiche. Pertanto, l'aspetto di un punto di sospensione è soggetto alla modalità di mapping della finestra.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Visibilità del caret](#caret-visibility)
-   [Ora di lampeggiamento del cursore](#caret-blink-time)
-   [Posizione del cursore](#caret-position)
-   [Rimozione di un punto di controllo](#removing-a-caret)

## <a name="caret-visibility"></a>Visibilità del caret

Dopo aver definito il caret, usare la [**funzione ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) per rendere visibile il caret. Quando viene visualizzato, il punto di controllo inizia automaticamente a lampeggiare. Per visualizzare un punto di selezione a tinta unita, il sistema inverte ogni pixel nel rettangolo; per visualizzare un punto di selezione grigio, il sistema inverte ogni altro pixel; per visualizzare un punto di memorizzazione bitmap, il sistema inverte solo i bit bianchi della bitmap.

## <a name="caret-blink-time"></a>Ora di lampeggiamento del cursore

Il tempo trascorso, in millisecondi, necessario per invertire il cursore viene chiamato ora *di lampeggiamento.* Il cursore lampeggia finché il thread proprietario della coda di messaggi dispone di un message pump che elabora i messaggi.

L'utente può impostare l'ora di lampeggiamento del cursore usando il Pannello di controllo e le applicazioni devono rispettare le impostazioni scelte dall'utente. Un'applicazione può determinare l'ora di lampeggiamento del cursore usando [**la funzione GetCaretBlinkTime.**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) Se si scrive un'applicazione che consente all'utente di regolare l'ora di lampeggiamento, ad esempio un'applet Pannello di controllo, usare la funzione [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) per impostare la frequenza del lampeggiamento su un numero di millisecondi specificato.

Il *tempo flash* è il tempo trascorso, in millisecondi, necessario per visualizzare, invertire e ripristinare la visualizzazione del punto di controllo. L'ora di lampeggiamento di un cursore è doppia rispetto all'ora di lampeggiamento.

## <a name="caret-position"></a>Posizione del cursore

È possibile determinare la posizione del cursore usando la [**funzione GetCaretPos.**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos) La posizione, nelle coordinate del client, viene copiata in una struttura specificata da un parametro in **GetCaretPos.** Un'applicazione può spostare un punto di accesso in una finestra usando la [**funzione SetCaretPos.**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) Una finestra può spostare un punto di controllo solo se è già proprietario del punto di controllo. **SetCaretPos può** spostare il caret indipendentemente dal fatto che sia visibile o meno.

## <a name="removing-a-caret"></a>Rimozione di un punto di controllo

È possibile rimuovere temporaneamente un punto di controllo nasconderlo oppure rimuoverlo definitivamente. Per nascondere il caret, usare la [**funzione HideCaret.**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) Ciò è utile quando l'applicazione deve ridisegnare lo schermo durante l'elaborazione di un messaggio, ma deve mantenere il punto di non visualizzazione. Al termine del disegno, l'applicazione può visualizzare nuovamente il caret usando la [**funzione ShowCaret.**](/windows/desktop/api/Winuser/nf-winuser-showcaret) Nascondere il cursore non elimina la forma o invalida il punto di inserimento. Nascondere il caret è cumulativo. ciò significa che se l'applicazione chiama **HideCaret** cinque volte, deve chiamare **anche ShowCaret** cinque volte prima che il caret venga nuovamente visualizzato.

Per rimuovere il punto di controllo dallo schermo ed eliminarne la forma, usare la [**funzione DestroyCaret.**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) **DestroyCaret** elimina il caret solo se la finestra coinvolta nell'attività corrente è proprietaria del caret.

 

 