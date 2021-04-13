---
title: Funzione RtmIsRoute (RTM. h)
description: La funzione RtmIsRoute determina se esistono una o più route per una rete di destinazione specificata. In tal caso, la funzione restituisce informazioni per la migliore route alla rete.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- RAS funzione RtmIsRoute
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64621732f2f7a35223421e5f0fc86a309d332c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478221"
---
# <a name="rtmisroute-function"></a><span data-ttu-id="5f0ed-105">RtmIsRoute (funzione)</span><span class="sxs-lookup"><span data-stu-id="5f0ed-105">RtmIsRoute function</span></span>

<span data-ttu-id="5f0ed-106">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5f0ed-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="5f0ed-107">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="5f0ed-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="5f0ed-108">La funzione **RtmIsRoute** determina se esistono una o più route per una rete di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="5f0ed-108">The **RtmIsRoute** function determines if one or more routes to a specified destination network exist.</span></span> <span data-ttu-id="5f0ed-109">In tal caso, la funzione restituisce informazioni per la migliore route alla rete.</span><span class="sxs-lookup"><span data-stu-id="5f0ed-109">If so, the function returns information for the best route to that network.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f0ed-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f0ed-110">Syntax</span></span>


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="5f0ed-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f0ed-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f0ed-112">*ProtocolFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f0ed-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0ed-113">Specifica il tipo di struttura dei dati a cui punta il parametro di *rete* , ad [**esempio \_ rete IP**](ip-network.md), [**\_ rete IPX**](ipx-network.md).</span><span class="sxs-lookup"><span data-stu-id="5f0ed-113">Specifies the type of data structure pointed to by the *Network* parameter, for example, [**IP\_NETWORK**](ip-network.md), [**IPX\_NETWORK**](ipx-network.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f0ed-114">*Rete* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f0ed-114">*Network* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0ed-115">Puntatore a una struttura che specifica i dati del numero di rete specifici della famiglia di protocolli.</span><span class="sxs-lookup"><span data-stu-id="5f0ed-115">Pointer to a structure that specifies protocol-family-specific network number data.</span></span> <span data-ttu-id="5f0ed-116">Questi dati identificano la rete per cui il chiamante Cerca le informazioni sulla route.</span><span class="sxs-lookup"><span data-stu-id="5f0ed-116">This data identifies the network for which the caller seeks route information.</span></span>

</dd> <dt>

<span data-ttu-id="5f0ed-117">*BestRoute* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5f0ed-117">*BestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0ed-118">Puntatore a una struttura specifica della famiglia di protocolli che riceve le informazioni sulla route migliore correnti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="5f0ed-118">Pointer to a protocol-family-specific structure that receives the current best route information, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f0ed-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f0ed-119">Return value</span></span>

<span data-ttu-id="5f0ed-120">Il valore restituito è uno dei codici seguenti.</span><span class="sxs-lookup"><span data-stu-id="5f0ed-120">The return value is one of the following codes.</span></span>



| <span data-ttu-id="5f0ed-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5f0ed-121">Value</span></span>                                                                                                       | <span data-ttu-id="5f0ed-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f0ed-122">Description</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5f0ed-123"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ed-123"><dt>**TRUE**</dt></span></span> </dl>                         | <span data-ttu-id="5f0ed-124">Esiste almeno una route per la rete specificata.</span><span class="sxs-lookup"><span data-stu-id="5f0ed-124">At least one route to the specified network exists.</span></span> <span data-ttu-id="5f0ed-125">La route migliore viene restituita nella struttura a cui punta il parametro *BestRoute* .</span><span class="sxs-lookup"><span data-stu-id="5f0ed-125">The best route is returned in the structure pointed to by the *BestRoute* parameter.</span></span><br/>      |
| <dl> <span data-ttu-id="5f0ed-126"><dt>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ed-126"><dt>**FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="5f0ed-127">Non è presente alcuna route per la rete specificata oppure l'operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="5f0ed-127">There is no route to the specified network, or the operation failed.</span></span> <span data-ttu-id="5f0ed-128">Chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere ulteriori informazioni:</span><span class="sxs-lookup"><span data-stu-id="5f0ed-128">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information:</span></span><br/> |
| <dl> <span data-ttu-id="5f0ed-129"><dt>**Nessun \_ errore**</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ed-129"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="5f0ed-130">L'operazione è stata completata, ma non è presente alcuna route per la rete specificata.</span><span class="sxs-lookup"><span data-stu-id="5f0ed-130">The operation succeeded, but there is no route to the specified network.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="5f0ed-131"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ed-131"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="5f0ed-132">Il valore del parametro *ProtocolFamily* non corrisponde ad alcuna famiglia di protocolli installata.</span><span class="sxs-lookup"><span data-stu-id="5f0ed-132">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/>                                             |
| <dl> <span data-ttu-id="5f0ed-133"><dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ed-133"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="5f0ed-134">Risorse insufficienti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5f0ed-134">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="5f0ed-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f0ed-135">Requirements</span></span>



| <span data-ttu-id="5f0ed-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f0ed-136">Requirement</span></span> | <span data-ttu-id="5f0ed-137">Valore</span><span class="sxs-lookup"><span data-stu-id="5f0ed-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5f0ed-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f0ed-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5f0ed-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5f0ed-139">None supported</span></span><br/>                                                          |
| <span data-ttu-id="5f0ed-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f0ed-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5f0ed-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f0ed-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5f0ed-142">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="5f0ed-142">End of server support</span></span><br/>    | <span data-ttu-id="5f0ed-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5f0ed-143">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="5f0ed-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f0ed-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f0ed-145"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ed-145"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f0ed-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="5f0ed-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f0ed-147"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ed-147"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="5f0ed-148">DLL</span><span class="sxs-lookup"><span data-stu-id="5f0ed-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f0ed-149"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ed-149"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f0ed-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f0ed-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f0ed-151">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="5f0ed-151">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="5f0ed-152">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="5f0ed-152">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="5f0ed-153">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="5f0ed-153">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="5f0ed-154">**\_rete IP**</span><span class="sxs-lookup"><span data-stu-id="5f0ed-154">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="5f0ed-155">**\_rete IPX**</span><span class="sxs-lookup"><span data-stu-id="5f0ed-155">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="5f0ed-156">Identificatori della famiglia di protocolli RTMv1</span><span class="sxs-lookup"><span data-stu-id="5f0ed-156">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

