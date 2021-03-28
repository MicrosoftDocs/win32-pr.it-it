---
description: In genere, un'applicazione viene disegnata in una finestra in risposta a un \_ messaggio di disegno WM.
ms.assetid: b2317ce9-e775-450e-91f5-00f735f256a3
title: Messaggio di WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69f7dab736972d8b7226890144efd8763de856a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995120"
---
# <a name="the-wm_paint-message"></a>Messaggio di \_ disegno WM

In genere, un'applicazione viene disegnata in una finestra in risposta a un messaggio di [**\_ disegno WM**](wm-paint.md) . Il sistema invia questo messaggio a una procedura della finestra quando le modifiche apportate alla finestra hanno modificato il contenuto dell'area client. Il sistema invia il messaggio solo se non sono presenti altri messaggi nella coda di messaggi dell'applicazione.

Al momento della ricezione di un messaggio di [**\_ disegno WM**](wm-paint.md) , un'applicazione può chiamare [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) per recuperare il contesto del dispositivo di visualizzazione per l'area client e utilizzarlo nelle chiamate alle funzioni GDI per eseguire tutte le operazioni di disegno necessarie per aggiornare l'area client. Dopo aver completato le operazioni di disegno, l'applicazione chiama la funzione [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) per rilasciare il contesto del dispositivo di visualizzazione.

Prima che [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) restituisca il contesto del dispositivo di visualizzazione, il sistema prepara il contesto di dispositivo per la finestra specificata. Innanzitutto, imposta l'area di ridimensionamento affinché il contesto di dispositivo sia uguale all'intersezione della parte della finestra che deve essere aggiornata e alla parte visibile per l'utente. Vengono ridisegnato solo le parti della finestra modificate. I tentativi di estrazione al di fuori di questa area vengono ritagliati e non vengono visualizzati sullo schermo.

Il sistema può anche inviare messaggi [**WM \_ NCPAINT**](wm-ncpaint.md) e [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) alla routine della finestra prima che [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) restituisca. Questi messaggi indirizzano l'applicazione per creare l'area non client e lo sfondo della finestra. L' *area non client* è la parte di una finestra che si trova al di fuori dell'area client. L'area include funzionalità quali la barra del titolo, il menu finestra (noto anche come menu di **sistema** ) e le barre di scorrimento. La maggior parte delle applicazioni si basa sulla funzione finestra predefinita, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), per creare quest'area e quindi passare il messaggio **WM \_ NCPAINT** a questa funzione. Lo *sfondo della finestra* è il colore o il motivo per cui una finestra viene riempita prima che vengano avviate altre operazioni di disegno. Lo sfondo copre tutte le immagini precedentemente presenti nella finestra o sullo schermo sotto la finestra. Se una finestra appartiene a una classe della finestra con un pennello per lo sfondo della classe, la funzione **DefWindowProc** disegna automaticamente lo sfondo della finestra.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) riempie una struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) con informazioni quali le dimensioni della parte della finestra da aggiornare e un flag che indica se lo sfondo della finestra è stato disegnato. L'applicazione può utilizzare queste informazioni per ottimizzare il disegno. Ad esempio, può usare le dimensioni dell'area di aggiornamento, specificate dal membro **rcPaint** , per limitare il disegno solo alle parti della finestra che devono essere aggiornate. Se un'applicazione dispone di un output molto semplice, può ignorare l'area di aggiornamento e creare nell'intera finestra, basandosi sul sistema per eliminare (ritagliare) qualsiasi output non necessario. Poiché il disegno delle clip di sistema che si estende al di fuori dell'area di visualizzazione, è visibile solo il disegno che si trova nell'area di aggiornamento.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) imposta l'area di aggiornamento di una finestra su **null**. Questa operazione cancella l'area e impedisce la generazione di messaggi [**di \_ disegno WM**](wm-paint.md) successivi. Se un'applicazione elabora un messaggio di **\_ disegno WM** ma non chiama **BeginPaint** o cancella altrimenti l'area di aggiornamento, l'applicazione continua a ricevere i messaggi di **\_ disegno WM** finché l'area non è vuota. In tutti i casi, un'applicazione deve cancellare l'area di aggiornamento prima di restituire il messaggio di **\_ disegno WM** .

Al termine del disegno, l'applicazione deve chiamare [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint). Per la maggior parte delle finestre, **EndPaint** rilascia il contesto del dispositivo di visualizzazione, rendendolo disponibile ad altre finestre. **EndPaint** Mostra anche il cursore, se è stato precedentemente nascosto da [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint). **BeginPaint** nasconde il punto di inserimento per evitare che le operazioni di disegno danneggino il punto di inserimento.

-   [Area di aggiornamento](the-update-region.md)
-   [Invalidare e convalidare l'area di aggiornamento](invalidating-and-validating-the-update-region.md)
-   [Recupero dell'area di aggiornamento](retrieving-the-update-region.md)
-   [Esclusione dell'area di aggiornamento](excluding-the-update-region.md)
-   [Disegno sincrono e asincrono](synchronous-and-asynchronous-drawing.md)

 

 
