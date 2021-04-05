---
title: Funzione RtmGetRouteAge (RTM. h)
description: La funzione RtmGetRouteAge restituisce l'età di una route. L'età è il tempo, in secondi, da quando è stato creato o ultimo aggiornamento.
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- RAS funzione RtmGetRouteAge
topic_type:
- apiref
api_name:
- RtmGetRouteAge
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484bb5684fde974ce5fa704c0d0cca38c320851
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742183"
---
# <a name="rtmgetrouteage-function"></a><span data-ttu-id="c0a0e-105">RtmGetRouteAge (funzione)</span><span class="sxs-lookup"><span data-stu-id="c0a0e-105">RtmGetRouteAge function</span></span>

<span data-ttu-id="c0a0e-106">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c0a0e-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="c0a0e-107">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="c0a0e-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="c0a0e-108">La funzione **RtmGetRouteAge** restituisce l'età di una route.</span><span class="sxs-lookup"><span data-stu-id="c0a0e-108">The **RtmGetRouteAge** function returns the age of a route.</span></span> <span data-ttu-id="c0a0e-109">L'età è il tempo, in secondi, da quando è stato creato o ultimo aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c0a0e-109">The age is the time, in seconds, since it was created or last updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0a0e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0a0e-110">Syntax</span></span>


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="c0a0e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0a0e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0a0e-112">*Route* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0a0e-112">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0a0e-113">Puntatore a una struttura specifica della famiglia di protocolli che specifica i dati di route ottenuti di recente da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="c0a0e-113">Pointer to a protocol-family-specific structure that specifies route data recently obtained from the routing table manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0a0e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0a0e-114">Return value</span></span>

<span data-ttu-id="c0a0e-115">Il valore restituito è uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c0a0e-115">The return value is one of the following values.</span></span>



| <span data-ttu-id="c0a0e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c0a0e-116">Value</span></span>                                                                                   | <span data-ttu-id="c0a0e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0a0e-117">Description</span></span>                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0a0e-118"><dt>**Instradamento**</dt></span><span class="sxs-lookup"><span data-stu-id="c0a0e-118"><dt>**RouteAge**</dt></span></span> </dl> | <span data-ttu-id="c0a0e-119">Tempo in secondi dall'inizio della creazione o dell'ultimo aggiornamento di una route.</span><span class="sxs-lookup"><span data-stu-id="c0a0e-119">The time in seconds since a route was created or last updated.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="c0a0e-120"><dt>**INFINITE**</dt></span><span class="sxs-lookup"><span data-stu-id="c0a0e-120"><dt>**INFINITE**</dt></span></span> </dl> | <span data-ttu-id="c0a0e-121">Il contenuto della struttura di route non è valido.</span><span class="sxs-lookup"><span data-stu-id="c0a0e-121">The content of the route structure is invalid.</span></span> <span data-ttu-id="c0a0e-122">In questo caso, una chiamata a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' \_ errore \_ parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="c0a0e-122">In this case, a call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_PARAMETER.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0a0e-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0a0e-123">Remarks</span></span>

<span data-ttu-id="c0a0e-124">L'età della route viene calcolata dal \_ membro del timestamp RR della struttura a cui punta il parametro di *Route* .</span><span class="sxs-lookup"><span data-stu-id="c0a0e-124">The route age is computed from the RR\_TimeStamp member of the structure that is pointed to by the *Route* parameter.</span></span> <span data-ttu-id="c0a0e-125">Gestione tabelle di routing imposta il valore di questo membro quando viene aggiunta o aggiornata una route.</span><span class="sxs-lookup"><span data-stu-id="c0a0e-125">The routing table manager sets the value of this member when a route is added or updated.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0a0e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0a0e-126">Requirements</span></span>



| <span data-ttu-id="c0a0e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0a0e-127">Requirement</span></span> | <span data-ttu-id="c0a0e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c0a0e-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a0e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0a0e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c0a0e-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c0a0e-130">None supported</span></span><br/>                                                          |
| <span data-ttu-id="c0a0e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0a0e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c0a0e-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c0a0e-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c0a0e-133">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="c0a0e-133">End of server support</span></span><br/>    | <span data-ttu-id="c0a0e-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c0a0e-134">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="c0a0e-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0a0e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0a0e-136"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0a0e-136"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0a0e-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="c0a0e-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0a0e-138"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0a0e-138"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="c0a0e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c0a0e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0a0e-140"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0a0e-140"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0a0e-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0a0e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0a0e-142">Riferimento di gestione tabelle di routing versione \_ 1</span><span class="sxs-lookup"><span data-stu-id="c0a0e-142">Routing Table Manager Version\_1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="c0a0e-143">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="c0a0e-143">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="c0a0e-144">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="c0a0e-144">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="c0a0e-145">**\_route IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="c0a0e-145">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="c0a0e-146">**\_Route IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="c0a0e-146">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

