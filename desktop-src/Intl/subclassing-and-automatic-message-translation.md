---
description: La sottoclasse è una tecnica che consente a un'applicazione di intercettare ed elaborare i messaggi inviati o pubblicati in una determinata finestra prima che una routine della finestra abbia la possibilità di elaborarli.
ms.assetid: 6f7ee9ff-479d-4cb0-8de1-1c3b671551f9
title: Sottoclassi e conversione automatica di messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7f0aebabe4bde259a982152327ce61a14de915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314804"
---
# <a name="subclassing-and-automatic-message-translation"></a>Sottoclassi e conversione automatica di messaggi

La sottoclasse è una tecnica che consente a un'applicazione di intercettare ed elaborare i messaggi inviati o pubblicati in una determinata finestra prima che una routine della finestra abbia la possibilità di elaborarli. Il sistema operativo converte automaticamente i messaggi in una [tabella codici di Windows (ANSI)](code-pages.md) o in un formato [Unicode](unicode.md) , a seconda del form della funzione che ha sottoclassato la routine della finestra.

La chiamata seguente alla funzione [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) consente di sottoclasse la routine della finestra corrente associata alla finestra identificata dal parametro *HWND* . In alternativa, un'applicazione può usare [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra). La nuova procedura della finestra **NewWndProc**, riceverà messaggi con testo nel formato della tabella codici di Windows.


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



Al termine dell'elaborazione di un messaggio da parte di **NewWndProc** , viene utilizzata la funzione [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) come indicato di seguito per passare il messaggio a **OldWndProc**.


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



Se **OldWndProc** è stato creato con uno stile di classe Unicode, i messaggi vengono convertiti dal form della tabella codici di Windows ricevuto da **NewWndProc** in Unicode.

Analogamente, una chiamata alla funzione [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) o [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) sottoclasse la routine della finestra corrente con una routine della finestra che prevede messaggi di testo Unicode. La conversione dei messaggi, se necessario, viene eseguita durante l'elaborazione della funzione [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) .

Per ulteriori informazioni sulla sottoclasse, vedere [routine della finestra](../winmsg/window-procedures.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di set di caratteri e Unicode](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
