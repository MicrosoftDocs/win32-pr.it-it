---
description: Una barra degli strumenti del desktop dell'applicazione (detta anche AppBar) è una finestra simile alla barra delle applicazioni di Windows.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Uso delle barre degli strumenti del desktop applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140ef94c1daeb571cd0d766dfbd4dc28b7991efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128470"
---
# <a name="using-application-desktop-toolbars"></a><span data-ttu-id="f86e2-103">Uso delle barre degli strumenti del desktop applicazione</span><span class="sxs-lookup"><span data-stu-id="f86e2-103">Using Application Desktop Toolbars</span></span>

<span data-ttu-id="f86e2-104">Una *barra degli strumenti del desktop dell'applicazione* (detta anche AppBar) è una finestra simile alla barra delle applicazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="f86e2-104">An *application desktop toolbar* (also called an appbar) is a window that is similar to the Windows taskbar.</span></span> <span data-ttu-id="f86e2-105">È ancorato a un bordo dello schermo e contiene in genere pulsanti che consentono all'utente di accedere rapidamente ad altre applicazioni e finestre.</span><span class="sxs-lookup"><span data-stu-id="f86e2-105">It is anchored to an edge of the screen, and it typically contains buttons that give the user quick access to other applications and windows.</span></span> <span data-ttu-id="f86e2-106">Il sistema impedisce ad altre applicazioni di utilizzare l'area desktop utilizzata da un AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-106">The system prevents other applications from using the desktop area used by an appbar.</span></span> <span data-ttu-id="f86e2-107">Sul desktop può esistere un numero qualsiasi di AppBar in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="f86e2-107">Any number of appbars can exist on the desktop at any given time.</span></span>

<span data-ttu-id="f86e2-108">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f86e2-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f86e2-109">Informazioni sulle barre degli strumenti del desktop applicazione</span><span class="sxs-lookup"><span data-stu-id="f86e2-109">About Application Desktop Toolbars</span></span>](#about-application-desktop-toolbars)
    -   [<span data-ttu-id="f86e2-110">sending messages</span><span class="sxs-lookup"><span data-stu-id="f86e2-110">Sending Messages</span></span>](#sending-messages)
    -   [<span data-ttu-id="f86e2-111">Registrazione</span><span class="sxs-lookup"><span data-stu-id="f86e2-111">Registration</span></span>](#registration)
    -   [<span data-ttu-id="f86e2-112">Dimensioni e posizione AppBar</span><span class="sxs-lookup"><span data-stu-id="f86e2-112">Appbar Size and Position</span></span>](#appbar-size-and-position)
    -   [<span data-ttu-id="f86e2-113">Nascondi automaticamente le barre degli strumenti del desktop dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="f86e2-113">Autohide Application Desktop Toolbars</span></span>](#autohide-application-desktop-toolbars)
    -   [<span data-ttu-id="f86e2-114">Messaggi di notifica AppBar</span><span class="sxs-lookup"><span data-stu-id="f86e2-114">Appbar Notification Messages</span></span>](#appbar-notification-messages)
-   [<span data-ttu-id="f86e2-115">Registrazione di una barra degli strumenti del desktop dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="f86e2-115">Registering an Application Desktop Toolbar</span></span>](#registering-an-application-desktop-toolbar)
-   [<span data-ttu-id="f86e2-116">Impostazione delle dimensioni e della posizione del AppBar</span><span class="sxs-lookup"><span data-stu-id="f86e2-116">Setting the Appbar Size and Position</span></span>](#setting-the-appbar-size-and-position)
-   [<span data-ttu-id="f86e2-117">Elaborazione dei messaggi di notifica AppBar</span><span class="sxs-lookup"><span data-stu-id="f86e2-117">Processing Appbar Notification Messages</span></span>](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a><span data-ttu-id="f86e2-118">Informazioni sulle barre degli strumenti del desktop applicazione</span><span class="sxs-lookup"><span data-stu-id="f86e2-118">About Application Desktop Toolbars</span></span>

<span data-ttu-id="f86e2-119">Windows fornisce un'API che consente di sfruttare i vantaggi offerti dai servizi AppBar forniti dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f86e2-119">Windows provides an API that lets you take advantage of appbar services provided by the system.</span></span> <span data-ttu-id="f86e2-120">I servizi consentono di garantire che i AppBar definiti dall'applicazione funzionino senza problemi tra loro e con la barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f86e2-120">The services help ensure that application-defined appbars operate smoothly with one another and with the taskbar.</span></span> <span data-ttu-id="f86e2-121">Il sistema mantiene le informazioni su ogni AppBar e invia i messaggi AppBar per notificare gli eventi che possono influire sulle dimensioni, sulla posizione e sull'aspetto.</span><span class="sxs-lookup"><span data-stu-id="f86e2-121">The system maintains information about each appbar and sends the appbars messages to notify them about events that can affect their size, position, and appearance.</span></span>

### <a name="sending-messages"></a><span data-ttu-id="f86e2-122">sending messages</span><span class="sxs-lookup"><span data-stu-id="f86e2-122">Sending Messages</span></span>

<span data-ttu-id="f86e2-123">Un'applicazione usa uno speciale set di messaggi, denominati messaggi AppBar, per aggiungere o rimuovere un AppBar, impostare le dimensioni e la posizione di AppBar e recuperare le informazioni sulle dimensioni, sulla posizione e sullo stato della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f86e2-123">An application uses a special set of messages, called appbar messages, to add or remove an appbar, set an appbar's size and position, and retrieve information about the size, position, and state of the taskbar.</span></span> <span data-ttu-id="f86e2-124">Per inviare un messaggio AppBar, un'applicazione deve usare la funzione [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-124">To send an appbar message, an application must use the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function.</span></span> <span data-ttu-id="f86e2-125">I parametri della funzione includono un identificatore del messaggio, ad esempio [**ABM \_ New**](abm-new.md), e l'indirizzo di una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-125">The function's parameters include a message identifier, such as [**ABM\_NEW**](abm-new.md), and the address of an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="f86e2-126">I membri della struttura contengono informazioni necessarie al sistema per elaborare il messaggio specificato.</span><span class="sxs-lookup"><span data-stu-id="f86e2-126">The structure members contain information that the system needs to process the given message.</span></span>

<span data-ttu-id="f86e2-127">Per ogni messaggio AppBar, il sistema usa alcuni membri della struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) e ignora gli altri.</span><span class="sxs-lookup"><span data-stu-id="f86e2-127">For any given appbar message, the system uses some members of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure and ignores the others.</span></span> <span data-ttu-id="f86e2-128">Tuttavia, il sistema usa sempre i membri **cbSize** e **HWND** , quindi un'applicazione deve compilare tali membri per ogni messaggio di AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-128">However, the system always uses the **cbSize** and **hWnd** members, so an application must fill these members for every appbar message.</span></span> <span data-ttu-id="f86e2-129">Il membro **cbSize** specifica le dimensioni della struttura e il membro **HWND** è l'handle per la finestra di AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-129">The **cbSize** member specifies the size of the structure, and the **hWnd** member is the handle to the appbar's window.</span></span>

<span data-ttu-id="f86e2-130">Alcuni messaggi AppBar richiedono informazioni dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f86e2-130">Some appbar messages request information from the system.</span></span> <span data-ttu-id="f86e2-131">Durante l'elaborazione di questi messaggi, il sistema copia le informazioni richieste nella struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-131">When processing these messages, the system copies the requested information into the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

### <a name="registration"></a><span data-ttu-id="f86e2-132">Registrazione</span><span class="sxs-lookup"><span data-stu-id="f86e2-132">Registration</span></span>

<span data-ttu-id="f86e2-133">Il sistema mantiene un elenco interno di AppBar e gestisce le informazioni su ogni barra dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="f86e2-133">The system keeps an internal list of appbars and maintains information about each bar in the list.</span></span> <span data-ttu-id="f86e2-134">Il sistema utilizza le informazioni per gestire AppBar, per eseguirne i servizi e per inviare messaggi di notifica.</span><span class="sxs-lookup"><span data-stu-id="f86e2-134">The system uses the information to manage appbars, perform services for them, and send them notification messages.</span></span>

<span data-ttu-id="f86e2-135">Un'applicazione deve registrare un AppBar (ovvero aggiungerlo all'elenco interno) prima di poter ricevere i servizi AppBar dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f86e2-135">An application must register an appbar (that is, add it to the internal list) before it can receive appbar services from the system.</span></span> <span data-ttu-id="f86e2-136">Per registrare un AppBar, un'applicazione invia il [**\_ nuovo messaggio ABM**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-136">To register an appbar, an application sends the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="f86e2-137">La struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) associata include l'handle per la finestra di AppBar e un identificatore di messaggio definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f86e2-137">The accompanying [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure includes the handle to the appbar's window and an application-defined message identifier.</span></span> <span data-ttu-id="f86e2-138">Il sistema utilizza l'identificatore del messaggio per inviare messaggi di notifica alla routine della finestra AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-138">The system uses the message identifier to send notification messages to the window procedure of the appbar window.</span></span> <span data-ttu-id="f86e2-139">Per ulteriori informazioni, vedere AppBar Notification messages.</span><span class="sxs-lookup"><span data-stu-id="f86e2-139">For more information, see Appbar Notification Messages.</span></span>

<span data-ttu-id="f86e2-140">Un'applicazione annulla la registrazione di un AppBar inviando il messaggio di [**\_ rimozione di ABM**](abm-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-140">An application unregisters an appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="f86e2-141">L'annullamento della registrazione di un AppBar lo rimuove dall'elenco interno del sistema di AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-141">Unregistering an appbar removes it from the system's internal list of appbars.</span></span> <span data-ttu-id="f86e2-142">Il sistema non invia più messaggi di notifica a AppBar o impedisce ad altre applicazioni di utilizzare l'area dello schermo utilizzata dal AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-142">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span> <span data-ttu-id="f86e2-143">Un'applicazione deve sempre inviare **la \_ rimozione di ABM** prima di eliminare un AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-143">An application should always send **ABM\_REMOVE** before destroying an appbar.</span></span>

### <a name="appbar-size-and-position"></a><span data-ttu-id="f86e2-144">Dimensioni e posizione AppBar</span><span class="sxs-lookup"><span data-stu-id="f86e2-144">Appbar Size and Position</span></span>

<span data-ttu-id="f86e2-145">Un'applicazione deve impostare le dimensioni e la posizione di un AppBar in modo che non interferisca con altri AppBar o la barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f86e2-145">An application should set an appbar's size and position so that it does not interfere with any other appbars or the taskbar.</span></span> <span data-ttu-id="f86e2-146">Ogni AppBar deve essere ancorato a un bordo particolare dello schermo e più AppBar possono essere ancorati a un bordo.</span><span class="sxs-lookup"><span data-stu-id="f86e2-146">Every appbar must be anchored to a particular edge of the screen, and multiple appbars can be anchored to an edge.</span></span> <span data-ttu-id="f86e2-147">Tuttavia, se un AppBar è ancorato allo stesso bordo della barra delle applicazioni, il sistema garantisce che la barra delle applicazioni si trovi sempre sul bordo più esterno.</span><span class="sxs-lookup"><span data-stu-id="f86e2-147">However, if an appbar is anchored to the same edge as the taskbar, the system ensures that the taskbar is always on the outermost edge.</span></span>

<span data-ttu-id="f86e2-148">Per impostare le dimensioni e la posizione di un AppBar, un'applicazione propone prima di tutto un bordo dello schermo e un rettangolo di delimitazione per il AppBar inviando il messaggio di [**\_ QUERYPOS ABM**](abm-querypos.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-148">To set the size and position of an appbar, an application first proposes a screen edge and bounding rectangle for the appbar by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="f86e2-149">Il sistema determina se una parte dell'area dello schermo all'interno del rettangolo proposto viene utilizzata dalla barra delle applicazioni o da un altro AppBar, regola il rettangolo (se necessario) e restituisce il rettangolo modificato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f86e2-149">The system determines whether any part of the screen area within the proposed rectangle is used by the taskbar or another appbar, adjusts the rectangle (if necessary), and returns the adjusted rectangle to the application.</span></span>

<span data-ttu-id="f86e2-150">Successivamente, l'applicazione invia il [**messaggio \_ SETPOS di ABM**](abm-setpos.md) per impostare il nuovo rettangolo di delimitazione per il AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-150">Next, the application sends the [**ABM\_SETPOS**](abm-setpos.md) message to set the new bounding rectangle for the appbar.</span></span> <span data-ttu-id="f86e2-151">Anche in questo caso, il sistema può regolare il rettangolo prima di restituirlo all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f86e2-151">Again, the system may adjust the rectangle before returning it to the application.</span></span> <span data-ttu-id="f86e2-152">Per questo motivo, l'applicazione deve usare il rettangolo modificato restituito da **ABM \_ SETPOS** per impostare le dimensioni e la posizione finali.</span><span class="sxs-lookup"><span data-stu-id="f86e2-152">For this reason, the application should use the adjusted rectangle returned by **ABM\_SETPOS** to set the final size and position.</span></span> <span data-ttu-id="f86e2-153">L'applicazione può usare la funzione [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) per spostare il AppBar in posizione.</span><span class="sxs-lookup"><span data-stu-id="f86e2-153">The application can use the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="f86e2-154">Utilizzando un processo in due passaggi per impostare le dimensioni e la posizione, il sistema consente all'applicazione di fornire feedback intermedio all'utente durante l'operazione di spostamento.</span><span class="sxs-lookup"><span data-stu-id="f86e2-154">By using a two-step process to set the size and position, the system enables the application to provide intermediate feedback to the user during the move operation.</span></span> <span data-ttu-id="f86e2-155">Se, ad esempio, l'utente trascina un AppBar, l'applicazione potrebbe visualizzare un rettangolo ombreggiato che indica la nuova posizione prima che il AppBar venga effettivamente spostato.</span><span class="sxs-lookup"><span data-stu-id="f86e2-155">For example, if the user drags an appbar, the application might display a shaded rectangle indicating the new position before the appbar actually moves.</span></span>

<span data-ttu-id="f86e2-156">Un'applicazione deve impostare la dimensione e la posizione del relativo AppBar dopo la registrazione e ogni volta che il AppBar riceve il messaggio di notifica [**\_ POSCHANGED di ABN**](abn-poschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-156">An application should set the size and position of its appbar after registering it and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="f86e2-157">Un AppBar riceve questo messaggio di notifica ogni volta che si verifica una modifica nella dimensione, nella posizione o nello stato di visibilità della barra delle applicazioni e ogni volta che un altro AppBar sullo stesso lato dello schermo viene ridimensionato, aggiunto o rimosso.</span><span class="sxs-lookup"><span data-stu-id="f86e2-157">An appbar receives this notification message whenever a change occurs in the taskbar's size, position, or visibility state and whenever another appbar on the same side of the screen is resized, added, or removed.</span></span>

<span data-ttu-id="f86e2-158">Ogni volta che un AppBar riceve il \_ messaggio di attivazione WM, deve inviare il messaggio di [**\_ attivazione di ABM**](abm-activate.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-158">Whenever an appbar receives the WM\_ACTIVATE message, it should send the [**ABM\_ACTIVATE**](abm-activate.md) message.</span></span> <span data-ttu-id="f86e2-159">Analogamente, quando un AppBar riceve un \_ messaggio WM WINDOWPOSCHANGED, deve chiamare [**ABM \_ WINDOWPOSCHANGED**](abm-windowposchanged.md).</span><span class="sxs-lookup"><span data-stu-id="f86e2-159">Similarly, when an appbar receives a WM\_WINDOWPOSCHANGED message, it must call [**ABM\_WINDOWPOSCHANGED**](abm-windowposchanged.md).</span></span> <span data-ttu-id="f86e2-160">L'invio di questi messaggi garantisce che il sistema imposti correttamente lo z-order di qualsiasi AppBar di Nascondi automaticamente sullo stesso perimetro.</span><span class="sxs-lookup"><span data-stu-id="f86e2-160">Sending these messages ensures that the system properly sets the z-order of any autohide appbars on the same edge.</span></span>

### <a name="autohide-application-desktop-toolbars"></a><span data-ttu-id="f86e2-161">Nascondi automaticamente le barre degli strumenti del desktop dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="f86e2-161">Autohide Application Desktop Toolbars</span></span>

<span data-ttu-id="f86e2-162">Un AppBar di Nascondi automaticamente è uno che in genere è nascosto ma diventa visibile quando l'utente sposta il cursore del mouse sul bordo dello schermo a cui è associato il AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-162">An autohide appbar is one that is normally hidden but becomes visible when the user moves the mouse cursor to the screen edge with which the appbar is associated.</span></span> <span data-ttu-id="f86e2-163">Il AppBar si nasconde nuovamente quando l'utente sposta il cursore del mouse fuori dal rettangolo di delimitazione della barra.</span><span class="sxs-lookup"><span data-stu-id="f86e2-163">The appbar hides itself again when the user moves the mouse cursor out of the bar's bounding rectangle.</span></span>

<span data-ttu-id="f86e2-164">Sebbene il sistema consenta un numero di AppBar diversi in un determinato momento, consente solo un AppBar di Nascondi alla volta per ogni bordo dello schermo in base alla prima, prima di tutto.</span><span class="sxs-lookup"><span data-stu-id="f86e2-164">Although the system allows a number of different appbars at any given time, it allows only one autohide appbar at a time for each screen edge on a first-come, first-served basis.</span></span> <span data-ttu-id="f86e2-165">Il sistema mantiene automaticamente l'ordine z di un AppBar di Nascondi automaticamente (solo all'interno del gruppo z order).</span><span class="sxs-lookup"><span data-stu-id="f86e2-165">The system automatically maintains the z-order of an autohide appbar (within its z-order group only).</span></span>

<span data-ttu-id="f86e2-166">Un'applicazione usa il [**messaggio \_ SETAUTOHIDEBAR di ABM**](abm-setautohidebar.md) per registrare o annullare la registrazione di un AppBar di Nascondi automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f86e2-166">An application uses the [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) message to register or unregister an autohide appbar.</span></span> <span data-ttu-id="f86e2-167">Il messaggio specifica il bordo per AppBar e un flag che specifica se il AppBar deve essere registrato o annullato.</span><span class="sxs-lookup"><span data-stu-id="f86e2-167">The message specifies the edge for the appbar and a flag that specifies whether the appbar is to be registered or unregistered.</span></span> <span data-ttu-id="f86e2-168">Il messaggio ha esito negativo se un AppBar di Nascondi automaticamente viene registrato, ma ne è già associato uno al bordo specificato.</span><span class="sxs-lookup"><span data-stu-id="f86e2-168">The message fails if an autohide appbar is being registered but one is already associated with the specified edge.</span></span> <span data-ttu-id="f86e2-169">Un'applicazione può recuperare l'handle per il AppBar di Nascondi automaticamente associato a un bordo inviando il messaggio di [**\_ GETAUTOHIDEBAR ABM**](abm-getautohidebar.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-169">An application can retrieve the handle to the autohide appbar associated with an edge by sending the [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) message.</span></span>

<span data-ttu-id="f86e2-170">Non è necessario che un AppBar di Nascondi automaticamente si registri come AppBar normali; Ciò significa che non è necessario registrarlo inviando il nuovo messaggio [**ABM \_**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-170">An autohide appbar does not need to register as a normal appbar; that is, it does not need to be registered by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="f86e2-171">Un AppBar non registrato da **ABM \_ New** si sovrappone a qualsiasi AppBar ancorato sullo stesso bordo dello schermo.</span><span class="sxs-lookup"><span data-stu-id="f86e2-171">An appbar that is not registered by **ABM\_NEW** overlaps any appbars anchored on the same edge of the screen.</span></span>

### <a name="appbar-notification-messages"></a><span data-ttu-id="f86e2-172">Messaggi di notifica AppBar</span><span class="sxs-lookup"><span data-stu-id="f86e2-172">Appbar Notification Messages</span></span>

<span data-ttu-id="f86e2-173">Il sistema invia messaggi per notificare a un AppBar gli eventi che possono influire sulla posizione e sull'aspetto.</span><span class="sxs-lookup"><span data-stu-id="f86e2-173">The system sends messages to notify an appbar about events that can affect its position and appearance.</span></span> <span data-ttu-id="f86e2-174">I messaggi vengono inviati nel contesto di un messaggio definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f86e2-174">The messages are sent in the context of an application-defined message.</span></span> <span data-ttu-id="f86e2-175">L'applicazione specifica l'identificatore del messaggio quando invia il nuovo messaggio [**ABM \_**](abm-new.md) per registrare il AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-175">The application specifies the identifier of the message when it sends the [**ABM\_NEW**](abm-new.md) message to register the appbar.</span></span> <span data-ttu-id="f86e2-176">Il codice di notifica si trova nel parametro *wParam* del messaggio definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f86e2-176">The notification code is in the *wParam* parameter of the application-defined message.</span></span>

<span data-ttu-id="f86e2-177">Un AppBar riceve il messaggio di notifica [**\_ POSCHANGED di ABN**](abn-poschanged.md) quando cambia la dimensione, la posizione o lo stato di visibilità della barra delle applicazioni, quando un altro AppBar viene aggiunto allo stesso bordo dello schermo o quando un altro AppBar sullo stesso bordo dello schermo viene ridimensionato o rimosso.</span><span class="sxs-lookup"><span data-stu-id="f86e2-177">An appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message when the taskbar's size, position, or visibility state changes, when another appbar is added to the same edge of the screen, or when another appbar on the same edge of the screen is resized or removed.</span></span> <span data-ttu-id="f86e2-178">Un AppBar deve rispondere a questo messaggio di notifica inviando i messaggi [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-178">An appbar should respond to this notification message by sending [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="f86e2-179">Se la posizione di un AppBar è cambiata, deve chiamare la funzione [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) per spostarsi alla nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="f86e2-179">If an appbar's position has changed, it should call the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

<span data-ttu-id="f86e2-180">Il sistema invia il messaggio di notifica [**\_ STATECHANGE di ABN**](abn-statechange.md) ogni volta che lo stato di Nascondi automaticamente o sempre in primo piano della barra delle applicazioni è cambiato, ovvero quando l'utente seleziona o deseleziona la casella di controllo **Always on top** o **Nascondi automaticamente** nella finestra delle proprietà della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f86e2-180">The system sends the [**ABN\_STATECHANGE**](abn-statechange.md) notification message whenever the taskbar's autohide or always-on-top state has changed—that is, when the user selects or clears the **Always on top** or **Auto hide** check box on the taskbar's property sheet.</span></span> <span data-ttu-id="f86e2-181">Un AppBar può utilizzare questo messaggio di notifica per impostare lo stato di conformità a quello della barra delle applicazioni, se lo si desidera.</span><span class="sxs-lookup"><span data-stu-id="f86e2-181">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

<span data-ttu-id="f86e2-182">Quando viene avviata un'applicazione a schermo intero o quando viene chiusa l'ultima applicazione a schermo intero, un AppBar riceve il messaggio di notifica [**\_ FULLSCREENAPP di ABN**](abn-fullscreenapp.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-182">When a full-screen application is started or when the last full-screen application is closed, an appbar receives the [**ABN\_FULLSCREENAPP**](abn-fullscreenapp.md) notification message.</span></span> <span data-ttu-id="f86e2-183">Il parametro *lParam* indica se l'applicazione a schermo intero è in apertura o in chiusura.</span><span class="sxs-lookup"><span data-stu-id="f86e2-183">The *lParam* parameter indicates whether the full-screen application is opening or closing.</span></span> <span data-ttu-id="f86e2-184">Se si apre, il AppBar deve essere rilasciato nella parte inferiore dello z-order.</span><span class="sxs-lookup"><span data-stu-id="f86e2-184">If it is opening, the appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="f86e2-185">Il AppBar deve ripristinare la posizione dell'ordine z quando l'ultima applicazione a schermo intero è stata chiusa.</span><span class="sxs-lookup"><span data-stu-id="f86e2-185">The appbar should restore its z-order position when the last full-screen application has closed.</span></span>

<span data-ttu-id="f86e2-186">Un AppBar riceve il messaggio di notifica [**\_ WINDOWARRANGE di ABN**](abn-windowarrange.md) quando l'utente seleziona il comando Cascade, affianca orizzontalmente o Affianca verticalmente dal menu di scelta rapida della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f86e2-186">An appbar receives the [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) notification message when the user selects the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span> <span data-ttu-id="f86e2-187">Il sistema invia il messaggio due volte, prima di ridisporre le finestre (*lParam* è **true**) e dopo la disposizione di Windows (*lParam* è **false**).</span><span class="sxs-lookup"><span data-stu-id="f86e2-187">The system sends the message two times—before rearranging the windows (*lParam* is **TRUE**) and after arranging the windows (*lParam* is **FALSE**).</span></span>

<span data-ttu-id="f86e2-188">Un AppBar può usare i messaggi [**\_ WINDOWARRANGE di ABN**](abn-windowarrange.md) per escludere se stesso dall'operazione Cascade o Tile.</span><span class="sxs-lookup"><span data-stu-id="f86e2-188">An appbar can use [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) messages to exclude itself from the cascade or tile operation.</span></span> <span data-ttu-id="f86e2-189">Per escludere se stesso, AppBar deve nascondersi quando *lParam* è **true** e mostrarsi quando *lParam* è **false**.</span><span class="sxs-lookup"><span data-stu-id="f86e2-189">To exclude itself, the appbar should hide itself when *lParam* is **TRUE** and show itself when *lParam* is **FALSE**.</span></span> <span data-ttu-id="f86e2-190">Se un AppBar si nasconde in risposta a questo messaggio, non è necessario inviare i messaggi [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS**](abm-setpos.md) in risposta all'operazione Cascade o Tile.</span><span class="sxs-lookup"><span data-stu-id="f86e2-190">If an appbar hides itself in response to this message, it does not need to send the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages in response to the cascade or tile operation.</span></span>

## <a name="registering-an-application-desktop-toolbar"></a><span data-ttu-id="f86e2-191">Registrazione di una barra degli strumenti del desktop dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="f86e2-191">Registering an Application Desktop Toolbar</span></span>

<span data-ttu-id="f86e2-192">Un'applicazione deve registrare un AppBar inviando il [**\_ nuovo messaggio ABM**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-192">An application must register an appbar by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="f86e2-193">La registrazione di un AppBar lo aggiunge all'elenco interno del sistema e fornisce al sistema un identificatore di messaggio da usare per inviare messaggi di notifica al AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-193">Registering an appbar adds it to the system's internal list and provides the system with a message identifier to use to send notification messages to the appbar.</span></span> <span data-ttu-id="f86e2-194">Prima di uscire, un'applicazione deve annullare la registrazione del AppBar inviando il messaggio di [**\_ rimozione di ABM**](abm-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-194">Before exiting, an application must unregister the appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="f86e2-195">L'annullamento della registrazione rimuove il AppBar dall'elenco interno del sistema e impedisce alla barra di ricevere messaggi di notifica AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-195">Unregistering removes the appbar from the system's internal list and prevents the bar from receiving appbar notification messages.</span></span>

<span data-ttu-id="f86e2-196">La funzione nell'esempio seguente registra o Annulla la registrazione di un AppBar, a seconda del valore di un parametro del flag booleano.</span><span class="sxs-lookup"><span data-stu-id="f86e2-196">The function in the following example either registers or unregisters an appbar, depending on the value of a Boolean flag parameter.</span></span>


```C++
// RegisterAccessBar - registers or unregisters an appbar. 
// Returns TRUE if successful, or FALSE otherwise. 

// hwndAccessBar - handle to the appbar 
// fRegister - register and unregister flag 

// Global variables 
//     g_uSide - screen edge (defaults to ABE_TOP) 
//     g_fAppRegistered - flag indicating whether the bar is registered 

BOOL RegisterAccessBar(HWND hwndAccessBar, BOOL fRegister) 
{ 
    APPBARDATA abd; 
    
    // An application-defined message identifier
    APPBAR_CALLBACK = (WM_USER + 0x01);
    
    // Specify the structure size and handle to the appbar. 
    abd.cbSize = sizeof(APPBARDATA); 
    abd.hWnd = hwndAccessBar; 

    if (fRegister) 
    { 
        // Provide an identifier for notification messages. 
        abd.uCallbackMessage = APPBAR_CALLBACK; 

        // Register the appbar. 
        if (!SHAppBarMessage(ABM_NEW, &abd)) 
            return FALSE; 

        g_uSide = ABE_TOP;       // default edge 
        g_fAppRegistered = TRUE; 

    } 
    else 
    { 
        // Unregister the appbar. 
        SHAppBarMessage(ABM_REMOVE, &abd); 
        g_fAppRegistered = FALSE; 
    } 

    return TRUE; 
}
```



## <a name="setting-the-appbar-size-and-position"></a><span data-ttu-id="f86e2-197">Impostazione delle dimensioni e della posizione del AppBar</span><span class="sxs-lookup"><span data-stu-id="f86e2-197">Setting the Appbar Size and Position</span></span>

<span data-ttu-id="f86e2-198">Un'applicazione deve impostare le dimensioni e la posizione di un AppBar dopo la registrazione del AppBar, dopo che l'utente ha spostato o ridimensionato il AppBar e ogni volta che il AppBar riceve il messaggio di notifica [**\_ POSCHANGED di ABN**](abn-poschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-198">An application should set an appbar's size and position after registering the appbar, after the user user moves or sizes the appbar, and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="f86e2-199">Prima di impostare le dimensioni e la posizione del AppBar, l'applicazione esegue una query sul sistema per un rettangolo di delimitazione approvato inviando il messaggio di [**\_ QUERYPOS ABM**](abm-querypos.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-199">Before setting the size and position of the appbar, the application queries the system for an approved bounding rectangle by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="f86e2-200">Il sistema restituisce un rettangolo di delimitazione che non interferisce con la barra delle applicazioni o con altri AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-200">The system returns a bounding rectangle that does not interfere with the taskbar or any other appbar.</span></span> <span data-ttu-id="f86e2-201">Il sistema regola il rettangolo esclusivamente in base alla sottrazione del rettangolo. non è possibile mantenere le dimensioni iniziali del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="f86e2-201">The system adjusts the rectangle purely by rectangle subtraction; it makes no effort to preserve the rectangle's initial size.</span></span> <span data-ttu-id="f86e2-202">Per questo motivo, il AppBar deve modificare il rettangolo, se necessario, dopo l'invio **di \_ QUERYPOS ABM**.</span><span class="sxs-lookup"><span data-stu-id="f86e2-202">For this reason, the appbar should readjust the rectangle, as necessary, after sending **ABM\_QUERYPOS**.</span></span>

<span data-ttu-id="f86e2-203">Successivamente, l'applicazione passa di nuovo il rettangolo di delimitazione al sistema tramite il [**messaggio \_ SETPOS di ABM**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="f86e2-203">Next, the application passes the bounding rectangle back to the system by using the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span> <span data-ttu-id="f86e2-204">Chiama quindi la funzione [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) per spostare il AppBar in posizione.</span><span class="sxs-lookup"><span data-stu-id="f86e2-204">Then it calls the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="f86e2-205">Nell'esempio seguente viene illustrato come impostare le dimensioni e la posizione di un AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-205">The following example shows how to set an appbar's size and position.</span></span>


```C++
// AppBarQuerySetPos - sets the size and position of an appbar. 

// uEdge - screen edge to which the appbar is to be anchored 
// lprc - current bounding rectangle of the appbar 
// pabd - address of the APPBARDATA structure with the hWnd and cbSize members filled

void PASCAL AppBarQuerySetPos(UINT uEdge, LPRECT lprc, PAPPBARDATA pabd) 
{ 
    int iHeight = 0; 
    int iWidth = 0; 

    pabd->rc = *lprc; 
    pabd->uEdge = uEdge; 

    // Copy the screen coordinates of the appbar's bounding 
    // rectangle into the APPBARDATA structure. 
    if ((uEdge == ABE_LEFT) || (uEdge == ABE_RIGHT)) 
    { 
        iWidth = pabd->rc.right - pabd->rc.left; 
        pabd->rc.top = 0; 
        pabd->rc.bottom = GetSystemMetrics(SM_CYSCREEN); 
    } 
    else 
    { 
        iHeight = pabd->rc.bottom - pabd->rc.top; 
        pabd->rc.left = 0; 
        pabd->rc.right = GetSystemMetrics(SM_CXSCREEN); 
    } 

    // Query the system for an approved size and position. 
    SHAppBarMessage(ABM_QUERYPOS, pabd); 

    // Adjust the rectangle, depending on the edge to which the appbar is anchored.
    switch (uEdge) 
    { 
        case ABE_LEFT: 
            pabd->rc.right = pabd->rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            pabd->rc.left = pabd->rc.right - iWidth; 
            break; 

        case ABE_TOP: 
            pabd->rc.bottom = pabd->rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            pabd->rc.top = pabd->rc.bottom - iHeight; 
            break; 
    } 

    // Pass the final bounding rectangle to the system. 
    SHAppBarMessage(ABM_SETPOS, pabd); 

    // Move and size the appbar so that it conforms to the 
    // bounding rectangle passed to the system. 
    MoveWindow(pabd->hWnd, 
               pabd->rc.left, 
               pabd->rc.top, 
               pabd->rc.right - pabd->rc.left, 
               pabd->rc.bottom - pabd->rc.top, 
               TRUE); 

}
```



## <a name="processing-appbar-notification-messages"></a><span data-ttu-id="f86e2-206">Elaborazione dei messaggi di notifica AppBar</span><span class="sxs-lookup"><span data-stu-id="f86e2-206">Processing Appbar Notification Messages</span></span>

<span data-ttu-id="f86e2-207">Un AppBar riceve un messaggio di notifica quando viene modificato lo stato della barra delle applicazioni, quando viene avviata un'applicazione a schermo intero (o l'ultimo si chiude) o quando si verifica un evento che può influire sulle dimensioni e la posizione di AppBar.</span><span class="sxs-lookup"><span data-stu-id="f86e2-207">An appbar receives a notification message when the state of the taskbar changes, when a full-screen application starts (or the last one closes), or when an event occurs that can affect the appbar's size and position.</span></span> <span data-ttu-id="f86e2-208">Nell'esempio seguente viene illustrato come elaborare i vari messaggi di notifica.</span><span class="sxs-lookup"><span data-stu-id="f86e2-208">The following example shows how to process the various notification messages.</span></span>


```C++
// AppBarCallback - processes notification messages sent by the system. 

// hwndAccessBar - handle to the appbar 
// uNotifyMsg - identifier of the notification message 
// lParam - message parameter 

void AppBarCallback(HWND hwndAccessBar, UINT uNotifyMsg, 
    LPARAM lParam) 
{ 
    APPBARDATA abd; 
    UINT uState; 

    abd.cbSize = sizeof(abd); 
    abd.hWnd = hwndAccessBar; 

    switch (uNotifyMsg) 
    { 
        case ABN_STATECHANGE: 

            // Check to see if the taskbar's always-on-top state has changed
            // and, if it has, change the appbar's state accordingly.
            uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

            SetWindowPos(hwndAccessBar, 
                         (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                         0, 0, 0, 0, 
                         SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 

            break; 

        case ABN_FULLSCREENAPP: 

            // A full-screen application has started, or the last full-screen
            // application has closed. Set the appbar's z-order appropriately.
            if (lParam) 
            { 
                SetWindowPos(hwndAccessBar, 
                             (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                             0, 0, 0, 0, 
                             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 
            else 
            { 
                uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

                if (uState & ABS_ALWAYSONTOP) 
                    SetWindowPos(hwndAccessBar, 
                                 HWND_TOPMOST, 
                                 0, 0, 0, 0, 
                                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 

        case ABN_POSCHANGED: 

            // The taskbar or another appbar has changed its size or position.
            AppBarPosChanged(&abd); 
            break; 
    } 
}
```



<span data-ttu-id="f86e2-209">La funzione seguente regola il rettangolo di delimitazione di un AppBar e quindi chiama la funzione AppBarQuerySetPos definita dall'applicazione (inclusa nella sezione precedente) per impostare di conseguenza le dimensioni e la posizione della barra.</span><span class="sxs-lookup"><span data-stu-id="f86e2-209">The following function adjusts an appbar's bounding rectangle and then calls the application-defined AppBarQuerySetPos function (included in the previous section) to set the bar's size and position accordingly.</span></span>


```C++
// AppBarPosChanged - adjusts the appbar's size and position. 

// pabd - address of an APPBARDATA structure that contains information 
//        used to adjust the size and position. 

void PASCAL AppBarPosChanged(PAPPBARDATA pabd) 
{ 
    RECT rc; 
    RECT rcWindow; 
    int iHeight; 
    int iWidth; 

    rc.top = 0; 
    rc.left = 0; 
    rc.right = GetSystemMetrics(SM_CXSCREEN); 
    rc.bottom = GetSystemMetrics(SM_CYSCREEN); 

    GetWindowRect(pabd->hWnd, &rcWindow); 

    iHeight = rcWindow.bottom - rcWindow.top; 
    iWidth = rcWindow.right - rcWindow.left; 

    switch (g_uSide) 
    { 
        case ABE_TOP: 
            rc.bottom = rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            rc.top = rc.bottom - iHeight; 
            break; 

        case ABE_LEFT: 
            rc.right = rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            rc.left = rc.right - iWidth; 
            break; 
    } 

    AppBarQuerySetPos(g_uSide, &rc, pabd); 
}
```



 

 
