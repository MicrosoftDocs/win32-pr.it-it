---
description: KTM definisce le seguenti maschere di accesso all'elenco da utilizzare per l'apertura di una gestione transazioni (TM).
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Maschere di accesso di gestione transazioni (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881210"
---
# <a name="transaction-manager-access-masks"></a><span data-ttu-id="ac0dc-103">Maschere di accesso di gestione transazioni</span><span class="sxs-lookup"><span data-stu-id="ac0dc-103">Transaction Manager Access Masks</span></span>

<span data-ttu-id="ac0dc-104">KTM definisce le seguenti maschere di accesso all'elenco da utilizzare per l'apertura di una gestione transazioni (TM).</span><span class="sxs-lookup"><span data-stu-id="ac0dc-104">KTM defines the following enlistment access masks to be used when opening a transaction manager (TM).</span></span>

<dl> <dt>

<span data-ttu-id="ac0dc-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**\_ \_ informazioni sulle query TRANSACTIONMANAGER**</span><span class="sxs-lookup"><span data-stu-id="ac0dc-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**TRANSACTIONMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac0dc-106">0x00001</span><span class="sxs-lookup"><span data-stu-id="ac0dc-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="ac0dc-107">Il chiamante può eseguire query sulle informazioni relative a questa TM.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-107">The caller can query information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac0dc-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**\_informazioni sui set di TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="ac0dc-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**TRANSACTIONMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac0dc-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="ac0dc-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="ac0dc-110">Il chiamante può impostare informazioni su questo TM.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-110">The caller can set information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac0dc-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**\_ripristino TRANSACTIONMANAGER**</span><span class="sxs-lookup"><span data-stu-id="ac0dc-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**TRANSACTIONMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac0dc-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="ac0dc-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="ac0dc-113">Il chiamante può recuperare questa TM.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-113">The caller can recover this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac0dc-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**ridenominazione TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="ac0dc-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**TRANSACTIONMANAGER\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac0dc-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="ac0dc-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="ac0dc-116">Il chiamante può rinominare un'istanza TM.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-116">The caller can rename a TM instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac0dc-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER \_ creare \_ RM**</span><span class="sxs-lookup"><span data-stu-id="ac0dc-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER\_CREATE\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac0dc-118">0x00010</span><span class="sxs-lookup"><span data-stu-id="ac0dc-118">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="ac0dc-119">Il chiamante può creare un gestore di risorse associato a questa TM.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-119">The caller can create a resource manager that is associated with this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac0dc-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**\_transazione di binding TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="ac0dc-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**TRANSACTIONMANAGER\_BIND\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac0dc-121">0x00020</span><span class="sxs-lookup"><span data-stu-id="ac0dc-121">0x00020</span></span>
</dt> <dt>



<span data-ttu-id="ac0dc-122">Questo valore è riservato.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-122">This value is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac0dc-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**\_lettura generica TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="ac0dc-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**TRANSACTIONMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac0dc-124">0x20001</span><span class="sxs-lookup"><span data-stu-id="ac0dc-124">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="ac0dc-125">Il chiamante dispone dei privilegi seguenti: **informazioni \_ sui diritti standard \_ Read** e **TRANSACTIONMANAGER \_ query \_**.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **TRANSACTIONMANAGER\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac0dc-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**\_scrittura generica TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="ac0dc-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**TRANSACTIONMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac0dc-127">0x2001E</span><span class="sxs-lookup"><span data-stu-id="ac0dc-127">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="ac0dc-128">Il chiamante presenta i privilegi seguenti: **standard \_ Rights \_ Write**, **TRANSACTIONMANAGER \_ set \_ Information**, **TRANSACTIONMANAGER \_ Recover**, **TRANSACTIONMANAGER \_ Rename** e **TRANSACTIONMANAGER \_ Create \_ RM**.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTIONMANAGER\_SET\_INFORMATION**, **TRANSACTIONMANAGER\_RECOVER**, **TRANSACTIONMANAGER\_RENAME**, and **TRANSACTIONMANAGER\_CREATE\_RM**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac0dc-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**\_esecuzione generica TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="ac0dc-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**TRANSACTIONMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac0dc-130">0x20000</span><span class="sxs-lookup"><span data-stu-id="ac0dc-130">0x20000</span></span>
</dt> <dt>



<span data-ttu-id="ac0dc-131">Il chiamante presenta il privilegio seguente: **\_ diritti standard \_ Execute**.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-131">The caller has the following privilege: **STANDARD\_RIGHTS\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac0dc-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER \_ tutti gli \_ accessi**</span><span class="sxs-lookup"><span data-stu-id="ac0dc-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac0dc-133">0xF003F</span><span class="sxs-lookup"><span data-stu-id="ac0dc-133">0xF003F</span></span>
</dt> <dt>



<span data-ttu-id="ac0dc-134">Questo valore imposta tutti i bit validi per un valore di accesso TM.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-134">This value sets all valid bits for a TM access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac0dc-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac0dc-135">Requirements</span></span>



| <span data-ttu-id="ac0dc-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac0dc-136">Requirement</span></span> | <span data-ttu-id="ac0dc-137">Valore</span><span class="sxs-lookup"><span data-stu-id="ac0dc-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac0dc-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac0dc-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ac0dc-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac0dc-139">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="ac0dc-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac0dc-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ac0dc-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac0dc-141">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="ac0dc-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac0dc-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac0dc-143"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac0dc-143"><dt>WinNT.h</dt></span></span> </dl> |



 

 




