---
title: Interfaccia IBackgroundCopyManager (Deliveryoptimization. h)
description: Crea processi di trasferimento, recupera un oggetto enumeratore che contiene i processi nella coda e recupera singoli processi dalla coda.
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- Interfaccia IBackgroundCopyManager
- Interfaccia IBackgroundCopyManager, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fa752398c0849c987e2a28b804e65a8361e15b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964342"
---
# <a name="ibackgroundcopymanager-interface"></a><span data-ttu-id="80067-105">Interfaccia IBackgroundCopyManager</span><span class="sxs-lookup"><span data-stu-id="80067-105">IBackgroundCopyManager interface</span></span>

<span data-ttu-id="80067-106">Crea processi di trasferimento, recupera un oggetto enumeratore che contiene i processi nella coda e recupera singoli processi dalla coda.</span><span class="sxs-lookup"><span data-stu-id="80067-106">Creates transfer jobs, retrieves an enumerator object that contains the jobs in the queue, and retrieves individual jobs from the queue.</span></span>

## <a name="members"></a><span data-ttu-id="80067-107">Membri</span><span class="sxs-lookup"><span data-stu-id="80067-107">Members</span></span>

<span data-ttu-id="80067-108">L'interfaccia **IBackgroundCopyManager** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="80067-108">The **IBackgroundCopyManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="80067-109">**IBackgroundCopyManager** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="80067-109">**IBackgroundCopyManager** also has these types of members:</span></span>

-   [<span data-ttu-id="80067-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="80067-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="80067-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="80067-111">Methods</span></span>

<span data-ttu-id="80067-112">L'interfaccia **IBackgroundCopyManager** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="80067-112">The **IBackgroundCopyManager** interface has these methods.</span></span>



| <span data-ttu-id="80067-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="80067-113">Method</span></span>                                                | <span data-ttu-id="80067-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80067-114">Description</span></span>                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="80067-115">**CreateJob**</span><span class="sxs-lookup"><span data-stu-id="80067-115">**CreateJob**</span></span>](ibackgroundcopymanager-createjob.md) | <span data-ttu-id="80067-116">Crea un processo di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="80067-116">Creates a transfer job.</span></span><br/>                   |
| [<span data-ttu-id="80067-117">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="80067-117">**GetJob**</span></span>](ibackgroundcopymanager-getjob.md)       | <span data-ttu-id="80067-118">Recupera un processo specificato dalla coda.</span><span class="sxs-lookup"><span data-stu-id="80067-118">Retrieves a specified job from the queue.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="80067-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80067-119">Requirements</span></span>



| <span data-ttu-id="80067-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="80067-120">Requirement</span></span> | <span data-ttu-id="80067-121">Valore</span><span class="sxs-lookup"><span data-stu-id="80067-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80067-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80067-122">Minimum supported client</span></span><br/> | <span data-ttu-id="80067-123">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="80067-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="80067-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80067-124">Minimum supported server</span></span><br/> | <span data-ttu-id="80067-125">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="80067-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="80067-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80067-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="80067-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="80067-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="80067-128">IDL</span><span class="sxs-lookup"><span data-stu-id="80067-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80067-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="80067-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="80067-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="80067-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="80067-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80067-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="80067-132">DLL</span><span class="sxs-lookup"><span data-stu-id="80067-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80067-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80067-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="80067-134">IID</span><span class="sxs-lookup"><span data-stu-id="80067-134">IID</span></span><br/>                      | <span data-ttu-id="80067-135">IID_IBackgroundCopyManager viene definito come 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="80067-135">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="80067-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80067-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80067-137">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="80067-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

