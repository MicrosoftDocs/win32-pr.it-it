---
description: In genere, un'applicazione disegna in una finestra in risposta a un messaggio WM \_ PAINT.
ms.assetid: b2317ce9-e775-450e-91f5-00f735f256a3
title: Messaggio WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138913771621699abb27d4f5648e732b21a607ff5466ec4766726ab278d46fed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965181"
---
# <a name="the-wm_paint-message"></a>Messaggio WM \_ PAINT

In genere, un'applicazione disegna in una finestra in risposta a un [**messaggio WM \_ PAINT.**](wm-paint.md) Il sistema invia questo messaggio a una routine della finestra quando le modifiche apportate alla finestra hanno modificato il contenuto dell'area client. Il sistema invia il messaggio solo se non sono presenti altri messaggi nella coda di messaggi dell'applicazione.

Quando si riceve un [**messaggio WM \_ PAINT,**](wm-paint.md) un'applicazione può chiamare [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) per recuperare il contesto di dispositivo di visualizzazione per l'area client e usarlo nelle chiamate alle funzioni GDI per eseguire tutte le operazioni di disegno necessarie per aggiornare l'area client. Dopo aver completato le operazioni di disegno, l'applicazione chiama la [**funzione EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) per rilasciare il contesto di dispositivo di visualizzazione.

Prima [**che BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) restituisca il contesto di dispositivo di visualizzazione, il sistema prepara il contesto di dispositivo per la finestra specificata. Imposta innanzitutto l'area di ritaglio per il contesto di dispositivo in modo che sia uguale all'intersezione della parte della finestra che richiede l'aggiornamento e della parte visibile all'utente. Vengono ridisegnate solo le parti della finestra modificate. I tentativi di disegnare all'esterno di questa area vengono ritagliati e non vengono visualizzati sullo schermo.

Il sistema può anche inviare [**messaggi WM \_ NCPAINT**](wm-ncpaint.md) e [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) alla routine della finestra prima del ritorno [**di BeginPaint.**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) Questi messaggi indirizzano l'applicazione a disegnare l'area non client e lo sfondo della finestra. *L'area non client* è la parte di una finestra esterna all'area client. L'area include funzionalità come la barra del titolo, il menu della finestra (noto anche come **menu** Di sistema) e le barre di scorrimento. La maggior parte delle applicazioni si basa sulla funzione finestra [**predefinita, DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), per disegnare questa area e quindi passare il **messaggio WM \_ NCPAINT** a questa funzione. Lo *sfondo della finestra* è il colore o il motivo con cui viene riempita una finestra prima che inizino altre operazioni di disegno. Lo sfondo copre tutte le immagini in precedenza nella finestra o sullo schermo sotto la finestra. Se una finestra appartiene a una classe finestra con un pennello di sfondo della classe, la **funzione DefWindowProc** disegna automaticamente lo sfondo della finestra.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) riempie una [**struttura PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) con informazioni quali le dimensioni della parte della finestra da aggiornare e un flag che indica se lo sfondo della finestra è stato disegnato. L'applicazione può usare queste informazioni per ottimizzare il disegno. Ad esempio, può usare le dimensioni dell'area di aggiornamento, specificate dal membro **rcPaint,** per limitare il disegno solo alle parti della finestra che devono essere aggiornate. Se un'applicazione ha un output molto semplice, può ignorare l'area di aggiornamento e disegnare nell'intera finestra, affidandosi al sistema per eliminare (ritagliare) qualsiasi output non necessario. Poiché il disegno di sistema si estende all'esterno dell'area di ritaglio, è visibile solo il disegno presente nell'area di aggiornamento.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) imposta l'area di aggiornamento di una finestra su **NULL.** Questa operazione cancella l'area, impedendo la generazione di messaggi [**WM \_ PAINT**](wm-paint.md) successivi. Se un'applicazione elabora un messaggio **WM \_ PAINT** ma non chiama **BeginPaint** o cancella in altro modo l'area di aggiornamento, l'applicazione continua a ricevere messaggi **WM \_ PAINT** purché l'area non sia vuota. In tutti i casi, un'applicazione deve cancellare l'area di aggiornamento prima di restituire il messaggio **WM \_ PAINT.**

Al termine del disegno, l'applicazione deve chiamare [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint). Per la maggior parte delle finestre, **EndPaint** rilascia il contesto di dispositivo di visualizzazione, rendendolo disponibile per altre finestre. **EndPaint** mostra anche il punto di chiusura, se in precedenza era nascosto da [**BeginPaint.**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) **BeginPaint** nasconde il caret per impedire che le operazioni di disegno lo corrompono.

-   [Area di aggiornamento](the-update-region.md)
-   [Invalidazione e convalida dell'area di aggiornamento](invalidating-and-validating-the-update-region.md)
-   [Recupero dell'area di aggiornamento](retrieving-the-update-region.md)
-   [Esclusione dell'area di aggiornamento](excluding-the-update-region.md)
-   [Disegno sincrono e asincrono](synchronous-and-asynchronous-drawing.md)

 

 
