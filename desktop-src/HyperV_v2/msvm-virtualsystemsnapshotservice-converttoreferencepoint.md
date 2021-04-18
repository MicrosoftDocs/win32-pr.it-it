---
description: Converte uno snapshot del sistema virtuale esistente in un punto di riferimento. Lo snapshot viene eliminato come effetto collaterale. Solo gli snapshot di ripristino possono essere convertiti in punti di riferimento.
ms.assetid: c634d749-e18f-4a11-a574-2aee705c0722
title: Metodo ConvertToReferencePoint della classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 18eecc1677abaec5893b3749b4ee82f757cbe93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305981"
---
# <a name="converttoreferencepoint-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="00bee-105">Metodo ConvertToReferencePoint della classe MSVM \_ VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="00bee-105">ConvertToReferencePoint method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="00bee-106">Converte uno snapshot del sistema virtuale esistente in un punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="00bee-106">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="00bee-107">Lo snapshot viene eliminato come effetto collaterale.</span><span class="sxs-lookup"><span data-stu-id="00bee-107">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="00bee-108">Solo gli snapshot di ripristino possono essere convertiti in punti di riferimento.</span><span class="sxs-lookup"><span data-stu-id="00bee-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="00bee-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00bee-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      CIM_VirtualSystemSettingData     REF AffectedSnapshot,
  [in]      string                               ReferencePointSettings,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="00bee-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="00bee-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00bee-111">*AffectedSnapshot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00bee-111">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00bee-112">Riferimento allo snapshot del sistema virtuale interessato.</span><span class="sxs-lookup"><span data-stu-id="00bee-112">Reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="00bee-113">*ReferencePointSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00bee-113">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00bee-114">Impostazioni parametri.</span><span class="sxs-lookup"><span data-stu-id="00bee-114">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="00bee-115">*ResultingReferencePoint* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="00bee-115">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="00bee-116">Punto di riferimento del sistema virtuale risultante</span><span class="sxs-lookup"><span data-stu-id="00bee-116">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="00bee-117">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="00bee-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00bee-118">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo.</span><span class="sxs-lookup"><span data-stu-id="00bee-118">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00bee-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00bee-119">Return value</span></span>

<span data-ttu-id="00bee-120">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="00bee-120">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="00bee-121">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="00bee-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="00bee-122">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="00bee-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="00bee-123">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="00bee-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="00bee-124">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="00bee-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="00bee-125">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="00bee-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="00bee-126">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="00bee-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="00bee-127">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="00bee-127">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="00bee-128">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="00bee-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="00bee-129">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="00bee-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="00bee-130">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="00bee-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="00bee-131">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="00bee-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="00bee-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00bee-132">Requirements</span></span>



| <span data-ttu-id="00bee-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="00bee-133">Requirement</span></span> | <span data-ttu-id="00bee-134">Valore</span><span class="sxs-lookup"><span data-stu-id="00bee-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00bee-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00bee-135">Minimum supported client</span></span><br/> | <span data-ttu-id="00bee-136">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="00bee-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="00bee-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00bee-137">Minimum supported server</span></span><br/> | <span data-ttu-id="00bee-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="00bee-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="00bee-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="00bee-139">Namespace</span></span><br/>                | <span data-ttu-id="00bee-140">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="00bee-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="00bee-141">MOF</span><span class="sxs-lookup"><span data-stu-id="00bee-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00bee-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00bee-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="00bee-143">DLL</span><span class="sxs-lookup"><span data-stu-id="00bee-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00bee-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="00bee-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="00bee-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00bee-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00bee-146">**\_VirtualSystemSnapshotService MSVM**</span><span class="sxs-lookup"><span data-stu-id="00bee-146">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




