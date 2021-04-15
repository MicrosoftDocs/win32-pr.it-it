---
title: Funzione RtmBlockDeleteRoutes (RTM. h)
description: La funzione RtmBlockDeleteRoutes Elimina tutte le route nel subset specificato di route nella tabella.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- RAS funzione RtmBlockDeleteRoutes
topic_type:
- apiref
api_name:
- RtmBlockDeleteRoutes
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71090371fe8a84698b84b84391e5a782fdc636f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477512"
---
# <a name="rtmblockdeleteroutes-function"></a><span data-ttu-id="ef0dd-104">RtmBlockDeleteRoutes (funzione)</span><span class="sxs-lookup"><span data-stu-id="ef0dd-104">RtmBlockDeleteRoutes function</span></span>

<span data-ttu-id="ef0dd-105">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="ef0dd-106">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="ef0dd-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="ef0dd-107">La funzione **RtmBlockDeleteRoutes** Elimina tutte le route nel subset specificato di route nella tabella.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-107">The **RtmBlockDeleteRoutes** function deletes all routes in the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef0dd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef0dd-108">Syntax</span></span>


```C++
HANDLE RtmBlockDeleteRoutes(
  _In_ HANDLE ClientHandle,
  _In_ DWORD  EnumerationFlags,
  _In_ PVOID  CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="ef0dd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef0dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef0dd-110">*ClientHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef0dd-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef0dd-111">Handle che identifica il client e, di conseguenza, il protocollo di routing delle route da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-111">Handle that identifies the client, and therefore the routing protocol, of the routes to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="ef0dd-112">*EnumerationFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef0dd-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef0dd-113">Specifica le route da enumerare.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="ef0dd-114">Questo parametro limita il set di route eliminate a un subset definito dai seguenti flag e i valori dei membri corrispondenti della struttura a cui punta il parametro *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="ef0dd-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="ef0dd-115">I flag sono identici a quelli usati in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) , ad eccezione del fatto che RTM \_ solo le \_ \_ Route migliori sono ridondanti per **RtmBlockDeleteRoutes**.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) except that RTM\_ONLY\_BEST\_ROUTES is redundant for **RtmBlockDeleteRoutes**.</span></span> <span data-ttu-id="ef0dd-116">La designazione della migliore route viene regolata quando le route vengono eliminate, quindi la funzione Elimina tutte le route nel subset.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-116">The best-route designation is adjusted as routes are deleted, so the function eventually deletes all the routes in the subset.</span></span>

</dd> <dt>

<span data-ttu-id="ef0dd-117">*CriteriaRoute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef0dd-117">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef0dd-118">Puntatore a una struttura di route specifica della famiglia di protocolli [**( \_ \_ route IP RTM**](rtm-ip-route.md) o [**\_ \_ Route IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="ef0dd-118">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="ef0dd-119">I valori dei membri in questa struttura corrispondono ai flag specificati dal parametro *EnumerationFlags* .</span><span class="sxs-lookup"><span data-stu-id="ef0dd-119">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef0dd-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef0dd-120">Return value</span></span>

<span data-ttu-id="ef0dd-121">Se la funzione ha esito positivo, il valore restituito non è un \_ errore.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="ef0dd-122">Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="ef0dd-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ef0dd-123">Value</span></span>                                                                                                       | <span data-ttu-id="ef0dd-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef0dd-124">Description</span></span>                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef0dd-125"><dt>**ERRORE \_ Nessuna \_ Route**</dt></span><span class="sxs-lookup"><span data-stu-id="ef0dd-125"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="ef0dd-126">Non sono presenti route con i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-126">There are no routes that have the specified criteria.</span></span><br/>                                           |
| <dl> <span data-ttu-id="ef0dd-127"><dt>**ERRORE \_ handle non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef0dd-127"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="ef0dd-128">Il parametro *ClientHandle* non è valido.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-128">The *ClientHandle* parameter is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="ef0dd-129"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef0dd-129"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="ef0dd-130">Uno o più parametri di input non sono validi. ad esempio, i flag di enumerazione non sono validi.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-130">One or more of the input parameters is invalid, for example, the enumeration flags are invalid.</span></span><br/> |
| <dl> <span data-ttu-id="ef0dd-131"><dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef0dd-131"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="ef0dd-132">Risorse insufficienti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-132">There are insufficient resources to carry out the operation.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ef0dd-133"><dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ef0dd-133"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="ef0dd-134">Memoria insufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-134">There is insufficient memory to carry out the operation.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="ef0dd-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef0dd-135">Remarks</span></span>

<span data-ttu-id="ef0dd-136">La funzione genera messaggi di notifica appropriati a tutti i client registrati, incluso il chiamante.</span><span class="sxs-lookup"><span data-stu-id="ef0dd-136">The function generates appropriate notification messages to all registered clients including the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef0dd-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef0dd-137">Requirements</span></span>



| <span data-ttu-id="ef0dd-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef0dd-138">Requirement</span></span> | <span data-ttu-id="ef0dd-139">Valore</span><span class="sxs-lookup"><span data-stu-id="ef0dd-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef0dd-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef0dd-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ef0dd-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ef0dd-141">None supported</span></span><br/>                                                          |
| <span data-ttu-id="ef0dd-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef0dd-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ef0dd-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef0dd-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ef0dd-144">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ef0dd-144">End of server support</span></span><br/>    | <span data-ttu-id="ef0dd-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ef0dd-145">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="ef0dd-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef0dd-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef0dd-147"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef0dd-147"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef0dd-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="ef0dd-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef0dd-149"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef0dd-149"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="ef0dd-150">DLL</span><span class="sxs-lookup"><span data-stu-id="ef0dd-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef0dd-151"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef0dd-151"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef0dd-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef0dd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef0dd-153">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="ef0dd-153">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="ef0dd-154">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="ef0dd-154">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="ef0dd-155">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="ef0dd-155">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="ef0dd-156">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="ef0dd-156">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





