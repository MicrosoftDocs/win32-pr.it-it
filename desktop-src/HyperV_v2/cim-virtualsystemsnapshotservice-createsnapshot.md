---
description: Crea uno snapshot di un sistema virtuale.
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: Metodo CreateSnapshot della classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee96098477501123cffc1fd59a52734bbbea35d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315514"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="a19d1-103">Metodo CreateSnapshot della classe CIM \_ VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="a19d1-103">CreateSnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="a19d1-104">Crea uno snapshot di un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a19d1-104">Creates a snapshot of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a19d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a19d1-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a19d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a19d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a19d1-107">*AffectedSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a19d1-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a19d1-108">Riferimento [**CIM \_ ComputerSystem**](cim-computersystem.md) al sistema virtuale interessato.</span><span class="sxs-lookup"><span data-stu-id="a19d1-108">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="a19d1-109">*SnapshotSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a19d1-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a19d1-110">Impostazioni parametri.</span><span class="sxs-lookup"><span data-stu-id="a19d1-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="a19d1-111">*SnapshotType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a19d1-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a19d1-112">Tipo di snapshot richiesto:</span><span class="sxs-lookup"><span data-stu-id="a19d1-112">Requested snapshot type:</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="a19d1-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Snapshot completo** (2)</span><span class="sxs-lookup"><span data-stu-id="a19d1-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a19d1-114">Completare lo snapshot del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a19d1-114">Complete snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="a19d1-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Snapshot del disco** (3)</span><span class="sxs-lookup"><span data-stu-id="a19d1-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a19d1-116">Snapshot dei dischi del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a19d1-116">Snapshot of virtual system disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a19d1-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="a19d1-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="a19d1-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a19d1-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="a19d1-119">*ResultingSnapshot* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a19d1-119">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a19d1-120">Riferimento [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) allo snapshot del sistema virtuale risultante.</span><span class="sxs-lookup"><span data-stu-id="a19d1-120">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the resulting virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a19d1-121">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a19d1-121">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a19d1-122">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo.</span><span class="sxs-lookup"><span data-stu-id="a19d1-122">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="a19d1-123">In questo caso, l'istanza della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) che rappresenta il nuovo snapshot del sistema virtuale viene presentata tramite l'associazione [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) con il valore della proprietà **affected** che fa riferimento alla nuova istanza della classe **CIM \_ VirtualSystemSettingData** che rappresenta lo snapshot del sistema virtuale e il valore di **ElementEffects** impostato su 5 (Create).</span><span class="sxs-lookup"><span data-stu-id="a19d1-123">In this case, the instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing the new virtual system snapshot is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **CIM\_VirtualSystemSettingData** class representing the virtual system snapshot and the value of the **ElementEffects** set to 5 (Create).</span></span>

> [!Note]  
> <span data-ttu-id="a19d1-124">Questo parametro è di lettura/scrittura in Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="a19d1-124">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a19d1-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a19d1-125">Return value</span></span>

<span data-ttu-id="a19d1-126">In caso di esito positivo, restituisce 0; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="a19d1-126">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a19d1-127">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="a19d1-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a19d1-128">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="a19d1-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a19d1-129">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="a19d1-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a19d1-130">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="a19d1-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a19d1-131">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="a19d1-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a19d1-132">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="a19d1-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a19d1-133">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="a19d1-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a19d1-134">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="a19d1-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a19d1-135">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="a19d1-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a19d1-136">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a19d1-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a19d1-137">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a19d1-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a19d1-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a19d1-138">Requirements</span></span>



| <span data-ttu-id="a19d1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a19d1-139">Requirement</span></span> | <span data-ttu-id="a19d1-140">Valore</span><span class="sxs-lookup"><span data-stu-id="a19d1-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a19d1-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a19d1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a19d1-142">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a19d1-142">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a19d1-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a19d1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a19d1-144">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a19d1-144">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a19d1-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a19d1-145">Namespace</span></span><br/>                | <span data-ttu-id="a19d1-146">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a19d1-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a19d1-147">MOF</span><span class="sxs-lookup"><span data-stu-id="a19d1-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a19d1-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a19d1-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a19d1-149">DLL</span><span class="sxs-lookup"><span data-stu-id="a19d1-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a19d1-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a19d1-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a19d1-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a19d1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a19d1-152">**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a19d1-152">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




