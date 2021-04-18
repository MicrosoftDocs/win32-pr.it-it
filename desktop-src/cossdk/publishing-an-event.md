---
description: Pubblicazione di un evento
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Pubblicazione di un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304938"
---
# <a name="publishing-an-event"></a><span data-ttu-id="eae65-103">Pubblicazione di un evento</span><span class="sxs-lookup"><span data-stu-id="eae65-103">Publishing an Event</span></span>

<span data-ttu-id="eae65-104">Per pubblicare un evento, è sufficiente creare un'istanza di un oggetto evento chiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o il metodo **CreateObject** di Microsoft Visual Basic usando EventClassID o EventClassName come argomento.</span><span class="sxs-lookup"><span data-stu-id="eae65-104">To publish an event, just instantiate an event object by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or the Microsoft Visual Basic **CreateObject** method using EventClassID or EventClassName as an argument.</span></span> <span data-ttu-id="eae65-105">Il server di pubblicazione chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto evento per ottenere le interfacce supportate dall'oggetto della classe di evento e richiama un metodo sull'oggetto evento tramite l'interfaccia per pubblicare l'evento.</span><span class="sxs-lookup"><span data-stu-id="eae65-105">The publisher calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the event object to obtain the interfaces supported by the event class object and invokes a method on the event object through the interface to publish the event.</span></span> <span data-ttu-id="eae65-106">Il sistema di eventi pubblica quindi gli eventi nella classe di evento CLSID \_ EventObjectChange con l'ID di interfaccia IID \_ IEventObjectChange.</span><span class="sxs-lookup"><span data-stu-id="eae65-106">The event system then publishes events on the event class CLSID\_EventObjectChange with the interface ID IID\_IEventObjectChange.</span></span>

<span data-ttu-id="eae65-107">Per supportare il recapito di eventi a più sottoscrittori, i metodi della classe di evento devono contenere solo parametri in.</span><span class="sxs-lookup"><span data-stu-id="eae65-107">To support delivery of events to multiple subscribers, event class methods should contain only in parameters.</span></span>

<span data-ttu-id="eae65-108">Utilizzando la proprietà FireInParallel dell'oggetto [classe di evento](the-com--event-class-object.md) , i publisher possono richiedere che il sistema di eventi utilizzi più thread per recapitare un evento a più Sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="eae65-108">By using the FireInParallel property of the [event class](the-com--event-class-object.md) object, publishers can request that the event system use multiple threads to deliver an event to more than one subscriber.</span></span> <span data-ttu-id="eae65-109">La selezione di un meccanismo di recapito in parallelo non garantisce il recapito simultaneo dell'evento a più sottoscrittori, ma indica al servizio eventi COM+ di consentire questo problema.</span><span class="sxs-lookup"><span data-stu-id="eae65-109">Selecting an in-parallel delivery mechanism does not guarantee simultaneous delivery of the event to multiple subscribers, but it instructs the COM+ events service to permit this to happen.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eae65-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eae65-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eae65-111">Pubblicazione e distribuzione di eventi in COM+</span><span class="sxs-lookup"><span data-stu-id="eae65-111">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
