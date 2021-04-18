---
title: Interfaccia IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Utilizzare l'interfaccia IEnumBackgroundCopyFiles per enumerare i file contenuti in un processo. Per ottenere un puntatore a interfaccia IEnumBackgroundCopyFiles, chiamare il metodo Metodo ibackgroundcopyjob EnumFiles.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- Interfaccia IEnumBackgroundCopyFiles
- Interfaccia IEnumBackgroundCopyFiles, descritta
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e46e94139a0c82e6c5b45f9397d76de8b4fdb43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301591"
---
# <a name="ienumbackgroundcopyfiles-interface"></a><span data-ttu-id="63327-106">Interfaccia IEnumBackgroundCopyFiles</span><span class="sxs-lookup"><span data-stu-id="63327-106">IEnumBackgroundCopyFiles interface</span></span>

<span data-ttu-id="63327-107">Utilizzare l'interfaccia **IEnumBackgroundCopyFiles** per enumerare i file contenuti in un processo.</span><span class="sxs-lookup"><span data-stu-id="63327-107">Use the **IEnumBackgroundCopyFiles** interface to enumerate the files that a job contains.</span></span> <span data-ttu-id="63327-108">Per ottenere un puntatore a interfaccia **IEnumBackgroundCopyFiles** , chiamare il metodo [**Metodo ibackgroundcopyjob:: EnumFiles**](ibackgroundcopyjob-enumfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="63327-108">To get an **IEnumBackgroundCopyFiles** interface pointer, call the [**IBackgroundCopyJob::EnumFiles**](ibackgroundcopyjob-enumfiles.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="63327-109">Membri</span><span class="sxs-lookup"><span data-stu-id="63327-109">Members</span></span>

<span data-ttu-id="63327-110">L'interfaccia **IEnumBackgroundCopyFiles** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="63327-110">The **IEnumBackgroundCopyFiles** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="63327-111">**IEnumBackgroundCopyFiles** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="63327-111">**IEnumBackgroundCopyFiles** also has these types of members:</span></span>

-   [<span data-ttu-id="63327-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="63327-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="63327-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="63327-113">Methods</span></span>

<span data-ttu-id="63327-114">L'interfaccia **IEnumBackgroundCopyFiles** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="63327-114">The **IEnumBackgroundCopyFiles** interface has these methods.</span></span>



| <span data-ttu-id="63327-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="63327-115">Method</span></span>                                                | <span data-ttu-id="63327-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63327-116">Description</span></span>                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="63327-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="63327-117">**GetCount**</span></span>](ienumbackgroundcopyfiles-getcount.md) | <span data-ttu-id="63327-118">Recupera il numero di elementi nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="63327-118">Retrieves the number of items in the enumeration.</span></span><br/>                  |
| [<span data-ttu-id="63327-119">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="63327-119">**Next**</span></span>](ienumbackgroundcopyfiles-next.md)         | <span data-ttu-id="63327-120">Recupera un determinato numero di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="63327-120">Retrieves a specified number of items in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="63327-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="63327-121">**Reset**</span></span>](ienumbackgroundcopyfiles-reset.md)       | <span data-ttu-id="63327-122">Riporta all'inizio la sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="63327-122">Resets the enumeration sequence to the beginning.</span></span><br/>                  |
| [<span data-ttu-id="63327-123">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="63327-123">**Skip**</span></span>](ienumbackgroundcopyfiles-skip.md)         | <span data-ttu-id="63327-124">Ignora un determinato numero di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="63327-124">Skips a specified number of items in the enumeration sequence.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="63327-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63327-125">Requirements</span></span>



| <span data-ttu-id="63327-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="63327-126">Requirement</span></span> | <span data-ttu-id="63327-127">Valore</span><span class="sxs-lookup"><span data-stu-id="63327-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63327-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63327-128">Minimum supported client</span></span><br/> | <span data-ttu-id="63327-129">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="63327-129">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="63327-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63327-130">Minimum supported server</span></span><br/> | <span data-ttu-id="63327-131">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="63327-131">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="63327-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63327-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="63327-133"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="63327-133"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="63327-134">IDL</span><span class="sxs-lookup"><span data-stu-id="63327-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63327-135"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63327-135"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="63327-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="63327-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="63327-137"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63327-137"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="63327-138">DLL</span><span class="sxs-lookup"><span data-stu-id="63327-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63327-139"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63327-139"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="63327-140">IID</span><span class="sxs-lookup"><span data-stu-id="63327-140">IID</span></span><br/>                      | <span data-ttu-id="63327-141">IID_IEnumBackgroundCopyFiles viene definito come CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="63327-141">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="63327-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63327-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63327-143">**Metodo ibackgroundcopyjob:: EnumFiles**</span><span class="sxs-lookup"><span data-stu-id="63327-143">**IBackgroundCopyJob::EnumFiles**</span></span>](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

