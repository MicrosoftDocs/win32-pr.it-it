---
title: Funzione RtmDequeueRouteChangeMessage (RTM. h)
description: La funzione RtmDequeueRouteChangeMessage restituisce il successivo messaggio di modifica della route nella coda associata al client specificato.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- RAS funzione RtmDequeueRouteChangeMessage
topic_type:
- apiref
api_name:
- RtmDequeueRouteChangeMessage
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448df230742b03f82294de102bf14b50fefa035c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120243"
---
# <a name="rtmdequeueroutechangemessage-function"></a><span data-ttu-id="f16e8-104">RtmDequeueRouteChangeMessage (funzione)</span><span class="sxs-lookup"><span data-stu-id="f16e8-104">RtmDequeueRouteChangeMessage function</span></span>

<span data-ttu-id="f16e8-105">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f16e8-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="f16e8-106">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="f16e8-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="f16e8-107">La funzione **RtmDequeueRouteChangeMessage** restituisce il successivo messaggio di modifica della route nella coda associata al client specificato.</span><span class="sxs-lookup"><span data-stu-id="f16e8-107">The **RtmDequeueRouteChangeMessage** function returns the next route-change message in the queue associated with the specified client.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16e8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f16e8-108">Syntax</span></span>


```C++
DWORD RtmDequeueRouteChangeMessage(
  _In_  HANDLE ClientHandle,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="f16e8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f16e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f16e8-110">*ClientHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f16e8-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f16e8-111">Handle che identifica il client per il quale viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f16e8-111">Handle that identifies the client for which the operation is performed.</span></span> <span data-ttu-id="f16e8-112">Ottenere questo handle chiamando [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="f16e8-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="f16e8-113">*Flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f16e8-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f16e8-114">Puntatore a una variabile **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f16e8-114">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="f16e8-115">Il valore di questa variabile viene impostato da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="f16e8-115">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="f16e8-116">Il valore specifica il tipo del messaggio di modifica e le informazioni che sono state restituite nei buffer forniti.</span><span class="sxs-lookup"><span data-stu-id="f16e8-116">The value specifies the type of the change message, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="f16e8-117">Questo parametro è uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="f16e8-117">This parameter is one of the following.</span></span>



| <span data-ttu-id="f16e8-118">Flags</span><span class="sxs-lookup"><span data-stu-id="f16e8-118">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="f16e8-119">Significato</span><span class="sxs-lookup"><span data-stu-id="f16e8-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="f16e8-120"><dt>**\_route RTM \_ aggiunta**</dt></span><span class="sxs-lookup"><span data-stu-id="f16e8-120"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="f16e8-121">La prima route è stata aggiunta per una determinata rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f16e8-121">The first route was added for a particular destination network.</span></span> <span data-ttu-id="f16e8-122">Il parametro *CurBestRoute* punta alle informazioni per la route aggiunta.</span><span class="sxs-lookup"><span data-stu-id="f16e8-122">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="f16e8-123"><dt>**\_route RTM \_ eliminata**</dt></span><span class="sxs-lookup"><span data-stu-id="f16e8-123"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="f16e8-124">L'unica route disponibile per una determinata rete di destinazione è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="f16e8-124">The only route available for a particular destination network was deleted.</span></span> <span data-ttu-id="f16e8-125">Il parametro *PrevBestRoute* punta alle informazioni per la route eliminata.</span><span class="sxs-lookup"><span data-stu-id="f16e8-125">The *PrevBestRoute* parameter points to the information for the deleted route.</span></span><br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="f16e8-126"><dt>**\_route RTM \_ modificata**</dt></span><span class="sxs-lookup"><span data-stu-id="f16e8-126"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="f16e8-127">Almeno uno dei parametri significativi è stato modificato per una route migliore a una determinata rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f16e8-127">At least one of the significant parameters was changed for a best route to a particular destination network.</span></span> <span data-ttu-id="f16e8-128">I parametri significativi sono:</span><span class="sxs-lookup"><span data-stu-id="f16e8-128">The significant parameters are:</span></span> <br/> <span data-ttu-id="f16e8-129">Identificatore di protocollo</span><span class="sxs-lookup"><span data-stu-id="f16e8-129">Protocol identifier</span></span><br/> <span data-ttu-id="f16e8-130">Indice dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="f16e8-130">Interface index</span></span><br/> <span data-ttu-id="f16e8-131">Indirizzo hop successivo</span><span class="sxs-lookup"><span data-stu-id="f16e8-131">Next-hop address</span></span><br/> <span data-ttu-id="f16e8-132">Dati specifici della famiglia di protocolli (incluse le metriche di route)</span><span class="sxs-lookup"><span data-stu-id="f16e8-132">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="f16e8-133">Il parametro *PrevBestRoute* punta alle informazioni della route come prima della modifica.</span><span class="sxs-lookup"><span data-stu-id="f16e8-133">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="f16e8-134">Il parametro *CurBestRoute* punta alle informazioni della route Current (ovvero after-Change).</span><span class="sxs-lookup"><span data-stu-id="f16e8-134">The *CurBestRoute* parameter points to current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="f16e8-135">*CurBestRoute* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f16e8-135">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f16e8-136">Puntatore a una struttura che riceve le informazioni sulla route migliore correnti (se presenti).</span><span class="sxs-lookup"><span data-stu-id="f16e8-136">Pointer to a structure that receives the current best-route information (if any).</span></span> <span data-ttu-id="f16e8-137">Il tipo della struttura è specifico per la famiglia di protocolli, ad esempio, IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="f16e8-137">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="f16e8-138">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f16e8-138">This parameter is optional.</span></span> <span data-ttu-id="f16e8-139">Se il chiamante specifica **null** per questo parametro, non vengono restituite le informazioni relative alla route più recenti.</span><span class="sxs-lookup"><span data-stu-id="f16e8-139">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="f16e8-140">*PrevBestRoute* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f16e8-140">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f16e8-141">Puntatore a una struttura che riceve le informazioni sulla route migliore precedenti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="f16e8-141">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="f16e8-142">Il tipo della struttura è specifico per la famiglia di protocolli, ad esempio, IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="f16e8-142">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="f16e8-143">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f16e8-143">This parameter is optional.</span></span> <span data-ttu-id="f16e8-144">Se il chiamante specifica **null** per questo parametro, le informazioni precedenti sulla route migliore non vengono restituite.</span><span class="sxs-lookup"><span data-stu-id="f16e8-144">If the caller specifies **NULL** for this parameter, the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f16e8-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f16e8-145">Return value</span></span>

<span data-ttu-id="f16e8-146">Il valore restituito è uno dei codici seguenti.</span><span class="sxs-lookup"><span data-stu-id="f16e8-146">The return value is one of the following codes.</span></span>



| <span data-ttu-id="f16e8-147">Valore</span><span class="sxs-lookup"><span data-stu-id="f16e8-147">Value</span></span>                                                                                                       | <span data-ttu-id="f16e8-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f16e8-148">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f16e8-149"><dt>**Nessun \_ errore**</dt></span><span class="sxs-lookup"><span data-stu-id="f16e8-149"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="f16e8-150">Questo messaggio è stato l'ultimo messaggio nella coda del client.</span><span class="sxs-lookup"><span data-stu-id="f16e8-150">This message was the last message in the client's queue.</span></span> <span data-ttu-id="f16e8-151">L'oggetto evento viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="f16e8-151">The event object is reset.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="f16e8-152"><dt>**ERRORE \_ handle non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f16e8-152"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="f16e8-153">Il parametro *ClientHandle* non è un handle valido o alla registrazione il client non ha fornito un oggetto evento per la notifica dei messaggi di modifica (vedere [**RtmRegisterClient**](rtmregisterclient.md)).</span><span class="sxs-lookup"><span data-stu-id="f16e8-153">The *ClientHandle* parameter is not a valid handle, or at registration the client did not provide an event object for change message notification (see [**RtmRegisterClient**](rtmregisterclient.md)).</span></span><br/>                           |
| <dl> <span data-ttu-id="f16e8-154"><dt>**\_altri \_ messaggi di errore**</dt></span><span class="sxs-lookup"><span data-stu-id="f16e8-154"><dt>**ERROR\_MORE\_MESSAGES**</dt></span></span> </dl>        | <span data-ttu-id="f16e8-155">La coda del client contiene messaggi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="f16e8-155">The client's queue contains additional messages.</span></span> <span data-ttu-id="f16e8-156">Il client deve chiamare nuovamente **RtmDequeueRouteChangeMessage** il prima possibile per consentire a gestione tabelle di routing di liberare le risorse associate ai messaggi in sospeso.</span><span class="sxs-lookup"><span data-stu-id="f16e8-156">The client should call **RtmDequeueRouteChangeMessage** again as soon as possible to allow the routing table manager to free the resources associated with the pending messages.</span></span><br/> |
| <dl> <span data-ttu-id="f16e8-157"><dt>**ERRORE \_ nessun \_ messaggio**</dt></span><span class="sxs-lookup"><span data-stu-id="f16e8-157"><dt>**ERROR\_NO\_MESSAGES**</dt></span></span> </dl>          | <span data-ttu-id="f16e8-158">La coda del client non contiene messaggi; la chiamata non è stata richiesta.</span><span class="sxs-lookup"><span data-stu-id="f16e8-158">The client's queue contains no messages; the call was unsolicited.</span></span> <span data-ttu-id="f16e8-159">L'evento viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="f16e8-159">The event is reset.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="f16e8-160"><dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f16e8-160"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="f16e8-161">Risorse insufficienti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f16e8-161">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="f16e8-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f16e8-162">Requirements</span></span>



| <span data-ttu-id="f16e8-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="f16e8-163">Requirement</span></span> | <span data-ttu-id="f16e8-164">Valore</span><span class="sxs-lookup"><span data-stu-id="f16e8-164">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f16e8-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f16e8-165">Minimum supported client</span></span><br/> | <span data-ttu-id="f16e8-166">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f16e8-166">None supported</span></span><br/>                                                          |
| <span data-ttu-id="f16e8-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f16e8-167">Minimum supported server</span></span><br/> | <span data-ttu-id="f16e8-168">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f16e8-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f16e8-169">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f16e8-169">End of server support</span></span><br/>    | <span data-ttu-id="f16e8-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f16e8-170">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="f16e8-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f16e8-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="f16e8-172"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="f16e8-172"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="f16e8-173">Libreria</span><span class="sxs-lookup"><span data-stu-id="f16e8-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="f16e8-174"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f16e8-174"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="f16e8-175">DLL</span><span class="sxs-lookup"><span data-stu-id="f16e8-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f16e8-176"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f16e8-176"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f16e8-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f16e8-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16e8-178">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="f16e8-178">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="f16e8-179">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="f16e8-179">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="f16e8-180">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="f16e8-180">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





