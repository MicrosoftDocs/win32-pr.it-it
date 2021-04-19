---
description: KTM definisce le seguenti maschere di accesso alle transazioni da utilizzare per l'apertura di una transazione.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Maschere di accesso alle transazioni (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b815bcb04a97dbd059c85c6c615a7d607bf77ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311130"
---
# <a name="transaction-access-masks"></a><span data-ttu-id="b1b97-103">Maschere di accesso alle transazioni</span><span class="sxs-lookup"><span data-stu-id="b1b97-103">Transaction Access Masks</span></span>

<span data-ttu-id="b1b97-104">KTM definisce le seguenti maschere di accesso alle transazioni da utilizzare per l'apertura di una transazione.</span><span class="sxs-lookup"><span data-stu-id="b1b97-104">KTM defines the following transaction access masks to be used when opening a transaction.</span></span>

<dl> <dt>

<span data-ttu-id="b1b97-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**\_informazioni query \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="b1b97-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**TRANSACTION\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b97-106">0x000001</span><span class="sxs-lookup"><span data-stu-id="b1b97-106">0x000001</span></span>
</dt> <dt>



<span data-ttu-id="b1b97-107">Il chiamante può eseguire query sulle informazioni sulle transazioni.</span><span class="sxs-lookup"><span data-stu-id="b1b97-107">The caller can query transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b97-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**\_informazioni sul set di transazioni \_**</span><span class="sxs-lookup"><span data-stu-id="b1b97-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**TRANSACTION\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b97-109">0x000002</span><span class="sxs-lookup"><span data-stu-id="b1b97-109">0x000002</span></span>
</dt> <dt>



<span data-ttu-id="b1b97-110">Il chiamante può impostare le informazioni sulle transazioni.</span><span class="sxs-lookup"><span data-stu-id="b1b97-110">The caller can set transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b97-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**integrazione della transazione \_**</span><span class="sxs-lookup"><span data-stu-id="b1b97-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**TRANSACTION\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b97-112">0x000004</span><span class="sxs-lookup"><span data-stu-id="b1b97-112">0x000004</span></span>
</dt> <dt>



<span data-ttu-id="b1b97-113">Il chiamante può integrarsi in questa transazione.</span><span class="sxs-lookup"><span data-stu-id="b1b97-113">The caller can enlist in this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b97-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**\_commit transazione**</span><span class="sxs-lookup"><span data-stu-id="b1b97-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**TRANSACTION\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b97-115">0x000008</span><span class="sxs-lookup"><span data-stu-id="b1b97-115">0x000008</span></span>
</dt> <dt>



<span data-ttu-id="b1b97-116">Il chiamante può eseguire il commit della transazione.</span><span class="sxs-lookup"><span data-stu-id="b1b97-116">The caller can commit this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b97-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**ROLLBACK delle transazioni \_**</span><span class="sxs-lookup"><span data-stu-id="b1b97-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**TRANSACTION\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b97-118">0x000010</span><span class="sxs-lookup"><span data-stu-id="b1b97-118">0x000010</span></span>
</dt> <dt>



<span data-ttu-id="b1b97-119">Il chiamante può eseguire il rollback della transazione.</span><span class="sxs-lookup"><span data-stu-id="b1b97-119">The caller can roll back this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b97-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**\_propagazione transazione**</span><span class="sxs-lookup"><span data-stu-id="b1b97-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**TRANSACTION\_PROPAGATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b97-121">0x000020</span><span class="sxs-lookup"><span data-stu-id="b1b97-121">0x000020</span></span>
</dt> <dt>



<span data-ttu-id="b1b97-122">Il chiamante può propagare questa transazione a un gestore di risorse superiore, ad esempio il Distributed Transaction Coordinator (DTC).</span><span class="sxs-lookup"><span data-stu-id="b1b97-122">The caller can propagate this transaction to a superior resource manager, such as the Distributed Transaction Coordinator (DTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b97-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**\_lettura generica transazione \_**</span><span class="sxs-lookup"><span data-stu-id="b1b97-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**TRANSACTION\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b97-124">0x120001</span><span class="sxs-lookup"><span data-stu-id="b1b97-124">0x120001</span></span>
</dt> <dt>



<span data-ttu-id="b1b97-125">Il chiamante dispone dei privilegi seguenti: **\_ diritti standard \_ letti**, **\_ \_ informazioni sulle query di transazione** e **sincronizzazione**.</span><span class="sxs-lookup"><span data-stu-id="b1b97-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ**, **TRANSACTION\_QUERY\_INFORMATION**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b97-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**\_scrittura generica transazione \_**</span><span class="sxs-lookup"><span data-stu-id="b1b97-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**TRANSACTION\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b97-127">0x12003E</span><span class="sxs-lookup"><span data-stu-id="b1b97-127">0x12003E</span></span>
</dt> <dt>



<span data-ttu-id="b1b97-128">Il chiamante dispone dei privilegi seguenti: **\_ \_ scrittura diritti standard**, **\_ \_ informazioni sui set di transazioni**, **\_ commit transazioni**, **\_ integrazione transazioni**, **\_ rollback transazioni**, **\_ propagazione transazioni** e **sincronizzazione**.</span><span class="sxs-lookup"><span data-stu-id="b1b97-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ENLIST**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b97-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**\_esecuzione generica transazione \_**</span><span class="sxs-lookup"><span data-stu-id="b1b97-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**TRANSACTION\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b97-130">0x120018</span><span class="sxs-lookup"><span data-stu-id="b1b97-130">0x120018</span></span>
</dt> <dt>



<span data-ttu-id="b1b97-131">Il chiamante dispone dei privilegi seguenti: **\_ diritti standard \_ Execute**, **\_ commit transazione**, **\_ rollback transazioni** e **sincronizzazione**.</span><span class="sxs-lookup"><span data-stu-id="b1b97-131">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ROLLBACK**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b97-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**\_accesso a tutte le transazioni \_**</span><span class="sxs-lookup"><span data-stu-id="b1b97-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**TRANSACTION\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b97-133">0x12003F</span><span class="sxs-lookup"><span data-stu-id="b1b97-133">0x12003F</span></span>
</dt> <dt>



<span data-ttu-id="b1b97-134">Il chiamante dispone del privilegio seguente: **\_ diritti standard \_ necessari**, **\_ \_ lettura generica** transazione **, \_ \_ scrittura** generica transazione e **\_ \_ esecuzione generica transazione**.</span><span class="sxs-lookup"><span data-stu-id="b1b97-134">The caller has the following privilege: **STANDARD\_RIGHTS\_REQUIRED**, **TRANSACTION\_GENERIC\_READ**, **TRANSACTION\_GENERIC\_WRITE**, and **TRANSACTION\_GENERIC\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1b97-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**\_diritti di \_ gestione \_ risorse transazioni**</span><span class="sxs-lookup"><span data-stu-id="b1b97-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1b97-136">0x120037</span><span class="sxs-lookup"><span data-stu-id="b1b97-136">0x120037</span></span>
</dt> <dt>



<span data-ttu-id="b1b97-137">Il chiamante dispone dei privilegi seguenti: **transazione \_ \_ lettura generica**, **\_ \_ scrittura diritti standard**, **\_ \_ informazioni sui set di transazioni**, **\_ rollback delle** transazioni, **\_ integrazione delle** transazioni, **\_ propagazione delle transazioni** e **sincronizzazione**.</span><span class="sxs-lookup"><span data-stu-id="b1b97-137">The caller has the following privileges: **TRANSACTION\_GENERIC\_READ**, **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_ENLIST**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1b97-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1b97-138">Remarks</span></span>

<span data-ttu-id="b1b97-139">È consigliabile che i gestori di risorse, durante l'integrazione in una transazione, specifichino **\_ \_ \_ i diritti di gestione delle risorse di transazione** durante l'apertura di una transazione.</span><span class="sxs-lookup"><span data-stu-id="b1b97-139">It is recommended that resource managers, when enlisting in a transaction, specify **TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS** when opening a transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1b97-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1b97-140">Requirements</span></span>



| <span data-ttu-id="b1b97-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1b97-141">Requirement</span></span> | <span data-ttu-id="b1b97-142">Valore</span><span class="sxs-lookup"><span data-stu-id="b1b97-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1b97-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1b97-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b1b97-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1b97-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="b1b97-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1b97-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b1b97-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1b97-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="b1b97-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1b97-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1b97-148"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1b97-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 




