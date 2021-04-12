---
description: Rimuove l'elemento gestito specificato come membro del \_ COLLECTIONOFMSES CIM con l'identificatore specificato. Questa operazione avrà esito positivo anche se l'oggetto con tale identificatore non è presente.
ms.assetid: 641535f0-ce71-4f57-a4e1-4775b3bb2374
title: Metodo RemoveMemberById della classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMemberById
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31c30d8698b16ac9bf128aa13ab80a64f09a40c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234203"
---
# <a name="removememberbyid-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="1a412-104">Metodo RemoveMemberById della classe MSVM \_ CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="1a412-104">RemoveMemberById method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="1a412-105">Rimuove l'elemento gestito specificato come membro del [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="1a412-105">Removes the specified managed element as a member of the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) with the given identifier.</span></span> <span data-ttu-id="1a412-106">Questa operazione avrà esito positivo anche se l'oggetto con tale identificatore non è presente.</span><span class="sxs-lookup"><span data-stu-id="1a412-106">This will succeed even if the object with that identifier is not present.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a412-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a412-107">Syntax</span></span>


```mof
uint32 RemoveMemberById(
  [in]  CIM_ManagedElement REF Member,
  [in]  string                 CollectionId,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1a412-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a412-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a412-109">*Membro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1a412-109">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a412-110">Membro da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1a412-110">The member to remove.</span></span>

</dd> <dt>

<span data-ttu-id="1a412-111">*CollectionId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a412-111">*CollectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a412-112">ID della raccolta da cui rimuovere il membro.</span><span class="sxs-lookup"><span data-stu-id="1a412-112">The collection ID of the collection to remove the member from.</span></span>

</dd> <dt>

<span data-ttu-id="1a412-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="1a412-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a412-114">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="1a412-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a412-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a412-115">Return value</span></span>

<span data-ttu-id="1a412-116">Restituisce 0 se ha esito positivo oppure 4096 se il processo è stato avviato. in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="1a412-116">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1a412-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="1a412-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1a412-118">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="1a412-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1a412-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="1a412-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1a412-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="1a412-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1a412-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="1a412-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1a412-122">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="1a412-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1a412-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="1a412-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1a412-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="1a412-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1a412-125">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="1a412-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1a412-126">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="1a412-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1a412-127">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="1a412-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1a412-128">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="1a412-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1a412-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="1a412-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="1a412-130">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="1a412-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1a412-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a412-131">Requirements</span></span>



| <span data-ttu-id="1a412-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a412-132">Requirement</span></span> | <span data-ttu-id="1a412-133">Valore</span><span class="sxs-lookup"><span data-stu-id="1a412-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a412-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a412-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1a412-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1a412-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="1a412-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a412-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1a412-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1a412-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1a412-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1a412-138">Namespace</span></span><br/>                | <span data-ttu-id="1a412-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1a412-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1a412-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1a412-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a412-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a412-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a412-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1a412-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a412-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1a412-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1a412-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a412-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a412-145">**\_CollectionManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="1a412-145">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




