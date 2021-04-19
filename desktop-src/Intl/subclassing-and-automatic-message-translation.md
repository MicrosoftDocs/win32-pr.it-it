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
# <a name="subclassing-and-automatic-message-translation"></a><span data-ttu-id="f24b4-103">Sottoclassi e conversione automatica di messaggi</span><span class="sxs-lookup"><span data-stu-id="f24b4-103">Subclassing and Automatic Message Translation</span></span>

<span data-ttu-id="f24b4-104">La sottoclasse è una tecnica che consente a un'applicazione di intercettare ed elaborare i messaggi inviati o pubblicati in una determinata finestra prima che una routine della finestra abbia la possibilità di elaborarli.</span><span class="sxs-lookup"><span data-stu-id="f24b4-104">Subclassing is a technique that allows an application to intercept and process messages sent or posted to a particular window before a window procedure has a chance to process them.</span></span> <span data-ttu-id="f24b4-105">Il sistema operativo converte automaticamente i messaggi in una [tabella codici di Windows (ANSI)](code-pages.md) o in un formato [Unicode](unicode.md) , a seconda del form della funzione che ha sottoclassato la routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="f24b4-105">The operating system automatically translates messages into [Windows (ANSI) code page](code-pages.md) or [Unicode](unicode.md) form, depending on the form of the function that has subclassed the window procedure.</span></span>

<span data-ttu-id="f24b4-106">La chiamata seguente alla funzione [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) consente di sottoclasse la routine della finestra corrente associata alla finestra identificata dal parametro *HWND* .</span><span class="sxs-lookup"><span data-stu-id="f24b4-106">The following call to the [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function subclasses the current window procedure associated with the window identified by the *hWnd* parameter.</span></span> <span data-ttu-id="f24b4-107">In alternativa, un'applicazione può usare [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra).</span><span class="sxs-lookup"><span data-stu-id="f24b4-107">Alternatively, an application can use [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra).</span></span> <span data-ttu-id="f24b4-108">La nuova procedura della finestra **NewWndProc**, riceverà messaggi con testo nel formato della tabella codici di Windows.</span><span class="sxs-lookup"><span data-stu-id="f24b4-108">The new window procedure **NewWndProc**, will receive messages with text in Windows code page format.</span></span>


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



<span data-ttu-id="f24b4-109">Al termine dell'elaborazione di un messaggio da parte di **NewWndProc** , viene utilizzata la funzione [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) come indicato di seguito per passare il messaggio a **OldWndProc**.</span><span class="sxs-lookup"><span data-stu-id="f24b4-109">When **NewWndProc** has finished processing a message, it uses the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function as follows to pass the message to **OldWndProc**.</span></span>


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



<span data-ttu-id="f24b4-110">Se **OldWndProc** è stato creato con uno stile di classe Unicode, i messaggi vengono convertiti dal form della tabella codici di Windows ricevuto da **NewWndProc** in Unicode.</span><span class="sxs-lookup"><span data-stu-id="f24b4-110">If **OldWndProc** was created with a class style of UNICODE, messages are translated from the Windows code page form received by **NewWndProc** into Unicode.</span></span>

<span data-ttu-id="f24b4-111">Analogamente, una chiamata alla funzione [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) o [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) sottoclasse la routine della finestra corrente con una routine della finestra che prevede messaggi di testo Unicode.</span><span class="sxs-lookup"><span data-stu-id="f24b4-111">Similarly, a call to the [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) function subclasses the current window procedure with a window procedure that expects Unicode text messages.</span></span> <span data-ttu-id="f24b4-112">La conversione dei messaggi, se necessario, viene eseguita durante l'elaborazione della funzione [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="f24b4-112">Message translation, if necessary, is performed during the processing of the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function.</span></span>

<span data-ttu-id="f24b4-113">Per ulteriori informazioni sulla sottoclasse, vedere [routine della finestra](../winmsg/window-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="f24b4-113">For more information about subclassing, see [Window Procedures](../winmsg/window-procedures.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f24b4-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f24b4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f24b4-115">Utilizzo di set di caratteri e Unicode</span><span class="sxs-lookup"><span data-stu-id="f24b4-115">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
