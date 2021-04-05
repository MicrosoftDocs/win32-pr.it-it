---
title: Funzione RtmGetNetworkCount (RTM. h)
description: La funzione RtmGetNetworkCount Recupera il numero di reti a cui sono indirizzate le route di gestione tabelle di routing.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- RAS funzione RtmGetNetworkCount
topic_type:
- apiref
api_name:
- RtmGetNetworkCount
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab4babd1e9d98071b2fbe6ab30c9b92d4a23f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741410"
---
# <a name="rtmgetnetworkcount-function"></a><span data-ttu-id="0aefd-104">RtmGetNetworkCount (funzione)</span><span class="sxs-lookup"><span data-stu-id="0aefd-104">RtmGetNetworkCount function</span></span>

<span data-ttu-id="0aefd-105">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0aefd-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="0aefd-106">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="0aefd-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="0aefd-107">La funzione **RtmGetNetworkCount** Recupera il numero di reti a cui sono indirizzate le route di gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="0aefd-107">The **RtmGetNetworkCount** function retrieves the number of networks to which the routing table manager has routes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aefd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0aefd-108">Syntax</span></span>


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a><span data-ttu-id="0aefd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0aefd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aefd-110">*ProtocolFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0aefd-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aefd-111">Specifica per quale tipo di rete ottenere informazioni sulla Route, ad esempio IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="0aefd-111">Specifies for which type of network to obtain route information, for example, IP or IPX.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aefd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0aefd-112">Return value</span></span>

<span data-ttu-id="0aefd-113">Se la funzione ha esito positivo, il valore restituito è il conteggio della rete, il numero di reti note ai protocolli di routing della famiglia di protocolli specificata.</span><span class="sxs-lookup"><span data-stu-id="0aefd-113">If the function succeeds, the return value is the network count, the number of networks known to the routing protocols of the specified protocol family.</span></span>

<span data-ttu-id="0aefd-114">Se il valore restituito è zero, non sono disponibili route o l'operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="0aefd-114">If the return value is zero, either no routes are available, or the operation failed.</span></span> <span data-ttu-id="0aefd-115">Chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="0aefd-115">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="0aefd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0aefd-116">Value</span></span>                                                                                                    | <span data-ttu-id="0aefd-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0aefd-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0aefd-118"><dt>**Nessun \_ errore**</dt></span><span class="sxs-lookup"><span data-stu-id="0aefd-118"><dt>**NO\_ERROR**</dt></span></span> </dl>                 | <span data-ttu-id="0aefd-119">L'operazione è stata completata, ma non sono disponibili route.</span><span class="sxs-lookup"><span data-stu-id="0aefd-119">The operation succeeded, but no routes are available.</span></span><br/>                                             |
| <dl> <span data-ttu-id="0aefd-120"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0aefd-120"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="0aefd-121">Il valore del parametro *ProtocolFamily* non corrisponde ad alcuna famiglia di protocolli installata.</span><span class="sxs-lookup"><span data-stu-id="0aefd-121">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0aefd-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0aefd-122">Requirements</span></span>



| <span data-ttu-id="0aefd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aefd-123">Requirement</span></span> | <span data-ttu-id="0aefd-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0aefd-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0aefd-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aefd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0aefd-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0aefd-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="0aefd-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aefd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0aefd-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0aefd-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0aefd-129">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="0aefd-129">End of server support</span></span><br/>    | <span data-ttu-id="0aefd-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0aefd-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="0aefd-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0aefd-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aefd-132"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aefd-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="0aefd-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="0aefd-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="0aefd-134"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0aefd-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="0aefd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0aefd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0aefd-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0aefd-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aefd-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0aefd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aefd-138">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="0aefd-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="0aefd-139">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="0aefd-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="0aefd-140">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="0aefd-140">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="0aefd-141">Identificatori della famiglia di protocolli RTMv1</span><span class="sxs-lookup"><span data-stu-id="0aefd-141">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

