---
description: Lo sfondo della finestra è il colore o il motivo utilizzato per riempire l'area client prima che venga avviata la creazione di una finestra.
ms.assetid: d0613f9b-e65b-4de2-887d-2b642d36b22d
title: Sfondo finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d567b0bdc38866cd9332ff8ed399bfb23f53c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880965"
---
# <a name="window-background"></a>Sfondo finestra

Lo sfondo della finestra è il colore o il motivo utilizzato per riempire l'area client prima che venga avviata la creazione di una finestra. Lo sfondo della finestra copre tutto ciò che era sullo schermo prima che la finestra venisse spostata, cancellando le immagini esistenti e impedendo che il nuovo output dell'applicazione venisse misto con informazioni non correlate.

Il sistema dipinge lo sfondo di una finestra o fornisce alla finestra la possibilità di farlo inviando un messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) quando l'applicazione chiama [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint). Se un'applicazione non elabora il messaggio ma lo passa a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), il sistema cancella lo sfondo riempiendo il modello nel pennello di sfondo specificato dalla classe della finestra. Se il pennello non è valido o la classe non dispone di un pennello per lo sfondo, il sistema imposta il membro **fErase** nella struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) restituita da **BeginPaint** , ma non esegue altre azioni. L'applicazione ha quindi una seconda possibilità di creare lo sfondo della finestra, se necessario.

Se elabora [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md), l'applicazione deve usare il parametro *wParam* del messaggio per creare lo sfondo. Questo parametro contiene un handle per il contesto del dispositivo di visualizzazione per la finestra. Dopo aver disegnato lo sfondo, l'applicazione deve restituire un valore diverso da zero. Ciò garantisce che [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) non imposti erroneamente il membro **FErase** della struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) su un valore diverso da zero (che indica che lo sfondo deve essere cancellato) quando l'applicazione elabora il messaggio di [**\_ disegno WM**](wm-paint.md) successivo.

Un'applicazione può definire un pennello per lo sfondo di una classe assegnando un handle di pennello o un valore di colore di sistema al membro **hbrBackground** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) quando si registra la classe con la funzione [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . La funzione [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) o [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) può essere utilizzata per creare un handle del pennello. Un valore di colore di sistema può essere uno dei valori definiti per la funzione [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) . (Il valore deve essere aumentato di uno prima che venga assegnato al membro).

Un'applicazione può elaborare il messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) anche se è definito un pennello per lo sfondo di una classe. Questo è tipico nelle applicazioni che consentono all'utente di modificare il colore o il modello di sfondo della finestra per una finestra specificata senza influire sulle altre finestre della classe. In questi casi, l'applicazione non deve passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Non è necessario che un'applicazione allineati i pennelli, perché il sistema disegna il pennello usando l'origine della finestra come punto di riferimento. Dato questo, l'utente può spostare la finestra senza influire sull'allineamento dei pennelli del pattern.

 

 
