---
title: Funzione RtmAddRoute (RTM. h)
description: La funzione RtmAddRoute aggiunge una voce di route o aggiorna una voce di route esistente.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- RAS funzione RtmAddRoute
topic_type:
- apiref
api_name:
- RtmAddRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c3ee68c9b026fc37457819777e69d2be7984e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301915"
---
# <a name="rtmaddroute-function"></a><span data-ttu-id="2722b-104">RtmAddRoute (funzione)</span><span class="sxs-lookup"><span data-stu-id="2722b-104">RtmAddRoute function</span></span>

<span data-ttu-id="2722b-105">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2722b-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="2722b-106">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="2722b-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="2722b-107">La funzione **RtmAddRoute** aggiunge una voce di route o aggiorna una voce di route esistente.</span><span class="sxs-lookup"><span data-stu-id="2722b-107">The **RtmAddRoute** function adds a route entry or updates an existing route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="2722b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2722b-108">Syntax</span></span>


```C++
DWORD RtmAddRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _In_  DWORD  TimeToLive,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="2722b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2722b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2722b-110">*ClientHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2722b-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2722b-111">Handle che identifica il client e, di conseguenza, il protocollo di routing che ha aggiunto o aggiornato la route.</span><span class="sxs-lookup"><span data-stu-id="2722b-111">Handle that identifies the client, and therefore the routing protocol, that added or updated the route.</span></span> <span data-ttu-id="2722b-112">Ottenere questo handle chiamando [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="2722b-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="2722b-113">*Route* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2722b-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2722b-114">Puntatore a una struttura specifica della famiglia di protocolli che specifica la route nuova o aggiornata.</span><span class="sxs-lookup"><span data-stu-id="2722b-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="2722b-115">I campi seguenti vengono utilizzati da Gestione tabelle di routing per aggiornare la tabella di routing:</span><span class="sxs-lookup"><span data-stu-id="2722b-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="2722b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2722b-116">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="2722b-117">Significato</span><span class="sxs-lookup"><span data-stu-id="2722b-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="2722b-118"><dt>**\_Rete RR**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-118"><dt>**RR\_Network**</dt></span></span> </dl>                                                     | <span data-ttu-id="2722b-119">Specifica il numero di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2722b-119">Specifies the destination network number.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="2722b-120"><dt>**\_INTERFACEID RR**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>                                     | <span data-ttu-id="2722b-121">Specifica l'indice dell'interfaccia tramite la quale è stata ricevuta la route.</span><span class="sxs-lookup"><span data-stu-id="2722b-121">Specifies the index of the interface through which the route was received.</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="2722b-122"><dt>**\_NEXTHOPADDRESS RR**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl>                         | <span data-ttu-id="2722b-123">Specifica l'indirizzo del router di hop successivo.</span><span class="sxs-lookup"><span data-stu-id="2722b-123">Specifies the address of the next-hop router.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <span data-ttu-id="2722b-124"><dt>**\_FAMILYSPECIFICDATA RR**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-124"><dt>**RR\_FamilySpecificData**</dt></span></span> </dl>         | <span data-ttu-id="2722b-125">Specifica i dati specifici della famiglia di protocolli.</span><span class="sxs-lookup"><span data-stu-id="2722b-125">Specifies data that is specific to the protocol family.</span></span> <span data-ttu-id="2722b-126">Sebbene i dati siano trasparenti per Gestione tabelle di routing, vengono considerati quando si confrontano le route per determinare se le informazioni sulla route sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="2722b-126">Although the data is transparent to the routing table manager, it is considered when comparing routes to determine if route information has changed.</span></span> <span data-ttu-id="2722b-127">I dati vengono inoltre utilizzati per impostare i valori delle metriche indipendenti dal protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="2722b-127">The data is also used to set metric values that are independent of the routing protocol.</span></span> <span data-ttu-id="2722b-128">Di conseguenza, questi dati vengono utilizzati per determinare il percorso migliore per la rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2722b-128">Consequently, this data is used to determine the best route for the destination network.</span></span><br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <span data-ttu-id="2722b-129"><dt>**\_PROTOCOLSPECIFICDATA RR**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-129"><dt>**RR\_ProtocolSpecificData**</dt></span></span> </dl> | <span data-ttu-id="2722b-130">Specifica i dati specifici del protocollo di routing che ha fornito la route.</span><span class="sxs-lookup"><span data-stu-id="2722b-130">Specifies data which is specific to the routing protocol that supplied the route.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <span data-ttu-id="2722b-131"><dt>**\_Timestamp RR**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-131"><dt>**RR\_TimeStamp**</dt></span></span> </dl>                                             | <span data-ttu-id="2722b-132">Specifica l'ora di sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="2722b-132">Specifies the current system time.</span></span> <span data-ttu-id="2722b-133">Questo campo viene impostato da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="2722b-133">This field is set by the routing table manager.</span></span><br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="2722b-134">*TimeToLive* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2722b-134">*TimeToLive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2722b-135">Specifica il numero di secondi per cui la route specificata deve essere mantenuta nella tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="2722b-135">Specifies the number of seconds the specified route should be kept in the routing table.</span></span> <span data-ttu-id="2722b-136">Se questo parametro è impostato su infinite, la route viene mantenuta fino a quando non viene eliminata in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="2722b-136">If this parameter is set to INFINITE, the route is kept until it is explicitly deleted.</span></span> <span data-ttu-id="2722b-137">Il limite corrente per *TimeToLive* è 2147483 sec (24 + giorni).</span><span class="sxs-lookup"><span data-stu-id="2722b-137">The current limit for *TimeToLive* is 2147483 sec (24+ days).</span></span>

</dd> <dt>

<span data-ttu-id="2722b-138">*Flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2722b-138">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2722b-139">Puntatore a una variabile **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="2722b-139">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="2722b-140">Il valore di questa variabile viene impostato da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="2722b-140">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="2722b-141">Il valore indica il tipo di modifica e le informazioni che sono state restituite nei buffer forniti.</span><span class="sxs-lookup"><span data-stu-id="2722b-141">The value indicates the type of the change, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="2722b-142">Questo parametro è uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="2722b-142">This parameter is one of the following.</span></span>



| <span data-ttu-id="2722b-143">Flags</span><span class="sxs-lookup"><span data-stu-id="2722b-143">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="2722b-144">Significato</span><span class="sxs-lookup"><span data-stu-id="2722b-144">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="2722b-145"><dt>**\_Nessuna \_ modifica RTM**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-145"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="2722b-146">L'aggiunta o l'aggiornamento non ha modificato alcun parametro di route significativo oppure la voce della route interessata non è la migliore route tra le voci per la rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2722b-146">The addition or update either did not change any of the significant route parameters, or the route entry affected is not the best route among the entries for the destination network.</span></span><br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="2722b-147"><dt>**\_route RTM \_ aggiunta**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-147"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="2722b-148">La route è stata aggiunta per la rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2722b-148">The route was added for the destination network.</span></span> <span data-ttu-id="2722b-149">Il parametro *CurBestRoute* punta alle informazioni per la route aggiunta.</span><span class="sxs-lookup"><span data-stu-id="2722b-149">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="2722b-150"><dt>**\_route RTM \_ modificata**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-150"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="2722b-151">Almeno uno dei parametri significativi è stato modificato per la migliore route alla rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2722b-151">At least one of the significant parameters was changed for the best route to the destination network.</span></span> <span data-ttu-id="2722b-152">I parametri significativi sono:</span><span class="sxs-lookup"><span data-stu-id="2722b-152">The significant parameters are:</span></span> <br/> <span data-ttu-id="2722b-153">Identificatore di protocollo</span><span class="sxs-lookup"><span data-stu-id="2722b-153">Protocol identifier</span></span><br/> <span data-ttu-id="2722b-154">Indice dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="2722b-154">Interface index</span></span><br/> <span data-ttu-id="2722b-155">Indirizzo hop successivo</span><span class="sxs-lookup"><span data-stu-id="2722b-155">Next-hop address</span></span><br/> <span data-ttu-id="2722b-156">Dati specifici della famiglia di protocolli (incluse le metriche di route)</span><span class="sxs-lookup"><span data-stu-id="2722b-156">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="2722b-157">Il parametro *PrevBestRoute* punta alle informazioni della route come prima della modifica.</span><span class="sxs-lookup"><span data-stu-id="2722b-157">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="2722b-158">Il parametro *CurBestRoute* punta alle informazioni sulla route correnti, ovvero dopo la modifica.</span><span class="sxs-lookup"><span data-stu-id="2722b-158">The *CurBestRoute* parameter points to the current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="2722b-159">*CurBestRoute* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2722b-159">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2722b-160">Puntatore a una struttura che riceve le informazioni sulla route migliore correnti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="2722b-160">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="2722b-161">Il tipo della struttura è specifico per la famiglia di protocolli, ad esempio, IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="2722b-161">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="2722b-162">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2722b-162">This parameter is optional.</span></span> <span data-ttu-id="2722b-163">Se il chiamante specifica **null** per questo parametro, non vengono restituite le informazioni relative alla route più recenti.</span><span class="sxs-lookup"><span data-stu-id="2722b-163">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="2722b-164">*PrevBestRoute* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2722b-164">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2722b-165">Puntatore a una struttura che riceve le informazioni sulla route migliore precedenti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="2722b-165">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="2722b-166">Il tipo della struttura è specifico per la famiglia di protocolli, ad esempio, IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="2722b-166">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="2722b-167">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2722b-167">This parameter is optional.</span></span> <span data-ttu-id="2722b-168">Se il chiamante specifica un **valore null** per questo parametro, non vengono restituite le informazioni sulla route migliore precedenti.</span><span class="sxs-lookup"><span data-stu-id="2722b-168">If the caller specifies **NULL** for this parameter the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2722b-169">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2722b-169">Return value</span></span>

<span data-ttu-id="2722b-170">Il valore restituito è uno dei codici seguenti.</span><span class="sxs-lookup"><span data-stu-id="2722b-170">The return value is one of the following codes.</span></span>



| <span data-ttu-id="2722b-171">Valore</span><span class="sxs-lookup"><span data-stu-id="2722b-171">Value</span></span>                                                                                                       | <span data-ttu-id="2722b-172">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2722b-172">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2722b-173"><dt>**Nessun \_ errore**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-173"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="2722b-174">La route è stata aggiunta o aggiornata correttamente.</span><span class="sxs-lookup"><span data-stu-id="2722b-174">The route was added or updated successfully.</span></span><br/>                 |
| <dl> <span data-ttu-id="2722b-175"><dt>**ERRORE \_ handle non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-175"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="2722b-176">Il parametro dell'handle client non è un handle valido.</span><span class="sxs-lookup"><span data-stu-id="2722b-176">The client handle parameter is not a valid handle.</span></span><br/>           |
| <dl> <span data-ttu-id="2722b-177"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-177"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="2722b-178">La struttura di route contiene un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="2722b-178">The route structure contains an invalid parameter.</span></span><br/>           |
| <dl> <span data-ttu-id="2722b-179"><dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-179"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="2722b-180">Risorse insufficienti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2722b-180">There are insufficient resources to carry out the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2722b-181"><dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-181"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="2722b-182">La memoria disponibile non è sufficiente per allocare la voce di route.</span><span class="sxs-lookup"><span data-stu-id="2722b-182">There is insufficient memory to allocate the route entry.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="2722b-183">Commenti</span><span class="sxs-lookup"><span data-stu-id="2722b-183">Remarks</span></span>

<span data-ttu-id="2722b-184">La funzione genera un messaggio di modifica della route se la route migliore a una rete di destinazione è cambiata in seguito a questa operazione.</span><span class="sxs-lookup"><span data-stu-id="2722b-184">The function generates a route-change message if the best route to a destination network has changed as the result of this operation.</span></span> <span data-ttu-id="2722b-185">Tuttavia, il messaggio di modifica della route non viene inviato al client che effettua questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="2722b-185">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="2722b-186">Al contrario, le informazioni rilevanti vengono restituite direttamente da questa funzione a tale client tramite i parametri *Flags*, *CurBestRoute* e *PrevBestRoute* .</span><span class="sxs-lookup"><span data-stu-id="2722b-186">Instead, relevant information is returned by this function directly to that client through the *Flags*, *CurBestRoute*, and *PrevBestRoute* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="2722b-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2722b-187">Requirements</span></span>



| <span data-ttu-id="2722b-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="2722b-188">Requirement</span></span> | <span data-ttu-id="2722b-189">Valore</span><span class="sxs-lookup"><span data-stu-id="2722b-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2722b-190">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2722b-190">Minimum supported client</span></span><br/> | <span data-ttu-id="2722b-191">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2722b-191">None supported</span></span><br/>                                                          |
| <span data-ttu-id="2722b-192">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2722b-192">Minimum supported server</span></span><br/> | <span data-ttu-id="2722b-193">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2722b-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2722b-194">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="2722b-194">End of server support</span></span><br/>    | <span data-ttu-id="2722b-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2722b-195">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="2722b-196">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2722b-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="2722b-197"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-197"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="2722b-198">Libreria</span><span class="sxs-lookup"><span data-stu-id="2722b-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="2722b-199"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-199"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="2722b-200">DLL</span><span class="sxs-lookup"><span data-stu-id="2722b-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2722b-201"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2722b-201"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2722b-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2722b-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2722b-203">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="2722b-203">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="2722b-204">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="2722b-204">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="2722b-205">**RtmDeleteRoute**</span><span class="sxs-lookup"><span data-stu-id="2722b-205">**RtmDeleteRoute**</span></span>](rtmdeleteroute.md)
</dt> <dt>

[<span data-ttu-id="2722b-206">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="2722b-206">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





