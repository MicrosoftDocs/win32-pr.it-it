---
description: Le \_ costanti LINEADDRFEATURE elencano le operazioni che possono essere richiamate su un indirizzo.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: Costanti LINEADDRFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825902c2943806d1d495e14a0f0a5042f2949796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328314"
---
# <a name="lineaddrfeature_-constants"></a><span data-ttu-id="9e5c9-103">\_Costanti LINEADDRFEATURE</span><span class="sxs-lookup"><span data-stu-id="9e5c9-103">LINEADDRFEATURE\_ Constants</span></span>

<span data-ttu-id="9e5c9-104">Le **costanti \_ LINEADDRFEATURE** elencano le operazioni che possono essere richiamate su un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-104">The **LINEADDRFEATURE\_** constants list the operations that can be invoked on an address.</span></span>

<dl> <dt>

<span data-ttu-id="9e5c9-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE \_ in futuro**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-106">L'indirizzo può essere inviato.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-106">The address can be forwarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5c9-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**\_MAKECALL LINEADDRFEATURE**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-108">È possibile inserire una chiamata in uscita sull'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-108">An outgoing call can be placed on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5c9-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**LINEADDRFEATURE \_ pickup**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**LINEADDRFEATURE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-110">È possibile prelevare una chiamata all'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-110">A call can be picked up at the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5c9-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**\_PICKUPDIRECT LINEADDRFEATURE**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE\_PICKUPDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-112">La funzione [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) può essere usata per prelevare una chiamata su un indirizzo specifico.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-112">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call on a specific address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5c9-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**\_PICKUPGROUP LINEADDRFEATURE**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE\_PICKUPGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-114">La funzione [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) può essere usata per selezionare una chiamata nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-114">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call in the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5c9-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**\_PICKUPHELD LINEADDRFEATURE**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE\_PICKUPHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-116">La funzione [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (con un indirizzo di destinazione **null** ) può essere usata per selezionare una chiamata mantenuta sull'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-116">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call that is held on the address.</span></span> <span data-ttu-id="9e5c9-117">Questa operazione viene in genere usata solo in una disposizione con bridging esclusivo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-117">This is normally used only in a bridged-exclusive arrangement.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5c9-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**\_PICKUPWAITING LINEADDRFEATURE**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE\_PICKUPWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-119">La funzione [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (con un indirizzo di destinazione **null** ) può essere usata per selezionare una chiamata in attesa.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-119">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call waiting call.</span></span> <span data-ttu-id="9e5c9-120">Si noti che questo non indica necessariamente che è effettivamente presente una chiamata in attesa, perché spesso è impossibile per un dispositivo di telefonia rilevare automaticamente tale chiamata; viene tuttavia indicato che la funzione hook-Flash verrà richiamata per tentare di passare a una chiamata di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-120">Note that this does not necessarily indicate that a waiting call is actually present, because it is often impossible for a telephony device to automatically detect such a call; it does, however, indicate that the hook-flash function will be invoked to attempt to switch to such a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5c9-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**\_SETMEDIACONTROL LINEADDRFEATURE**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-122">Il controllo multimediale può essere impostato su questo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-122">Media control can be set on this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5c9-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE \_**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-124">È possibile impostare le modalità Terminal per questo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-124">The terminal modes for this address can be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5c9-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**\_SETUPCONF LINEADDRFEATURE**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE\_SETUPCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-126">A questo indirizzo è possibile configurare una chiamata di conferenza con una chiamata iniziale **null** .</span><span class="sxs-lookup"><span data-stu-id="9e5c9-126">A conference call with a **NULL** initial call can be set up at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5c9-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**\_UNCOMPLETECALL LINEADDRFEATURE**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE\_UNCOMPLETECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-128">Le richieste di completamento delle chiamate possono essere annullate a questo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-128">Call completion requests can be canceled at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5c9-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE \_ UNpark**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-130">È possibile deparcheggiare le chiamate usando questo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-130">Calls can be unparked using this address.</span></span>

> [!Note]  
> <span data-ttu-id="9e5c9-131">Se nessuno dei nuovi bit "PICKUP" modificati è impostato nel membro **dwAddressFeatures** in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) ma \_ è impostato il bit di prelievo LINEADDRFEATURE, è possibile che una qualsiasi delle modalità di prelievo funzioni. il provider di servizi non ha specificato semplicemente quelli.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-131">If none of the new modified "PICKUP" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_PICKUP bit is set, then any of the pickup modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5c9-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**\_FORWARDDND LINEADDRFEATURE**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-133">La funzione [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (con un indirizzo di destinazione vuoto) può essere usata per attivare la funzionalità non disturbare sull'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-133">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on the address.</span></span> <span data-ttu-id="9e5c9-134">\_Verrà impostato anche LINEADDRFEATURE in futuro.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-134">LINEADDRFEATURE\_FORWARD will also be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9e5c9-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**\_FORWARDFWD LINEADDRFEATURE**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e5c9-136">La funzione [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) può essere usata per inviare chiamate sull'indirizzo ad altri numeri.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-136">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on the address to other numbers.</span></span> <span data-ttu-id="9e5c9-137">\_Verrà impostato anche LINEADDRFEATURE in futuro.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-137">LINEADDRFEATURE\_FORWARD will also be set.</span></span>

> [!Note]  
> <span data-ttu-id="9e5c9-138">Se nessuno dei nuovi bit "in" modificati è impostato nel membro **dwAddressFeatures** in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) ma \_ viene impostato il bit di avanzamento LINEADDRFEATURE, è possibile che una qualsiasi delle modalità di avanzamento funzioni. il provider di servizi non ha specificato semplicemente quelli.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-138">If neither of the new modified "FORWARD" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_FORWARD bit is set, then any of the forward modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e5c9-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e5c9-139">Remarks</span></span>

<span data-ttu-id="9e5c9-140">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-140">No extensibility.</span></span> <span data-ttu-id="9e5c9-141">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-141">All 32 bits are reserved.</span></span>

<span data-ttu-id="9e5c9-142">Questa costante viene usata sia in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (restituito da [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) che in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (restituito da [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)).</span><span class="sxs-lookup"><span data-stu-id="9e5c9-142">This constant is used both in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (returned by [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) and in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (returned by [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)).</span></span> <span data-ttu-id="9e5c9-143">**LINEADDRESSCAPS** segnala la disponibilità delle funzionalità degli indirizzi da parte del provider di servizi (principalmente il Commuti) per un determinato indirizzo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-143">**LINEADDRESSCAPS** reports the availability of the address features by the service provider (mainly the switch) for a given address.</span></span> <span data-ttu-id="9e5c9-144">Un'applicazione determina questa decisione quando Inizializza.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-144">An application would make this determination when it initializes.</span></span> <span data-ttu-id="9e5c9-145">La struttura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) segnala, per un determinato indirizzo, le funzionalità che possono essere effettivamente richiamate mentre l'indirizzo si trova nello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-145">The [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure reports, for a given address, which address features can actually be invoked while the address is in the current state.</span></span> <span data-ttu-id="9e5c9-146">Un'applicazione rende questa determinazione dinamicamente dopo le modifiche dello stato dell'indirizzo, in genere dovute alle attività relative alle chiamate sull'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-146">An application would make this determination dynamically after address-state changes, typically caused by call-related activities on the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e5c9-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e5c9-147">Requirements</span></span>



| <span data-ttu-id="9e5c9-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e5c9-148">Requirement</span></span> | <span data-ttu-id="9e5c9-149">Valore</span><span class="sxs-lookup"><span data-stu-id="9e5c9-149">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9e5c9-150">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="9e5c9-150">TAPI version</span></span><br/> | <span data-ttu-id="9e5c9-151">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9e5c9-151">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="9e5c9-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e5c9-152">Header</span></span><br/>       | <dl> <span data-ttu-id="9e5c9-153"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e5c9-153"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e5c9-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e5c9-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e5c9-155">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-155">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="9e5c9-156">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-156">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="9e5c9-157">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-157">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="9e5c9-158">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-158">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="9e5c9-159">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-159">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="9e5c9-160">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="9e5c9-160">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




