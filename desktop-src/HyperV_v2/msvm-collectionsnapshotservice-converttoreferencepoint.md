---
description: Converte uno snapshot di raccolta esistente in una raccolta di punti di riferimento. La raccolta snapshot viene eliminata come effetto collaterale. Solo gli snapshot di ripristino possono essere convertiti in punti di riferimento.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Metodo ConvertToReferencePoint della classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 810761b67303ad33ced6fdaef857c96f65365091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885729"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="f5e2e-105">Metodo ConvertToReferencePoint della classe MSVM \_ CollectionSnapshotService</span><span class="sxs-lookup"><span data-stu-id="f5e2e-105">ConvertToReferencePoint method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="f5e2e-106">Converte uno snapshot di raccolta esistente in una raccolta di punti di riferimento.</span><span class="sxs-lookup"><span data-stu-id="f5e2e-106">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="f5e2e-107">La raccolta snapshot viene eliminata come effetto collaterale.</span><span class="sxs-lookup"><span data-stu-id="f5e2e-107">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="f5e2e-108">Solo gli snapshot di ripristino possono essere convertiti in punti di riferimento.</span><span class="sxs-lookup"><span data-stu-id="f5e2e-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5e2e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5e2e-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      Msvm_SnapshotCollection       REF AffectedSnapshotCollection,
  [in, out] Msvm_ReferencePointCollection REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f5e2e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5e2e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5e2e-111">*AffectedSnapshotCollection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5e2e-111">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5e2e-112">Riferimento a un [**MSVM \_ snapshotcollection**](msvm-snapshotcollection.md) che contiene la raccolta di snapshot del sistema virtuale interessata.</span><span class="sxs-lookup"><span data-stu-id="f5e2e-112">Reference to a [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) containing the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="f5e2e-113">*ResultingReferencePointCollection* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f5e2e-113">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5e2e-114">Riferimento a un [**\_ ReferencePointCollection MSVM**](msvm-referencepointcollection.md) che contiene la raccolta di punti di riferimento del sistema virtuale risultante</span><span class="sxs-lookup"><span data-stu-id="f5e2e-114">Reference to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) containing the resulting virtual system reference point collection</span></span>

</dd> <dt>

<span data-ttu-id="f5e2e-115">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="f5e2e-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5e2e-116">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo.</span><span class="sxs-lookup"><span data-stu-id="f5e2e-116">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5e2e-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5e2e-117">Return value</span></span>

<span data-ttu-id="f5e2e-118">In caso di esito positivo, restituisce 0 (completa) o 4096 (processo avviato); in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="f5e2e-118">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f5e2e-119">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="f5e2e-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f5e2e-120">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="f5e2e-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f5e2e-121">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="f5e2e-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f5e2e-122">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="f5e2e-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f5e2e-123">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="f5e2e-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f5e2e-124">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="f5e2e-124">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f5e2e-125">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="f5e2e-125">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f5e2e-126">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f5e2e-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f5e2e-127">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="f5e2e-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f5e2e-128">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f5e2e-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f5e2e-129">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f5e2e-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f5e2e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5e2e-130">Requirements</span></span>



| <span data-ttu-id="f5e2e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5e2e-131">Requirement</span></span> | <span data-ttu-id="f5e2e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f5e2e-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5e2e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5e2e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f5e2e-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f5e2e-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f5e2e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5e2e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f5e2e-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f5e2e-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f5e2e-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f5e2e-137">Namespace</span></span><br/>                | <span data-ttu-id="f5e2e-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f5e2e-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f5e2e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f5e2e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5e2e-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5e2e-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5e2e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f5e2e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5e2e-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f5e2e-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f5e2e-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5e2e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5e2e-144">**\_CollectionSnapshotService MSVM**</span><span class="sxs-lookup"><span data-stu-id="f5e2e-144">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




