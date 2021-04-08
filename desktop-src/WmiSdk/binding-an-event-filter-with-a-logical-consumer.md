---
description: Dopo aver creato il consumer di eventi logici e il filtro eventi, è necessario collegarli, che registra il consumer logico per la ricezione di notifiche sugli eventi specificati dal filtro.
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: Associazione di un filtro eventi a un consumer logico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884433"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a><span data-ttu-id="14e22-103">Associazione di un filtro eventi a un consumer logico</span><span class="sxs-lookup"><span data-stu-id="14e22-103">Binding an Event Filter with a Logical Consumer</span></span>

<span data-ttu-id="14e22-104">Dopo aver creato il consumer di eventi logici e il filtro eventi, è necessario collegarli, che registra il consumer logico per la ricezione di notifiche sugli eventi specificati dal filtro.</span><span class="sxs-lookup"><span data-stu-id="14e22-104">After you create the logical event consumer and the event filter you must link them, which registers the logical consumer to receive notification about the events specified by the filter.</span></span>

<span data-ttu-id="14e22-105">Nella procedura seguente viene descritto come associare un filtro eventi a un consumer logico.</span><span class="sxs-lookup"><span data-stu-id="14e22-105">The following procedure describes how to bind an event filter with a logical consumer.</span></span>

<span data-ttu-id="14e22-106">**Per associare un filtro eventi a un consumer logico**</span><span class="sxs-lookup"><span data-stu-id="14e22-106">**To bind an event filter with a logical consumer**</span></span>

1.  <span data-ttu-id="14e22-107">Creare un'istanza della classe di sistema [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="14e22-107">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) system class in the WMI repository.</span></span>

    <span data-ttu-id="14e22-108">La classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) è una classe di associazione che collega l'istanza del filtro eventi e l'istanza del consumer logico tramite le proprietà di riferimento del **filtro** e del **consumer** .</span><span class="sxs-lookup"><span data-stu-id="14e22-108">The [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class is an association class that links the event filter instance and the logical consumer instance together through the **Filter** and **Consumer** reference properties.</span></span> <span data-ttu-id="14e22-109">Per ulteriori informazioni, vedere [dichiarazione di una classe di associazione](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="14e22-109">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

2.  <span data-ttu-id="14e22-110">Impostare la proprietà **Filter** sull'istanza del filtro.</span><span class="sxs-lookup"><span data-stu-id="14e22-110">Set the **Filter** property to the instance of your filter.</span></span>
3.  <span data-ttu-id="14e22-111">Impostare la proprietà **consumer** sull'istanza del consumer logico.</span><span class="sxs-lookup"><span data-stu-id="14e22-111">Set the **Consumer** property to the instance of your logical consumer.</span></span>
4.  <span data-ttu-id="14e22-112">Impostare la proprietà **DeliverSynchronously** per determinare il tipo di recapito desiderato.</span><span class="sxs-lookup"><span data-stu-id="14e22-112">Set the **DeliverSynchronously** property to determine the type of delivery you want.</span></span>

    <span data-ttu-id="14e22-113">La proprietà **DeliverSynchronously** determina quando WMI recapita le notifiche degli eventi in modo sincrono o asincrono.</span><span class="sxs-lookup"><span data-stu-id="14e22-113">The **DeliverSynchronously** property determines when WMI delivers event notifications synchronously or asynchronously.</span></span> <span data-ttu-id="14e22-114">Se si imposta questa proprietà su **true** , viene richiesto un recapito sincrono.</span><span class="sxs-lookup"><span data-stu-id="14e22-114">Setting this property to **TRUE** requests a synchronous delivery.</span></span> <span data-ttu-id="14e22-115">Usare il recapito sincrono solo quando l'utente permanente può elaborare gli eventi entro circa 100 microsecondi.</span><span class="sxs-lookup"><span data-stu-id="14e22-115">Use synchronous delivery only when the permanent consumer can process events within approximately 100 microseconds.</span></span>

    > [!Note]  
    > <span data-ttu-id="14e22-116">Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="14e22-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="14e22-117">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="14e22-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

     

5.  <span data-ttu-id="14e22-118">Quando si annulla la registrazione del consumer di eventi logici, assicurarsi di eliminare l'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="14e22-118">When unregistering your logical event consumer, ensure you delete the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance.</span></span>

    <span data-ttu-id="14e22-119">Ogni istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) rappresenta una registrazione per una specifica notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="14e22-119">Each [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance represents a registration for a specific event notification.</span></span> <span data-ttu-id="14e22-120">Quando si elimina un'associazione, WMI disattiva la registrazione.</span><span class="sxs-lookup"><span data-stu-id="14e22-120">When you delete a binding, WMI deactivates the registration.</span></span> <span data-ttu-id="14e22-121">Potrebbe essere necessario eliminare le istanze del consumer logico e del filtro eventi per disattivare la registrazione, a seconda dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="14e22-121">You might have to delete the logical consumer and event filter instances to deactivate registration, depending on the implementation.</span></span>

<span data-ttu-id="14e22-122">Nell'esempio di codice seguente viene illustrata un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) che associa un'istanza di una classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) a un filtro eventi specifico (l'istanza del consumer di eventi è stata creata nell'argomento [creazione di un consumer logico](creating-a-logical-consumer.md) e il filtro eventi è stato creato nell'argomento [creazione di un filtro eventi](creating-an-event-filter.md) ).</span><span class="sxs-lookup"><span data-stu-id="14e22-122">The following code example shows you a [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance that associates an instance of an [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class with a specific event filter (the instance of the event consumer was created in the [Creating a Logical Consumer](creating-a-logical-consumer.md) topic, and the event filter was created in the [Creating an Event Filter](creating-an-event-filter.md) topic).</span></span>

``` syntax
instance of __FilterToConsumerBinding
{
    Filter = $FILTER;
    Consumer = $CONSUMER;
    DeliverSynchronously=FALSE;

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="14e22-123">Due consumer, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) e [**CommandLineEventConsumer**](commandlineeventconsumer.md), non funzioneranno a meno che l'autore non sia un membro del gruppo Administrators locale.</span><span class="sxs-lookup"><span data-stu-id="14e22-123">Two consumers, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) and [**CommandLineEventConsumer**](commandlineeventconsumer.md), will not work unless their creator is a member of the local Administrators group.</span></span>

<span data-ttu-id="14e22-124">**:** Quando un amministratore crea una sottoscrizione, il SID non viene utilizzato per la proprietà **CreatorSID** , ma viene utilizzato il SID del gruppo Administrators locale.</span><span class="sxs-lookup"><span data-stu-id="14e22-124">**:** When an administrator creates a subscription, his SID is not used for the **CreatorSID** property, but the SID of the local Administrators group is used instead.</span></span> <span data-ttu-id="14e22-125">Pertanto, le istanze possono essere create da amministratori diversi e la sottoscrizione continuerà a funzionare.</span><span class="sxs-lookup"><span data-stu-id="14e22-125">Therefore, instances can be created by different administrators and the subscription will still work.</span></span> <span data-ttu-id="14e22-126">Per altre informazioni, vedere [ricezione di eventi](receiving-events-securely.md)in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="14e22-126">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="14e22-127">Quando un filtro è associato a un consumer logico, l'evento viene registrato da [Event Tracing](/windows/desktop/ETW/event-tracing-portal) for Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="14e22-127">When a filter is bound to a logical consumer the event is recorded by [Event Tracing](/windows/desktop/ETW/event-tracing-portal) for Windows (ETW).</span></span> <span data-ttu-id="14e22-128">Per ulteriori informazioni, vedere [traccia dell'attività WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="14e22-128">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14e22-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14e22-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14e22-130">Ricezione di eventi in qualsiasi momento</span><span class="sxs-lookup"><span data-stu-id="14e22-130">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 
