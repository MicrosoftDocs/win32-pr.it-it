---
title: Funzione RtmEnumerateGetNextRoute (RTM. h)
description: La funzione RtmEnumerateGetNextRoute restituisce la voce di route successiva nell'enumerazione avviata da una chiamata a RtmCreateEnumerationHandle.
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- RAS funzione RtmEnumerateGetNextRoute
topic_type:
- apiref
api_name:
- RtmEnumerateGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e74cc5aa15c1014056075e876efca296556066d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301914"
---
# <a name="rtmenumerategetnextroute-function"></a><span data-ttu-id="6c02f-104">RtmEnumerateGetNextRoute (funzione)</span><span class="sxs-lookup"><span data-stu-id="6c02f-104">RtmEnumerateGetNextRoute function</span></span>

<span data-ttu-id="6c02f-105">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6c02f-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="6c02f-106">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="6c02f-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="6c02f-107">La funzione **RtmEnumerateGetNextRoute** restituisce la voce di route successiva nell'enumerazione avviata da una chiamata a [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="6c02f-107">The **RtmEnumerateGetNextRoute** function returns the next-route entry in the enumeration started by a call to [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c02f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c02f-108">Syntax</span></span>


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a><span data-ttu-id="6c02f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c02f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c02f-110">*EnumerationHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c02f-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c02f-111">Handle che identifica l'enumerazione e ne specifica l'ambito.</span><span class="sxs-lookup"><span data-stu-id="6c02f-111">Handle that identifies the enumeration and specifies its scope.</span></span> <span data-ttu-id="6c02f-112">Ottenere questo handle chiamando [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="6c02f-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c02f-113">*Route* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c02f-113">*Route* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c02f-114">Puntatore a una struttura di route specifica della famiglia di protocolli [**( \_ \_ route IP RTM**](rtm-ip-route.md) o [**\_ \_ Route IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="6c02f-114">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="6c02f-115">Questa struttura riceverà la route successiva nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="6c02f-115">This structure will receive the next route in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c02f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c02f-116">Return value</span></span>

<span data-ttu-id="6c02f-117">Se la funzione ha esito positivo, il valore restituito non è un \_ errore.</span><span class="sxs-lookup"><span data-stu-id="6c02f-117">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="6c02f-118">Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="6c02f-118">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="6c02f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6c02f-119">Value</span></span>                                                                                                       | <span data-ttu-id="6c02f-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c02f-120">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c02f-121"><dt>**ERRORE \_ handle non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c02f-121"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="6c02f-122">Il parametro *EnumerationHandle* non è valido.</span><span class="sxs-lookup"><span data-stu-id="6c02f-122">The *EnumerationHandle* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="6c02f-123"><dt>**ERRORE \_ \_ altre \_ Route**</dt></span><span class="sxs-lookup"><span data-stu-id="6c02f-123"><dt>**ERROR\_NO\_MORE\_ROUTES**</dt></span></span> </dl>      | <span data-ttu-id="6c02f-124">Nell'enumerazione non sono presenti altre route.</span><span class="sxs-lookup"><span data-stu-id="6c02f-124">There are no more routes in the enumeration.</span></span><br/>                 |
| <dl> <span data-ttu-id="6c02f-125"><dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c02f-125"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="6c02f-126">Risorse insufficienti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6c02f-126">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6c02f-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c02f-127">Remarks</span></span>

<span data-ttu-id="6c02f-128">Sebbene le route non vengano restituite in un ordine particolare, ogni route nell'enumerazione viene restituita una sola volta.</span><span class="sxs-lookup"><span data-stu-id="6c02f-128">Although routes are not returned in any particular order, each route in the enumeration is returned only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c02f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c02f-129">Requirements</span></span>



| <span data-ttu-id="6c02f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c02f-130">Requirement</span></span> | <span data-ttu-id="6c02f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="6c02f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c02f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c02f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6c02f-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6c02f-133">None supported</span></span><br/>                                                          |
| <span data-ttu-id="6c02f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c02f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6c02f-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6c02f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6c02f-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="6c02f-136">End of server support</span></span><br/>    | <span data-ttu-id="6c02f-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c02f-137">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="6c02f-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c02f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c02f-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c02f-139"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c02f-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="6c02f-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c02f-141"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c02f-141"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="6c02f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6c02f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c02f-143"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c02f-143"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c02f-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c02f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c02f-145">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="6c02f-145">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="6c02f-146">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="6c02f-146">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="6c02f-147">**\_route IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="6c02f-147">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="6c02f-148">**\_Route IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="6c02f-148">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="6c02f-149">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="6c02f-149">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="6c02f-150">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="6c02f-150">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 





