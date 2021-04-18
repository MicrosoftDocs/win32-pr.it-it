---
description: Applica uno snapshot del sistema virtuale al sistema virtuale dal quale è stato creato.
ms.assetid: acd90ce0-7f82-48d9-9d23-903ba6815779
title: Metodo ApplySnapshot della classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 252f7d7d9a57b439ac00fa663fa0a0e816ebada0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315515"
---
# <a name="applysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="82fa1-103">Metodo ApplySnapshot della classe CIM \_ VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="82fa1-103">ApplySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="82fa1-104">Applica uno snapshot del sistema virtuale al sistema virtuale dal quale è stato creato.</span><span class="sxs-lookup"><span data-stu-id="82fa1-104">Applies a virtual system snapshot to the virtual system that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="82fa1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82fa1-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="82fa1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="82fa1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82fa1-107">*Snapshot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82fa1-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82fa1-108">Riferimento [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) allo snapshot del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="82fa1-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="82fa1-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="82fa1-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82fa1-110">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito facoltativamente un [**\_ ConcreteJob CIM**](cim-concretejob.md) che rappresenta il processo.</span><span class="sxs-lookup"><span data-stu-id="82fa1-110">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="82fa1-111">Questo parametro è di lettura/scrittura in Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="82fa1-111">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82fa1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82fa1-112">Return value</span></span>

<span data-ttu-id="82fa1-113">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="82fa1-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="82fa1-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="82fa1-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="82fa1-115">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="82fa1-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="82fa1-116">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="82fa1-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="82fa1-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="82fa1-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="82fa1-118">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="82fa1-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="82fa1-119">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="82fa1-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="82fa1-120">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="82fa1-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="82fa1-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="82fa1-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="82fa1-122">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="82fa1-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="82fa1-123">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="82fa1-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="82fa1-124">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="82fa1-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="82fa1-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82fa1-125">Requirements</span></span>



| <span data-ttu-id="82fa1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="82fa1-126">Requirement</span></span> | <span data-ttu-id="82fa1-127">Valore</span><span class="sxs-lookup"><span data-stu-id="82fa1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82fa1-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82fa1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="82fa1-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="82fa1-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="82fa1-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82fa1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="82fa1-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="82fa1-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="82fa1-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="82fa1-132">Namespace</span></span><br/>                | <span data-ttu-id="82fa1-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="82fa1-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="82fa1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="82fa1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82fa1-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82fa1-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="82fa1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="82fa1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82fa1-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82fa1-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="82fa1-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82fa1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82fa1-139">**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="82fa1-139">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




