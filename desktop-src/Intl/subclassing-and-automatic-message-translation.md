---
description: La sottoclassazione è una tecnica che consente a un'applicazione di intercettare ed elaborare i messaggi inviati o inviati a una determinata finestra prima che una routine della finestra abbia la possibilità di elaborarli.
ms.assetid: 6f7ee9ff-479d-4cb0-8de1-1c3b671551f9
title: Creazione di sottoclassi e conversione automatica dei messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20147567bb4cd591d31e0da5f08b76a29d0229c9bc345b8c1827fc5350dd62d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390224"
---
# <a name="subclassing-and-automatic-message-translation"></a>Creazione di sottoclassi e conversione automatica dei messaggi

La sottoclassazione è una tecnica che consente a un'applicazione di intercettare ed elaborare i messaggi inviati o inviati a una determinata finestra prima che una routine della finestra abbia la possibilità di elaborarli. Il sistema operativo converte automaticamente i messaggi [in Windows (ANSI)](code-pages.md) o [in formato Unicode,](unicode.md) a seconda della forma della funzione che ha creato una sottoclasse della routine della finestra.

La chiamata seguente alla [**funzione SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) sottoclassa la routine della finestra corrente associata alla finestra identificata dal *parametro hWnd.* In alternativa, un'applicazione può usare [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra). La nuova routine della finestra **NewWndProc** riceverà messaggi con testo Windows tabella codici.


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



Al termine dell'elaborazione di un messaggio, **NewWndProc** usa la [**funzione CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) come indicato di seguito per passare il messaggio a **OldWndProc**.


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



Se **OldWndProc** è stato creato con uno stile di classe UNICODE, i messaggi vengono convertiti dal modulo della tabella codici Windows ricevuto da **NewWndProc** in Unicode.

Analogamente, una chiamata alla funzione [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) o [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) sottoclassa la routine della finestra corrente con una routine finestra che prevede messaggi di testo Unicode. La conversione dei messaggi, se necessario, viene eseguita durante l'elaborazione della [**funzione CallWindowProc.**](/windows/win32/api/winuser/nf-winuser-callwindowproca)

Per altre informazioni sulla creazione di sottoclassi, vedere [Procedure della finestra](../winmsg/window-procedures.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di unicode e set di caratteri](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
