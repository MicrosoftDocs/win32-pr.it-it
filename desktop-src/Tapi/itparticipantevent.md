---
description: L'interfaccia ITParticipantEvent contiene metodi che recuperano la descrizione degli eventi del partecipante.
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: Interfaccia ITParticipantEvent (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac6e2b43a528bc041a71962e84b4e1be62152a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328728"
---
# <a name="itparticipantevent-interface"></a><span data-ttu-id="a3871-103">Interfaccia ITParticipantEvent</span><span class="sxs-lookup"><span data-stu-id="a3871-103">ITParticipantEvent interface</span></span>

<span data-ttu-id="a3871-104">\[**ITParticipantEvent** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a3871-104">\[**ITParticipantEvent** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a3871-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a3871-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a3871-106">L'interfaccia **ITParticipantEvent** contiene metodi che recuperano la descrizione degli eventi del partecipante.</span><span class="sxs-lookup"><span data-stu-id="a3871-106">The **ITParticipantEvent** interface contains methods that retrieve the description of participant events.</span></span> <span data-ttu-id="a3871-107">Quando l'implementazione dell'applicazione del metodo [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) indica un [**\_ evento TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) uguale a **te \_ private**, il parametro *pEvent* del metodo è un puntatore **IDispatch** per l'interfaccia **ITParticipantEvent** .</span><span class="sxs-lookup"><span data-stu-id="a3871-107">When the application's implementation of the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method indicates a [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) equal to **TE\_PRIVATE**, the method's *pEvent* parameter is an **IDispatch** pointer for the **ITParticipantEvent** interface.</span></span> <span data-ttu-id="a3871-108">I metodi di questa interfaccia possono essere utilizzati per recuperare le informazioni relative a una modifica del partecipante che si è verificata.</span><span class="sxs-lookup"><span data-stu-id="a3871-108">The methods of this interface can be used to retrieve information concerning a participant change that has occurred.</span></span>

> [!Note]  
> <span data-ttu-id="a3871-109">È necessario chiamare il metodo [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) e impostare una maschera di filtro eventi che includa l'evento **\_ privato te** per abilitare la ricezione degli eventi del partecipante.</span><span class="sxs-lookup"><span data-stu-id="a3871-109">You must call the [**ITTAPI::put\_EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) method and set an event filter mask that includes the **TE\_PRIVATE** event to enable reception of participant events.</span></span> <span data-ttu-id="a3871-110">Se non si chiama **ITTAPI::p UT \_ EventFilter**, l'applicazione non riceverà alcun evento.</span><span class="sxs-lookup"><span data-stu-id="a3871-110">If you do not call **ITTAPI::put\_EventFilter**, your application will not receive any events.</span></span> <span data-ttu-id="a3871-111">Per ulteriori informazioni, vedere Cenni preliminari [sugli eventi](events.md) .</span><span class="sxs-lookup"><span data-stu-id="a3871-111">For more information, see the [Events](events.md) overview.</span></span>

 

## <a name="members"></a><span data-ttu-id="a3871-112">Membri</span><span class="sxs-lookup"><span data-stu-id="a3871-112">Members</span></span>

<span data-ttu-id="a3871-113">L'interfaccia **ITParticipantEvent** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a3871-113">The **ITParticipantEvent** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a3871-114">**ITParticipantEvent** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a3871-114">**ITParticipantEvent** also has these types of members:</span></span>

-   [<span data-ttu-id="a3871-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="a3871-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a3871-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="a3871-116">Methods</span></span>

<span data-ttu-id="a3871-117">L'interfaccia **ITParticipantEvent** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a3871-117">The **ITParticipantEvent** interface has these methods.</span></span>



| <span data-ttu-id="a3871-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="a3871-118">Method</span></span>                                                         | <span data-ttu-id="a3871-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3871-119">Description</span></span>                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3871-120">**Ottieni \_ evento**</span><span class="sxs-lookup"><span data-stu-id="a3871-120">**get\_Event**</span></span>](itparticipantevent-get-event.md)             | <span data-ttu-id="a3871-121">Ottiene il descrittore di [**\_ eventi del partecipante**](participant-event.md) dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a3871-121">Gets the [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span><br/>                                                    |
| [<span data-ttu-id="a3871-122">**Ottieni \_ partecipante**</span><span class="sxs-lookup"><span data-stu-id="a3871-122">**get\_Participant**</span></span>](itparticipantevent-get-participant.md) | <span data-ttu-id="a3871-123">Ottiene un puntatore a una matrice di interfacce [**ITParticipant**](itparticipant.md) che rappresentano i partecipanti coinvolti nell'evento.</span><span class="sxs-lookup"><span data-stu-id="a3871-123">Gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span><br/> |
| [<span data-ttu-id="a3871-124">**ottenere il \_ Sottoflusso**</span><span class="sxs-lookup"><span data-stu-id="a3871-124">**get\_SubStream**</span></span>](itparticipantevent-get-substream.md)     | <span data-ttu-id="a3871-125">Ottiene un puntatore a una matrice di interfacce [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) che rappresentano i flussi sottoflussi necessari nell'evento.</span><span class="sxs-lookup"><span data-stu-id="a3871-125">Gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="a3871-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3871-126">Requirements</span></span>



| <span data-ttu-id="a3871-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3871-127">Requirement</span></span> | <span data-ttu-id="a3871-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a3871-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3871-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="a3871-129">TAPI version</span></span><br/> | <span data-ttu-id="a3871-130">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a3871-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a3871-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3871-131">Header</span></span><br/>       | <dl> <span data-ttu-id="a3871-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3871-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="a3871-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="a3871-133">Library</span></span><br/>      | <dl> <span data-ttu-id="a3871-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3871-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a3871-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a3871-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="a3871-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3871-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a3871-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3871-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3871-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="a3871-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="a3871-139">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="a3871-139">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="a3871-140">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="a3871-140">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="a3871-141">**\_evento partecipante**</span><span class="sxs-lookup"><span data-stu-id="a3871-141">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> <dt>

[<span data-ttu-id="a3871-142">**ITTAPIEventNotification:: Event**</span><span class="sxs-lookup"><span data-stu-id="a3871-142">**ITTAPIEventNotification::Event**</span></span>](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[<span data-ttu-id="a3871-143">**\_evento TAPI**</span><span class="sxs-lookup"><span data-stu-id="a3871-143">**TAPI\_EVENT**</span></span>](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[<span data-ttu-id="a3871-144">Frammento di codice eventi di registrazione</span><span class="sxs-lookup"><span data-stu-id="a3871-144">Register Events code snippet</span></span>](register-events.md)
</dt> </dl>

 

