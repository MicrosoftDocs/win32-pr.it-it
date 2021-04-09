---
title: Interfaccia IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Usare questa interfaccia per eseguire una query o impostare diversi comportamenti facoltativi di un processo.
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- Interfaccia IBackgroundCopyJob5
- Interfaccia IBackgroundCopyJob5, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e76898f7bbfe4d4dc34aec035b842e6671091630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120867"
---
# <a name="ibackgroundcopyjob5-interface"></a><span data-ttu-id="2e6ac-105">Interfaccia IBackgroundCopyJob5</span><span class="sxs-lookup"><span data-stu-id="2e6ac-105">IBackgroundCopyJob5 interface</span></span>

<span data-ttu-id="2e6ac-106">Usare questa interfaccia per eseguire una query o impostare diversi comportamenti facoltativi di un processo.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-106">Use this interface to query or set several optional behaviors of a job.</span></span>

<span data-ttu-id="2e6ac-107">Per ottenere questa interfaccia, chiamare il metodo **Metodo ibackgroundcopyjob:: QueryInterface** usando `__uuidof(IBackgroundCopyJob5)` come identificatore di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-107">To get this interface, call the **IBackgroundCopyJob::QueryInterface** method using `__uuidof(IBackgroundCopyJob5)` as the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="2e6ac-108">Membri</span><span class="sxs-lookup"><span data-stu-id="2e6ac-108">Members</span></span>

<span data-ttu-id="2e6ac-109">L'interfaccia **IBackgroundCopyJob5** eredita da [**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md).</span><span class="sxs-lookup"><span data-stu-id="2e6ac-109">The **IBackgroundCopyJob5** interface inherits from [**IBackgroundCopyJob**](ibackgroundcopyjob-.md).</span></span> <span data-ttu-id="2e6ac-110">**IBackgroundCopyJob5** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2e6ac-110">**IBackgroundCopyJob5** also has these types of members:</span></span>

-   [<span data-ttu-id="2e6ac-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="2e6ac-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2e6ac-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="2e6ac-112">Methods</span></span>

<span data-ttu-id="2e6ac-113">L'interfaccia **IBackgroundCopyJob5** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-113">The **IBackgroundCopyJob5** interface has these methods.</span></span>



| <span data-ttu-id="2e6ac-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="2e6ac-114">Method</span></span>                                                 | <span data-ttu-id="2e6ac-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e6ac-115">Description</span></span>                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="2e6ac-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="2e6ac-116">**GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md) | <span data-ttu-id="2e6ac-117">Metodo generico per ottenere le proprietà del processo.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-117">A generic method for getting DO job properties.</span></span><br/> |
| [<span data-ttu-id="2e6ac-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="2e6ac-118">**SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md) | <span data-ttu-id="2e6ac-119">Metodo generico per l'impostazione delle proprietà del processo.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-119">A generic method for setting DO job properties.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2e6ac-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e6ac-120">Requirements</span></span>



| <span data-ttu-id="2e6ac-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e6ac-121">Requirement</span></span> | <span data-ttu-id="2e6ac-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2e6ac-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e6ac-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e6ac-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2e6ac-124">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e6ac-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2e6ac-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e6ac-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2e6ac-126">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2e6ac-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2e6ac-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e6ac-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e6ac-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e6ac-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e6ac-129">IDL</span><span class="sxs-lookup"><span data-stu-id="2e6ac-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e6ac-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e6ac-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2e6ac-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="2e6ac-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e6ac-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e6ac-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2e6ac-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2e6ac-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e6ac-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e6ac-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2e6ac-135">IID</span><span class="sxs-lookup"><span data-stu-id="2e6ac-135">IID</span></span><br/>                      | <span data-ttu-id="2e6ac-136">IID_IBackgroundCopyJob5 viene definito come E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="2e6ac-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="2e6ac-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e6ac-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e6ac-138">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="2e6ac-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





