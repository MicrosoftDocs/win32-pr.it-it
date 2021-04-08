---
title: Chiusura della finestra
description: Quando l'utente chiude una finestra, tale azione attiva una sequenza di messaggi di finestra.
ms.assetid: f0449f11-0569-4a3a-92bc-bced7e0db516
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6422966d6b0351654632a1c77b7ebf07e2b5ffef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872533"
---
# <a name="closing-the-window"></a><span data-ttu-id="bca4f-103">Chiusura della finestra</span><span class="sxs-lookup"><span data-stu-id="bca4f-103">Closing the Window</span></span>

<span data-ttu-id="bca4f-104">Quando l'utente chiude una finestra, tale azione attiva una sequenza di messaggi di finestra.</span><span class="sxs-lookup"><span data-stu-id="bca4f-104">When the user closes a window, that action triggers a sequence of window messages.</span></span>

<span data-ttu-id="bca4f-105">L'utente può chiudere una finestra dell'applicazione facendo clic sul pulsante **Chiudi** oppure utilizzando un tasto di scelta rapida, ad esempio ALT + F4.</span><span class="sxs-lookup"><span data-stu-id="bca4f-105">The user can close an application window by clicking the **Close** button, or by using a keyboard shortcut such as ALT+F4.</span></span> <span data-ttu-id="bca4f-106">Ognuna di queste azioni causa la ricezione di un messaggio [**di \_ chiusura WM**](/windows/desktop/winmsg/wm-close) da parte della finestra.</span><span class="sxs-lookup"><span data-stu-id="bca4f-106">Any of these actions causes the window to receive a [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) message.</span></span> <span data-ttu-id="bca4f-107">Il messaggio **WM \_ Close** consente di richiedere conferma all'utente prima di chiudere la finestra.</span><span class="sxs-lookup"><span data-stu-id="bca4f-107">The **WM\_CLOSE** message gives you an opportunity to prompt the user before closing the window.</span></span> <span data-ttu-id="bca4f-108">Se si vuole effettivamente chiudere la finestra, chiamare la funzione [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) .</span><span class="sxs-lookup"><span data-stu-id="bca4f-108">If you really do want to close the window, call the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function.</span></span> <span data-ttu-id="bca4f-109">In caso contrario, è sufficiente restituire zero dal messaggio **WM \_ Close** e il sistema operativo ignorerà il messaggio e non eliminerà definitivamente la finestra.</span><span class="sxs-lookup"><span data-stu-id="bca4f-109">Otherwise, simply return zero from the **WM\_CLOSE** message, and the operating system will ignore the message and not destroy the window.</span></span>

<span data-ttu-id="bca4f-110">Di seguito è riportato un esempio di come un programma può gestire [**WM \_ Close**](/windows/desktop/winmsg/wm-close).</span><span class="sxs-lookup"><span data-stu-id="bca4f-110">Here is an example of how a program might handle [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span>

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

<span data-ttu-id="bca4f-111">In questo esempio, la funzione [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) Mostra una finestra di dialogo modale che contiene i pulsanti **OK** e **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="bca4f-111">In this example, the [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) function shows a modal dialog that contains **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="bca4f-112">Se l'utente fa clic su **OK**, il programma chiama [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow).</span><span class="sxs-lookup"><span data-stu-id="bca4f-112">If the user clicks **OK**, the program calls [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow).</span></span> <span data-ttu-id="bca4f-113">In caso contrario, se l'utente fa clic su **Annulla**, la chiamata a **DestroyWindow** viene ignorata e la finestra rimane aperta.</span><span class="sxs-lookup"><span data-stu-id="bca4f-113">Otherwise, if the user clicks **Cancel**, the call to **DestroyWindow** is skipped, and the window remains open.</span></span> <span data-ttu-id="bca4f-114">In entrambi i casi, restituire zero per indicare che è stato gestito il messaggio.</span><span class="sxs-lookup"><span data-stu-id="bca4f-114">In either case, return zero to indicate that you handled the message.</span></span>

<span data-ttu-id="bca4f-115">Se si desidera chiudere la finestra senza richiedere conferma all'utente, è possibile chiamare semplicemente [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) senza la chiamata a [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).</span><span class="sxs-lookup"><span data-stu-id="bca4f-115">If you want to close the window without prompting the user, you could simply call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) without the call to [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).</span></span> <span data-ttu-id="bca4f-116">Tuttavia, in questo caso è presente un collegamento.</span><span class="sxs-lookup"><span data-stu-id="bca4f-116">However, there is a shortcut in this case.</span></span> <span data-ttu-id="bca4f-117">Ricordare che [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) esegue l'azione predefinita per qualsiasi messaggio della finestra.</span><span class="sxs-lookup"><span data-stu-id="bca4f-117">Recall that [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) executes the default action for any window message.</span></span> <span data-ttu-id="bca4f-118">Nel caso di [**WM \_ Close**](/windows/desktop/winmsg/wm-close), **DefWindowProc** chiama automaticamente **DestroyWindow**.</span><span class="sxs-lookup"><span data-stu-id="bca4f-118">In the case of [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close), **DefWindowProc** automatically calls **DestroyWindow**.</span></span> <span data-ttu-id="bca4f-119">Ciò significa che se si ignora il messaggio **WM \_ Close** nell'istruzione **Switch** , la finestra viene distrutta per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bca4f-119">That means if you ignore the **WM\_CLOSE** message in your **switch** statement, the window is destroyed by default.</span></span>

<span data-ttu-id="bca4f-120">Quando una finestra sta per essere distrutta, riceve un messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="bca4f-120">When a window is about to be destroyed, it receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="bca4f-121">Questo messaggio viene inviato dopo la rimozione della finestra dallo schermo, ma prima che venga eseguita la distruzione (in particolare, prima che qualsiasi finestra figlio venga distrutta).</span><span class="sxs-lookup"><span data-stu-id="bca4f-121">This message is sent after the window is removed from the screen, but before the destruction occurs (in particular, before any child windows are destroyed).</span></span>

<span data-ttu-id="bca4f-122">Nella finestra principale dell'applicazione, in genere si risponde a [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) chiamando [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).</span><span class="sxs-lookup"><span data-stu-id="bca4f-122">In your main application window, you will typically respond to [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) by calling [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).</span></span>

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

<span data-ttu-id="bca4f-123">Nella sezione messaggi della [finestra](window-messages.md) è stato visualizzato un messaggio [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) nella coda di messaggi [**, che causa**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) la fine del ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="bca4f-123">We saw in the [Window Messages](window-messages.md) section that [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) puts a [**WM\_QUIT**](/windows/desktop/winmsg/wm-quit) message on the message queue, causing the message loop to end.</span></span>

<span data-ttu-id="bca4f-124">Ecco un diagramma di flusso che mostra il modo tipico per elaborare i messaggi [**WM \_ Close**](/windows/desktop/winmsg/wm-close) e [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) :</span><span class="sxs-lookup"><span data-stu-id="bca4f-124">Here is a flow chart showing the typical way to process [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) and [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) messages:</span></span>

![diagramma di flusso che illustra come gestire \- i messaggi WM Close e WM \- Destroy](images/wmclose01.png)

## <a name="next"></a><span data-ttu-id="bca4f-126">Prossima</span><span class="sxs-lookup"><span data-stu-id="bca4f-126">Next</span></span>

[<span data-ttu-id="bca4f-127">Gestione dello stato di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="bca4f-127">Managing Application State</span></span>](managing-application-state-.md)