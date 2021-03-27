---
description: Questa Guida introduttiva illustra come generare una notifica di tipo avviso popup da un'applicazione desktop.
title: Invio di una notifica di tipo avviso popup dal desktop
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 36f9da25c20d99da74be30046fc5f9f4789dfd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882793"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a><span data-ttu-id="aa4a5-103">Guida introduttiva: invio di una notifica di tipo avviso popup dal desktop</span><span class="sxs-lookup"><span data-stu-id="aa4a5-103">Quickstart: Sending a toast notification from the desktop</span></span>

<span data-ttu-id="aa4a5-104">Questa Guida introduttiva illustra come generare una notifica di tipo avviso popup da un'applicazione desktop.</span><span class="sxs-lookup"><span data-stu-id="aa4a5-104">This quickstart shows how to raise a toast notification from a desktop app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="aa4a5-105">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="aa4a5-105">Prerequisites</span></span>

-   <span data-ttu-id="aa4a5-106">Librerie</span><span class="sxs-lookup"><span data-stu-id="aa4a5-106">Libraries</span></span>
    -   <span data-ttu-id="aa4a5-107">C++: Runtime. Object. lib</span><span class="sxs-lookup"><span data-stu-id="aa4a5-107">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="aa4a5-108">C \# : Windows. winmd</span><span class="sxs-lookup"><span data-stu-id="aa4a5-108">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="aa4a5-109">Un collegamento all'app, con [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), deve essere installato nella schermata Start.</span><span class="sxs-lookup"><span data-stu-id="aa4a5-109">A shortcut to your app, with a [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), must be installed to the Start screen.</span></span> <span data-ttu-id="aa4a5-110">Si noti, tuttavia, che non è necessario che venga aggiunto alla schermata Start.</span><span class="sxs-lookup"><span data-stu-id="aa4a5-110">Note, however, that it does not need to be pinned to the Start screen.</span></span> <span data-ttu-id="aa4a5-111">Per ulteriori informazioni, vedere [come abilitare le notifiche di tipo avviso popup sul desktop tramite un AppUserModelID](enable-desktop-toast-with-appusermodelid.md).</span><span class="sxs-lookup"><span data-stu-id="aa4a5-111">For more information, see [How to enable desktop toast notifications through an AppUserModelID](enable-desktop-toast-with-appusermodelid.md).</span></span>
-   <span data-ttu-id="aa4a5-112">Una versione di Microsoft Visual Studio che supporta almeno Windows 8</span><span class="sxs-lookup"><span data-stu-id="aa4a5-112">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="aa4a5-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="aa4a5-113">Instructions</span></span>

### <a name="1-create-your-toast-content"></a><span data-ttu-id="aa4a5-114">1. creare il contenuto del popup</span><span class="sxs-lookup"><span data-stu-id="aa4a5-114">1. Create your toast content</span></span>

> [!Note]  
> <span data-ttu-id="aa4a5-115">Quando si specifica un modello di avviso popup che include un'immagine, tenere presente che le app desktop possono usare solo le immagini locali; le immagini Web non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="aa4a5-115">When you specify a toast template that includes an image, be aware that desktop apps can use only local images; web images are not supported.</span></span> <span data-ttu-id="aa4a5-116">Inoltre, il percorso del file di immagine locale deve essere specificato come percorso assoluto (non relativo).</span><span class="sxs-lookup"><span data-stu-id="aa4a5-116">Also, the path to the local image file must be provided as an absolute (not relative) path.</span></span>

 


```csharp
// Get a toast XML template
XmlDocument toastXml = ToastNotificationManager.GetTemplateContent(ToastTemplateType.ToastImageAndText04);

// Fill in the text elements
XmlNodeList stringElements = toastXml.GetElementsByTagName("text");
for (int i = 0; i < stringElements.Length; i++)
{
    stringElements[i].AppendChild(toastXml.CreateTextNode("Line " + i));
}

// Specify the absolute path to an image
String imagePath = "file:///" + Path.GetFullPath("toastImageAndText.png");
XmlNodeList imageElements = toastXml.GetElementsByTagName("image");

ToastNotification toast = new ToastNotification(toastXml);
```



### <a name="2-create-and-attach-the-event-handlers"></a><span data-ttu-id="aa4a5-117">2. creare e alleghi i gestori eventi</span><span class="sxs-lookup"><span data-stu-id="aa4a5-117">2. Create and attach the event handlers</span></span>

<span data-ttu-id="aa4a5-118">Registrare i gestori per gli eventi di tipo avviso popup: activated, unmissed e failed.</span><span class="sxs-lookup"><span data-stu-id="aa4a5-118">Register handlers for the toast events: Activated, Dismissed, and Failed.</span></span> <span data-ttu-id="aa4a5-119">Un'applicazione desktop deve almeno sottoscrivere l'evento attivato, in modo che possa gestire l'attivazione prevista dell'app dal popup quando viene selezionata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="aa4a5-119">A desktop app must at least subscribe to the Activated event so that it can handle the expected activation of the app from the toast when the user selects it.</span></span>


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a><span data-ttu-id="aa4a5-120">3. inviare il popup</span><span class="sxs-lookup"><span data-stu-id="aa4a5-120">3. Send the toast</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa4a5-121">È necessario includere il [AppUserModelID](../properties/props-system-appusermodel-id.md) del collegamento dell'app nella schermata Start ogni volta che si chiama [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041).</span><span class="sxs-lookup"><span data-stu-id="aa4a5-121">You must include the [AppUserModelID](../properties/props-system-appusermodel-id.md) of your app's shortcut on the Start screen each time that you call [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041).</span></span> <span data-ttu-id="aa4a5-122">Se non si riesce a eseguire questa operazione, il popup non verrà visualizzato.</span><span class="sxs-lookup"><span data-stu-id="aa4a5-122">If you fail to do this, your toast will not be displayed.</span></span>

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a><span data-ttu-id="aa4a5-123">4. gestire i callback</span><span class="sxs-lookup"><span data-stu-id="aa4a5-123">4. Handle the callbacks</span></span>

<span data-ttu-id="aa4a5-124">Portare la finestra dell'app in primo piano se riceve un callback "attivato" dalla notifica di tipo avviso popup.</span><span class="sxs-lookup"><span data-stu-id="aa4a5-124">Bring your app's window to the foreground if it receives an "activated" callback from the toast notification.</span></span> <span data-ttu-id="aa4a5-125">Quando un utente seleziona un avviso popup, si prevede che l'app verrà avviata a una visualizzazione relativa al contenuto del popup.</span><span class="sxs-lookup"><span data-stu-id="aa4a5-125">When a user selects a toast, the expectation is that the app will be launched to a view related to the content of that toast..</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa4a5-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa4a5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa4a5-127">Esempio di invio notifiche di tipo avviso popup da app desktop</span><span class="sxs-lookup"><span data-stu-id="aa4a5-127">Sending toast notifications from desktop apps sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[<span data-ttu-id="aa4a5-128">Come abilitare le notifiche di tipo avviso popup sul desktop tramite un AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="aa4a5-128">How to enable desktop toast notifications through an AppUserModelID</span></span>](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[<span data-ttu-id="aa4a5-129">XML Schema popup</span><span class="sxs-lookup"><span data-stu-id="aa4a5-129">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="aa4a5-130">[Panoramica delle notifiche di tipo avviso popup](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="aa4a5-130">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="aa4a5-131">[Guida introduttiva: invio di una notifica di tipo avviso popup](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="aa4a5-131">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="aa4a5-132">[Guida introduttiva: invio di notifiche push di tipo avviso popup](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="aa4a5-132">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="aa4a5-133">Linee guida ed elenco di controllo per notifiche di tipo avviso popup</span><span class="sxs-lookup"><span data-stu-id="aa4a5-133">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

<span data-ttu-id="aa4a5-134">[Come scegliere e usare un modello di avviso popup](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="aa4a5-134">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="aa4a5-135">[Come gestire l'attivazione da una notifica di tipo avviso popup](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="aa4a5-135">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="aa4a5-136">[Come acconsentire esplicitamente per le notifiche di tipo avviso popup](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="aa4a5-136">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="aa4a5-137">[Scelta di un modello di avviso popup](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="aa4a5-137">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="aa4a5-138">[Opzioni audio popup](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="aa4a5-138">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 
