---
title: 'Messaggi dei pulsanti '
description: Un pulsante può inviare messaggi alla relativa finestra padre e una finestra padre può inviare messaggi a un pulsante.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1601f269ec1242a10579d2ace812723d3ead7f84
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103734042"
---
# <a name="button-messages"></a><span data-ttu-id="513f3-103">Messaggi dei pulsanti </span><span class="sxs-lookup"><span data-stu-id="513f3-103">Button Messages</span></span>

<span data-ttu-id="513f3-104">Un pulsante può inviare messaggi alla relativa finestra padre e una finestra padre può inviare messaggi a un pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-104">A button can send messages to its parent window, and a parent window can send messages to a button.</span></span>

<span data-ttu-id="513f3-105">In questa sezione vengono descritti gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="513f3-105">The following topics are discussed in this section.</span></span>

-   [<span data-ttu-id="513f3-106">Invio di messaggi ai pulsanti</span><span class="sxs-lookup"><span data-stu-id="513f3-106">Sending Messages to Buttons</span></span>](#sending-messages-to-buttons)
-   [<span data-ttu-id="513f3-107">Gestione dei messaggi da un pulsante</span><span class="sxs-lookup"><span data-stu-id="513f3-107">Handling Messages from a Button</span></span>](#handling-messages-from-a-button)
-   [<span data-ttu-id="513f3-108">Messaggi di notifica dai pulsanti</span><span class="sxs-lookup"><span data-stu-id="513f3-108">Notification Messages from Buttons</span></span>](#notification-messages-from-buttons)
-   [<span data-ttu-id="513f3-109">Messaggi colori pulsante</span><span class="sxs-lookup"><span data-stu-id="513f3-109">Button Color Messages</span></span>](#button-color-messages)
-   [<span data-ttu-id="513f3-110">Elaborazione dei messaggi predefiniti del pulsante</span><span class="sxs-lookup"><span data-stu-id="513f3-110">Button Default Message Processing</span></span>](#button-default-message-processing)
-   [<span data-ttu-id="513f3-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="513f3-111">Related topics</span></span>](#related-topics)

## <a name="sending-messages-to-buttons"></a><span data-ttu-id="513f3-112">Invio di messaggi ai pulsanti</span><span class="sxs-lookup"><span data-stu-id="513f3-112">Sending Messages to Buttons</span></span>

<span data-ttu-id="513f3-113">Una finestra padre può inviare messaggi a un pulsante in una finestra sovrapposta o figlio utilizzando la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) oppure può inviare messaggi a un pulsante in una finestra di dialogo utilizzando le funzioni [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)e [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .</span><span class="sxs-lookup"><span data-stu-id="513f3-113">A parent window can send messages to a button in an overlapped or child window by using the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, or it can send messages to a button in a dialog box by using the [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton), and [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) functions.</span></span>

<span data-ttu-id="513f3-114">Un'applicazione può usare il messaggio [**BM \_ GetCheck**](bm-getcheck.md) per recuperare lo stato di selezione di una casella di controllo o di un pulsante di opzione.</span><span class="sxs-lookup"><span data-stu-id="513f3-114">An application can use the [**BM\_GETCHECK**](bm-getcheck.md) message to retrieve the check state of a check box or radio button.</span></span> <span data-ttu-id="513f3-115">Un'applicazione può anche usare il messaggio [**BM \_ GetState**](bm-getstate.md) per recuperare gli stati correnti del pulsante (stato di selezione, stato di push e stato attivo).</span><span class="sxs-lookup"><span data-stu-id="513f3-115">An application can also use the [**BM\_GETSTATE**](bm-getstate.md) message to retrieve the button's current states (the check state, push state, and focus state).</span></span> <span data-ttu-id="513f3-116">Per ottenere informazioni su uno stato specifico, utilizzare una maschera di maschera sul valore dello stato restituito.</span><span class="sxs-lookup"><span data-stu-id="513f3-116">To get information about a specific state, use a bitmask on the returned state value.</span></span>

<span data-ttu-id="513f3-117">Il [**messaggio \_ di controllo BM**](bm-setcheck.md) imposta lo stato di selezione di una casella di controllo o di un pulsante di opzione. il messaggio restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="513f3-117">The [**BM\_SETCHECK**](bm-setcheck.md) message sets the check state of a check box or radio button; the message returns zero.</span></span> <span data-ttu-id="513f3-118">Il messaggio di [**\_ stato BM**](bm-setstate.md) imposta lo stato di push di un pulsante. il messaggio restituisce anche zero.</span><span class="sxs-lookup"><span data-stu-id="513f3-118">The [**BM\_SETSTATE**](bm-setstate.md) message sets the push state of a button; this message also returns zero.</span></span> <span data-ttu-id="513f3-119">Il messaggio [**BM \_ Sestyle**](bm-setstyle.md) modifica lo stile di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-119">The [**BM\_SETSTYLE**](bm-setstyle.md) message changes the style of a button.</span></span> <span data-ttu-id="513f3-120">È progettato per modificare gli stili dei pulsanti all'interno di un tipo (ad esempio, la modifica di una casella di controllo in una casella di controllo automatica).</span><span class="sxs-lookup"><span data-stu-id="513f3-120">It is designed for changing button styles within a type (for example, changing a check box to an automatic check box).</span></span> <span data-ttu-id="513f3-121">Non è progettato per la modifica tra i tipi, ad esempio la modifica di una casella di controllo in un pulsante di opzione.</span><span class="sxs-lookup"><span data-stu-id="513f3-121">It is not designed for changing between types (for example, changing a check box to a radio button).</span></span> <span data-ttu-id="513f3-122">Un'applicazione non deve modificare un pulsante da un tipo a un altro.</span><span class="sxs-lookup"><span data-stu-id="513f3-122">An application should not change a button from one type to another.</span></span>

<span data-ttu-id="513f3-123">Un pulsante della [**\_ bitmap BS**](button-styles.md) o dello stile dell' [**\_ icona BS**](button-styles.md) Visualizza una bitmap o un'icona anziché un testo.</span><span class="sxs-lookup"><span data-stu-id="513f3-123">A button of the [**BS\_BITMAP**](button-styles.md) or [**BS\_ICON**](button-styles.md) style displays a bitmap or icon instead of text.</span></span> <span data-ttu-id="513f3-124">Il messaggio [**BM \_ diImage**](bm-setimage.md) associa un handle a una bitmap o a un'icona con un pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-124">The [**BM\_SETIMAGE**](bm-setimage.md) message associates a handle to a bitmap or icon with a button.</span></span> <span data-ttu-id="513f3-125">Il messaggio [**BM \_ GetImage**](bm-getimage.md) recupera un handle per la bitmap o l'icona associata a un pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-125">The [**BM\_GETIMAGE**](bm-getimage.md) message retrieves a handle to the bitmap or icon associated with a button.</span></span>

<span data-ttu-id="513f3-126">Un'applicazione può inoltre utilizzare il messaggio [**DM \_ GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) per recuperare l'identificatore del controllo pulsante di push predefinito in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="513f3-126">An application can also use the [**DM\_GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) message to retrieve the identifier of the default push button control in a dialog box.</span></span> <span data-ttu-id="513f3-127">Un'applicazione può utilizzare il messaggio [**DM \_ SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) per impostare il pulsante di push predefinito per una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="513f3-127">An application can use the [**DM\_SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) message to set the default push button for a dialog box.</span></span>

<span data-ttu-id="513f3-128">La chiamata della funzione [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) o [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) equivale all'invio di un messaggio di [**\_ controllo BM**](bm-setcheck.md) .</span><span class="sxs-lookup"><span data-stu-id="513f3-128">Calling the [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) or [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) function is equivalent to sending a [**BM\_SETCHECK**](bm-setcheck.md) message.</span></span> <span data-ttu-id="513f3-129">La chiamata della funzione [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) equivale all'invio di un messaggio [**BM \_ GetCheck**](bm-getcheck.md) .</span><span class="sxs-lookup"><span data-stu-id="513f3-129">Calling the [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) function is equivalent to sending a [**BM\_GETCHECK**](bm-getcheck.md) message.</span></span>

## <a name="handling-messages-from-a-button"></a><span data-ttu-id="513f3-130">Gestione dei messaggi da un pulsante</span><span class="sxs-lookup"><span data-stu-id="513f3-130">Handling Messages from a Button</span></span>

<span data-ttu-id="513f3-131">Le notifiche da un pulsante vengono inviate tramite [**il \_ comando WM**](/windows/desktop/menurc/wm-command) o i messaggi di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="513f3-131">Notifications from a button are sent as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="513f3-132">Le informazioni sul messaggio utilizzato sono reperibili nella pagina di riferimento per ogni notifica.</span><span class="sxs-lookup"><span data-stu-id="513f3-132">Information about which message is used can be found on the reference page for each notification.</span></span>

<span data-ttu-id="513f3-133">Per ulteriori informazioni sulla gestione dei messaggi, vedere [Control Messages](control-messages.md).</span><span class="sxs-lookup"><span data-stu-id="513f3-133">For more information on how to handle messages, see [Control Messages](control-messages.md).</span></span> <span data-ttu-id="513f3-134">Vedere anche messaggi dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="513f3-134">See also Button Messages.</span></span>

## <a name="notification-messages-from-buttons"></a><span data-ttu-id="513f3-135">Messaggi di notifica dai pulsanti</span><span class="sxs-lookup"><span data-stu-id="513f3-135">Notification Messages from Buttons</span></span>

<span data-ttu-id="513f3-136">Quando l'utente fa clic su un pulsante, lo stato cambia e il pulsante Invia i codici di notifica, sotto forma di messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) , alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="513f3-136">When the user clicks a button, its state changes, and the button sends notification codes, in the form of [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages, to its parent window.</span></span> <span data-ttu-id="513f3-137">Ad esempio, un controllo pulsante di comando Invia il codice di notifica [ \_ fatto clic su BN](bn-clicked.md) ogni volta che l'utente sceglie il pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-137">For example, a push button control sends the [BN\_CLICKED](bn-clicked.md) notification code whenever the user chooses the button.</span></span> <span data-ttu-id="513f3-138">In tutti i casi (ad eccezione di [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)), la parola di basso livello del parametro *wParam* contiene l'identificatore di controllo, la parola più significativa di *wParam* contiene il codice di notifica e il parametro *lParam* contiene l'handle della finestra di controllo.</span><span class="sxs-lookup"><span data-stu-id="513f3-138">In all cases (except for [BCN\_HOTITEMCHANGE](bcn-hotitemchange.md)), the low-order word of the *wParam* parameter contains the control identifier, the high-order word of *wParam* contains the notification code, and the *lParam* parameter contains the control window handle.</span></span>

<span data-ttu-id="513f3-139">Il messaggio e la risposta della finestra padre dipendono dal tipo, dallo stile e dallo stato corrente del pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-139">Both the message and the parent window's response depend on the type, style, and current state of the button.</span></span> <span data-ttu-id="513f3-140">Di seguito sono riportati i codici di notifica dei pulsanti che un'applicazione deve monitorare ed elaborare.</span><span class="sxs-lookup"><span data-stu-id="513f3-140">Following are the button notification codes an application should monitor and process.</span></span>



| <span data-ttu-id="513f3-141">Codice di notifica</span><span class="sxs-lookup"><span data-stu-id="513f3-141">Notification code</span></span>                                                        | <span data-ttu-id="513f3-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="513f3-142">Description</span></span>                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="513f3-143">\_HOTITEMCHANGE BCN</span><span class="sxs-lookup"><span data-stu-id="513f3-143">BCN\_HOTITEMCHANGE</span></span>](bcn-hotitemchange.md)                              | <span data-ttu-id="513f3-144">Il mouse è stato immesso o lasciato l'area client di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-144">The mouse entered or left the client area of a button.</span></span> |
| [<span data-ttu-id="513f3-145">BN \_ selezionato</span><span class="sxs-lookup"><span data-stu-id="513f3-145">BN\_CLICKED</span></span>](bn-clicked.md)                                            | <span data-ttu-id="513f3-146">L'utente ha fatto clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-146">The user clicked a button.</span></span>                             |
| <span data-ttu-id="513f3-147">[BN \_ DBLCLK](bn-dblclk.md) o [BN con \_ DoubleClick](bn-doubleclicked.md)</span><span class="sxs-lookup"><span data-stu-id="513f3-147">[BN\_DBLCLK](bn-dblclk.md) or [BN\_DOUBLECLICKED](bn-doubleclicked.md)</span></span> | <span data-ttu-id="513f3-148">L'utente ha fatto doppio clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-148">The user double-clicked a button.</span></span>                      |
| [<span data-ttu-id="513f3-149">BN- \_ disabilitazione</span><span class="sxs-lookup"><span data-stu-id="513f3-149">BN\_DISABLE</span></span>](bn-disable.md)                                            | <span data-ttu-id="513f3-150">Un pulsante è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="513f3-150">A button is disabled.</span></span>                                  |
| <span data-ttu-id="513f3-151">[BN \_ PUSH](bn-pushed.md) o [BN \_ HILITE](bn-hilite.md)</span><span class="sxs-lookup"><span data-stu-id="513f3-151">[BN\_PUSHED](bn-pushed.md) or [BN\_HILITE](bn-hilite.md)</span></span>               | <span data-ttu-id="513f3-152">L'utente ha eseguito il push di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-152">The user pushed a button.</span></span>                              |
| [<span data-ttu-id="513f3-153">BN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="513f3-153">BN\_KILLFOCUS</span></span>](bn-killfocus.md)                                        | <span data-ttu-id="513f3-154">Il pulsante ha perso lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="513f3-154">The button lost the keyboard focus.</span></span>                    |
| [<span data-ttu-id="513f3-155">\_disegno BN</span><span class="sxs-lookup"><span data-stu-id="513f3-155">BN\_PAINT</span></span>](bn-paint.md)                                                | <span data-ttu-id="513f3-156">È necessario disegnare il pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-156">The button should be painted.</span></span>                          |
| [<span data-ttu-id="513f3-157">\_CONattivazione BN</span><span class="sxs-lookup"><span data-stu-id="513f3-157">BN\_SETFOCUS</span></span>](bn-setfocus.md)                                          | <span data-ttu-id="513f3-158">Il pulsante ha ottenuto lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="513f3-158">The button gained the keyboard focus.</span></span>                  |
| <span data-ttu-id="513f3-159">[BN \_ Unpushd](bn-unpushed.md) o [BN \_ UNHILITE](bn-unhilite.md)</span><span class="sxs-lookup"><span data-stu-id="513f3-159">[BN\_UNPUSHED](bn-unpushed.md) or [BN\_UNHILITE](bn-unhilite.md)</span></span>       | <span data-ttu-id="513f3-160">Il pulsante non viene più inserito.</span><span class="sxs-lookup"><span data-stu-id="513f3-160">The button is no longer pushed.</span></span>                        |



 

<span data-ttu-id="513f3-161">Un pulsante Invia i [BN \_ Disable](bn-disable.md), [BN \_ push](bn-pushed.md), [BN \_ KILLFOCUS](bn-killfocus.md), [BN \_ Paint](bn-paint.md), [BN \_ SetFocus](bn-setfocus.md)e BN i codici di notifica [ \_ unpushed](bn-unpushed.md) solo se lo stile di [**\_ notifica BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="513f3-161">A button sends the [BN\_DISABLE](bn-disable.md), [BN\_PUSHED](bn-pushed.md), [BN\_KILLFOCUS](bn-killfocus.md), [BN\_PAINT](bn-paint.md), [BN\_SETFOCUS](bn-setfocus.md), and [BN\_UNPUSHED](bn-unpushed.md) notification codes only if it has the [**BS\_NOTIFY**](button-styles.md) style.</span></span> <span data-ttu-id="513f3-162">[BN \_](bn-dblclk.md) I codici di notifica DBLCLK vengono inviati automaticamente per i pulsanti [**BS \_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)e [**BS \_ OWNERDRAW**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="513f3-162">[BN\_DBLCLK](bn-dblclk.md) notification codes are sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="513f3-163">Altri tipi di pulsante inviano BN \_ DBLCLK solo se hanno lo stile di **\_ notifica BS** .</span><span class="sxs-lookup"><span data-stu-id="513f3-163">Other button types send BN\_DBLCLK only if they have the **BS\_NOTIFY** style.</span></span> <span data-ttu-id="513f3-164">Tutti i pulsanti inviano il codice di notifica [ \_ fatto clic su BN](bn-clicked.md) indipendentemente dagli stili dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="513f3-164">All buttons send the [BN\_CLICKED](bn-clicked.md) notification code regardless of their button styles.</span></span>

<span data-ttu-id="513f3-165">Per i pulsanti automatici, il sistema modifica lo stato di push e disegna il pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-165">For automatic buttons, the system changes the push state and paints the button.</span></span> <span data-ttu-id="513f3-166">In questo caso, l'applicazione in genere elabora solo i [BN \_ clic](bn-clicked.md) e i codici di notifica [ \_ DBLCLK BN](bn-dblclk.md) .</span><span class="sxs-lookup"><span data-stu-id="513f3-166">In this case, the application typically processes only the [BN\_CLICKED](bn-clicked.md) and [BN\_DBLCLK](bn-dblclk.md) notification codes.</span></span> <span data-ttu-id="513f3-167">Per i pulsanti non automatici, l'applicazione in genere risponde al codice di notifica inviando un messaggio per modificare lo stato del pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-167">For buttons that are not automatic, the application typically responds to the notification code by sending a message to change the state of the button.</span></span> <span data-ttu-id="513f3-168">Per informazioni sull'invio di messaggi ai pulsanti, vedere l'argomento relativo [all'invio di messaggi ai pulsanti](#sending-messages-to-buttons).</span><span class="sxs-lookup"><span data-stu-id="513f3-168">For information about sending messages to buttons, see [Sending Messages to Buttons](#sending-messages-to-buttons).</span></span>

<span data-ttu-id="513f3-169">Quando l'utente seleziona un pulsante creato dal proprietario, il pulsante Invia alla finestra padre un messaggio [**WM \_ DrawItem**](wm-drawitem.md) contenente l'identificatore del controllo da disegnare e le informazioni sulle dimensioni e sullo stato.</span><span class="sxs-lookup"><span data-stu-id="513f3-169">When the user selects an owner-drawn button, the button sends its parent window a [**WM\_DRAWITEM**](wm-drawitem.md) message containing the identifier of the control to be drawn and information about its dimensions and state.</span></span>

## <a name="button-color-messages"></a><span data-ttu-id="513f3-170">Messaggi colori pulsante</span><span class="sxs-lookup"><span data-stu-id="513f3-170">Button Color Messages</span></span>

<span data-ttu-id="513f3-171">Il sistema fornisce valori di colore predefiniti per i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="513f3-171">The system provides default color values for buttons.</span></span> <span data-ttu-id="513f3-172">Un'applicazione può recuperare i valori predefiniti per questi colori chiamando la funzione [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) o impostare i valori chiamando la funzione [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) .</span><span class="sxs-lookup"><span data-stu-id="513f3-172">An application can retrieve the default values for these colors by calling the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) function, or set the values by calling the [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) function.</span></span> <span data-ttu-id="513f3-173">Nella tabella seguente vengono illustrati i valori predefiniti dei colori dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="513f3-173">The following table shows the default button-color values.</span></span>



| <span data-ttu-id="513f3-174">Valore</span><span class="sxs-lookup"><span data-stu-id="513f3-174">Value</span></span>               | <span data-ttu-id="513f3-175">Elemento colorato</span><span class="sxs-lookup"><span data-stu-id="513f3-175">Element colored</span></span>                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="513f3-176">\_BTNFACE colore</span><span class="sxs-lookup"><span data-stu-id="513f3-176">COLOR\_BTNFACE</span></span>      | <span data-ttu-id="513f3-177">Visi pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-177">Button faces.</span></span>                                                                                                              |
| <span data-ttu-id="513f3-178">\_BTNHIGHLIGHT colore</span><span class="sxs-lookup"><span data-stu-id="513f3-178">COLOR\_BTNHIGHLIGHT</span></span> | <span data-ttu-id="513f3-179">Area evidenziata (i bordi superiore e sinistro) di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-179">Highlight area (the top and left edges) of a button.</span></span>                                                                       |
| <span data-ttu-id="513f3-180">\_BTNSHADOW colore</span><span class="sxs-lookup"><span data-stu-id="513f3-180">COLOR\_BTNSHADOW</span></span>    | <span data-ttu-id="513f3-181">Area ombreggiata (bordi inferiore e destro) di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-181">Shadow area (the bottom and right edges) of a button.</span></span>                                                                      |
| <span data-ttu-id="513f3-182">\_BTNTEXT colore</span><span class="sxs-lookup"><span data-stu-id="513f3-182">COLOR\_BTNTEXT</span></span>      | <span data-ttu-id="513f3-183">Testo normale (non in grigio) nei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="513f3-183">Regular (nongrayed) text in buttons.</span></span>                                                                                       |
| <span data-ttu-id="513f3-184">\_GRAYTEXT colore</span><span class="sxs-lookup"><span data-stu-id="513f3-184">COLOR\_GRAYTEXT</span></span>     | <span data-ttu-id="513f3-185">Testo disabilitato (grigio) nei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="513f3-185">Disabled (gray) text in buttons.</span></span> <span data-ttu-id="513f3-186">Questo colore è impostato su 0 se il driver di visualizzazione corrente non supporta un colore grigio a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="513f3-186">This color is set to 0 if the current display driver does not support a solid gray color.</span></span> |
| <span data-ttu-id="513f3-187">\_finestra colori</span><span class="sxs-lookup"><span data-stu-id="513f3-187">COLOR\_WINDOW</span></span>       | <span data-ttu-id="513f3-188">Sfondi della finestra.</span><span class="sxs-lookup"><span data-stu-id="513f3-188">Window backgrounds.</span></span>                                                                                                        |
| <span data-ttu-id="513f3-189">\_WINDOWFRAME colore</span><span class="sxs-lookup"><span data-stu-id="513f3-189">COLOR\_WINDOWFRAME</span></span>  | <span data-ttu-id="513f3-190">Frame della finestra.</span><span class="sxs-lookup"><span data-stu-id="513f3-190">Window frames.</span></span>                                                                                                             |
| <span data-ttu-id="513f3-191">\_WINDOWTEXT colore</span><span class="sxs-lookup"><span data-stu-id="513f3-191">COLOR\_WINDOWTEXT</span></span>   | <span data-ttu-id="513f3-192">Testo di Windows.</span><span class="sxs-lookup"><span data-stu-id="513f3-192">Text in windows.</span></span>                                                                                                           |



 

<span data-ttu-id="513f3-193">Tuttavia, la chiamata di [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) ha effetto su tutte le applicazioni, pertanto non è necessario chiamare questa funzione per personalizzare i pulsanti per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="513f3-193">However, calling [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) affects all applications, so you should not call this function to customize buttons for your application.</span></span>

<span data-ttu-id="513f3-194">Il sistema invia un messaggio [**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md) alla finestra padre di un pulsante prima di disegnare un pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-194">The system sends a [**WM\_CTLCOLORBTN**](wm-ctlcolorbtn.md) message to a button's parent window before drawing a button.</span></span> <span data-ttu-id="513f3-195">Questo messaggio contiene un handle per il contesto di dispositivo del pulsante e un handle per la finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="513f3-195">This message contains a handle to the button's device context and a handle to the child window.</span></span> <span data-ttu-id="513f3-196">La finestra padre può usare questi handle per modificare il testo del pulsante e i colori di sfondo.</span><span class="sxs-lookup"><span data-stu-id="513f3-196">The parent window can use these handles to change the button's text and background colors.</span></span> <span data-ttu-id="513f3-197">Tuttavia, solo i pulsanti creati dal proprietario rispondono alla finestra padre che elabora il messaggio.</span><span class="sxs-lookup"><span data-stu-id="513f3-197">However, only owner-drawn buttons respond to the parent window processing the message.</span></span>

## <a name="button-default-message-processing"></a><span data-ttu-id="513f3-198">Elaborazione dei messaggi predefiniti del pulsante</span><span class="sxs-lookup"><span data-stu-id="513f3-198">Button Default Message Processing</span></span>

<span data-ttu-id="513f3-199">La routine della finestra per la classe della finestra di controllo Button predefinita esegue l'elaborazione predefinita per tutti i messaggi che la routine di controllo Button non elabora.</span><span class="sxs-lookup"><span data-stu-id="513f3-199">The window procedure for the predefined button control window class carries out default processing for all messages that the button control procedure does not process.</span></span> <span data-ttu-id="513f3-200">Quando la procedura di controllo Button restituisce **false** per qualsiasi messaggio, la routine della finestra predefinita controlla i messaggi ed esegue le azioni predefinite elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="513f3-200">When the button control procedure returns **FALSE** for any message, the predefined window procedure checks the messages and performs the default actions listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="513f3-201">Message</span><span class="sxs-lookup"><span data-stu-id="513f3-201">Message</span></span></th>
<th><span data-ttu-id="513f3-202">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="513f3-202">Default action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="513f3-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span></span></td>
<td><span data-ttu-id="513f3-204">Invia al pulsante un <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> e un messaggio di <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> e invia alla finestra padre un <a href="bn-clicked.md">BN_CLICKED</a> codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="513f3-204">Sends the button a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> and a <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> message, and sends the parent window a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="513f3-206">Restituisce lo stato di selezione del pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-206">Returns the check state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="513f3-208">Restituisce un handle per la bitmap o l'icona associata al pulsante o <strong>null</strong> se il pulsante non dispone di una bitmap o di un'icona.</span><span class="sxs-lookup"><span data-stu-id="513f3-208">Returns a handle to the bitmap or icon associated with the button or <strong>NULL</strong> if the button has no bitmap or icon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="513f3-210">Restituisce lo stato di selezione corrente, lo stato di push e lo stato di attivazione del pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-210">Returns the current check state, push state, and focus state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="513f3-212">Imposta lo stato di selezione di tutti gli stili di pulsanti di opzione e caselle di controllo.</span><span class="sxs-lookup"><span data-stu-id="513f3-212">Sets the check state for all styles of radio buttons and check boxes.</span></span> <span data-ttu-id="513f3-213">Se il parametro <em>wParam</em> è maggiore di zero per i pulsanti di opzione, al pulsante viene assegnato lo stile <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="513f3-213">If the <em>wParam</em> parameter is greater than zero for radio buttons, the button is given the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> style.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="513f3-215">Associa l'handle di bitmap o icona specificato al pulsante e restituisce un handle per la bitmap o l'icona precedente.</span><span class="sxs-lookup"><span data-stu-id="513f3-215">Associates the specified bitmap or icon handle with the button and returns a handle to the previous bitmap or icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="513f3-217">Imposta lo stato di push del pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-217">Sets the push state of the button.</span></span> <span data-ttu-id="513f3-218">Per i pulsanti creati dal proprietario, viene inviato un messaggio di <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> alla finestra padre se lo stato del pulsante è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="513f3-218">For owner-drawn buttons, a <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> message is sent to the parent window if the state of the button has changed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span></span></td>
<td><span data-ttu-id="513f3-220">Imposta lo stile del pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-220">Sets the button style.</span></span> <span data-ttu-id="513f3-221">Se la parola di ordine inferiore del parametro <em>lParam</em> è <strong>true</strong>, il pulsante viene ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="513f3-221">If the low-order word of the <em>lParam</em> parameter is <strong>TRUE</strong>, the button is redrawn.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span></span></td>
<td><span data-ttu-id="513f3-223">Controlla una casella di controllo o una casella di controllo automatica quando l'utente preme le chiavi più (+) o uguale (=).</span><span class="sxs-lookup"><span data-stu-id="513f3-223">Checks a check box or automatic check box when the user presses the plus (+) or equal (=) keys.</span></span> <span data-ttu-id="513f3-224">Deseleziona una casella di controllo o una casella di controllo automatica quando l'utente preme il tasto meno (–).</span><span class="sxs-lookup"><span data-stu-id="513f3-224">Clears a check box or automatic check box when the user presses the minus (–) key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span></span></td>
<td><span data-ttu-id="513f3-226">Disegna il pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-226">Paints the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span></span></td>
<td><span data-ttu-id="513f3-228">Cancella lo sfondo per i pulsanti creati dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="513f3-228">Erases the background for owner-drawn buttons.</span></span> <span data-ttu-id="513f3-229">Gli sfondi di altri pulsanti vengono cancellati come parte del <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> e <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="513f3-229">The backgrounds of other buttons are erased as part of the <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> and <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span></span></td>
<td><span data-ttu-id="513f3-231">Restituisce valori che indicano il tipo di input elaborato dalla routine del pulsante predefinito, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="513f3-231">Returns values that indicate the type of input processed by the default button procedure, as shown in the following table.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="513f3-232">Stile pulsante</span><span class="sxs-lookup"><span data-stu-id="513f3-232">Button style</span></span></th>
<th><span data-ttu-id="513f3-233">Restituisce</span><span class="sxs-lookup"><span data-stu-id="513f3-233">Returns</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="513f3-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="513f3-235">DLGC_WANTCHARS | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="513f3-235">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="513f3-237">DLGC_RADIOBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="513f3-237">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="513f3-239">DLGC_WANTCHARS | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="513f3-239">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="513f3-241">DLGC_DEFPUSHBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="513f3-241">DLGC_DEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span></span></td>
<td><span data-ttu-id="513f3-243">DLGC_STATIC</span><span class="sxs-lookup"><span data-stu-id="513f3-243">DLGC_STATIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="513f3-245">DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="513f3-245">DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="513f3-247">DLGC_RADIOBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="513f3-247">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span></span></td>
<td><span data-ttu-id="513f3-249">Restituisce un handle per il tipo di carattere corrente.</span><span class="sxs-lookup"><span data-stu-id="513f3-249">Returns a handle to the current font.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span></span></td>
<td><span data-ttu-id="513f3-251">Inserisce il pulsante se l'utente preme la barra SPAZIAtrice.</span><span class="sxs-lookup"><span data-stu-id="513f3-251">Pushes the button if the user presses the SPACEBAR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span></span></td>
<td><span data-ttu-id="513f3-253">Rilascia l'acquisizione del mouse per tutti i case tranne il tasto TAB.</span><span class="sxs-lookup"><span data-stu-id="513f3-253">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="513f3-255">Rimuove il rettangolo di attivazione da un pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-255">Removes the focus rectangle from a button.</span></span> <span data-ttu-id="513f3-256">Per i pulsanti di push e i pulsanti di push predefiniti, il rettangolo di attivazione è invalidato.</span><span class="sxs-lookup"><span data-stu-id="513f3-256">For push buttons and default push buttons, the focus rectangle is invalidated.</span></span> <span data-ttu-id="513f3-257">Se il pulsante ha l'acquisizione del mouse, l'acquisizione viene rilasciata, il pulsante non viene selezionato e viene rimosso qualsiasi stato di push.</span><span class="sxs-lookup"><span data-stu-id="513f3-257">If the button has the mouse capture, the capture is released, the button is not clicked, and any push state is removed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span></span></td>
<td><span data-ttu-id="513f3-259">Invia un codice di notifica <a href="bn-dblclk.md">BN_DBLCLK</a> alla finestra padre per i pulsanti di opzione e i pulsanti creati dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="513f3-259">Sends a <a href="bn-dblclk.md">BN_DBLCLK</a> notification code to the parent window for radio buttons and owner-drawn buttons.</span></span> <span data-ttu-id="513f3-260">Per gli altri pulsanti, un doppio clic viene elaborato come messaggio <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="513f3-260">For other buttons, a double-click is processed as a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span></span></td>
<td><span data-ttu-id="513f3-262">Evidenzia il pulsante se la posizione del cursore del mouse si trova all'interno del rettangolo client del pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-262">Highlights the button if the position of the mouse cursor is within the button's client rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span></span></td>
<td><span data-ttu-id="513f3-264">Rilascia l'acquisizione del mouse se il pulsante ha l'acquisizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="513f3-264">Releases the mouse capture if the button had the mouse capture.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span></span></td>
<td><span data-ttu-id="513f3-266">Esegue la stessa azione di <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, se il pulsante ha l'acquisizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="513f3-266">Performs the same action as <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, if the button has the mouse capture.</span></span> <span data-ttu-id="513f3-267">In caso contrario, non viene eseguita alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="513f3-267">Otherwise, no action is performed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span></span></td>
<td><span data-ttu-id="513f3-269">Consente di trasformare qualsiasi <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> pulsante in un pulsante <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="513f3-269">Turns any <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> button into a <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> button.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span></span></td>
<td><span data-ttu-id="513f3-271">Restituisce HTTRANSPARENT se il controllo Button è una casella di gruppo.</span><span class="sxs-lookup"><span data-stu-id="513f3-271">Returns HTTRANSPARENT, if the button control is a group box.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span></span></td>
<td><span data-ttu-id="513f3-273">Disegna il pulsante in base allo stile e allo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="513f3-273">Draws the button according to its style and current state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="513f3-275">Disegna un rettangolo di attivazione sul pulsante per ottenere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="513f3-275">Draws a focus rectangle on the button getting the focus.</span></span> <span data-ttu-id="513f3-276">Per i pulsanti di opzione e i pulsanti di opzione automatici, alla finestra padre viene inviato un <a href="bn-clicked.md">BN_CLICKED</a> codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="513f3-276">For radio buttons and automatic radio buttons, the parent window is sent a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span></span></td>
<td><span data-ttu-id="513f3-278">Imposta un nuovo tipo di carattere e, facoltativamente, aggiorna la finestra.</span><span class="sxs-lookup"><span data-stu-id="513f3-278">Sets a new font and optionally updates the window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="513f3-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span></span></td>
<td><span data-ttu-id="513f3-280">Imposta il testo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="513f3-280">Sets the text of the button.</span></span> <span data-ttu-id="513f3-281">Nel caso di una casella di gruppo, il messaggio viene disegnato sul testo preesistente prima di ridisegnare la casella di gruppo con il nuovo testo.</span><span class="sxs-lookup"><span data-stu-id="513f3-281">In the case of a group box, the message paints over the preexisting text before repainting the group box with the new text.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="513f3-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="513f3-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span></span></td>
<td><span data-ttu-id="513f3-283">Rilascia l'acquisizione del mouse per tutti i case tranne il tasto TAB.</span><span class="sxs-lookup"><span data-stu-id="513f3-283">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="513f3-284">La routine della finestra predefinita passa tutti gli altri messaggi alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per l'elaborazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="513f3-284">The predefined window procedure passes all other messages to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function for default processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="513f3-285">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="513f3-285">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="513f3-286">Messaggi di controllo</span><span class="sxs-lookup"><span data-stu-id="513f3-286">Control Messages</span></span>](control-messages.md)
</dt> </dl>

 

 