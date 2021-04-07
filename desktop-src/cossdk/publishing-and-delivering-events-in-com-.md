---
description: Per pubblicare un evento, è sufficiente creare un'istanza di un oggetto della classe di evento e richiamare il metodo desiderato; per istruzioni dettagliate su come eseguire questa operazione nel codice, vedere pubblicazione di un evento.
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: Pubblicazione e distribuzione di eventi in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a444b64501156191590c115d6000f4c0bda153
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748855"
---
# <a name="publishing-and-delivering-events-in-com"></a><span data-ttu-id="680aa-103">Pubblicazione e distribuzione di eventi in COM+</span><span class="sxs-lookup"><span data-stu-id="680aa-103">Publishing and Delivering Events in COM+</span></span>

<span data-ttu-id="680aa-104">Per pubblicare un evento, è sufficiente creare un'istanza di un oggetto della [classe di evento](the-com--event-class-object.md) e richiamare il metodo desiderato; per istruzioni dettagliate su come eseguire questa operazione nel codice, vedere [pubblicazione di un evento](publishing-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="680aa-104">To publish an event, simply instantiate an [event class](the-com--event-class-object.md) object and invoke the desired method; for detailed instructions on how to do this in code, see [Publishing an Event](publishing-an-event.md).</span></span>

<span data-ttu-id="680aa-105">Quando un server di pubblicazione genera un evento, il servizio eventi COM+ Cerca nel database di sottoscrizione tutti i Sottoscrittori che hanno registrato sottoscrizioni alla classe di evento di cui è stata creata un'istanza.</span><span class="sxs-lookup"><span data-stu-id="680aa-105">When a publisher fires an event, the COM+ Events service searches the subscription database to find all the subscribers who have registered subscriptions to the instantiated event class.</span></span> <span data-ttu-id="680aa-106">Si connette a tali Sottoscrittori (per creazione diretta, moniker o componenti in coda) e chiama il metodo.</span><span class="sxs-lookup"><span data-stu-id="680aa-106">It connects to those subscribers (by direct creation, monikers, or queued components) and calls the method.</span></span> <span data-ttu-id="680aa-107">Per supportare più di una notifica del Sottoscrittore per un evento, i metodi possono contenere solo parametri in e devono restituire solo valori **HRESULT** di esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="680aa-107">To support more than one subscriber notification for an event, methods can contain only in parameters and must return only success or failure **HRESULT** values.</span></span>

> [!Note]  
> <span data-ttu-id="680aa-108">Questa versione degli eventi COM+ non supporta un archivio eventi distribuito.</span><span class="sxs-lookup"><span data-stu-id="680aa-108">This version of COM+ events does not support a distributed event store.</span></span> <span data-ttu-id="680aa-109">Un Sottoscrittore deve sottoscrivere un evento in ogni computer da cui vuole ricevere una notifica.</span><span class="sxs-lookup"><span data-stu-id="680aa-109">A subscriber must subscribe to an event on each computer from which it wants to receive notification.</span></span> <span data-ttu-id="680aa-110">In alternativa, è possibile registrare l'oggetto della classe di evento e le sottoscrizioni in un computer centrale e creare un'istanza di questo oggetto classe di evento dai computer remoti in cui vengono pubblicati gli eventi.</span><span class="sxs-lookup"><span data-stu-id="680aa-110">As an alternative, you can register the event class object and subscriptions on a central computer and instantiate this event class object from the remote computers on which you publish events.</span></span> <span data-ttu-id="680aa-111">Il recapito degli eventi viene fornito da DCOM o dal servizio componenti accodati COM+.</span><span class="sxs-lookup"><span data-stu-id="680aa-111">Delivery of events is provided either by DCOM or by the COM+ queued components service.</span></span> <span data-ttu-id="680aa-112">Per ulteriori informazioni sull'utilizzo del servizio componenti in coda COM+, vedere [utilizzo di eventi com+ con componenti accodati com+](using-com--events-with-com--queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="680aa-112">For more information about using the COM+ queued components service, see [Using COM+ Events with COM+ Queued Components](using-com--events-with-com--queued-components.md).</span></span>

 

<span data-ttu-id="680aa-113">Per impostazione predefinita, il servizio eventi COM+ genera gli eventi uno alla volta, in base a un ordine non determinato o ripetibile.</span><span class="sxs-lookup"><span data-stu-id="680aa-113">By default, the COM+ events service fires events one at a time, in no determined or repeatable order.</span></span> <span data-ttu-id="680aa-114">Gli editori che devono controllare l'ordine in cui i sottoscrittori ricevono un evento possono implementare un filtro di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="680aa-114">Publishers that need to control the order in which subscribers receive an event can implement a publisher filter.</span></span> <span data-ttu-id="680aa-115">Per ulteriori informazioni, vedere [filtro di eventi in com+](filtering-events-in-com-.md).</span><span class="sxs-lookup"><span data-stu-id="680aa-115">(For more information, see [Filtering Events in COM+](filtering-events-in-com-.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="680aa-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="680aa-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="680aa-117">Filtro di eventi in COM+</span><span class="sxs-lookup"><span data-stu-id="680aa-117">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="680aa-118">Sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="680aa-118">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="680aa-119">Oggetto della classe di evento COM+</span><span class="sxs-lookup"><span data-stu-id="680aa-119">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="680aa-120">Uso di eventi COM+ con componenti in coda COM+</span><span class="sxs-lookup"><span data-stu-id="680aa-120">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



