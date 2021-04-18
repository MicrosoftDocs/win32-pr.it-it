---
description: Il servizio di notifica eventi di sistema funziona con il sistema di eventi COM+.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Architettura SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32976a716ab0ba5651ce6605fe524d639820696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316627"
---
# <a name="sens-architecture"></a><span data-ttu-id="88669-103">Architettura SENS</span><span class="sxs-lookup"><span data-stu-id="88669-103">SENS Architecture</span></span>

<span data-ttu-id="88669-104">Il servizio di notifica eventi di sistema funziona con il sistema di eventi COM+.</span><span class="sxs-lookup"><span data-stu-id="88669-104">The System Event Notification Service works with the COM+ Event System.</span></span> <span data-ttu-id="88669-105">SENS è un autore di eventi per le classi di eventi monitorati: eventi di rete, di accesso e di alimentazione/batteria.</span><span class="sxs-lookup"><span data-stu-id="88669-105">SENS is an event publisher for the classes of events that it monitors: network, logon, and power/battery events.</span></span> <span data-ttu-id="88669-106">L'applicazione che riceve una notifica viene chiamata Sottoscrittore di eventi.</span><span class="sxs-lookup"><span data-stu-id="88669-106">The application receiving a notification is called an event subscriber.</span></span>

<span data-ttu-id="88669-107">Quando un'applicazione sottoscrive la ricezione di notifiche, può specificare anche i filtri associati agli eventi sottoscritti.</span><span class="sxs-lookup"><span data-stu-id="88669-107">When an application subscribes to receive notifications, it can also specify filters associated with the subscribed events.</span></span> <span data-ttu-id="88669-108">Gli eventi SENS e COM+ utilizzano i filtri per determinare ulteriormente quando l'applicazione deve ricevere notifiche.</span><span class="sxs-lookup"><span data-stu-id="88669-108">SENS and COM+ Events use the filters to further determine when the application should be notified.</span></span>

<span data-ttu-id="88669-109">Le notifiche sono asincrone, quindi l'applicazione che riceve la notifica non deve essere attiva quando viene inviata la notifica.</span><span class="sxs-lookup"><span data-stu-id="88669-109">Notifications are asynchronous, so the application receiving the notification does not have to be active when the notification is sent.</span></span> <span data-ttu-id="88669-110">Quando un'applicazione sottoscrive la ricezione di notifiche, può specificare se deve essere attivata quando si verifica l'evento o se viene inviata una notifica in un secondo momento quando è attiva.</span><span class="sxs-lookup"><span data-stu-id="88669-110">When an application subscribes to receive notifications, it can specify whether it should be activated when the event occurs or notified later when it is active.</span></span>

<span data-ttu-id="88669-111">La sottoscrizione può essere temporanea e valida solo fino a quando l'applicazione non viene arrestata oppure può essere persistente e valida fino a quando l'applicazione non viene rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="88669-111">The subscription can be transient and valid only until the application stops running, or it can be persistent and valid until the application is removed from the system.</span></span>

<span data-ttu-id="88669-112">Un archivio dati degli eventi COM+ contiene informazioni su server Publisher (SENS), sottoscrittori di eventi e filtri.</span><span class="sxs-lookup"><span data-stu-id="88669-112">A COM+ Events data store contains information about the event publisher (SENS), event subscribers, and filters.</span></span> <span data-ttu-id="88669-113">SENS definisce anche un'interfaccia in uscita per ogni classe di evento in una libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="88669-113">SENS also predefines an outgoing interface for each event class in a type library.</span></span>



| <span data-ttu-id="88669-114">classe di evento</span><span class="sxs-lookup"><span data-stu-id="88669-114">Event class</span></span>    | <span data-ttu-id="88669-115">GUID</span><span class="sxs-lookup"><span data-stu-id="88669-115">GUID</span></span>                          | <span data-ttu-id="88669-116">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="88669-116">Interface</span></span>    |
|----------------|-------------------------------|--------------|
| <span data-ttu-id="88669-117">Eventi di rete</span><span class="sxs-lookup"><span data-stu-id="88669-117">Network events</span></span> | <span data-ttu-id="88669-118">\_rete EVENTCLASS \_ SENSGUID</span><span class="sxs-lookup"><span data-stu-id="88669-118">SENSGUID\_EVENTCLASS\_NETWORK</span></span> | <span data-ttu-id="88669-119">ISensNetwork</span><span class="sxs-lookup"><span data-stu-id="88669-119">ISensNetwork</span></span> |
| <span data-ttu-id="88669-120">Eventi di accesso</span><span class="sxs-lookup"><span data-stu-id="88669-120">Logon events</span></span>   | <span data-ttu-id="88669-121">\_accesso EVENTCLASS di SENSGUID \_</span><span class="sxs-lookup"><span data-stu-id="88669-121">SENSGUID\_EVENTCLASS\_LOGON</span></span>   | <span data-ttu-id="88669-122">ISensLogon</span><span class="sxs-lookup"><span data-stu-id="88669-122">ISensLogon</span></span>   |
| <span data-ttu-id="88669-123">Eventi di alimentazione</span><span class="sxs-lookup"><span data-stu-id="88669-123">Power events</span></span>   | <span data-ttu-id="88669-124">SENSGUID \_ EVENTCLASS \_ ONNOW</span><span class="sxs-lookup"><span data-stu-id="88669-124">SENSGUID\_EVENTCLASS\_ONNOW</span></span>   | <span data-ttu-id="88669-125">ISensOnNow</span><span class="sxs-lookup"><span data-stu-id="88669-125">ISensOnNow</span></span>   |



 

<span data-ttu-id="88669-126">Per ricevere notifiche per uno di questi eventi, l'applicazione deve eseguire due operazioni:</span><span class="sxs-lookup"><span data-stu-id="88669-126">To receive notifications for any of these events, your application must do two things:</span></span>

-   <span data-ttu-id="88669-127">Sottoscrivere gli eventi SENS che interessano.</span><span class="sxs-lookup"><span data-stu-id="88669-127">Subscribe to the SENS events that interest you.</span></span> <span data-ttu-id="88669-128">Per sottoscrivere un evento, utilizzare le interfacce **IEventSubscription** e **IEVENTSYSTEM** negli eventi com+.</span><span class="sxs-lookup"><span data-stu-id="88669-128">To subscribe to an event, use the **IEventSubscription** and **IEventSystem** interfaces in COM+ Events.</span></span> <span data-ttu-id="88669-129">È necessario specificare un identificatore per le classi di evento e l'identificatore del server di pubblicazione SENS, SENSGUID \_ Publisher.</span><span class="sxs-lookup"><span data-stu-id="88669-129">You need to supply an identifier for the event classes and the SENS publisher identifier, SENSGUID\_PUBLISHER.</span></span> <span data-ttu-id="88669-130">Le sottoscrizioni sono a livello di ogni evento, quindi l'applicazione di sottoscrizione deve specificare anche gli eventi di interesse della classe.</span><span class="sxs-lookup"><span data-stu-id="88669-130">Subscriptions are on a per event level so the subscribing application must also specify which events within the class are of interest.</span></span> <span data-ttu-id="88669-131">Ogni evento corrisponde a un metodo nell'interfaccia corrispondente alla relativa classe di evento.</span><span class="sxs-lookup"><span data-stu-id="88669-131">Each event corresponds to a method in the interface corresponding to its event class.</span></span>
-   <span data-ttu-id="88669-132">Creare un oggetto sink con un'implementazione per ogni interfaccia gestita.</span><span class="sxs-lookup"><span data-stu-id="88669-132">Create a sink object with an implementation for each interface that you handle.</span></span> <span data-ttu-id="88669-133">Vedere [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)e [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) per ulteriori informazioni su queste interfacce e sugli eventi supportati in ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="88669-133">See [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon), and [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) for more information about these interfaces and the events supported in each one.</span></span>

<span data-ttu-id="88669-134">Quando si verifica uno degli eventi monitorati, SENS elabora ogni sottoscrizione con tutti i filtri associati e invia una notifica ai sottoscrittori tramite il sistema di eventi COM+.</span><span class="sxs-lookup"><span data-stu-id="88669-134">When one of the monitored events occurs, SENS processes each subscription with any associated filters and notifies the subscribers through the COM+ Event system.</span></span>

 

 



