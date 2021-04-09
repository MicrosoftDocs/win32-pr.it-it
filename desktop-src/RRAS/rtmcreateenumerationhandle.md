---
title: Funzione RtmCreateEnumerationHandle (RTM. h)
description: La funzione RtmCreateEnumerationHandle restituisce un handle da usare con RtmEnumerateGetNextRoute per analizzare tutte le route o un subset di route, noto a gestione tabelle di routing.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- RAS funzione RtmCreateEnumerationHandle
topic_type:
- apiref
api_name:
- RtmCreateEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14086639db299038139e0e7d02eb12bb892042bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119222"
---
# <a name="rtmcreateenumerationhandle-function"></a><span data-ttu-id="9f44a-104">RtmCreateEnumerationHandle (funzione)</span><span class="sxs-lookup"><span data-stu-id="9f44a-104">RtmCreateEnumerationHandle function</span></span>

<span data-ttu-id="9f44a-105">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9f44a-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="9f44a-106">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="9f44a-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="9f44a-107">La funzione **RtmCreateEnumerationHandle** restituisce un handle da usare con [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) per analizzare tutte le route o un subset di route, noto a gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="9f44a-107">The **RtmCreateEnumerationHandle** function returns a handle to use with [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) to scan through all routes, or a subset of routes, known to the routing table manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f44a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f44a-108">Syntax</span></span>


```C++
HANDLE RtmCreateEnumerationHandle(
  _In_ DWORD ProtocolFamily,
  _In_ DWORD EnumerationFlags,
  _In_ PVOID CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="9f44a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f44a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f44a-110">*ProtocolFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f44a-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f44a-111">Specifica la famiglia di protocolli delle route da enumerare.</span><span class="sxs-lookup"><span data-stu-id="9f44a-111">Specifies the protocol family of the routes to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="9f44a-112">*EnumerationFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f44a-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f44a-113">Specifica le route da enumerare.</span><span class="sxs-lookup"><span data-stu-id="9f44a-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="9f44a-114">Questo parametro limita il set di route restituite dall'API di enumerazione a un subset definito dai flag seguenti e i valori nei membri corrispondenti della struttura a cui punta il parametro *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="9f44a-114">This parameter limits the set of routes returned by the enumeration API to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="9f44a-115">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9f44a-115">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="9f44a-116">EnumerationFlags</span><span class="sxs-lookup"><span data-stu-id="9f44a-116">EnumerationFlags</span></span>                                                                                                                                                                              | <span data-ttu-id="9f44a-117">Significato</span><span class="sxs-lookup"><span data-stu-id="9f44a-117">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <span data-ttu-id="9f44a-118"><dt>**\_solo RTM \_ questa \_ rete**</dt></span><span class="sxs-lookup"><span data-stu-id="9f44a-118"><dt>**RTM\_ONLY\_THIS\_NETWORK**</dt></span></span> </dl>       | <span data-ttu-id="9f44a-119">Enumerare solo le route che hanno lo stesso numero di rete del \_ membro di rete RR della struttura a cui punta CriteriaRoute.</span><span class="sxs-lookup"><span data-stu-id="9f44a-119">Enumerate only those routes that have the same network number as the RR\_Network member of the structure pointed to by CriteriaRoute.</span></span><br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <span data-ttu-id="9f44a-120"><dt>**\_solo RTM \_ questa \_ interfaccia**</dt></span><span class="sxs-lookup"><span data-stu-id="9f44a-120"><dt>**RTM\_ONLY\_THIS\_INTERFACE**</dt></span></span> </dl> | <span data-ttu-id="9f44a-121">Enumerare solo le route ottenute tramite l'interfaccia specificata dal campo RR \_ InterfaceID della struttura a cui punta CriteriaRoute.</span><span class="sxs-lookup"><span data-stu-id="9f44a-121">Enumerate only those routes that were obtained through the interface specified by the RR\_InterfaceID field of the structure pointed to by CriteriaRoute.</span></span><br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <span data-ttu-id="9f44a-122"><dt>**\_solo RTM \_ questo \_ protocollo**</dt></span><span class="sxs-lookup"><span data-stu-id="9f44a-122"><dt>**RTM\_ONLY\_THIS\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="9f44a-123">Enumerare solo le route aggiunte dal protocollo di routing specificato dal \_ campo RR RoutingProtocol della struttura a cui punta CriteriaRoute.</span><span class="sxs-lookup"><span data-stu-id="9f44a-123">Enumerate only those routes that were added by the routing protocol specified by the RR\_RoutingProtocol field of the structure pointed to by CriteriaRoute.</span></span><br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <span data-ttu-id="9f44a-124"><dt>**\_ \_ Route migliori solo per RTM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9f44a-124"><dt>**RTM\_ONLY\_BEST\_ROUTES**</dt></span></span> </dl>          | <span data-ttu-id="9f44a-125">Enumerare solo le route migliori a ognuna delle reti nel set.</span><span class="sxs-lookup"><span data-stu-id="9f44a-125">Enumerate only the best routes to each of the networks in the set.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="9f44a-126">*CriteriaRoute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f44a-126">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f44a-127">Puntatore a una struttura di route specifica della famiglia di protocolli [**( \_ \_ route IP RTM**](rtm-ip-route.md) o [**\_ \_ Route IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="9f44a-127">Pointer to a protocol-family-specific route structure ([**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="9f44a-128">I valori dei membri in questa struttura corrispondono ai flag specificati dal parametro *EnumerationFlags* .</span><span class="sxs-lookup"><span data-stu-id="9f44a-128">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f44a-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f44a-129">Return value</span></span>

<span data-ttu-id="9f44a-130">Se la funzione ha esito positivo, il valore restituito è un **handle** da usare con le successive chiamate di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="9f44a-130">If the function succeeds, the return value is a **HANDLE** to use with subsequent enumeration calls.</span></span>

<span data-ttu-id="9f44a-131">Se la funzione ha esito negativo o non esistono route con i criteri specificati, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="9f44a-131">If the function fails, or no routes exist with the specified criteria, the return value is **NULL**.</span></span> <span data-ttu-id="9f44a-132">Chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="9f44a-132">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="9f44a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="9f44a-133">Value</span></span>                                                                                                       | <span data-ttu-id="9f44a-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f44a-134">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9f44a-135"><dt>**ERRORE \_ Nessuna \_ Route**</dt></span><span class="sxs-lookup"><span data-stu-id="9f44a-135"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="9f44a-136">Non sono presenti route con i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="9f44a-136">There are no routes that have the specified criteria.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="9f44a-137"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9f44a-137"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="9f44a-138">Uno o più parametri di input non sono validi (ad esempio, la famiglia di protocolli sconosciuta, i flag di enumerazione non validi).</span><span class="sxs-lookup"><span data-stu-id="9f44a-138">One or more of the input parameters is invalid (for example, unknown protocol family, invalid enumeration flags).</span></span><br/> |
| <dl> <span data-ttu-id="9f44a-139"><dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9f44a-139"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="9f44a-140">Risorse insufficienti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="9f44a-140">There are insufficient resources to carry out the operation.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="9f44a-141"><dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9f44a-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="9f44a-142">Memoria insufficiente per l'allocazione dell'handle.</span><span class="sxs-lookup"><span data-stu-id="9f44a-142">There is insufficient memory to allocate the handle.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="9f44a-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f44a-143">Requirements</span></span>



| <span data-ttu-id="9f44a-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f44a-144">Requirement</span></span> | <span data-ttu-id="9f44a-145">Valore</span><span class="sxs-lookup"><span data-stu-id="9f44a-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9f44a-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f44a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9f44a-147">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9f44a-147">None supported</span></span><br/>                                                          |
| <span data-ttu-id="9f44a-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f44a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9f44a-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f44a-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9f44a-150">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="9f44a-150">End of server support</span></span><br/>    | <span data-ttu-id="9f44a-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9f44a-151">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="9f44a-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f44a-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f44a-153"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f44a-153"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f44a-154">Libreria</span><span class="sxs-lookup"><span data-stu-id="9f44a-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f44a-155"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f44a-155"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="9f44a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="9f44a-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f44a-157"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f44a-157"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f44a-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f44a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f44a-159">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="9f44a-159">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="9f44a-160">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="9f44a-160">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="9f44a-161">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="9f44a-161">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="9f44a-162">**\_route IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="9f44a-162">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="9f44a-163">**\_Route IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="9f44a-163">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="9f44a-164">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="9f44a-164">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="9f44a-165">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="9f44a-165">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 

