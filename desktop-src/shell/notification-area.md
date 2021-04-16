---
description: L'area di notifica è una parte della barra delle applicazioni che fornisce un'origine temporanea per le notifiche e lo stato.
ms.assetid: D37E2BF7-1887-4780-81AD-85B2117321E4
title: Notifiche e area di notifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af1d0b8af0b41674f79325f0eeb389cbc8f2c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344141"
---
# <a name="notifications-and-the-notification-area"></a><span data-ttu-id="964ae-103">Notifiche e area di notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-103">Notifications and the Notification Area</span></span>

<span data-ttu-id="964ae-104">L'area di notifica è una parte della barra delle applicazioni che fornisce un'origine temporanea per le notifiche e lo stato.</span><span class="sxs-lookup"><span data-stu-id="964ae-104">The notification area is a portion of the taskbar that provides a temporary source for notifications and status.</span></span> <span data-ttu-id="964ae-105">Può anche essere usato per visualizzare le icone per le funzionalità di sistema e di programma che non hanno presenza sul desktop, ad esempio il livello di batteria, il controllo del volume e lo stato della rete.</span><span class="sxs-lookup"><span data-stu-id="964ae-105">It can also be used to display icons for system and program features that have no presence on the desktop, such as battery level, volume control, and network status.</span></span> <span data-ttu-id="964ae-106">L'area di notifica è nota storicamente come area di stato o barra di sistema.</span><span class="sxs-lookup"><span data-stu-id="964ae-106">The notification area has been known historically as the system tray or status area.</span></span>

<span data-ttu-id="964ae-107">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="964ae-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="964ae-108">Linee guida per le notifiche e l'area di notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-108">Notification and Notification Area Guidelines</span></span>](#notification-and-notification-area-guidelines)
-   [<span data-ttu-id="964ae-109">Creazione e visualizzazione di una notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-109">Creating and Displaying a Notification</span></span>](#notifications-and-the-notification-area)
    -   [<span data-ttu-id="964ae-110">Aggiungere un'icona di notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-110">Add a Notification Icon</span></span>](#add-a-notification-icon)
    -   [<span data-ttu-id="964ae-111">Definire la versione di NOTIFYICONDATA</span><span class="sxs-lookup"><span data-stu-id="964ae-111">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
    -   [<span data-ttu-id="964ae-112">Definire l'aspetto e il contenuto della notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-112">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
    -   [<span data-ttu-id="964ae-113">Verificare lo stato utente</span><span class="sxs-lookup"><span data-stu-id="964ae-113">Check the User Status</span></span>](#check-the-user-status)
    -   [<span data-ttu-id="964ae-114">Visualizza la notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-114">Display the Notification</span></span>](#display-the-notification)
    -   [<span data-ttu-id="964ae-115">Rimozione di un'icona</span><span class="sxs-lookup"><span data-stu-id="964ae-115">Removing an Icon</span></span>](#removing-an-icon)
-   [<span data-ttu-id="964ae-116">Esempio SDK</span><span class="sxs-lookup"><span data-stu-id="964ae-116">SDK Sample</span></span>](#sdk-sample)
-   [<span data-ttu-id="964ae-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="964ae-117">Related topics</span></span>](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a><span data-ttu-id="964ae-118">Linee guida per le notifiche e l'area di notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-118">Notification and Notification Area Guidelines</span></span>

<span data-ttu-id="964ae-119">Vedere le sezioni [notifiche](../uxguide/mess-notif.md) e [area di notifica](../uxguide/winenv-notification.md) delle linee guida sull'interazione dell'esperienza utente di Windows per le procedure consigliate per l'uso delle notifiche e dell'area di notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-119">See the [Notifications](../uxguide/mess-notif.md) and [Notification Area](../uxguide/winenv-notification.md) sections of the Windows User Experience Interaction Guidelines for best practices in the use of notifications and the notification area.</span></span> <span data-ttu-id="964ae-120">L'obiettivo è fornire il vantaggio dell'utente tramite l'uso appropriato delle notifiche, senza irritare o distrazione.</span><span class="sxs-lookup"><span data-stu-id="964ae-120">The goal is to provide user benefit through appropriate use of notifications, without being annoying or distracting.</span></span>

<span data-ttu-id="964ae-121">L'area di notifica non è destinata a informazioni critiche che devono essere eseguite immediatamente.</span><span class="sxs-lookup"><span data-stu-id="964ae-121">The notification area is not for critical information that must be acted on immediately.</span></span> <span data-ttu-id="964ae-122">Non è inoltre concepito per l'accesso rapido a programmi o comandi.</span><span class="sxs-lookup"><span data-stu-id="964ae-122">It is also not intended for quick program or command access.</span></span> <span data-ttu-id="964ae-123">A partire da Windows 7, gran parte di queste funzionalità viene eseguita in modo ottimale tramite il pulsante della barra delle applicazioni di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="964ae-123">As of Windows 7, much of that functionality is best accomplished through an application's taskbar button.</span></span>

<span data-ttu-id="964ae-124">Windows 7 consente a un utente di disattivare tutte le notifiche da un'applicazione, se scelgono, in modo da consentirne la progettazione e l'utilizzo in modo che l'utente possa continuare a visualizzarle.</span><span class="sxs-lookup"><span data-stu-id="964ae-124">Windows 7 allows a user to suppress all notifications from an application if they choose, so thoughtful notification design and use will incline the user to allow your application to continue to display them.</span></span> <span data-ttu-id="964ae-125">Le notifiche sono un'interruzione; Assicurarsi che valga la pena.</span><span class="sxs-lookup"><span data-stu-id="964ae-125">Notifications are an interruption; ensure that they are worth it.</span></span>

<span data-ttu-id="964ae-126">In Windows 7 è stato introdotto il concetto di "tempo di inquieto".</span><span class="sxs-lookup"><span data-stu-id="964ae-126">Windows 7 introduces the concept of "quiet time".</span></span> <span data-ttu-id="964ae-127">Il tempo di attesa è definito come prima ora dopo che un nuovo utente accede al proprio account per la prima volta o per la prima volta dopo un aggiornamento del sistema operativo o un'installazione pulita.</span><span class="sxs-lookup"><span data-stu-id="964ae-127">Quiet time is defined as the first hour after a new user logs into his or her account either for the first time or for the first time after an operating system upgrade or clean installation.</span></span> <span data-ttu-id="964ae-128">Questo tempo è accantonato per consentire all'utente di esplorare e acquisire familiarità con il nuovo ambiente senza la distrazione delle notifiche.</span><span class="sxs-lookup"><span data-stu-id="964ae-128">This time is set aside to allow the user to explore and familiarize themselves with the new environment without the distraction of notifications.</span></span> <span data-ttu-id="964ae-129">Durante questo periodo, la maggior parte delle notifiche non deve essere inviata o visualizzata.</span><span class="sxs-lookup"><span data-stu-id="964ae-129">During this time, most notifications should not be sent or shown.</span></span> <span data-ttu-id="964ae-130">Le eccezioni includono il feedback che l'utente si aspetta di vedere in risposta a un'azione dell'utente, ad esempio quando inserisce un dispositivo USB o stampa un documento.</span><span class="sxs-lookup"><span data-stu-id="964ae-130">Exceptions include feedback that the user would expect to see in response to a user action, such as when he or she plugs in a USB device or prints a document.</span></span> <span data-ttu-id="964ae-131">Le specifiche dell'API relative al tempo di indisponibilità sono descritte più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="964ae-131">API specifics of regarding quiet time are discussed later in this topic.</span></span>

## <a name="creating-and-displaying-a-notification"></a><span data-ttu-id="964ae-132">Creazione e visualizzazione di una notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-132">Creating and Displaying a Notification</span></span>

<span data-ttu-id="964ae-133">Le sezioni rimanenti di questo argomento illustrano la procedura di base da seguire per visualizzare una notifica dall'applicazione all'utente.</span><span class="sxs-lookup"><span data-stu-id="964ae-133">The remaining sections in this topic outline the basic procedure to follow to display a notification from your application to the user.</span></span>

1.  [<span data-ttu-id="964ae-134">Aggiungere un'icona di notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-134">Add a Notification Icon</span></span>](#add-a-notification-icon)
2.  [<span data-ttu-id="964ae-135">Definire la versione di NOTIFYICONDATA</span><span class="sxs-lookup"><span data-stu-id="964ae-135">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
3.  [<span data-ttu-id="964ae-136">Definire l'aspetto e il contenuto della notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-136">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
4.  [<span data-ttu-id="964ae-137">Verificare lo stato utente</span><span class="sxs-lookup"><span data-stu-id="964ae-137">Check the User Status</span></span>](#check-the-user-status)
5.  [<span data-ttu-id="964ae-138">Visualizza la notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-138">Display the Notification</span></span>](#display-the-notification)
6.  [<span data-ttu-id="964ae-139">Rimozione di un'icona</span><span class="sxs-lookup"><span data-stu-id="964ae-139">Removing an Icon</span></span>](#removing-an-icon)

### <a name="add-a-notification-icon"></a><span data-ttu-id="964ae-140">Aggiungere un'icona di notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-140">Add a Notification Icon</span></span>

<span data-ttu-id="964ae-141">Per visualizzare una notifica, è necessario disporre di un'icona nell'area di notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-141">To display a notification, you must have an icon in the notification area.</span></span> <span data-ttu-id="964ae-142">In alcuni casi, ad esempio Microsoft Communicator o il livello di batteria, tale icona sarà già presente.</span><span class="sxs-lookup"><span data-stu-id="964ae-142">In certain cases, such as Microsoft Communicator or battery level, that icon will already be present.</span></span> <span data-ttu-id="964ae-143">In molti altri casi, tuttavia, verrà aggiunta un'icona all'area di notifica solo se è necessario per visualizzare la notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-143">In many other cases, however, you will add an icon to the notification area only as long as is needed to show the notification.</span></span> <span data-ttu-id="964ae-144">In entrambi i casi, questa operazione viene eseguita utilizzando la funzione [**\_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) .</span><span class="sxs-lookup"><span data-stu-id="964ae-144">In either case, this is accomplished using the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) function.</span></span> <span data-ttu-id="964ae-145">**Shell \_ di NotifyIcon** consente di aggiungere, modificare o eliminare un'icona nell'area di notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-145">**Shell\_NotifyIcon** allows you to add, modify, or delete an icon in the notification area.</span></span>

![area di notifica contenente tre icone](images/taskbar/notificationareaicons.png)

<span data-ttu-id="964ae-147">Quando un'icona viene aggiunta all'area di notifica in Windows 7, viene aggiunta alla sezione overflow dell'area di notifica per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="964ae-147">When an icon is added to the notification area on Windows 7, it is added to the overflow section of the notification area by default.</span></span> <span data-ttu-id="964ae-148">Quest'area contiene icone dell'area di notifica attive, ma non visibili nell'area di notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-148">This area contains notification area icons that are active, but not visible in the notification area.</span></span> <span data-ttu-id="964ae-149">Solo l'utente può alzare di livello un'icona dall'overflow all'area di notifica, sebbene in determinate circostanze il sistema possa promuovere temporaneamente un'icona nell'area di notifica come anteprima breve (in un minuto).</span><span class="sxs-lookup"><span data-stu-id="964ae-149">Only the user can promote an icon from the overflow to the notification area, although in certain circumstances the system can temporarily promote an icon into the notification area as a short preview (under one minute).</span></span>

> [!Note]  
> <span data-ttu-id="964ae-150">L'utente deve avere la parola finale sulle icone che desidera visualizzare nell'area di notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-150">The user should have the final say on which icons they want to see in their notification area.</span></span> <span data-ttu-id="964ae-151">Prima di installare un'icona non temporanea nell'area di notifica, all'utente viene richiesta l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="964ae-151">Before installing a non-transient icon in the notification area, the user should be asked for permission.</span></span> <span data-ttu-id="964ae-152">È anche necessario specificare l'opzione (normalmente se il menu di scelta rapida) per rimuovere l'icona dall'area di notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-152">They should also be given the option (normally though its shortcut menu) to remove the icon from the notification area.</span></span>

 

<span data-ttu-id="964ae-153">La struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) inviata nella chiamata a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contiene informazioni che specificano sia l'icona dell'area di notifica che la notifica stessa.</span><span class="sxs-lookup"><span data-stu-id="964ae-153">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification itself.</span></span> <span data-ttu-id="964ae-154">Di seguito sono riportati gli elementi specifici dell'icona dell'area di notifica, che possono essere impostati tramite **NOTIFYICONDATA**.</span><span class="sxs-lookup"><span data-stu-id="964ae-154">The following are those items specific to the notification area icon itself that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="964ae-155">Risorsa da cui viene acquisita l'icona.</span><span class="sxs-lookup"><span data-stu-id="964ae-155">The resource from which the icon is taken.</span></span>
-   <span data-ttu-id="964ae-156">Identificatore univoco per l'icona.</span><span class="sxs-lookup"><span data-stu-id="964ae-156">A unique identifier for the icon.</span></span>
-   <span data-ttu-id="964ae-157">Stile della descrizione comando dell'icona.</span><span class="sxs-lookup"><span data-stu-id="964ae-157">The style of the icon's tooltip.</span></span>
-   <span data-ttu-id="964ae-158">Stato dell'icona (nascosto, condiviso o entrambi) nell'area di notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-158">The icon's state (hidden, shared, or both) in the notification area.</span></span>
-   <span data-ttu-id="964ae-159">Handle di una finestra dell'applicazione associata all'icona.</span><span class="sxs-lookup"><span data-stu-id="964ae-159">The handle of an application window associated with the icon.</span></span>
-   <span data-ttu-id="964ae-160">Identificatore del messaggio di callback che consente all'icona di comunicare gli eventi che si verificano all'interno del rettangolo di delimitazione dell'icona e la notifica dell'aerostato con la finestra dell'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="964ae-160">A callback message identifier that allows the icon to communicate events that occur within the icon's bounding rectangle and balloon notification with the associated application window.</span></span> <span data-ttu-id="964ae-161">Il rettangolo di delimitazione dell'icona può essere recuperato tramite la [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).</span><span class="sxs-lookup"><span data-stu-id="964ae-161">The icon's bounding rectangle can be retrieved through [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).</span></span>

<span data-ttu-id="964ae-162">Ogni icona nell'area di notifica può essere identificata in due modi:</span><span class="sxs-lookup"><span data-stu-id="964ae-162">Each icon in the notification area can be identified in two ways:</span></span>

-   <span data-ttu-id="964ae-163">GUID con cui l'icona viene dichiarata nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="964ae-163">The GUID with which the icon is declared in the registry.</span></span> <span data-ttu-id="964ae-164">Questo è il metodo preferito in Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="964ae-164">This is the preferred method on Windows 7 and later.</span></span>
-   <span data-ttu-id="964ae-165">Handle di una finestra associata all'icona dell'area di notifica, oltre a un identificatore di icona definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="964ae-165">The handle of a window associated with the notification area icon, plus an application-defined icon identifier.</span></span> <span data-ttu-id="964ae-166">Questo metodo viene utilizzato in Windows Vista e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="964ae-166">This method is used on Windows Vista and earlier.</span></span>

<span data-ttu-id="964ae-167">Le icone nell'area di notifica possono avere una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="964ae-167">Icons in the notification area can have a tooltip.</span></span> <span data-ttu-id="964ae-168">La descrizione comando può essere una descrizione comando standard (scelta consigliata) o un'interfaccia utente popup disegnata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="964ae-168">The tooltip can be either a standard tooltip (preferred) or an application-drawn, pop-up UI.</span></span> <span data-ttu-id="964ae-169">Sebbene non sia necessario, è consigliabile usare una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="964ae-169">While a tooltip is not required, it is recommended.</span></span>

<span data-ttu-id="964ae-170">Le icone dell'area di notifica devono essere compatibili con i valori DPI alti.</span><span class="sxs-lookup"><span data-stu-id="964ae-170">Notification area icons should be high-DPI aware.</span></span> <span data-ttu-id="964ae-171">Un'applicazione deve fornire sia un'icona di pixel 16x16 che un'icona 32x32 nel file di risorse, quindi usare [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) per assicurarsi che l'icona corretta venga caricata e ridimensionata in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="964ae-171">An application should provide both a 16x16 pixel icon and a 32x32 icon in its resource file, and then use [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) to ensure that the correct icon is loaded and scaled appropriately.</span></span>

<span data-ttu-id="964ae-172">L'applicazione responsabile dell'icona dell'area di notifica deve gestire un clic del mouse per l'icona.</span><span class="sxs-lookup"><span data-stu-id="964ae-172">The application responsible for the notification area icon should handle a mouse click for that icon.</span></span> <span data-ttu-id="964ae-173">Quando un utente fa clic con il pulsante destro del mouse sull'icona, deve visualizzare un menu di scelta rapida normale.</span><span class="sxs-lookup"><span data-stu-id="964ae-173">When a user right-clicks the icon, it should bring up a normal shortcut menu.</span></span> <span data-ttu-id="964ae-174">Tuttavia, il risultato di un solo clic con il pulsante sinistro del mouse può variare in funzione dell'icona.</span><span class="sxs-lookup"><span data-stu-id="964ae-174">However, the result of a single click with the left mouse button will vary with the function of the icon.</span></span> <span data-ttu-id="964ae-175">Dovrebbe visualizzare le informazioni che l'utente dovrebbe visualizzare nel formato più adatto al contenuto, ovvero una finestra popup, una finestra di dialogo o la finestra del programma.</span><span class="sxs-lookup"><span data-stu-id="964ae-175">It should display what the user would expect to see in the form best suited to that content—a popup window, a dialog box or the program window itself.</span></span> <span data-ttu-id="964ae-176">Ad esempio, potrebbe visualizzare il testo di stato per un'icona di stato o un dispositivo di scorrimento per il controllo volume.</span><span class="sxs-lookup"><span data-stu-id="964ae-176">For instance, it could show status text for a status icon, or a slider for the volume control.</span></span>

<span data-ttu-id="964ae-177">La posizione di una finestra popup o di una finestra di dialogo risultante dal clic deve essere posizionata vicino alla coordinata del clic nell'area di notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-177">The placement of a popup window or dialog box that results from the click should be placed near the coordinate of the click in the notification area.</span></span> <span data-ttu-id="964ae-178">Usare [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) per determinarne la posizione.</span><span class="sxs-lookup"><span data-stu-id="964ae-178">Use the [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) to determine its location.</span></span>

<span data-ttu-id="964ae-179">L'icona può essere aggiunta all'area di notifica senza visualizzare una notifica definendo solo i membri specifici dell'icona di [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (sopra illustrata) e chiamando l'oggetto [**\_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="964ae-179">The icon can be added to the notification area without displaying a notification by defining only the icon-specific members of [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (discussed above) and calling [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) as shown here:</span></span>


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



<span data-ttu-id="964ae-180">È anche possibile aggiungere l'icona all'area di notifica e visualizzare una notifica tutti in una sola chiamata all'oggetto [**\_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="964ae-180">You can also add the icon to the notification area and display a notification all in one call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="964ae-181">A tale scopo, continuare con le istruzioni riportate in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="964ae-181">To do so, continue with the instructions in this topic.</span></span>

### <a name="define-the-notifyicondata-version"></a><span data-ttu-id="964ae-182">Definire la versione di NOTIFYICONDATA</span><span class="sxs-lookup"><span data-stu-id="964ae-182">Define the NOTIFYICONDATA Version</span></span>

<span data-ttu-id="964ae-183">Con l'avanzamento di Windows, la struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) è stata espansa in modo da includere più membri per definire più funzionalità.</span><span class="sxs-lookup"><span data-stu-id="964ae-183">As Windows has progressed, the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure has expanded to include more members to define more functionality.</span></span> <span data-ttu-id="964ae-184">Le costanti vengono usate per dichiarare la versione di **NOTIFYICONDATA** da usare con l'icona dell'area di notifica, in modo da consentire la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="964ae-184">Constants are used to declare which version of **NOTIFYICONDATA** to use with your notification area icon, to allow for backward compatibility.</span></span> <span data-ttu-id="964ae-185">A meno che non esista un motivo valido per eseguire altre operazioni, è consigliabile utilizzare la versione di NOTIFYICON \_ versione \_ 4, introdotta in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="964ae-185">Unless there is a compelling reason to do otherwise, it is strongly recommended that you use the NOTIFYICON\_VERSION\_4 version, introduced in Windows Vista.</span></span> <span data-ttu-id="964ae-186">Questa versione fornisce le funzionalità complete disponibili, tra cui la possibilità di identificare l'icona dell'area di notifica anche se un GUID registrato, un meccanismo di callback superiore e un'accessibilità migliore.</span><span class="sxs-lookup"><span data-stu-id="964ae-186">This version provides the full available functionality, including the preferred ability to identify the notification area icon though a registered GUID, a superior callback mechanism, and better accessibility.</span></span>

<span data-ttu-id="964ae-187">Impostare la versione tramite le chiamate seguenti:</span><span class="sxs-lookup"><span data-stu-id="964ae-187">Set the version through the following calls:</span></span>


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



<span data-ttu-id="964ae-188">Si noti che questa chiamata a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) non visualizza una notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-188">Note that this call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) does not display a notification.</span></span>

### <a name="define-the-notification-look-and-contents"></a><span data-ttu-id="964ae-189">Definire l'aspetto e il contenuto della notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-189">Define the Notification Look and Contents</span></span>

<span data-ttu-id="964ae-190">Una notifica è un tipo speciale di controllo ToolTip a fumetti.</span><span class="sxs-lookup"><span data-stu-id="964ae-190">A notification is a special type of balloon tooltip control.</span></span> <span data-ttu-id="964ae-191">Contiene un titolo, un testo del corpo e un'icona.</span><span class="sxs-lookup"><span data-stu-id="964ae-191">It contains a title, body text, and an icon.</span></span> <span data-ttu-id="964ae-192">Analogamente a una finestra, presenta un pulsante **Chiudi** nell'angolo superiore destro.</span><span class="sxs-lookup"><span data-stu-id="964ae-192">Like a window, it has a **Close** button in its upper right corner.</span></span> <span data-ttu-id="964ae-193">Contiene inoltre un pulsante **Opzioni** che consente di aprire l'elemento icone area di notifica nel pannello di controllo, che consente all'utente di visualizzare o nascondere l'icona o di visualizzare solo le notifiche senza un'icona.</span><span class="sxs-lookup"><span data-stu-id="964ae-193">It also contains a **Options** button that opens the Notification Area Icons item in the Control Panel, which allows the user to show or hide the icon or show only notifications without an icon.</span></span>

![screenshot del fumetto di notifica che indica che l'alimentazione della batteria è insufficiente](images/taskbar/notificationballoon.png)

<span data-ttu-id="964ae-195">La struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) inviata nella chiamata a [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contiene informazioni che specificano l'icona dell'area di notifica e il fumetto di notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-195">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification balloon itself.</span></span> <span data-ttu-id="964ae-196">Di seguito sono riportati gli elementi specifici della notifica che possono essere impostati tramite **NOTIFYICONDATA**.</span><span class="sxs-lookup"><span data-stu-id="964ae-196">The following are those items specific to the notification that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="964ae-197">Icona da visualizzare nel fumetto di notifica, specificato dal tipo di notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-197">An icon to display in the notification balloon, which is specified by the notification type.</span></span> <span data-ttu-id="964ae-198">È possibile specificare le dimensioni dell'icona, nonché le icone personalizzate.</span><span class="sxs-lookup"><span data-stu-id="964ae-198">The size of the icon can be specified, as well as custom icons.</span></span>
-   <span data-ttu-id="964ae-199">Titolo della notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-199">A notification title.</span></span> <span data-ttu-id="964ae-200">Questo titolo deve avere una lunghezza massima di 48 caratteri in inglese (per adattarsi alla localizzazione).</span><span class="sxs-lookup"><span data-stu-id="964ae-200">This title should be a maximum of 48 characters long in English (to accommodate localization).</span></span> <span data-ttu-id="964ae-201">Il titolo è la prima riga della notifica e viene impostato con l'uso della dimensione del carattere, del colore e del peso.</span><span class="sxs-lookup"><span data-stu-id="964ae-201">The title is the first line of the notification, and set apart through the use of font size, color, and weight.</span></span>
-   <span data-ttu-id="964ae-202">Testo da utilizzare nel corpo della notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-202">Text for use in the body of the notification.</span></span> <span data-ttu-id="964ae-203">Questo testo deve essere costituito da un massimo di 200 caratteri in inglese (per adattarsi alla localizzazione).</span><span class="sxs-lookup"><span data-stu-id="964ae-203">This text should be a maximum of 200 characters in English (to accommodate localization).</span></span>
-   <span data-ttu-id="964ae-204">Indica se la notifica deve essere eliminata se non può essere visualizzata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="964ae-204">Whether the notification should be discarded if it cannot be displayed immediately.</span></span>
-   <span data-ttu-id="964ae-205">Timeout per la notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-205">A timeout for the notification.</span></span> <span data-ttu-id="964ae-206">Questa impostazione viene ignorata in Windows Vista e nei sistemi successivi a favore di un'impostazione di timeout di accessibilità a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="964ae-206">This setting is ignored in Windows Vista and later systems in favor of a system-wide accessibility timeout setting.</span></span>
-   <span data-ttu-id="964ae-207">Indica se la notifica deve rispettare l'ora non interattiva, impostata tramite il flag di ora di NIIF rispetto al valore di [**\_ \_ quiet \_**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) .</span><span class="sxs-lookup"><span data-stu-id="964ae-207">Whether the notification should respect quiet time, set through the [**NIIF\_RESPECT\_QUIET\_TIME**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) flag.</span></span>

> [!Note]  
> <span data-ttu-id="964ae-208">Le interfacce [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) e [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) sono wrapper Component Object Model (com) per l' [**oggetto \_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="964ae-208">The [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) and [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) interfaces are Component Object Model (COM) wrappers for [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="964ae-209">Al momento, tuttavia, non forniscono la funzionalità NOTIFYICON completa della \_ versione \_ 4 disponibile direttamente tramite l' **oggetto \_ NotifyIcon della shell** , incluso l'utilizzo di un GUID per identificare l'icona dell'area di notifica.</span><span class="sxs-lookup"><span data-stu-id="964ae-209">However, at this time, they do not provide the full NOTIFYICON\_VERSION\_4 functionality available through **Shell\_NotifyIcon** directly, including the use of a GUID to identify the notification area icon.</span></span>

 

### <a name="check-the-user-status"></a><span data-ttu-id="964ae-210">Verificare lo stato utente</span><span class="sxs-lookup"><span data-stu-id="964ae-210">Check the User Status</span></span>

<span data-ttu-id="964ae-211">Il sistema utilizza la funzione [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) per verificare se l'utente si trova in un tempo di attesa, distante dal computer o in uno stato non interrompebile, ad esempio la modalità presentazione.</span><span class="sxs-lookup"><span data-stu-id="964ae-211">The system uses the [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) function is used to check whether the user is in quiet time, away from the computer, or in an uninterruptable state such as Presentation mode.</span></span> <span data-ttu-id="964ae-212">Indica se il sistema Visualizza la notifica dipende da questo stato.</span><span class="sxs-lookup"><span data-stu-id="964ae-212">Whether the system displays your notification depends on this state.</span></span>

> [!Note]  
> <span data-ttu-id="964ae-213">Se l'applicazione usa un metodo di notifica personalizzato che non usa la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)o [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), deve sempre chiamare in modo esplicito [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) per determinare se deve visualizzare l'interfaccia utente di notifica in quel momento.</span><span class="sxs-lookup"><span data-stu-id="964ae-213">If your application is using a custom notification method that does not use [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification), or [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), it should always explicitly call [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) to determine whether it should display notification UI at that time.</span></span>

 

<span data-ttu-id="964ae-214">Le notifiche inviate quando l'utente è distante vengono accodate per la visualizzazione, ma poiché non è possibile sapere quando l'utente restituisce o se la notifica sarà ancora valida in quel momento, è possibile inviare nuovamente la notifica in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="964ae-214">Notifications sent when the user is away are queued for display, but because you cannot know when the user will return or whether the notification will still be valid at that time, you might consider resending the notification later.</span></span>

<span data-ttu-id="964ae-215">Le notifiche inviate durante l'intervallo di tempo silenzioso vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="964ae-215">Notifications sent during quiet time are discarded unshown.</span></span> <span data-ttu-id="964ae-216">Le linee guida di progettazione chiedono che tutte le notifiche siano ignorabili.</span><span class="sxs-lookup"><span data-stu-id="964ae-216">Design guidelines ask that all notifications be ignorable.</span></span> <span data-ttu-id="964ae-217">Non devono richiedere un'azione immediata da un utente.</span><span class="sxs-lookup"><span data-stu-id="964ae-217">They should not require immediate user action.</span></span> <span data-ttu-id="964ae-218">Pertanto, nessuna notifica è così importante che debba eseguire l'override del tempo di attesa.</span><span class="sxs-lookup"><span data-stu-id="964ae-218">Therefore, no notification is so important that it should override quiet time.</span></span>

### <a name="display-the-notification"></a><span data-ttu-id="964ae-219">Visualizza la notifica</span><span class="sxs-lookup"><span data-stu-id="964ae-219">Display the Notification</span></span>

<span data-ttu-id="964ae-220">Dopo aver impostato la versione [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) e definito la notifica in una struttura **NOTIFYICONDATA** , chiamare la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) per visualizzare l'icona.</span><span class="sxs-lookup"><span data-stu-id="964ae-220">Once you have set the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) version and defined the notification in a **NOTIFYICONDATA** structure, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to display the icon.</span></span>

-   <span data-ttu-id="964ae-221">Se l'icona dell'area di notifica non è presente, chiamare la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) per aggiungere l'icona.</span><span class="sxs-lookup"><span data-stu-id="964ae-221">If the notification area icon is not present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to add the icon.</span></span> <span data-ttu-id="964ae-222">Eseguire questa operazione per icone temporanee e non temporanee.</span><span class="sxs-lookup"><span data-stu-id="964ae-222">Do this for both transient and non-transient icons.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   <span data-ttu-id="964ae-223">Se l'icona dell'area di notifica è già presente, chiamare la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) per modificare l'icona.</span><span class="sxs-lookup"><span data-stu-id="964ae-223">If the notification area icon is already present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to modify the icon.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

<span data-ttu-id="964ae-224">Il codice seguente illustra un esempio di impostazione dei dati di [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) e l'invio tramite l'oggetto [**\_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="964ae-224">The following code shows an example of setting [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) data and sending it through [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="964ae-225">Si noti che questo esempio identifica l'icona di notifica tramite un GUID (scelta consigliata in Windows 7).</span><span class="sxs-lookup"><span data-stu-id="964ae-225">Note that this example identifies the notification icon through a GUID (preferred in Windows 7).</span></span>


```
// Declare NOTIFYICONDATA details. 
    // Error handling is omitted here for brevity. Do not omit it in your code.
    
    NOTIFYICONDATA nid = {};
    nid.cbSize = sizeof(nid);
    nid.hWnd = hWnd;
    nid.uFlags = NIF_ICON | NIF_TIP | NIF_GUID;
    
    // Note: This is an example GUID only and should not be used.
    // Normally, you should use a GUID-generating tool to provide the value to
    // assign to guidItem.
    static const GUID myGUID = 
    {0x23977b55, 0x10e0, 0x4041, {0xb8, 0x62, 0xb1, 0x95, 0x41, 0x96, 0x36, 0x69}};
    nid.guidItem = myGUID;
    
    nid.guidItem = guid;
    
    // This text will be shown as the icon's tooltip.
    StringCchCopy(nid.szTip, ARRAYSIZE(nid.szTip), L"Test application");
    
    // Load the icon for high DPI.
    LoadIconMetric(hInst, MAKEINTRESOURCE(IDI_SMALL), LIM_SMALL, &(nid.hIcon));
    
    // Show the notification.
    Shell_NotifyIcon(NIM_ADD, &nid) ? S_OK : E_FAIL;
```



### <a name="removing-an-icon"></a><span data-ttu-id="964ae-226">Rimozione di un'icona</span><span class="sxs-lookup"><span data-stu-id="964ae-226">Removing an Icon</span></span>

<span data-ttu-id="964ae-227">Per rimuovere un'icona (ad esempio, quando è stata aggiunta temporaneamente l'icona per trasmettere una notifica, chiamare la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="964ae-227">To remove an icon—for instance, when you have only added the icon temporarily to broadcast a notification—call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)as shown here.</span></span> <span data-ttu-id="964ae-228">In questa chiamata è necessaria solo una struttura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) minima che identifichi l'icona.</span><span class="sxs-lookup"><span data-stu-id="964ae-228">Only a minimal [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure that identifies the icon is needed in this call.</span></span>


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> <span data-ttu-id="964ae-229">Quando un'applicazione viene disinstallata, l'icona dell'area di notifica può ancora apparire all'utente come opzione nella pagina icone area di notifica nel pannello di controllo per un massimo di sette giorni.</span><span class="sxs-lookup"><span data-stu-id="964ae-229">When an application is uninstalled, its notification area icon can still appear to the user as an option in the Notification Area Icons page in the Control Panel for up to seven days.</span></span> <span data-ttu-id="964ae-230">Tuttavia, le modifiche apportate non avranno alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="964ae-230">However, any changes made there will have no effect.</span></span>

 

## <a name="sdk-sample"></a><span data-ttu-id="964ae-231">Esempio SDK</span><span class="sxs-lookup"><span data-stu-id="964ae-231">SDK Sample</span></span>

<span data-ttu-id="964ae-232">Vedere l'esempio di esempio di [NotificationIcon](samples-notificationicon.md) in Windows Software Development Kit (SDK) per un esempio completo dell'uso di [**\_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="964ae-232">See the [NotificationIcon Sample](samples-notificationicon.md) sample in the Windows Software Development Kit (SDK) for a full example of the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span>

## <a name="related-topics"></a><span data-ttu-id="964ae-233">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="964ae-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="964ae-234">**NotifyIcon della shell \_**</span><span class="sxs-lookup"><span data-stu-id="964ae-234">**Shell\_NotifyIcon**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
</dt> <dt>

[<span data-ttu-id="964ae-235">**\_NotifyIconGetRect Shell**</span><span class="sxs-lookup"><span data-stu-id="964ae-235">**Shell\_NotifyIconGetRect**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)
</dt> <dt>

[<span data-ttu-id="964ae-236">**NOTIFYICONDATA**</span><span class="sxs-lookup"><span data-stu-id="964ae-236">**NOTIFYICONDATA**</span></span>](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)
</dt> <dt>

[<span data-ttu-id="964ae-237">**SHQueryUserNotificationState**</span><span class="sxs-lookup"><span data-stu-id="964ae-237">**SHQueryUserNotificationState**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate)
</dt> <dt>

[<span data-ttu-id="964ae-238">**IUserNotification**</span><span class="sxs-lookup"><span data-stu-id="964ae-238">**IUserNotification**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)
</dt> <dt>

[<span data-ttu-id="964ae-239">**IUserNotification2**</span><span class="sxs-lookup"><span data-stu-id="964ae-239">**IUserNotification2**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)
</dt> <dt>

[<span data-ttu-id="964ae-240">Barra delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="964ae-240">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="964ae-241">Estensioni della barra delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="964ae-241">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
