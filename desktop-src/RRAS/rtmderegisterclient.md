---
title: Funzione RtmDeregisterClient (RTM. h)
description: La funzione RtmDeregisterClient Annulla la registrazione del client e libera le risorse associate al client.
ms.assetid: 5d04f276-86a7-4e63-8266-e93f0d6e5241
keywords:
- RAS funzione RtmDeregisterClient
topic_type:
- apiref
api_name:
- RtmDeregisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab1f56d3d65e13c083d8952f500cfba4638ab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400613"
---
# <a name="rtmderegisterclient-function"></a><span data-ttu-id="f61b9-104">RtmDeregisterClient (funzione)</span><span class="sxs-lookup"><span data-stu-id="f61b9-104">RtmDeregisterClient function</span></span>

<span data-ttu-id="f61b9-105">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f61b9-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="f61b9-106">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="f61b9-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="f61b9-107">La funzione **RtmDeregisterClient** Annulla la registrazione del client e libera le risorse associate al client.</span><span class="sxs-lookup"><span data-stu-id="f61b9-107">The **RtmDeregisterClient** function deregisters the client, and frees resources associated with the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="f61b9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f61b9-108">Syntax</span></span>


```C++
DWORD RtmDeregisterClient(
  _In_ HANDLE ClientHandle
);
```



## <a name="parameters"></a><span data-ttu-id="f61b9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f61b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f61b9-110">*ClientHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f61b9-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f61b9-111">Handle che identifica il client di cui annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="f61b9-111">Handle that identifies the client to deregister.</span></span> <span data-ttu-id="f61b9-112">Ottenere questo handle chiamando [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="f61b9-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f61b9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f61b9-113">Return value</span></span>

<span data-ttu-id="f61b9-114">Se la funzione ha esito positivo, il valore restituito non è un \_ errore.</span><span class="sxs-lookup"><span data-stu-id="f61b9-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="f61b9-115">Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="f61b9-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="f61b9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f61b9-116">Value</span></span>                                                                                                       | <span data-ttu-id="f61b9-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f61b9-117">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="f61b9-118"><dt>**ERRORE \_ handle non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f61b9-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="f61b9-119">Il parametro *ClientHandle* non è un handle valido.</span><span class="sxs-lookup"><span data-stu-id="f61b9-119">The *ClientHandle* parameter is not a valid handle.</span></span><br/> |
| <dl> <span data-ttu-id="f61b9-120"><dt>**ERRORE \_ senza \_ risorse di sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f61b9-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="f61b9-121">Risorse insufficienti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f61b9-121">Insufficient resources to carry out the operation.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="f61b9-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f61b9-122">Remarks</span></span>

<span data-ttu-id="f61b9-123">Questa funzione rimuove tutte le route aggiunte dal client.</span><span class="sxs-lookup"><span data-stu-id="f61b9-123">This function removes all routes that were added by the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="f61b9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f61b9-124">Requirements</span></span>



| <span data-ttu-id="f61b9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f61b9-125">Requirement</span></span> | <span data-ttu-id="f61b9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f61b9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f61b9-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f61b9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f61b9-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f61b9-128">None supported</span></span><br/>                                                          |
| <span data-ttu-id="f61b9-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f61b9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f61b9-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f61b9-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f61b9-131">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f61b9-131">End of server support</span></span><br/>    | <span data-ttu-id="f61b9-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f61b9-132">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="f61b9-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f61b9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f61b9-134"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="f61b9-134"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="f61b9-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="f61b9-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="f61b9-136"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f61b9-136"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="f61b9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f61b9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f61b9-138"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f61b9-138"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f61b9-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f61b9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f61b9-140">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="f61b9-140">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="f61b9-141">Funzioni di Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="f61b9-141">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="f61b9-142">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="f61b9-142">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





