---
title: Informazioni sui controlli Rebar
description: Un controllo Rebar funge da contenitore per le finestre figlio.
ms.assetid: vs|controls|~\controls\rebar\rebar.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55d34f76ca745f0807b849bd7c42c81944f11e4429fe2dc9670fa318cbd575ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434826"
---
# <a name="about-rebar-controls"></a>Informazioni sui controlli Rebar

Un *controllo Rebar* funge da contenitore per le finestre figlio. Può contenere una o più *bande* e ogni banda può avere qualsiasi combinazione di una barra di scorrimento, una bitmap, un'etichetta di testo e una finestra figlio. Un'applicazione assegna una finestra figlio, in genere un altro controllo, a una banda di controllo Rebar. Quando si riposiziona dinamicamente una banda di controllo Rebar, il controllo Rebar gestisce le dimensioni e la posizione della finestra figlio assegnata a tale banda. Inoltre, un'applicazione può specificare una bitmap di sfondo per una banda e il controllo Rebar visualizza la finestra figlio della banda sulla bitmap.

Lo screenshot seguente mostra un controllo Rebar con due bande. Una contiene una barra degli strumenti e l'altra contiene una casella combinata. Entrambe le bande hanno una manopola che ne consente lo spostamento e il ridimensionamento.

![Screenshot della finestra di dialogo che mostra un controllo Rebar con una banda contenente una barra degli strumenti e una banda contenente una casella combinata](images/rb-rebar.png)

> [!Note]  
> Il controllo rebar viene implementato nella versione 4.70 e successive di Comctl32.dll.

 

## <a name="rebar-bands-and-child-windows"></a>Rebar Bands e Child Windows

Un'applicazione definisce i tratti di una banda rebar usando i messaggi [**RB \_ INSERTBAND**](rb-insertband.md) e [**RB \_ SETBANDINFO.**](rb-setbandinfo.md) Questi messaggi accettano l'indirizzo di [**una struttura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) come *parametro lParam.* I **membri della struttura REBARBANDINFO** definiscono i tratti di una determinata banda. Per impostare i tratti di una banda, impostare il **membro cbsize** per indicare le dimensioni della struttura, in byte. Impostare quindi il **membro fMask** per indicare i membri della struttura compilati dall'applicazione.

Per assegnare una finestra figlio a una banda, includere il flag RBBIM CHILD nel membro \_ **fMask** della struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) e quindi impostare il membro **hwndChild** sull'handle della finestra figlio. Le applicazioni possono impostare la larghezza e l'altezza minime consentite di una finestra figlio nei **membri cxMinChild** **e cyMinChild.**

Quando un controllo Rebar viene eliminato, elimina tutte le finestre figlio assegnate alle bande al suo interno. Per impedire al controllo di eliminare definitivamente le finestre figlio assegnate alle relative bande, rimuovere le bande inviando il messaggio [**RB \_ DELETEBAND**](rb-deleteband.md) e quindi usare il [**messaggio RB \_ SETPARENT**](rb-setparent.md) per reimpostare l'elemento padre su un'altra finestra prima di eliminare definitivamente il controllo Rebar.

## <a name="the-rebar-control-user-interface"></a>Controllo Rebar Interfaccia utente

È possibile ridimensionare tutte le bande di controllo Rebar, ad eccezione di quelle che usano lo stile RBBS \_ FIXEDSIZE. Per ridimensionare o modificare l'ordine delle bande all'interno del controllo, fare clic e trascinare la barra di ridimensionamento di una banda. Il controllo Rebar ridimensiona e riposiziona automaticamente le finestre figlio assegnate alle bande. Inoltre, è possibile attivare o disattivare le dimensioni di una banda facendo clic sul testo della banda, se presente.

## <a name="the-rebar-controls-image-list"></a>Elenco di immagini del controllo Rebar

Se un'applicazione usa un elenco di immagini con un controllo Rebar, deve inviare il messaggio [**\_ RB SETBARINFO**](rb-setbarinfo.md) prima di aggiungere bande al controllo. Questo messaggio accetta l'indirizzo di una [**struttura REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) come *parametro lParam.* Prima di inviare il messaggio, preparare la struttura **REBARINFO** impostando il membro **cbSize** sulla dimensione della struttura, in byte. Quindi, se il controllo Rebar visualizza immagini sulle bande, imposta il membro **fMask** sul flag RBIM IMAGELIST e assegna un handle dell'elenco immagini al membro \_ **luil.** Se l'oggetto Rebar non userà immagini a banda, **impostare fMask** su zero.

## <a name="rebar-control-message-forwarding"></a>Inoltro dei messaggi di controllo Rebar

Un controllo Rebar inoltra tutti i [**messaggi della finestra WM \_ NOTIFY**](wm-notify.md) alla finestra padre. Inoltre, un controllo Rebar inoltra tutti i messaggi inviati dalle finestre assegnate alle relative bande, ad esempio [**WM \_ CHARTOITEM,**](wm-chartoitem.md) [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command)e altri.

 

 