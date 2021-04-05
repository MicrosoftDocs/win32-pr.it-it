---
title: Messaggi di controllo
description: Questa sezione contiene informazioni sul modo in cui i messaggi di Windows vengono usati per comunicare con i controlli.
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923a1b47d625a2797a900a6c582d00c5169097f3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873173"
---
# <a name="control-messages"></a><span data-ttu-id="94703-103">Messaggi di controllo</span><span class="sxs-lookup"><span data-stu-id="94703-103">Control Messages</span></span>

<span data-ttu-id="94703-104">Questa sezione contiene informazioni sul modo in cui i messaggi di Windows vengono usati per comunicare con i controlli.</span><span class="sxs-lookup"><span data-stu-id="94703-104">This section contains information about how Windows messages are used to communicate with controls.</span></span>

<span data-ttu-id="94703-105">Vengono illustrati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="94703-105">The following topics are discussed.</span></span>

-   [<span data-ttu-id="94703-106">Messaggi ai controlli comuni</span><span class="sxs-lookup"><span data-stu-id="94703-106">Messages to Common Controls</span></span>](#messages-to-common-controls)
-   [<span data-ttu-id="94703-107">Notifiche da controlli</span><span class="sxs-lookup"><span data-stu-id="94703-107">Notifications from Controls</span></span>](#notifications-from-controls)
-   [<span data-ttu-id="94703-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94703-108">Related topics</span></span>](#related-topics)

## <a name="messages-to-common-controls"></a><span data-ttu-id="94703-109">Messaggi ai controlli comuni</span><span class="sxs-lookup"><span data-stu-id="94703-109">Messages to Common Controls</span></span>

<span data-ttu-id="94703-110">Poiché i controlli comuni sono Windows, un'applicazione può comunicare con essi usando messaggi Microsoft Win32 comuni, ad esempio [**WM \_ GetFont**](/windows/desktop/winmsg/wm-getfont) o [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext).</span><span class="sxs-lookup"><span data-stu-id="94703-110">Because common controls are windows, an application can communicate with them by using common Microsoft Win32 messages such as [**WM\_GETFONT**](/windows/desktop/winmsg/wm-getfont) or [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span> <span data-ttu-id="94703-111">Inoltre, la classe della finestra di ogni controllo comune supporta un set di messaggi specifici del controllo.</span><span class="sxs-lookup"><span data-stu-id="94703-111">In addition, the window class of each common control supports a set of control-specific messages.</span></span> <span data-ttu-id="94703-112">In genere, un'applicazione utilizza [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) per passare messaggi al controllo (spesso ricevendo informazioni nel valore restituito).</span><span class="sxs-lookup"><span data-stu-id="94703-112">Typically, an application uses [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) or [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) to pass messages to the control (often receiving information in the return value).</span></span>

<span data-ttu-id="94703-113">Alcuni controlli comuni includono anche un set di macro che un'applicazione può usare anziché [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="94703-113">Some common controls also have a set of macros that an application can use instead of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="94703-114">Le macro sono in genere più semplici da utilizzare rispetto alle funzioni.</span><span class="sxs-lookup"><span data-stu-id="94703-114">The macros are typically easier to use than the functions.</span></span> <span data-ttu-id="94703-115">Nell'esempio di codice seguente viene recuperato il testo dell'elemento della visualizzazione albero selezionato, prima utilizzando i messaggi non elaborati e il secondo tramite le macro equivalenti.</span><span class="sxs-lookup"><span data-stu-id="94703-115">The following example code retrieves the text of the selected tree-view item, first by using the raw messages, and second by using the equivalent macros.</span></span> <span data-ttu-id="94703-116">Si supponga che *HWND* sia l'handle della finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="94703-116">Assume that *hwnd* is the handle of the control window.</span></span>


```
BOOL fSuccess;
WCHAR itemText[99];
TVITEM tvItem = { 0 };
tvItem.mask = TVIF_TEXT;
tvItem.cchTextMax = ARRAYSIZE(itemText);
tvItem.pszText = itemText;

// This...
tvItem.hItem = (HTREEITEM)SendMessage(hwnd, TVM_GETNEXTITEM, TVGN_CARET, NULL);
fSuccess = SendMessage(hwnd, TVM_GETITEM, 0, (LPARAM)&tvItem);

// ... is equivalent to this.
tvItem.hItem = TreeView_GetSelection(hwnd);
fSuccess = TreeView_GetItem(hwnd, &tvItem);
```



<span data-ttu-id="94703-117">Quando viene apportata una modifica alle impostazioni dei colori di sistema, Windows invia un messaggio [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) a tutte le finestre di primo livello.</span><span class="sxs-lookup"><span data-stu-id="94703-117">When a change is made to the system color settings, Windows sends a [**WM\_SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) message to all top-level windows.</span></span> <span data-ttu-id="94703-118">La finestra di primo livello deve trasmettere il messaggio **WM \_ SYSCOLORCHANGE** ai controlli comuni; in caso contrario, i controlli non riceveranno una notifica della modifica del colore.</span><span class="sxs-lookup"><span data-stu-id="94703-118">Your top-level window must forward the **WM\_SYSCOLORCHANGE** message to its common controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="94703-119">L'invio del messaggio assicura che i colori utilizzati dai controlli comuni siano coerenti con quelli utilizzati da altri oggetti dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="94703-119">Forwarding the message ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="94703-120">Ad esempio, un controllo Toolbar usa il colore "oggetti 3D" per creare i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="94703-120">For example, a toolbar control uses the "3-D Objects" color to draw its buttons.</span></span> <span data-ttu-id="94703-121">Se l'utente modifica il colore dell'oggetto 3D, ma il messaggio **WM \_ SYSCOLORCHANGE** non viene trasmesso alla barra degli strumenti, i pulsanti della barra degli strumenti rimarranno nel colore originale (o anche in una combinazione di colori vecchi e nuovi), mentre il colore degli altri pulsanti del sistema cambia.</span><span class="sxs-lookup"><span data-stu-id="94703-121">If the user changes the 3-D Object's color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color (or even change to a combination of old and new colors) while the color of other buttons in the system changes.</span></span>

## <a name="notifications-from-controls"></a><span data-ttu-id="94703-122">Notifiche da controlli</span><span class="sxs-lookup"><span data-stu-id="94703-122">Notifications from Controls</span></span>

<span data-ttu-id="94703-123">I controlli sono finestre figlio che inviano messaggi di notifica alla finestra padre quando gli eventi, in genere attivati dall'input dell'utente, si verificano nel controllo.</span><span class="sxs-lookup"><span data-stu-id="94703-123">Controls are child windows that send notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="94703-124">L'applicazione si basa su questi messaggi di notifica per determinare l'azione che l'utente desidera eseguire.</span><span class="sxs-lookup"><span data-stu-id="94703-124">The application relies on these notification messages to determine what action the user wants it to take.</span></span> <span data-ttu-id="94703-125">Ad eccezione di trackbars, che usano i messaggi [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) per notificare al padre le modifiche, i controlli comuni inviano le notifiche tramite il [**\_ comando WM**](/windows/desktop/menurc/wm-command) o [**WM \_ Notify**](wm-notify.md) , come specificato nell'argomento di riferimento per la notifica.</span><span class="sxs-lookup"><span data-stu-id="94703-125">Except for trackbars, which use the [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages to notify their parent of changes, common controls send notifications as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages, as specified in the reference topic for the notification.</span></span> <span data-ttu-id="94703-126">In genere, le notifiche precedenti (quelle che sono state nell'API per molto tempo) usano **il \_ comando WM**.</span><span class="sxs-lookup"><span data-stu-id="94703-126">Typically, older notifications (those that have been in the API for a long time) use **WM\_COMMAND**.</span></span>

<span data-ttu-id="94703-127">Il parametro *lParam* di [**WM \_ Notify**](wm-notify.md) è l'indirizzo di una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) o l'indirizzo di una struttura più ampia che include **NMHDR** come primo membro.</span><span class="sxs-lookup"><span data-stu-id="94703-127">The *lParam* parameter of [**WM\_NOTIFY**](wm-notify.md) is either the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure or the address of a larger structure that includes **NMHDR** as its first member.</span></span> <span data-ttu-id="94703-128">La struttura contiene il codice di notifica e identifica il controllo comune che ha inviato il messaggio di notifica.</span><span class="sxs-lookup"><span data-stu-id="94703-128">The structure contains the notification code and identifies the common control that sent the notification message.</span></span> <span data-ttu-id="94703-129">Il significato degli eventuali membri della struttura rimanenti varia a seconda del codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="94703-129">The meaning of the remaining structure members, if any, varies depending on the notification code.</span></span>

<span data-ttu-id="94703-130">Ogni tipo di controllo comune ha un set di codici di notifica corrispondente.</span><span class="sxs-lookup"><span data-stu-id="94703-130">Each type of common control has a corresponding set of notification codes.</span></span> <span data-ttu-id="94703-131">La libreria di controlli comuni fornisce anche codici di notifica che possono essere inviati da più di un tipo di controllo comune.</span><span class="sxs-lookup"><span data-stu-id="94703-131">The common control library also provides notification codes that can be sent by more than one type of common control.</span></span> <span data-ttu-id="94703-132">Vedere la documentazione relativa al controllo di interesse per individuare i codici di notifica che verranno inviati e il formato da essi presi.</span><span class="sxs-lookup"><span data-stu-id="94703-132">See the documentation for the control of interest to determine which notification codes it will send and what format they take.</span></span>

<span data-ttu-id="94703-133">Per un esempio di codice che illustra come gestire i messaggi di [**\_ notifica WM**](wm-notify.md) , vedere l'argomento di riferimento per il messaggio.</span><span class="sxs-lookup"><span data-stu-id="94703-133">For example code showing how to handle [**WM\_NOTIFY**](wm-notify.md) messages, see the reference topic for that message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94703-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94703-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94703-135">Riferimento al controllo generale</span><span class="sxs-lookup"><span data-stu-id="94703-135">General Control Reference</span></span>](common-control-reference.md)
</dt> </dl>

 

 
