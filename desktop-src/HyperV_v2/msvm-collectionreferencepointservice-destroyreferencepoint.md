---
description: Elimina definitivamente una raccolta di punti di riferimento esistente. Questo metodo può essere un effetto collaterale per eliminare altri punti di riferimento che dipendono dalla raccolta di punti di riferimento interessata.
ms.assetid: 72c116f4-f844-494c-96ea-e97c49a2af7e
title: Metodo DestroyReferencePoint della classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d7fb3fd9168778854518022744f1a0c5ba3c5f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132015"
---
# <a name="destroyreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="59d7e-104">Metodo DestroyReferencePoint della classe MSVM \_ CollectionReferencePointService</span><span class="sxs-lookup"><span data-stu-id="59d7e-104">DestroyReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="59d7e-105">Elimina definitivamente una raccolta di punti di riferimento esistente.</span><span class="sxs-lookup"><span data-stu-id="59d7e-105">Destroys an existing reference point collection.</span></span> <span data-ttu-id="59d7e-106">Questo metodo può essere un effetto collaterale per eliminare altri punti di riferimento che dipendono dalla raccolta di punti di riferimento interessata.</span><span class="sxs-lookup"><span data-stu-id="59d7e-106">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="59d7e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59d7e-107">Syntax</span></span>


```mof
uint32 DestroyReferencePoint(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="59d7e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="59d7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59d7e-109">*AffectedReferencePointCollection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59d7e-109">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59d7e-110">Riferimento alla raccolta di punti di riferimento del sistema virtuale interessata.</span><span class="sxs-lookup"><span data-stu-id="59d7e-110">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="59d7e-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="59d7e-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59d7e-112">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo.</span><span class="sxs-lookup"><span data-stu-id="59d7e-112">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59d7e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59d7e-113">Return value</span></span>

<span data-ttu-id="59d7e-114">Se ha esito positivo, restituisce 0 (nessun errore) o 4096 (processo avviato); in caso contrario, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="59d7e-114">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="59d7e-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="59d7e-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="59d7e-116">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="59d7e-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="59d7e-117">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="59d7e-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="59d7e-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="59d7e-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="59d7e-119">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="59d7e-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="59d7e-120">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="59d7e-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="59d7e-121">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="59d7e-121">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="59d7e-122">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="59d7e-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="59d7e-123">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="59d7e-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="59d7e-124">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="59d7e-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="59d7e-125">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="59d7e-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="59d7e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59d7e-126">Requirements</span></span>



| <span data-ttu-id="59d7e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="59d7e-127">Requirement</span></span> | <span data-ttu-id="59d7e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="59d7e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59d7e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59d7e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="59d7e-130">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="59d7e-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="59d7e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59d7e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="59d7e-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="59d7e-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="59d7e-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="59d7e-133">Namespace</span></span><br/>                | <span data-ttu-id="59d7e-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="59d7e-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="59d7e-135">MOF</span><span class="sxs-lookup"><span data-stu-id="59d7e-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59d7e-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59d7e-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="59d7e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="59d7e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59d7e-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="59d7e-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="59d7e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59d7e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59d7e-140">**\_CollectionReferencePointService MSVM**</span><span class="sxs-lookup"><span data-stu-id="59d7e-140">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




