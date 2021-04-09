---
title: Funzione RtmGetFirstRoute (RTM. h)
description: La funzione RtmGetFirstRoute restituisce la prima route dal subset specificato di route nella tabella.
ms.assetid: f2071b50-4b06-432f-8dbf-45696f8a5cb1
keywords:
- RAS funzione RtmGetFirstRoute
topic_type:
- apiref
api_name:
- RtmGetFirstRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e98a5deb0f925fbf3b27c21302060bbe4869b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120242"
---
# <a name="rtmgetfirstroute-function"></a><span data-ttu-id="09d3a-104">RtmGetFirstRoute (funzione)</span><span class="sxs-lookup"><span data-stu-id="09d3a-104">RtmGetFirstRoute function</span></span>

<span data-ttu-id="09d3a-105">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="09d3a-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="09d3a-106">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="09d3a-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="09d3a-107">La funzione **RtmGetFirstRoute** restituisce la prima route dal subset specificato di route nella tabella.</span><span class="sxs-lookup"><span data-stu-id="09d3a-107">The **RtmGetFirstRoute** function returns the first route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="09d3a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09d3a-108">Syntax</span></span>


```C++
DWORD RtmGetFirstRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="09d3a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="09d3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09d3a-110">*ProtocolFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09d3a-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d3a-111">Specifica la famiglia di protocolli di route da recuperare, ad esempio IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="09d3a-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="09d3a-112">*EnumerationFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09d3a-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d3a-113">Specifica che limita il set di route eliminate a un subset definito da questi flag e i valori nei membri corrispondenti della struttura a cui punta il parametro *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="09d3a-113">Specifies the limits the set of deleted routes to a subset defined by these flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="09d3a-114">I flag sono identici a quelli usati in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="09d3a-114">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="09d3a-115">*Route* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="09d3a-115">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="09d3a-116">In input, la *Route* punta a una struttura specifica della famiglia di protocolli [**( \_ \_ route IP RTM**](rtm-ip-route.md) o [**\_ \_ Route IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="09d3a-116">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="09d3a-117">La funzione chiamante fornisce i valori dei membri per questa struttura.</span><span class="sxs-lookup"><span data-stu-id="09d3a-117">The calling function provides member values for this structure.</span></span> <span data-ttu-id="09d3a-118">Questi valori, insieme al parametro *EnumerationFlags* , specificano il set dal quale restituire le route.</span><span class="sxs-lookup"><span data-stu-id="09d3a-118">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="09d3a-119">Out output, *Route* punta alla prima route corrispondente ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="09d3a-119">Out output, *Route* points to the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09d3a-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09d3a-120">Return value</span></span>

<span data-ttu-id="09d3a-121">Se la funzione ha esito positivo, il valore restituito non è un \_ errore.</span><span class="sxs-lookup"><span data-stu-id="09d3a-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="09d3a-122">Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="09d3a-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="09d3a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="09d3a-123">Value</span></span>                                                                                                       | <span data-ttu-id="09d3a-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09d3a-124">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09d3a-125"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09d3a-125"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="09d3a-126">Uno dei parametri non è valido.</span><span class="sxs-lookup"><span data-stu-id="09d3a-126">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="09d3a-127"><dt>**ERRORE \_ Nessuna \_ Route**</dt></span><span class="sxs-lookup"><span data-stu-id="09d3a-127"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="09d3a-128">Nessuna route corrispondente ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="09d3a-128">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="09d3a-129"><dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09d3a-129"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="09d3a-130">Risorse insufficienti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="09d3a-130">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09d3a-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="09d3a-131">Remarks</span></span>

<span data-ttu-id="09d3a-132">Le route vengono restituite nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="09d3a-132">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="09d3a-133">Numero di rete</span><span class="sxs-lookup"><span data-stu-id="09d3a-133">Network number</span></span>
2.  <span data-ttu-id="09d3a-134">Protocollo di routing</span><span class="sxs-lookup"><span data-stu-id="09d3a-134">Routing protocol</span></span>
3.  <span data-ttu-id="09d3a-135">Identificatore di interfaccia</span><span class="sxs-lookup"><span data-stu-id="09d3a-135">Interface identifier</span></span>
4.  <span data-ttu-id="09d3a-136">Indirizzo hop successivo</span><span class="sxs-lookup"><span data-stu-id="09d3a-136">Next-hop address</span></span>

<span data-ttu-id="09d3a-137">Questa funzione è meno efficiente della funzione di handle di enumerazione corrispondente, [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md).</span><span class="sxs-lookup"><span data-stu-id="09d3a-137">This function is less efficient than the corresponding enumeration handle function, [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09d3a-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09d3a-138">Requirements</span></span>



| <span data-ttu-id="09d3a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="09d3a-139">Requirement</span></span> | <span data-ttu-id="09d3a-140">Valore</span><span class="sxs-lookup"><span data-stu-id="09d3a-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09d3a-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09d3a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="09d3a-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="09d3a-142">None supported</span></span><br/>                                                          |
| <span data-ttu-id="09d3a-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09d3a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="09d3a-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="09d3a-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="09d3a-145">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="09d3a-145">End of server support</span></span><br/>    | <span data-ttu-id="09d3a-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09d3a-146">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="09d3a-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09d3a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="09d3a-148"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="09d3a-148"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="09d3a-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="09d3a-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="09d3a-150"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09d3a-150"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="09d3a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="09d3a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09d3a-152"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09d3a-152"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09d3a-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09d3a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09d3a-154">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="09d3a-154">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="09d3a-155">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="09d3a-155">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="09d3a-156">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="09d3a-156">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="09d3a-157">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="09d3a-157">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="09d3a-158">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="09d3a-158">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="09d3a-159">**RtmGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="09d3a-159">**RtmGetNextRoute**</span></span>](rtmgetnextroute.md)
</dt> </dl>

 

 





