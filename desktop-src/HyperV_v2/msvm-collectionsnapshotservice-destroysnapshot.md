---
description: Elimina uno snapshot esistente della raccolta di sistemi virtuali. Questo metodo può essere un effetto collaterale per eliminare altri snapshot che dipendono dallo snapshot interessato.
ms.assetid: 79a529d5-35bb-4e63-a1b7-8943de9580e8
title: Metodo DestroySnapshot della classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 399737a95db7725718b2e0ec620d2b6b7a7ae93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310019"
---
# <a name="destroysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="95cee-104">Metodo DestroySnapshot della classe MSVM \_ CollectionSnapshotService</span><span class="sxs-lookup"><span data-stu-id="95cee-104">DestroySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="95cee-105">Elimina uno snapshot esistente della raccolta di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="95cee-105">Destroys an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="95cee-106">Questo metodo può essere un effetto collaterale per eliminare altri snapshot che dipendono dallo snapshot interessato.</span><span class="sxs-lookup"><span data-stu-id="95cee-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="95cee-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95cee-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_Collection  REF AffectedSnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="95cee-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="95cee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95cee-109">*AffectedSnapshotCollection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95cee-109">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95cee-110">Riferimento a una [**\_ raccolta CIM**](cim-collection.md) che descrive la raccolta di snapshot del sistema virtuale interessata.</span><span class="sxs-lookup"><span data-stu-id="95cee-110">Reference to a [**CIM\_Collection**](cim-collection.md) that describes the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="95cee-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="95cee-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95cee-112">Riferimento facoltativo restituito se l'operazione viene eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="95cee-112">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="95cee-113">Se presente, il riferimento restituito a un'istanza di [**CIM \_ ConcreteJob**](cim-concretejob.md) può essere usato per monitorare lo stato di avanzamento e per ottenere il risultato del metodo.</span><span class="sxs-lookup"><span data-stu-id="95cee-113">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95cee-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95cee-114">Return value</span></span>

<span data-ttu-id="95cee-115">In caso di esito positivo, restituisce 0 (completa) o 4096 (processo avviato); in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="95cee-115">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="95cee-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="95cee-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="95cee-117">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="95cee-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="95cee-118">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="95cee-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="95cee-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="95cee-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="95cee-120">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="95cee-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="95cee-121">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="95cee-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="95cee-122">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="95cee-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="95cee-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="95cee-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="95cee-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="95cee-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="95cee-125">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="95cee-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="95cee-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="95cee-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="95cee-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95cee-127">Requirements</span></span>



| <span data-ttu-id="95cee-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="95cee-128">Requirement</span></span> | <span data-ttu-id="95cee-129">Valore</span><span class="sxs-lookup"><span data-stu-id="95cee-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95cee-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95cee-130">Minimum supported client</span></span><br/> | <span data-ttu-id="95cee-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="95cee-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="95cee-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95cee-132">Minimum supported server</span></span><br/> | <span data-ttu-id="95cee-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="95cee-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="95cee-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="95cee-134">Namespace</span></span><br/>                | <span data-ttu-id="95cee-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="95cee-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="95cee-136">MOF</span><span class="sxs-lookup"><span data-stu-id="95cee-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95cee-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95cee-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95cee-138">DLL</span><span class="sxs-lookup"><span data-stu-id="95cee-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95cee-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95cee-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="95cee-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95cee-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95cee-141">**\_CollectionSnapshotService MSVM**</span><span class="sxs-lookup"><span data-stu-id="95cee-141">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




