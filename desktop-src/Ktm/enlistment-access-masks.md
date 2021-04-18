---
description: KTM definisce le maschere di accesso all'elenco seguenti da usare per l'apertura delle integrazioni.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Maschere di accesso all'integrazione (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e4ebd67f93368215ebcdcd362595d0341adb52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318298"
---
# <a name="enlistment-access-masks"></a><span data-ttu-id="a1aa9-103">Maschere di accesso all'elenco</span><span class="sxs-lookup"><span data-stu-id="a1aa9-103">Enlistment Access Masks</span></span>

<span data-ttu-id="a1aa9-104">KTM definisce le maschere di accesso all'elenco seguenti da usare per l'apertura delle integrazioni.</span><span class="sxs-lookup"><span data-stu-id="a1aa9-104">KTM defines the following enlistment access masks to be used when opening enlistments.</span></span>

<dl> <dt>

<span data-ttu-id="a1aa9-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**\_informazioni sulle query di integrazione \_**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**ENLISTMENT\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1aa9-106">0x00001</span><span class="sxs-lookup"><span data-stu-id="a1aa9-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="a1aa9-107">Il chiamante può eseguire una query su KTM per ottenere informazioni sull'integrazione.</span><span class="sxs-lookup"><span data-stu-id="a1aa9-107">The caller can query KTM for information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a1aa9-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**\_informazioni sui set di integrazione \_**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**ENLISTMENT\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1aa9-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="a1aa9-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="a1aa9-110">Il chiamante può impostare informazioni sull'integrazione.</span><span class="sxs-lookup"><span data-stu-id="a1aa9-110">The caller can set information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a1aa9-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**ripristino dell'elenco \_**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**ENLISTMENT\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1aa9-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="a1aa9-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="a1aa9-113">Il chiamante può recuperare un'integrazione.</span><span class="sxs-lookup"><span data-stu-id="a1aa9-113">The caller can recover an enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a1aa9-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**\_diritti subordinati di integrazione \_**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**ENLISTMENT\_SUBORDINATE\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1aa9-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="a1aa9-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="a1aa9-116">Il chiamante può completare le azioni eseguite da un gestore di risorse per conto della transazione.</span><span class="sxs-lookup"><span data-stu-id="a1aa9-116">The caller can complete actions that a resource manager does on behalf of the transaction.</span></span> <span data-ttu-id="a1aa9-117">Di seguito è riportato un elenco di azioni:</span><span class="sxs-lookup"><span data-stu-id="a1aa9-117">The following is a list of actions:</span></span>

-   [<span data-ttu-id="a1aa9-118">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-118">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="a1aa9-119">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-119">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="a1aa9-120">**PrePrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-120">**PrePrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [<span data-ttu-id="a1aa9-121">**RollbackComplete**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-121">**RollbackComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [<span data-ttu-id="a1aa9-122">**ReadOnlyEnlistment**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-122">**ReadOnlyEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [<span data-ttu-id="a1aa9-123">**RollbackEnlistment**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-123">**RollbackEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [<span data-ttu-id="a1aa9-124">**SinglePhaseReject**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-124">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span data-ttu-id="a1aa9-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**diritti di integrazione \_ superiore \_**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**ENLISTMENT\_SUPERIOR\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1aa9-126">0x00010</span><span class="sxs-lookup"><span data-stu-id="a1aa9-126">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="a1aa9-127">Il chiamante può integrarsi nella transazione come gestione transazioni superiore.</span><span class="sxs-lookup"><span data-stu-id="a1aa9-127">The caller can enlist in the transaction as a superior transaction manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a1aa9-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**\_lettura generale dell'elenco \_**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**ENLISTMENT\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1aa9-129">0x20001</span><span class="sxs-lookup"><span data-stu-id="a1aa9-129">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="a1aa9-130">Il chiamante dispone dei privilegi seguenti: **\_ \_ informazioni sulle query** di lettura e integrazione **\_ dei diritti \_ standard** .</span><span class="sxs-lookup"><span data-stu-id="a1aa9-130">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **ENLISTMENT\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a1aa9-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**\_scrittura generica di integrazione \_**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**ENLISTMENT\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1aa9-132">0x2001E</span><span class="sxs-lookup"><span data-stu-id="a1aa9-132">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="a1aa9-133">Il chiamante dispone dei privilegi seguenti: **\_ \_ scrittura dei diritti standard**, **\_ \_ informazioni sui set di integrazione** e **\_ ripristino dell'integrazione**.</span><span class="sxs-lookup"><span data-stu-id="a1aa9-133">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **ENLISTMENT\_SET\_INFORMATION**, and **ENLISTMENT\_RECOVER**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a1aa9-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**\_esecuzione generica dell'elenco \_**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**ENLISTMENT\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1aa9-135">0x2001C</span><span class="sxs-lookup"><span data-stu-id="a1aa9-135">0x2001C</span></span>
</dt> <dt>



<span data-ttu-id="a1aa9-136">Il chiamante dispone dei privilegi seguenti: **diritti \_ standard \_ esecuzione**, **\_ ripristino dell'integrazione** e **\_ \_ diritti subordinati di integrazione**.</span><span class="sxs-lookup"><span data-stu-id="a1aa9-136">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **ENLISTMENT\_RECOVER**, and **ENLISTMENT\_SUBORDINATE\_RIGHTS**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a1aa9-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**ELENCO \_ tutti gli \_ accessi**</span><span class="sxs-lookup"><span data-stu-id="a1aa9-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**ENLISTMENT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1aa9-138">0xF001F</span><span class="sxs-lookup"><span data-stu-id="a1aa9-138">0xF001F</span></span>
</dt> <dt>



<span data-ttu-id="a1aa9-139">Questo valore imposta tutti i bit validi per un valore di accesso all'elenco.</span><span class="sxs-lookup"><span data-stu-id="a1aa9-139">This value sets all valid bits for an enlistment access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1aa9-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1aa9-140">Requirements</span></span>



| <span data-ttu-id="a1aa9-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1aa9-141">Requirement</span></span> | <span data-ttu-id="a1aa9-142">Valore</span><span class="sxs-lookup"><span data-stu-id="a1aa9-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1aa9-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1aa9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a1aa9-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1aa9-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="a1aa9-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1aa9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a1aa9-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1aa9-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="a1aa9-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1aa9-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1aa9-148"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1aa9-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 




