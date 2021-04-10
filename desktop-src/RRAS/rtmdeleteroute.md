---
title: Funzione RtmDeleteRoute (RTM. h)
description: La funzione RtmDeleteRoute Elimina una voce di route.
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- RAS funzione RtmDeleteRoute
topic_type:
- apiref
api_name:
- RtmDeleteRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 310364bdb6e6ba7daf285316fcaaf16884e53929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964446"
---
# <a name="rtmdeleteroute-function"></a><span data-ttu-id="691e0-104">RtmDeleteRoute (funzione)</span><span class="sxs-lookup"><span data-stu-id="691e0-104">RtmDeleteRoute function</span></span>

<span data-ttu-id="691e0-105">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="691e0-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="691e0-106">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="691e0-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="691e0-107">La funzione **RtmDeleteRoute** Elimina una voce di route.</span><span class="sxs-lookup"><span data-stu-id="691e0-107">The **RtmDeleteRoute** function deletes a route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="691e0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="691e0-108">Syntax</span></span>


```C++
DWORD RtmDeleteRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="691e0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="691e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="691e0-110">*ClientHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="691e0-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="691e0-111">Handle che identifica il client e quindi il protocollo di routing della route aggiunta o aggiornata.</span><span class="sxs-lookup"><span data-stu-id="691e0-111">Handle that identifies the client and therefore the routing protocol of the added or updated route.</span></span> <span data-ttu-id="691e0-112">Ottenere questo handle chiamando [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="691e0-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="691e0-113">*Route* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="691e0-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="691e0-114">Puntatore a una struttura specifica della famiglia di protocolli che specifica la route nuova o aggiornata.</span><span class="sxs-lookup"><span data-stu-id="691e0-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="691e0-115">I campi seguenti vengono utilizzati da Gestione tabelle di routing per aggiornare la tabella di routing:</span><span class="sxs-lookup"><span data-stu-id="691e0-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="691e0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="691e0-116">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="691e0-117">Significato</span><span class="sxs-lookup"><span data-stu-id="691e0-117">Meaning</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="691e0-118"><dt>**\_Rete RR**</dt></span><span class="sxs-lookup"><span data-stu-id="691e0-118"><dt>**RR\_Network**</dt></span></span> </dl>                             | <span data-ttu-id="691e0-119">Specifica il numero di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="691e0-119">Specifies the destination network number.</span></span> <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="691e0-120"><dt>**\_INTERFACEID RR**</dt></span><span class="sxs-lookup"><span data-stu-id="691e0-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>             | <span data-ttu-id="691e0-121">Specifica l'indice dell'interfaccia tramite la quale è stata ricevuta la route.</span><span class="sxs-lookup"><span data-stu-id="691e0-121">Specifies the index of the interface through which the route was received.</span></span><br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="691e0-122"><dt>**\_NEXTHOPADDRESS RR**</dt></span><span class="sxs-lookup"><span data-stu-id="691e0-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl> | <span data-ttu-id="691e0-123">Specifica l'indirizzo di rete del router di hop successivo.</span><span class="sxs-lookup"><span data-stu-id="691e0-123">Specifies the network address of the next-hop router.</span></span><br/>                      |



 

</dd> <dt>

<span data-ttu-id="691e0-124">*Flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="691e0-124">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="691e0-125">Puntatore a un set di flag che indicano il tipo del messaggio di modifica e le informazioni inserite nei buffer specificati.</span><span class="sxs-lookup"><span data-stu-id="691e0-125">Pointer to a set of flags that indicate the type of the change message, and what information was placed in the provided buffers.</span></span> <span data-ttu-id="691e0-126">Questo parametro è uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="691e0-126">This parameter is one of the following values.</span></span>



| <span data-ttu-id="691e0-127">Flags</span><span class="sxs-lookup"><span data-stu-id="691e0-127">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="691e0-128">Significato</span><span class="sxs-lookup"><span data-stu-id="691e0-128">Meaning</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="691e0-129"><dt>**\_Nessuna \_ modifica RTM**</dt></span><span class="sxs-lookup"><span data-stu-id="691e0-129"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="691e0-130">L'eliminazione della route non influisce sul percorso migliore per qualsiasi rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="691e0-130">Deleting the route did not affect the best route to any destination network.</span></span> <span data-ttu-id="691e0-131">In altre parole, un'altra voce rappresenta una route per la stessa rete di destinazione e ha una metrica inferiore.</span><span class="sxs-lookup"><span data-stu-id="691e0-131">In other words, another entry represents a route to the same destination network and has a lower metric.</span></span><br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="691e0-132"><dt>**\_route RTM \_ eliminata**</dt></span><span class="sxs-lookup"><span data-stu-id="691e0-132"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="691e0-133">La route eliminata è l'unica route disponibile per una determinata rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="691e0-133">The route deleted was the only route available for a particular destination network.</span></span><br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="691e0-134"><dt>**\_route RTM \_ modificata**</dt></span><span class="sxs-lookup"><span data-stu-id="691e0-134"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="691e0-135">Una volta eliminata questa route, un'altra route è stata il percorso migliore a una determinata rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="691e0-135">After this route was deleted, another route became the best route to a particular destination network.</span></span> <span data-ttu-id="691e0-136">*CurBestRoute* punta alle informazioni per la nuova route migliore.</span><span class="sxs-lookup"><span data-stu-id="691e0-136">*CurBestRoute* points to the information for the new best route.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="691e0-137">*CurBestRoute* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="691e0-137">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="691e0-138">Puntatore a una struttura che riceve le informazioni sulla route migliore correnti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="691e0-138">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="691e0-139">Il tipo della struttura è specifico per la famiglia di protocolli, ad esempio, IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="691e0-139">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="691e0-140">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="691e0-140">This parameter is optional.</span></span> <span data-ttu-id="691e0-141">Se il chiamante specifica **null** per questo parametro, non vengono restituite le informazioni relative alla route più recenti.</span><span class="sxs-lookup"><span data-stu-id="691e0-141">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="691e0-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="691e0-142">Return value</span></span>

<span data-ttu-id="691e0-143">Se la funzione ha esito positivo, il valore restituito **non è un \_ errore**.</span><span class="sxs-lookup"><span data-stu-id="691e0-143">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="691e0-144">Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="691e0-144">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="691e0-145">Valore</span><span class="sxs-lookup"><span data-stu-id="691e0-145">Value</span></span>                                                                                                       | <span data-ttu-id="691e0-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="691e0-146">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="691e0-147"><dt>**ERRORE \_ handle non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="691e0-147"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="691e0-148">Il parametro dell'handle client non è un handle valido.</span><span class="sxs-lookup"><span data-stu-id="691e0-148">The client handle parameter is not a valid handle.</span></span><br/>                                          |
| <dl> <span data-ttu-id="691e0-149"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="691e0-149"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="691e0-150">La struttura di route a cui fa riferimento il parametro di *Route* contiene un valore del membro.</span><span class="sxs-lookup"><span data-stu-id="691e0-150">The route structure pointed to by the *Route* parameter contains a member value.</span></span><br/>            |
| <dl> <span data-ttu-id="691e0-151"><dt>**ERRORE \_ di \_ tale \_ Route**</dt></span><span class="sxs-lookup"><span data-stu-id="691e0-151"><dt>**ERROR\_NO\_SUCH\_ROUTE**</dt></span></span> </dl>       | <span data-ttu-id="691e0-152">Non sono presenti voci nella tabella di routing che corrispondono ai parametri della route specificata.</span><span class="sxs-lookup"><span data-stu-id="691e0-152">There are no entries in the routing table that match the parameters of the specified route.</span></span><br/> |
| <dl> <span data-ttu-id="691e0-153"><dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="691e0-153"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="691e0-154">Risorse insufficienti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="691e0-154">There are insufficient resources to perform the operation.</span></span> <br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="691e0-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="691e0-155">Remarks</span></span>

<span data-ttu-id="691e0-156">La funzione genera un messaggio di modifica della route se la route migliore a una rete di destinazione è cambiata in seguito all'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="691e0-156">The function generates a route-change message if the best route to a destination network has changed as the result of the deletion.</span></span> <span data-ttu-id="691e0-157">Tuttavia, il messaggio di modifica della route non viene inviato al client che effettua questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="691e0-157">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="691e0-158">Al contrario, le informazioni rilevanti vengono restituite direttamente da questa funzione a tale client.</span><span class="sxs-lookup"><span data-stu-id="691e0-158">Instead, relevant information is returned by this function directly to that client.</span></span>

## <a name="requirements"></a><span data-ttu-id="691e0-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="691e0-159">Requirements</span></span>



| <span data-ttu-id="691e0-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="691e0-160">Requirement</span></span> | <span data-ttu-id="691e0-161">Valore</span><span class="sxs-lookup"><span data-stu-id="691e0-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="691e0-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="691e0-162">Minimum supported client</span></span><br/> | <span data-ttu-id="691e0-163">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="691e0-163">None supported</span></span><br/>                                                          |
| <span data-ttu-id="691e0-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="691e0-164">Minimum supported server</span></span><br/> | <span data-ttu-id="691e0-165">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="691e0-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="691e0-166">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="691e0-166">End of server support</span></span><br/>    | <span data-ttu-id="691e0-167">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="691e0-167">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="691e0-168">Intestazione</span><span class="sxs-lookup"><span data-stu-id="691e0-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="691e0-169"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="691e0-169"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="691e0-170">Libreria</span><span class="sxs-lookup"><span data-stu-id="691e0-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="691e0-171"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="691e0-171"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="691e0-172">DLL</span><span class="sxs-lookup"><span data-stu-id="691e0-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="691e0-173"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="691e0-173"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="691e0-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="691e0-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="691e0-175">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="691e0-175">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="691e0-176">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="691e0-176">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="691e0-177">**RtmAddRoute**</span><span class="sxs-lookup"><span data-stu-id="691e0-177">**RtmAddRoute**</span></span>](rtmaddroute.md)
</dt> <dt>

[<span data-ttu-id="691e0-178">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="691e0-178">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





