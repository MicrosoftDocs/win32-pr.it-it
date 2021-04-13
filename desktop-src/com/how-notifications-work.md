---
title: Come funzionano le notifiche
description: Come funzionano le notifiche
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9665b327d164a4e105f8adba3328be284fbe1fa0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399788"
---
# <a name="how-notifications-work"></a><span data-ttu-id="e8988-103">Come funzionano le notifiche</span><span class="sxs-lookup"><span data-stu-id="e8988-103">How Notifications Work</span></span>

<span data-ttu-id="e8988-104">Le notifiche hanno origine nell'applicazione oggetto e vengono propagate al contenitore tramite il gestore dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e8988-104">Notifications originate in the object application and flow to the container by way of the object handler.</span></span> <span data-ttu-id="e8988-105">Se l'oggetto è un oggetto collegato, l'oggetto collegato intercetta le notifiche dal gestore dell'oggetto e notifica direttamente il contenitore.</span><span class="sxs-lookup"><span data-stu-id="e8988-105">If the object is a linked object, the linked object intercepts the notifications from the object handler and notifies the container directly.</span></span>

<span data-ttu-id="e8988-106">Un'applicazione oggetto deve gestire le richieste di registrazione, tenendo traccia del punto in cui inviare le notifiche e inviare tali notifiche quando appropriato.</span><span class="sxs-lookup"><span data-stu-id="e8988-106">An object application must manage registration requests, keeping track of where to send which notifications and sending those notifications when appropriate.</span></span> <span data-ttu-id="e8988-107">OLE fornisce due oggetti componente per semplificare questa attività: OleAdviseHolder per le notifiche di documenti compositi e DataAdviseHolder per le notifiche dati.</span><span class="sxs-lookup"><span data-stu-id="e8988-107">OLE provides two component objects to simplify this task: the OleAdviseHolder for compound document notifications and the DataAdviseHolder for data notifications.</span></span>

<span data-ttu-id="e8988-108">Le applicazioni oggetto determinano le condizioni che richiedono l'invio di ogni notifica specifica e la frequenza con cui ogni notifica deve essere inviata.</span><span class="sxs-lookup"><span data-stu-id="e8988-108">Object applications determine the conditions that prompt the sending of each specific notification and the frequency with which each notification should be sent.</span></span> <span data-ttu-id="e8988-109">Quando è appropriato per l'invio di più notifiche, non è importante quale notifica venga inviata per prima; possono essere inviati in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="e8988-109">When it is appropriate for multiple notifications to be sent, it does not matter which notification is sent first; they can be sent in any order.</span></span>

<span data-ttu-id="e8988-110">La tempistica delle notifiche influiscono sulle prestazioni e sul coordinamento tra un'applicazione oggetto e i relativi contenitori.</span><span class="sxs-lookup"><span data-stu-id="e8988-110">The timing of notifications affects the performance and coordination between an object application and its containers.</span></span> <span data-ttu-id="e8988-111">Mentre le notifiche hanno inviato troppo spesso un'elaborazione lenta, le notifiche inviate con una frequenza eccessiva di un contenitore non sincronizzato.</span><span class="sxs-lookup"><span data-stu-id="e8988-111">Whereas notifications sent too frequently slow processing, notifications sent too infrequently result in an out-of-sync container.</span></span> <span data-ttu-id="e8988-112">La frequenza di notifica può essere confrontata con la velocità di ridisegno di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e8988-112">Notification frequency can be compared with the rate at which an application repaints.</span></span> <span data-ttu-id="e8988-113">Pertanto, l'utilizzo di una logica simile per la tempistica delle notifiche (come viene utilizzato per il ridisegno) è consigliabile.</span><span class="sxs-lookup"><span data-stu-id="e8988-113">Therefore, using similar logic for the timing of notifications (as is used for repainting) is wise.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8988-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e8988-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8988-115">**CreateDataAdviseHolder**</span><span class="sxs-lookup"><span data-stu-id="e8988-115">**CreateDataAdviseHolder**</span></span>](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[<span data-ttu-id="e8988-116">**CreateOleAdviseHolder**</span><span class="sxs-lookup"><span data-stu-id="e8988-116">**CreateOleAdviseHolder**</span></span>](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[<span data-ttu-id="e8988-117">Notifications</span><span class="sxs-lookup"><span data-stu-id="e8988-117">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 