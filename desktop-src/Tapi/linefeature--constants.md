---
description: Le \_ costanti LINEFEATURE elencano le operazioni che possono essere richiamate su una riga tramite questa API.
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: Costanti LINEFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac930123a10f401a7a79de8ccf6c61452df05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333551"
---
# <a name="linefeature_-constants"></a><span data-ttu-id="c4eac-103">\_Costanti LINEFEATURE</span><span class="sxs-lookup"><span data-stu-id="c4eac-103">LINEFEATURE\_ Constants</span></span>

<span data-ttu-id="c4eac-104">Le **\_ costanti LINEFEATURE** elencano le operazioni che possono essere richiamate su una riga tramite questa API.</span><span class="sxs-lookup"><span data-stu-id="c4eac-104">The **LINEFEATURE\_ constants** list the operations that can be invoked on a line using this API.</span></span>

<dl> <dt>

<span data-ttu-id="c4eac-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**\_DEVSPECIFIC LINEFEATURE**</span><span class="sxs-lookup"><span data-stu-id="c4eac-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4eac-106">È possibile usare le operazioni specifiche del dispositivo sulla riga.</span><span class="sxs-lookup"><span data-stu-id="c4eac-106">Device-specific operations can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4eac-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**\_DEVSPECIFICFEAT LINEFEATURE**</span><span class="sxs-lookup"><span data-stu-id="c4eac-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE\_DEVSPECIFICFEAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4eac-108">È possibile usare le funzionalità specifiche del dispositivo sulla riga.</span><span class="sxs-lookup"><span data-stu-id="c4eac-108">Device-specific features can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4eac-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE \_ in futuro**</span><span class="sxs-lookup"><span data-stu-id="c4eac-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4eac-110">L'invio di tutti gli indirizzi può essere usato sulla riga.</span><span class="sxs-lookup"><span data-stu-id="c4eac-110">Forwarding of all addresses can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4eac-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**\_FORWARDDND LINEFEATURE**</span><span class="sxs-lookup"><span data-stu-id="c4eac-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4eac-112">La funzione [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (con un indirizzo di destinazione vuoto) può essere usata per attivare la funzionalità non disturbare su tutti gli indirizzi sulla riga.</span><span class="sxs-lookup"><span data-stu-id="c4eac-112">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on all addresses on the line.</span></span> <span data-ttu-id="c4eac-113">\_Verrà impostato anche LINEFEATURE in futuro.</span><span class="sxs-lookup"><span data-stu-id="c4eac-113">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="c4eac-114">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="c4eac-114">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4eac-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**\_FORWARDFWD LINEFEATURE**</span><span class="sxs-lookup"><span data-stu-id="c4eac-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4eac-116">La funzione [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) può essere usata per inviare le chiamate su tutti gli indirizzi della riga ad altri numeri.</span><span class="sxs-lookup"><span data-stu-id="c4eac-116">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on all address on the line to other numbers.</span></span> <span data-ttu-id="c4eac-117">\_Verrà impostato anche LINEFEATURE in futuro.</span><span class="sxs-lookup"><span data-stu-id="c4eac-117">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="c4eac-118">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="c4eac-118">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4eac-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**\_MAKECALL LINEFEATURE**</span><span class="sxs-lookup"><span data-stu-id="c4eac-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4eac-120">Una chiamata in uscita può essere inserita in questa riga usando un indirizzo non specificato.</span><span class="sxs-lookup"><span data-stu-id="c4eac-120">An outgoing call can be placed on this line using an unspecified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4eac-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**\_SETDEVSTATUS LINEFEATURE**</span><span class="sxs-lookup"><span data-stu-id="c4eac-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE\_SETDEVSTATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4eac-122">La funzione [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) può essere richiamata sul dispositivo a linee.</span><span class="sxs-lookup"><span data-stu-id="c4eac-122">The [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) function can be invoked on the line device.</span></span> <span data-ttu-id="c4eac-123">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="c4eac-123">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4eac-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**\_SETMEDIACONTROL LINEFEATURE**</span><span class="sxs-lookup"><span data-stu-id="c4eac-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4eac-125">Il controllo multimediale può essere impostato su questa riga.</span><span class="sxs-lookup"><span data-stu-id="c4eac-125">Media control can be set on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4eac-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE \_**</span><span class="sxs-lookup"><span data-stu-id="c4eac-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4eac-127">È possibile impostare le modalità Terminal per questa riga.</span><span class="sxs-lookup"><span data-stu-id="c4eac-127">Terminal modes for this line can be set.</span></span>

> [!Note]  
> <span data-ttu-id="c4eac-128">Se nessuno dei nuovi bit "in" modificati è impostato nel membro **dwLineFeatures** in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) ma \_ viene impostato il bit di avanzamento LINEFEATURE, una qualsiasi delle modalità di avanzamento può funzionare. il provider di servizi non ha specificato semplicemente quelli.</span><span class="sxs-lookup"><span data-stu-id="c4eac-128">If neither of the new modified "FORWARD" bits is set in the **dwLineFeatures** member in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) but the LINEFEATURE\_FORWARD bit is set, then any of the forward modes can work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4eac-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4eac-129">Remarks</span></span>

<span data-ttu-id="c4eac-130">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="c4eac-130">No extensibility.</span></span> <span data-ttu-id="c4eac-131">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="c4eac-131">All 32 bits are reserved.</span></span>

<span data-ttu-id="c4eac-132">Le \_ costanti LINEFEATURE vengono usate in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (restituite da [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)).</span><span class="sxs-lookup"><span data-stu-id="c4eac-132">The LINEFEATURE\_ constants are used in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (returned by [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)).</span></span> <span data-ttu-id="c4eac-133">[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) segnala, per una determinata riga, le funzionalità della linea che possono essere effettivamente richiamate mentre la riga si trova nello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="c4eac-133">[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) reports, for a given line, which line features can actually be invoked while the line is in the current state.</span></span> <span data-ttu-id="c4eac-134">Un'applicazione rende questa determinazione dinamicamente dopo la modifica dello stato della riga, in genere causata dalle attività relative all'indirizzo o alla chiamata sulla riga.</span><span class="sxs-lookup"><span data-stu-id="c4eac-134">An application would make this determination dynamically after line state changes, typically caused by address or call-related activities on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4eac-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4eac-135">Requirements</span></span>



| <span data-ttu-id="c4eac-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4eac-136">Requirement</span></span> | <span data-ttu-id="c4eac-137">Valore</span><span class="sxs-lookup"><span data-stu-id="c4eac-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c4eac-138">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="c4eac-138">TAPI version</span></span><br/> | <span data-ttu-id="c4eac-139">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c4eac-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c4eac-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4eac-140">Header</span></span><br/>       | <dl> <span data-ttu-id="c4eac-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4eac-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4eac-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4eac-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4eac-143">**LINEDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="c4eac-143">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="c4eac-144">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="c4eac-144">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="c4eac-145">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="c4eac-145">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="c4eac-146">**lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="c4eac-146">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 




