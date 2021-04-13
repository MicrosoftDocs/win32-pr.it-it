---
title: Funzione RtmGetNextRoute (RTM. h)
description: La funzione RtmGetNextRoute restituisce la route successiva dal subset specificato di route nella tabella.
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- RAS funzione RtmGetNextRoute
topic_type:
- apiref
api_name:
- RtmGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8592855e0c30cef2ed43b7818badd336bc2ab6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518088"
---
# <a name="rtmgetnextroute-function"></a><span data-ttu-id="c0783-104">RtmGetNextRoute (funzione)</span><span class="sxs-lookup"><span data-stu-id="c0783-104">RtmGetNextRoute function</span></span>

<span data-ttu-id="c0783-105">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c0783-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="c0783-106">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="c0783-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="c0783-107">La funzione **RtmGetNextRoute** restituisce la route successiva dal subset specificato di route nella tabella.</span><span class="sxs-lookup"><span data-stu-id="c0783-107">The **RtmGetNextRoute** function returns the next route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0783-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0783-108">Syntax</span></span>


```C++
DWORD RtmGetNextRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="c0783-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0783-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0783-110">*ProtocolFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0783-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0783-111">Specifica la famiglia di protocolli di route da recuperare, ad esempio IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="c0783-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="c0783-112">*EnumerationFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0783-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0783-113">Specifica le route da enumerare.</span><span class="sxs-lookup"><span data-stu-id="c0783-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="c0783-114">Questo parametro limita il set di route eliminate a un subset definito dai seguenti flag e i valori dei membri corrispondenti della struttura a cui punta il parametro *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="c0783-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="c0783-115">I flag sono identici a quelli usati in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="c0783-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0783-116">*Route* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="c0783-116">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0783-117">In input, la *Route* punta a una struttura specifica della famiglia di protocolli [**( \_ \_ route IP RTM**](rtm-ip-route.md) o [**\_ \_ Route IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="c0783-117">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="c0783-118">La funzione chiamante fornisce i valori dei membri per questa struttura.</span><span class="sxs-lookup"><span data-stu-id="c0783-118">The calling function provides member values for this structure.</span></span> <span data-ttu-id="c0783-119">Questi valori, insieme al parametro *EnumerationFlags* , specificano il set dal quale restituire le route.</span><span class="sxs-lookup"><span data-stu-id="c0783-119">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="c0783-120">Nell'output, la *Route* punta a una struttura che riceve la prima route corrispondente ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="c0783-120">On output, *Route* points to a structure that receives the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0783-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0783-121">Return value</span></span>

<span data-ttu-id="c0783-122">Se la funzione ha esito positivo, il valore restituito **non è un \_ errore**.</span><span class="sxs-lookup"><span data-stu-id="c0783-122">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="c0783-123">Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="c0783-123">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="c0783-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c0783-124">Value</span></span>                                                                                                       | <span data-ttu-id="c0783-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0783-125">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0783-126"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0783-126"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="c0783-127">Uno dei parametri non è valido.</span><span class="sxs-lookup"><span data-stu-id="c0783-127">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="c0783-128"><dt>**ERRORE \_ Nessuna \_ Route**</dt></span><span class="sxs-lookup"><span data-stu-id="c0783-128"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="c0783-129">Nessuna route corrispondente ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="c0783-129">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="c0783-130"><dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0783-130"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="c0783-131">Risorse insufficienti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c0783-131">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0783-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0783-132">Remarks</span></span>

<span data-ttu-id="c0783-133">Le route vengono restituite nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="c0783-133">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="c0783-134">Numero di rete</span><span class="sxs-lookup"><span data-stu-id="c0783-134">Network number</span></span>
2.  <span data-ttu-id="c0783-135">Protocollo di routing</span><span class="sxs-lookup"><span data-stu-id="c0783-135">Routing protocol</span></span>
3.  <span data-ttu-id="c0783-136">Identificatore di interfaccia</span><span class="sxs-lookup"><span data-stu-id="c0783-136">Interface identifier</span></span>
4.  <span data-ttu-id="c0783-137">Indirizzo hop successivo</span><span class="sxs-lookup"><span data-stu-id="c0783-137">Next-hop address</span></span>

<span data-ttu-id="c0783-138">Questa funzione è meno efficiente delle funzioni di handle di enumerazione corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="c0783-138">This function is less efficient than the corresponding enumeration handle functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0783-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0783-139">Requirements</span></span>



| <span data-ttu-id="c0783-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0783-140">Requirement</span></span> | <span data-ttu-id="c0783-141">Valore</span><span class="sxs-lookup"><span data-stu-id="c0783-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0783-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0783-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c0783-143">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c0783-143">None supported</span></span><br/>                                                          |
| <span data-ttu-id="c0783-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0783-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c0783-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c0783-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c0783-146">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="c0783-146">End of server support</span></span><br/>    | <span data-ttu-id="c0783-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c0783-147">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="c0783-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0783-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0783-149"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0783-149"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0783-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="c0783-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0783-151"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0783-151"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="c0783-152">DLL</span><span class="sxs-lookup"><span data-stu-id="c0783-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0783-153"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0783-153"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0783-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0783-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0783-155">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="c0783-155">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="c0783-156">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="c0783-156">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="c0783-157">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="c0783-157">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="c0783-158">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="c0783-158">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="c0783-159">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="c0783-159">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="c0783-160">**RtmGetFirstRoute**</span><span class="sxs-lookup"><span data-stu-id="c0783-160">**RtmGetFirstRoute**</span></span>](rtmgetfirstroute.md)
</dt> </dl>

 

 





