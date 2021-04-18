---
description: Avvia la comunicazione con un provider di eventi utilizzando un set limitato di query.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Interfaccia IWbemEventSink (Wbemprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemEventSink
api_type:
- COM
api_location:
- Wbemsvc.dll
ms.openlocfilehash: 22a3a15920d26f482cedfa3a596fd439ea70c2f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315994"
---
# <a name="iwbemeventsink-interface"></a><span data-ttu-id="6e988-103">Interfaccia IWbemEventSink</span><span class="sxs-lookup"><span data-stu-id="6e988-103">IWbemEventSink interface</span></span>

<span data-ttu-id="6e988-104">L'interfaccia **IWbemEventSink** avvia la comunicazione con un provider di eventi usando un set di query limitato.</span><span class="sxs-lookup"><span data-stu-id="6e988-104">The **IWbemEventSink** interface initiates communication with an event provider using a restricted set of queries.</span></span> <span data-ttu-id="6e988-105">Questa interfaccia estende [**IWbemObjectSink**](iwbemobjectsink.md), fornendo nuovi metodi di gestione della sicurezza e delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="6e988-105">This interface extends [**IWbemObjectSink**](iwbemobjectsink.md), providing new methods dealing with security and performance.</span></span> <span data-ttu-id="6e988-106">Per ulteriori informazioni sull'utilizzo di questa interfaccia, vedere la pagina relativa alla [scrittura di un provider di eventi](writing-an-event-provider.md) e alla [protezione degli eventi WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="6e988-106">For more information about using this interface, see [Writing an Event Provider](writing-an-event-provider.md) and [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="members"></a><span data-ttu-id="6e988-107">Membri</span><span class="sxs-lookup"><span data-stu-id="6e988-107">Members</span></span>

<span data-ttu-id="6e988-108">L'interfaccia **IWbemEventSink** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6e988-108">The **IWbemEventSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="6e988-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="6e988-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6e988-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="6e988-110">Methods</span></span>

<span data-ttu-id="6e988-111">L'interfaccia **IWbemEventSink** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6e988-111">The **IWbemEventSink** interface has these methods.</span></span>



| <span data-ttu-id="6e988-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="6e988-112">Method</span></span>                                                                | <span data-ttu-id="6e988-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e988-113">Description</span></span>                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="6e988-114">**GetRestrictedSink**</span><span class="sxs-lookup"><span data-stu-id="6e988-114">**GetRestrictedSink**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | <span data-ttu-id="6e988-115">Chiamato dall'utente per configurare le query di eventi con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="6e988-115">Called by the consumer to set up restricted event queries.</span></span><br/> |
| [<span data-ttu-id="6e988-116">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="6e988-116">**IsActive**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | <span data-ttu-id="6e988-117">Controlla lo stato del sink di evento.</span><span class="sxs-lookup"><span data-stu-id="6e988-117">Checks status of event sink.</span></span><br/>                               |
| [<span data-ttu-id="6e988-118">**SetBatchingParameters**</span><span class="sxs-lookup"><span data-stu-id="6e988-118">**SetBatchingParameters**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | <span data-ttu-id="6e988-119">Chiamato dal consumer per impostare i parametri di invio in batch.</span><span class="sxs-lookup"><span data-stu-id="6e988-119">Called by the consumer to set batching parameters.</span></span><br/>         |
| [<span data-ttu-id="6e988-120">**SetSinkSecurity**</span><span class="sxs-lookup"><span data-stu-id="6e988-120">**SetSinkSecurity**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | <span data-ttu-id="6e988-121">Utilizzato per aggiornare il descrittore di sicurezza in un sink di evento.</span><span class="sxs-lookup"><span data-stu-id="6e988-121">Used to update the security descriptor on an event sink.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="6e988-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e988-122">Remarks</span></span>

<span data-ttu-id="6e988-123">Quando si implementa un sink di sottoscrizione di eventi ([**IWbemObjectSink**](iwbemobjectsink.md) o **IWbemEventSink**), non eseguire chiamate in WMI dall'interno dei metodi dell'oggetto sink.</span><span class="sxs-lookup"><span data-stu-id="6e988-123">When implementing an event subscription sink ([**IWbemObjectSink**](iwbemobjectsink.md) or **IWbemEventSink**), do not call into WMI from within the methods on the sink object.</span></span> <span data-ttu-id="6e988-124">Ad esempio, la chiamata di [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) per annullare il sink dall'interno di un'implementazione di [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) può interferire con lo stato WMI.</span><span class="sxs-lookup"><span data-stu-id="6e988-124">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) can interfere with the WMI state.</span></span> <span data-ttu-id="6e988-125">Per annullare una sottoscrizione di eventi, impostare un flag e chiamare **IWbemServices:: CancelAsyncCall** da un altro thread o oggetto.</span><span class="sxs-lookup"><span data-stu-id="6e988-125">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="6e988-126">Per le implementazioni non correlate a un sink di evento, ad esempio il recupero di oggetti, enum e query, è possibile richiamarlo in WMI.</span><span class="sxs-lookup"><span data-stu-id="6e988-126">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="6e988-127">Le implementazioni di sink devono elaborare la notifica degli eventi entro 100 MSEC perché il thread WMI che recapita la notifica degli eventi non può eseguire altre operazioni finché l'oggetto sink non ha completato l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="6e988-127">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="6e988-128">Se la notifica richiede una grande quantità di elaborazione, il sink può utilizzare una coda interna per gestire l'elaborazione da parte di un altro thread.</span><span class="sxs-lookup"><span data-stu-id="6e988-128">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e988-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e988-129">Requirements</span></span>



| <span data-ttu-id="6e988-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e988-130">Requirement</span></span> | <span data-ttu-id="6e988-131">Valore</span><span class="sxs-lookup"><span data-stu-id="6e988-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e988-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e988-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6e988-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e988-133">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="6e988-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e988-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6e988-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e988-135">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="6e988-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e988-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e988-137"><dt>Wbemprov. h (include Wbemidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e988-137"><dt>Wbemprov.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="6e988-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="6e988-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e988-139"><dt>Wbemuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e988-139"><dt>Wbemuuid.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6e988-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6e988-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e988-141"><dt>Wbemsvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e988-141"><dt>Wbemsvc.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="6e988-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e988-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e988-143">API COM per WMI</span><span class="sxs-lookup"><span data-stu-id="6e988-143">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 

 




