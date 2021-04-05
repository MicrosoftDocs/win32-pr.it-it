---
description: KTM definisce le maschere di accesso all'elenco seguenti da usare all'apertura di un gestore di risorse.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Maschere di accesso Gestione risorse (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0f579a96ed80de100a5cb41cb9c4e9b847a060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131518"
---
# <a name="resource-manager-access-masks"></a><span data-ttu-id="57812-103">Maschere di accesso Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="57812-103">Resource Manager Access Masks</span></span>

<span data-ttu-id="57812-104">KTM definisce le maschere di accesso all'elenco seguenti da usare all'apertura di un gestore di risorse.</span><span class="sxs-lookup"><span data-stu-id="57812-104">KTM defines the following enlistment access masks to be used when opening a resource manager.</span></span>

<dl> <dt>

<span data-ttu-id="57812-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**\_ \_ informazioni sulle query RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="57812-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**RESOURCEMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57812-106">Il chiamante può eseguire una query per le informazioni di Resource Manager (RM).</span><span class="sxs-lookup"><span data-stu-id="57812-106">The caller can query for the resource manager (RM) information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57812-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**\_informazioni sui set di RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="57812-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**RESOURCEMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57812-108">Il chiamante può impostare le informazioni RM.</span><span class="sxs-lookup"><span data-stu-id="57812-108">The caller can set the RM information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57812-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**ripristino di RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="57812-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**RESOURCEMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57812-110">Il chiamante può recuperare il RM specificato.</span><span class="sxs-lookup"><span data-stu-id="57812-110">The caller can recover the specified RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57812-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**integrazione di RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="57812-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**RESOURCEMANAGER\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57812-112">Il chiamante può integrare un RM in una transazione.</span><span class="sxs-lookup"><span data-stu-id="57812-112">The caller can enlist an RM in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57812-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**\_notifica Get di RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="57812-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**RESOURCEMANAGER\_GET\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57812-114">Il chiamante può ricevere una notifica per un RM.</span><span class="sxs-lookup"><span data-stu-id="57812-114">The caller can receive a notification for an RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57812-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**\_lettura generica RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="57812-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**RESOURCEMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57812-116">Il chiamante dispone dei privilegi seguenti: \_ diritti \_ di lettura standard, \_ \_ informazioni sulle query ResourceManager e \_ ripristino ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="57812-116">The caller has the following privileges: STANDARD\_RIGHTS\_READ, RESOURCEMANAGER\_QUERY\_INFORMATION, and RESOURCEMANAGER\_RECOVER.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57812-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**\_scrittura generica RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="57812-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**RESOURCEMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57812-118">Il chiamante presenta i privilegi seguenti: STANDARD \_ Rights \_ Write, ResourceManager \_ set \_ Information, RESOURCEMANAGER \_ integrate e ResourceManager \_ get \_ Notification.</span><span class="sxs-lookup"><span data-stu-id="57812-118">The caller has the following privileges: STANDARD\_RIGHTS\_WRITE, RESOURCEMANAGER\_SET\_INFORMATION, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57812-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**\_esecuzione generica RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="57812-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**RESOURCEMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57812-120">Il chiamante dispone dei privilegi seguenti: \_ diritti standard \_ Execute, ResourceManager \_ integrate e ResourceManager \_ get \_ Notification.</span><span class="sxs-lookup"><span data-stu-id="57812-120">The caller has the following privileges: STANDARD\_RIGHTS\_EXECUTE, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="57812-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**accesso a RESOURCEMANAGER \_ All \_**</span><span class="sxs-lookup"><span data-stu-id="57812-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**RESOURCEMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="57812-122">Il chiamante dispone del privilegio seguente: \_ diritti standard \_ richiesti.</span><span class="sxs-lookup"><span data-stu-id="57812-122">The caller has the following privilege: STANDARD\_RIGHTS\_REQUIRED.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57812-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57812-123">Requirements</span></span>



| <span data-ttu-id="57812-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="57812-124">Requirement</span></span> | <span data-ttu-id="57812-125">Valore</span><span class="sxs-lookup"><span data-stu-id="57812-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="57812-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57812-126">Minimum supported client</span></span><br/> | <span data-ttu-id="57812-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57812-127">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="57812-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57812-128">Minimum supported server</span></span><br/> | <span data-ttu-id="57812-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57812-129">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="57812-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57812-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="57812-131"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="57812-131"><dt>WinNT.h</dt></span></span> </dl> |



 

 




