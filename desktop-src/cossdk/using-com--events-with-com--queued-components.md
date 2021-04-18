---
description: Il servizio eventi COM+ viene utilizzato per gestire il recapito di eventi dai publisher ai sottoscrittori.
ms.assetid: 0945163b-1276-47f6-ae7f-9d932a1b586d
title: Uso di eventi COM+ con componenti in coda COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be31dd1088b720902295738c23173c28145cef2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305204"
---
# <a name="using-com-events-with-com-queued-components"></a><span data-ttu-id="f028e-103">Uso di eventi COM+ con componenti in coda COM+</span><span class="sxs-lookup"><span data-stu-id="f028e-103">Using COM+ Events with COM+ Queued Components</span></span>

<span data-ttu-id="f028e-104">Il servizio eventi COM+ viene utilizzato per gestire il recapito di eventi dai publisher ai sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="f028e-104">The COM+ events service is used to manage the delivery of events from publishers to subscribers.</span></span> <span data-ttu-id="f028e-105">Il servizio COM+ Queued Components può essere utilizzato per rendere indipendente il tempo di elaborazione del server di pubblicazione e del Sottoscrittore tramite l'accodamento del messaggio del server di pubblicazione e successivamente la riproduzione al Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="f028e-105">The COM+ queued components service can be used to make the publisher and subscriber processing time independent by queuing the publisher's message and later replaying it to the subscriber.</span></span> <span data-ttu-id="f028e-106">Indipendentemente dal fatto che sia necessario utilizzare il servizio componenti in coda dipende dalla logica di business sottostante dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f028e-106">Whether or not you need to use the queued components service depends on the underlying business logic of your application.</span></span> <span data-ttu-id="f028e-107">Se è necessario disporre di eventi indipendenti dal tempo, è possibile crearli utilizzando il servizio eventi COM+ con il servizio componenti accodati COM+.</span><span class="sxs-lookup"><span data-stu-id="f028e-107">If you need to have events that are time independent, you can create them by using the COM+ events service with COM+ queued components service.</span></span>

> [!Note]  
> <span data-ttu-id="f028e-108">Per ulteriori informazioni sull'utilizzo del servizio componenti in coda COM+, vedere [componenti in coda com+](com--queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="f028e-108">For additional information about using the COM+ queued components service, see [COM+ Queued Components](com--queued-components.md).</span></span>

 

<span data-ttu-id="f028e-109">Il servizio componenti in coda mantiene la chiamata di ordine di metodo all'interno di un singolo messaggio.</span><span class="sxs-lookup"><span data-stu-id="f028e-109">The queued components service maintains order-of-method invocation within a single message.</span></span> <span data-ttu-id="f028e-110">Il registratore esegue il batch di tutte le chiamate al metodo in un messaggio, quindi il lettore richiama tali metodi in ordine quando il messaggio viene elaborato.</span><span class="sxs-lookup"><span data-stu-id="f028e-110">The recorder batches all method invocations into a message, and then the player invokes those methods in order when the message is processed.</span></span>

<span data-ttu-id="f028e-111">Un registratore e un lettore di componenti in coda possono essere posizionati in una delle due posizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f028e-111">A queued components recorder and player can be positioned in either of the following two places:</span></span>

-   <span data-ttu-id="f028e-112">Tra il server di pubblicazione e l'oggetto evento</span><span class="sxs-lookup"><span data-stu-id="f028e-112">Between the publisher and event object</span></span>
-   <span data-ttu-id="f028e-113">Tra l'oggetto evento e il Sottoscrittore</span><span class="sxs-lookup"><span data-stu-id="f028e-113">Between the event object and subscriber</span></span>

<span data-ttu-id="f028e-114">Se si posizionano il registratore e il lettore tra il server di pubblicazione e l'oggetto evento, si sta rendendo il componente della [classe di evento](the-com--event-class-object.md) accodabile.</span><span class="sxs-lookup"><span data-stu-id="f028e-114">If you position the recorder and player between the publisher and event object, you are making the [event class](the-com--event-class-object.md) component queuable.</span></span> <span data-ttu-id="f028e-115">Il componente della classe di evento deve essere contrassegnato per l'accodamento e deve essere attivato dal lettore in un processo separato dal server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="f028e-115">The event class component must be marked for queuing and be activated by the player in a process that is separate from the publisher.</span></span>

<span data-ttu-id="f028e-116">Per recapitare gli eventi in modo asincrono, comporre il registratore e il lettore tra l'oggetto evento e il Sottoscrittore e impostare l'attributo in coda dell'oggetto sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f028e-116">To deliver events asynchronously, compose the recorder and player between the event object and subscriber and set the Queued attribute of the subscription object.</span></span> <span data-ttu-id="f028e-117">Imposta SubscriberMoniker come segue: "queue:/New:/ {12345678-1234-1234-1234-123456789012} ".</span><span class="sxs-lookup"><span data-stu-id="f028e-117">This sets SubscriberMoniker as follows: "queue:/new:/{12345678-1234-1234-1234-123456789012}".</span></span>

<span data-ttu-id="f028e-118">Quando si utilizzano i componenti in coda in una situazione di evento, è necessario considerare l'ordine di implicazioni del recapito.</span><span class="sxs-lookup"><span data-stu-id="f028e-118">There is an order of delivery implication to consider when using queued components in an event situation.</span></span> <span data-ttu-id="f028e-119">Poiché il servizio componenti in coda registra e riproduce tutte le chiamate entro la durata di un singolo oggetto in un unico messaggio, tutte le chiamate vengono riprodotte nell'ordine in cui sono state effettuate.</span><span class="sxs-lookup"><span data-stu-id="f028e-119">Because the queued components service records and plays back all calls within the lifetime of a single object in one message, all calls are replayed in the order in which they were made.</span></span> <span data-ttu-id="f028e-120">Tuttavia, se è presente più di una sessione con più di un oggetto, l'ordine non può essere garantito.</span><span class="sxs-lookup"><span data-stu-id="f028e-120">However, if there is more than one session with more than one object, order cannot be guaranteed.</span></span> <span data-ttu-id="f028e-121">Se l'ordine è importante, assicurarsi che le chiamate che devono essere riprodotte nell'ordine si trovino nella stessa istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f028e-121">If order is important, make sure that calls that need to be played back in order reside on the same object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f028e-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f028e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f028e-123">Filtro di eventi in COM+</span><span class="sxs-lookup"><span data-stu-id="f028e-123">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="f028e-124">Pubblicazione e distribuzione di eventi in COM+</span><span class="sxs-lookup"><span data-stu-id="f028e-124">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="f028e-125">Sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="f028e-125">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="f028e-126">Oggetto della classe di evento COM+</span><span class="sxs-lookup"><span data-stu-id="f028e-126">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



