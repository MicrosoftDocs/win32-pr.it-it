---
title: Informazioni sui controlli Rebar
description: Un controllo Rebar funge da contenitore per le finestre figlio.
ms.assetid: vs|controls|~\controls\rebar\rebar.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56bc68629db7387f4ba408a769f7d87a64256000
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047467"
---
# <a name="about-rebar-controls"></a>Informazioni sui controlli Rebar

Un *controllo Rebar* funge da contenitore per le finestre figlio. Può contenere una o più *bande* e ogni banda può avere qualsiasi combinazione di una barra di pinza, una bitmap, un'etichetta di testo e una finestra figlio. Un'applicazione assegna una finestra figlio, in genere un altro controllo, a una banda di controllo Rebar. Quando si riposiziona dinamicamente una banda di controllo Rebar, il controllo Rebar gestisce le dimensioni e la posizione della finestra figlio assegnata a tale banda. Inoltre, un'applicazione può specificare una bitmap di sfondo per una banda e il controllo Rebar visualizzerà la finestra figlio della banda sulla bitmap.

Lo screenshot seguente mostra un controllo Rebar con due bande. Una contiene una barra degli strumenti e l'altra contiene una casella combinata. Entrambe le bande hanno una pinza che consente lo spostamento e il ridimensionamento.

![screenshot della finestra di dialogo che mostra un controllo Rebar con una banda contenente una barra degli strumenti e una banda contenente una casella combinata](images/rb-rebar.png)

> [!Note]  
> Il controllo Rebar viene implementato nella versione 4,70 e successive di Comctl32.dll.

 

## <a name="rebar-bands-and-child-windows"></a>Bande Rebar e finestre figlio

Un'applicazione definisce i tratti di una banda Rebar usando i messaggi [**RB \_ INSERTBAND**](rb-insertband.md) e [**RB \_ SETBANDINFO**](rb-setbandinfo.md) . Questi messaggi accettano l'indirizzo di una struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) come parametro *lParam* . I membri della struttura **REBARBANDINFO** definiscono i tratti di una determinata banda. Per impostare i tratti di una banda, impostare il membro **cbSize** per indicare la dimensione, in byte, della struttura. Impostare quindi il membro **fmask** per indicare i membri della struttura che l'applicazione sta riempiendo.

Per assegnare una finestra figlio a una banda, includere il \_ flag figlio RBBIM nel membro **fmask** della struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) , quindi impostare il membro **hWndChild** sull'handle della finestra figlio. Le applicazioni possono impostare la larghezza e l'altezza minime consentite di una finestra figlio nei membri **cxMinChild** e **cyMinChild** .

Quando un controllo Rebar viene eliminato definitivamente, elimina qualsiasi finestra figlio assegnata alle bande al suo interno. Per impedire che il controllo distrugga le finestre figlio assegnate alle relative bande, rimuovere le bande inviando il messaggio [**RB \_ DELETEBAND**](rb-deleteband.md) , quindi utilizzare il messaggio [**RB \_ padre**](rb-setparent.md) per reimpostare l'elemento padre su un'altra finestra prima di eliminare definitivamente il controllo Rebar.

## <a name="the-rebar-control-user-interface"></a>Interfaccia utente del controllo Rebar

Tutte le bande di controllo Rebar possono essere ridimensionate, ad eccezione di quelle che usano lo \_ stile RBBS FIXEDSIZE. Per ridimensionare o modificare l'ordine delle bande all'interno del controllo, fare clic e trascinare la barra di pinza della banda. Il controllo Rebar ridimensiona e riposiziona automaticamente le finestre figlio assegnate alle bande. Inoltre, è possibile impostare la dimensione di una banda facendo clic sul testo della banda, se presente.

## <a name="the-rebar-controls-image-list"></a>Elenco immagini del controllo Rebar

Se un'applicazione usa un elenco immagini con un controllo Rebar, deve inviare il messaggio [**RB \_ SETBARINFO**](rb-setbarinfo.md) prima di aggiungere bande al controllo. Questo messaggio accetta l'indirizzo di una struttura [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) come parametro *lParam* . Prima di inviare il messaggio, preparare la struttura **REBARINFO** impostando il membro **cbSize** sulle dimensioni, in byte, della struttura. Quindi, se il controllo Rebar Visualizza le immagini sulle bande, impostare il membro **fmask** sul \_ flag ImageList RBIM e assegnare un handle dell'elenco immagini al membro **himl** . Se il controllo Rebar non userà le immagini a banda, impostare **fmask** su zero.

## <a name="rebar-control-message-forwarding"></a>Controllo Rebar (inoltri messaggi)

Un controllo Rebar Invia tutti i messaggi della finestra di [**\_ notifica WM**](wm-notify.md) alla finestra padre. Inoltre, un controllo Rebar inoltra tutti i messaggi inviati da Windows assegnati alle bande, ad esempio [**WM \_ CHARTOITEM**](wm-chartoitem.md), [**WM \_ Command**](/windows/desktop/menurc/wm-command)e altri.

 

 