---
title: Funzione RtmCloseEnumerationHandle (RTM. h)
description: RtmCloseEnumerationHandle termina un'enumerazione specificata e libera le risorse associate.
ms.assetid: 8daea42f-4304-4749-9894-d37f6ba733da
keywords:
- RAS funzione RtmCloseEnumerationHandle
topic_type:
- apiref
api_name:
- RtmCloseEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5adb47d40cb1300305c7ff6f9bb6f1c3c716f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048509"
---
# <a name="rtmcloseenumerationhandle-function"></a><span data-ttu-id="4c767-104">RtmCloseEnumerationHandle (funzione)</span><span class="sxs-lookup"><span data-stu-id="4c767-104">RtmCloseEnumerationHandle function</span></span>

<span data-ttu-id="4c767-105">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4c767-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="4c767-106">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="4c767-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="4c767-107">**RtmCloseEnumerationHandle** termina un'enumerazione specificata e libera le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="4c767-107">The **RtmCloseEnumerationHandle** terminates a specified enumeration and frees the associated resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c767-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c767-108">Syntax</span></span>


```C++
DWORD RtmCloseEnumerationHandle(
  _In_ HANDLE EnumerationHandle
);
```



## <a name="parameters"></a><span data-ttu-id="4c767-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c767-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c767-110">*EnumerationHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c767-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c767-111">Handle per l'enumerazione da terminare.</span><span class="sxs-lookup"><span data-stu-id="4c767-111">Handle to the enumeration to terminate.</span></span> <span data-ttu-id="4c767-112">Ottenere questo handle chiamando [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="4c767-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c767-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c767-113">Return value</span></span>

<span data-ttu-id="4c767-114">Se la funzione ha esito positivo, il valore restituito non è un \_ errore.</span><span class="sxs-lookup"><span data-stu-id="4c767-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="4c767-115">Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="4c767-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="4c767-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4c767-116">Value</span></span>                                                                                                       | <span data-ttu-id="4c767-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c767-117">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c767-118"><dt>**ERRORE \_ handle non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4c767-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="4c767-119">Il parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="4c767-119">The parameter is not valid.</span></span><br/>                                  |
| <dl> <span data-ttu-id="4c767-120"><dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4c767-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="4c767-121">Risorse insufficienti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="4c767-121">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4c767-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c767-122">Requirements</span></span>



| <span data-ttu-id="4c767-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c767-123">Requirement</span></span> | <span data-ttu-id="4c767-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4c767-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c767-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c767-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4c767-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4c767-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="4c767-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c767-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4c767-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4c767-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4c767-129">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4c767-129">End of server support</span></span><br/>    | <span data-ttu-id="4c767-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4c767-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="4c767-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c767-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c767-132"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c767-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c767-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c767-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c767-134"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c767-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="4c767-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4c767-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c767-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c767-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c767-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c767-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c767-138">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="4c767-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="4c767-139">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="4c767-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="4c767-140">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="4c767-140">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="4c767-141">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="4c767-141">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 

 





