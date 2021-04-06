---
title: Funzione RtmRegisterClient (RTM. h)
description: La funzione RtmRegisterClient registra un client come gestore del protocollo specificato. Stabilisce un meccanismo di notifica delle modifiche della route per il client e imposta le opzioni del protocollo.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- RAS funzione RtmRegisterClient
topic_type:
- apiref
api_name:
- RtmRegisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 564f47e68fd6cdce3d5437fe184bac1ed74d8322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743111"
---
# <a name="rtmregisterclient-function"></a><span data-ttu-id="facad-105">RtmRegisterClient (funzione)</span><span class="sxs-lookup"><span data-stu-id="facad-105">RtmRegisterClient function</span></span>

<span data-ttu-id="facad-106">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="facad-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="facad-107">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="facad-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="facad-108">La funzione **RtmRegisterClient** registra un client come gestore del protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="facad-108">The **RtmRegisterClient** function registers a client as a handler of the specified protocol.</span></span> <span data-ttu-id="facad-109">Stabilisce un meccanismo di notifica delle modifiche della route per il client e imposta le opzioni del protocollo.</span><span class="sxs-lookup"><span data-stu-id="facad-109">It establishes a route change notification mechanism for the client, and sets protocol options.</span></span>

## <a name="syntax"></a><span data-ttu-id="facad-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="facad-110">Syntax</span></span>


```C++
HANDLE RtmRegisterClient(
  _In_ DWORD  ProtocolFamily,
  _In_ DWORD  RoutingProtocol,
  _In_ HANDLE ChangeEvent,
  _In_ DWORD  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="facad-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="facad-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="facad-112">*ProtocolFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="facad-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="facad-113">Specifica la famiglia di protocolli del protocollo di routing da registrare.</span><span class="sxs-lookup"><span data-stu-id="facad-113">Specifies the protocol family of the routing protocol to register.</span></span>

</dd> <dt>

<span data-ttu-id="facad-114">*RoutingProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="facad-114">*RoutingProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="facad-115">Specifica l'identificatore del protocollo di routing, uguale a quello utilizzato per la registrazione con gestione router.</span><span class="sxs-lookup"><span data-stu-id="facad-115">Specifies the routing protocol identifier, the same as that used when registering with the router manager.</span></span> <span data-ttu-id="facad-116">Vedere [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).</span><span class="sxs-lookup"><span data-stu-id="facad-116">See [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).</span></span>

</dd> <dt>

<span data-ttu-id="facad-117">*ChangeEvent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="facad-117">*ChangeEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="facad-118">Specifica che è stata modificata una route migliore a una rete nella tabella.</span><span class="sxs-lookup"><span data-stu-id="facad-118">Specifies that a best route to a network in the table has changed.</span></span> <span data-ttu-id="facad-119">Il servizio di gestione delle tabelle di routing segnala questo evento dopo una modifica al percorso migliore per qualsiasi rete nella tabella.</span><span class="sxs-lookup"><span data-stu-id="facad-119">The routing table manager signals this event after a change to the best route to any network in the table.</span></span> <span data-ttu-id="facad-120">Per ulteriori informazioni sulla notifica di modifica di route, vedere [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) .</span><span class="sxs-lookup"><span data-stu-id="facad-120">See [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) for more information about route-change notification.</span></span>

<span data-ttu-id="facad-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="facad-121">This parameter is optional.</span></span> <span data-ttu-id="facad-122">Se il chiamante specifica **null** per questo parametro, il servizio di gestione delle tabelle di routing non comunica al client le modifiche nello stato della route migliore.</span><span class="sxs-lookup"><span data-stu-id="facad-122">If the caller specifies **NULL** for this parameter, the routing table manager does not notify the client of changes in best route status.</span></span>

</dd> <dt>

<span data-ttu-id="facad-123">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="facad-123">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="facad-124">Specifica le opzioni varie per la gestione speciale del protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="facad-124">Specifies miscellaneous options for special handling of the routing protocol.</span></span> <span data-ttu-id="facad-125">Il valore seguente è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="facad-125">The following value is currently supported.</span></span>



| <span data-ttu-id="facad-126">Flags</span><span class="sxs-lookup"><span data-stu-id="facad-126">Flags</span></span>                                                                                                                                                                                               | <span data-ttu-id="facad-127">Significato</span><span class="sxs-lookup"><span data-stu-id="facad-127">Meaning</span></span>                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <span data-ttu-id="facad-128"><dt>**\_ \_ Single route del protocollo RTM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="facad-128"><dt>**RTM\_PROTOCOL\_SINGLE\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="facad-129">Gestione tabelle di routing mantiene solo una route per rete di destinazione per il protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="facad-129">The routing table manager keeps only one route per destination network for the routing protocol.</span></span> <span data-ttu-id="facad-130">In altre parole, gestione tabelle di routing sostituisce le voci di route con gli stessi numeri di rete di destinazione invece di aggiungerne di nuove.</span><span class="sxs-lookup"><span data-stu-id="facad-130">In other words, the routing table manager replaces route entries that have the same destination network numbers instead of adding new ones.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="facad-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="facad-131">Return value</span></span>

<span data-ttu-id="facad-132">In esito positivo, restituisce un valore di **handle** che identifica il client nelle chiamate successive a gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="facad-132">On successful return, a **HANDLE** value that identifies the client in subsequent calls to the routing table manager.</span></span>

<span data-ttu-id="facad-133">Un handle **null** indica che Gestione tabelle di routing non è stato in grado di registrare il client.</span><span class="sxs-lookup"><span data-stu-id="facad-133">A **NULL** handle indicates that the routing table manager was unable to register the client.</span></span> <span data-ttu-id="facad-134">Chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere la causa dell'errore.</span><span class="sxs-lookup"><span data-stu-id="facad-134">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain the reason for the failure.</span></span>



| <span data-ttu-id="facad-135">Valore</span><span class="sxs-lookup"><span data-stu-id="facad-135">Value</span></span>                                                                                                         | <span data-ttu-id="facad-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="facad-136">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="facad-137"><dt>**il \_ client di errore \_ \_ esiste già**</dt></span><span class="sxs-lookup"><span data-stu-id="facad-137"><dt>**ERROR\_CLIENT\_ALREADY\_EXISTS**</dt></span></span> </dl> | <span data-ttu-id="facad-138">Un altro client è già registrato per gestire il protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="facad-138">Another client has already registered to handle the specified protocol.</span></span><br/>              |
| <dl> <span data-ttu-id="facad-139"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="facad-139"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>      | <span data-ttu-id="facad-140">La famiglia di protocolli specificata non è supportata o il parametro *Flags* non è valido.</span><span class="sxs-lookup"><span data-stu-id="facad-140">The specified protocol family is not supported, or the *Flags* parameter is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="facad-141"><dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="facad-141"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl>   | <span data-ttu-id="facad-142">Risorse insufficienti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="facad-142">Insufficient resources to carry out the operation.</span></span><br/>                                   |
| <dl> <span data-ttu-id="facad-143"><dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="facad-143"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>     | <span data-ttu-id="facad-144">Memoria insufficiente per allocare strutture di dati per il client.</span><span class="sxs-lookup"><span data-stu-id="facad-144">Insufficient memory to allocate data structures for the client.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="facad-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="facad-145">Requirements</span></span>



| <span data-ttu-id="facad-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="facad-146">Requirement</span></span> | <span data-ttu-id="facad-147">Valore</span><span class="sxs-lookup"><span data-stu-id="facad-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="facad-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="facad-148">Minimum supported client</span></span><br/> | <span data-ttu-id="facad-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="facad-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="facad-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="facad-150">Minimum supported server</span></span><br/> | <span data-ttu-id="facad-151">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="facad-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="facad-152">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="facad-152">End of server support</span></span><br/>    | <span data-ttu-id="facad-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="facad-153">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="facad-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="facad-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="facad-155"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="facad-155"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="facad-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="facad-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="facad-157"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="facad-157"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="facad-158">DLL</span><span class="sxs-lookup"><span data-stu-id="facad-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="facad-159"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="facad-159"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="facad-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="facad-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="facad-161">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="facad-161">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="facad-162">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="facad-162">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="facad-163">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="facad-163">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="facad-164">**RegisterProtocol**</span><span class="sxs-lookup"><span data-stu-id="facad-164">**RegisterProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[<span data-ttu-id="facad-165">Identificatori della famiglia di protocolli RTMv1</span><span class="sxs-lookup"><span data-stu-id="facad-165">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[<span data-ttu-id="facad-166">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="facad-166">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> <dt>

[<span data-ttu-id="facad-167">**RtmDeregisterClient**</span><span class="sxs-lookup"><span data-stu-id="facad-167">**RtmDeregisterClient**</span></span>](rtmderegisterclient.md)
</dt> </dl>

 

