---
description: Lo sfondo della finestra è il colore o il motivo utilizzato per riempire l'area client prima dell'inizio del disegno di una finestra.
ms.assetid: d0613f9b-e65b-4de2-887d-2b642d36b22d
title: Sfondo della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819f3bf333728909bdd0e374d41b7665f0517bcc17666b88c58f610e0127d942
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848941"
---
# <a name="window-background"></a>Sfondo della finestra

Lo sfondo della finestra è il colore o il motivo utilizzato per riempire l'area client prima dell'inizio del disegno di una finestra. Lo sfondo della finestra copre tutto ciò che era sullo schermo prima che la finestra fosse spostata, cancellando le immagini esistenti e impedendo che il nuovo output dell'applicazione venga misto a informazioni non correlate.

Il sistema disegna lo sfondo per una finestra o offre alla finestra la possibilità di farlo inviando un messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) quando l'applicazione chiama [**BeginPaint.**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) Se un'applicazione non elabora il messaggio ma lo passa a [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)il sistema cancella lo sfondo riempierlo con il modello nel pennello di sfondo specificato dalla classe della finestra. Se il pennello non è valido o la classe non ha un pennello di sfondo, il sistema imposta il membro **fErase** nella struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) restituita da **BeginPaint,** ma non esegue altre azioni. L'applicazione ha quindi una seconda possibilità di disegnare lo sfondo della finestra, se necessario.

Se elabora [**WM \_ ERASEBKGND,**](../winmsg/wm-erasebkgnd.md)l'applicazione deve usare il parametro *wParam* del messaggio per disegnare lo sfondo. Questo parametro contiene un handle per il contesto di periferica di visualizzazione per la finestra. Dopo aver disegnato lo sfondo, l'applicazione deve restituire un valore diverso da zero. Ciò garantisce che [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) non imposterà erroneamente il membro **fErase** della struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) su un valore diverso da zero (che indica che lo sfondo deve essere cancellato) quando l'applicazione elabora il messaggio [**WM \_ PAINT**](wm-paint.md) successivo.

Un'applicazione può definire un pennello di sfondo della classe assegnando un handle di pennello o un valore di colore di sistema al membro **hbrBackground** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) durante la registrazione della classe con la [**funzione RegisterClass.**](/windows/win32/api/winuser/nf-winuser-registerclassa) La [**funzione GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) o [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) può essere usata per creare un handle di pennello. Un valore di colore di sistema può essere uno di quelli definiti per la [**funzione SetSysColors.**](/windows/win32/api/winuser/nf-winuser-setsyscolors) Il valore deve essere aumentato di uno prima di essere assegnato al membro.

Un'applicazione può elaborare [**il messaggio WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) anche se è definito un pennello di sfondo della classe. Questo è tipico nelle applicazioni che consentono all'utente di modificare il colore di sfondo della finestra o il motivo per una finestra specificata senza influire sulle altre finestre nella classe . In questi casi, l'applicazione non deve passare il messaggio [**a DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

Non è necessario che un'applicazione allinea i pennelli, perché il sistema disegna il pennello usando l'origine della finestra come punto di riferimento. In questo caso, l'utente può spostare la finestra senza influire sull'allineamento dei pennelli del motivo.

 

 
