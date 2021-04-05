---
description: Crea uno snapshot di una raccolta di sistemi virtuali.
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: Metodo CreateSnapshot della classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 653dae65cc5fe50416b069da6a66e8c678c1b512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755154"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="8e4f3-103">Metodo CreateSnapshot della classe MSVM \_ CollectionSnapshotService</span><span class="sxs-lookup"><span data-stu-id="8e4f3-103">CreateSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="8e4f3-104">Crea uno snapshot di una raccolta di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="8e4f3-104">Creates a snapshot of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e4f3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e4f3-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8e4f3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e4f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e4f3-107">*Raccolta* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8e4f3-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e4f3-108">Riferimento a un [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) che descrive la raccolta di sistemi virtuali interessata.</span><span class="sxs-lookup"><span data-stu-id="8e4f3-108">Reference to a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that describes the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="8e4f3-109">*SnapshotSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e4f3-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e4f3-110">Contiene le impostazioni dei parametri.</span><span class="sxs-lookup"><span data-stu-id="8e4f3-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="8e4f3-111">*SnapshotType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e4f3-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e4f3-112">Tipo di snapshot richiesto:</span><span class="sxs-lookup"><span data-stu-id="8e4f3-112">Requested snapshot type:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e4f3-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span data-ttu-id="8e4f3-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Snapshot standard** (1)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Standard Snapshot** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8e4f3-115">Snapshot standard del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="8e4f3-115">Standard snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span data-ttu-id="8e4f3-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Snapshot di ripristino** (2)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Recovery Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8e4f3-117">Snapshot per gli scenari di ripristino, inclusi backup e replica di failover.</span><span class="sxs-lookup"><span data-stu-id="8e4f3-117">Snapshot for recovery scenarios including failover replication and backup.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8e4f3-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="8e4f3-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="8e4f3-120">*ResultingSnapshotCollection* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8e4f3-120">*ResultingSnapshotCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e4f3-121">Se l'operazione riesce, restituisce un riferimento alla [**\_ raccolta CIM**](cim-collection.md) contenente lo snapshot del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="8e4f3-121">On success, returns a [**CIM\_Collection**](cim-collection.md) reference containing the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="8e4f3-122">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="8e4f3-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e4f3-123">Riferimento facoltativo restituito se l'operazione viene eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="8e4f3-123">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="8e4f3-124">Se presente, il riferimento restituito a un'istanza di [**CIM \_ ConcreteJob**](cim-concretejob.md) può essere usato per monitorare lo stato di avanzamento e per ottenere il risultato del metodo.</span><span class="sxs-lookup"><span data-stu-id="8e4f3-124">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e4f3-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e4f3-125">Return value</span></span>

<span data-ttu-id="8e4f3-126">In caso di esito positivo, restituisce 0 (completa) o 4096 (processo avviato); in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="8e4f3-126">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8e4f3-127">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8e4f3-128">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8e4f3-129">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8e4f3-130">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8e4f3-131">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8e4f3-132">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8e4f3-133">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8e4f3-134">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8e4f3-135">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8e4f3-136">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8e4f3-137">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8e4f3-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8e4f3-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e4f3-138">Requirements</span></span>



| <span data-ttu-id="8e4f3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e4f3-139">Requirement</span></span> | <span data-ttu-id="8e4f3-140">Valore</span><span class="sxs-lookup"><span data-stu-id="8e4f3-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e4f3-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e4f3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8e4f3-142">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8e4f3-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8e4f3-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e4f3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8e4f3-144">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8e4f3-144">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8e4f3-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8e4f3-145">Namespace</span></span><br/>                | <span data-ttu-id="8e4f3-146">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8e4f3-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8e4f3-147">MOF</span><span class="sxs-lookup"><span data-stu-id="8e4f3-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e4f3-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e4f3-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e4f3-149">DLL</span><span class="sxs-lookup"><span data-stu-id="8e4f3-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e4f3-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8e4f3-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8e4f3-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e4f3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e4f3-152">**\_CollectionSnapshotService MSVM**</span><span class="sxs-lookup"><span data-stu-id="8e4f3-152">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




