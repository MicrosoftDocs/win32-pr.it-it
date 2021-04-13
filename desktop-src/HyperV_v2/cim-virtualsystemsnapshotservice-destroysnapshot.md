---
description: Elimina uno snapshot del sistema virtuale esistente. Questo metodo può essere un effetto collaterale per eliminare altri snapshot che dipendono dallo snapshot interessato.
ms.assetid: 69f60d0e-50ef-4a38-ad4b-88534b7fb3f8
title: Metodo DestroySnapshot della classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80d618374d2da4a12f2ce31284d7b3fa36ba65ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526773"
---
# <a name="destroysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="99dd0-104">Metodo DestroySnapshot della classe CIM \_ VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="99dd0-104">DestroySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="99dd0-105">Elimina uno snapshot del sistema virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="99dd0-105">Destroy an existing virtual system snapshot.</span></span> <span data-ttu-id="99dd0-106">Questo metodo può essere un effetto collaterale per eliminare altri snapshot che dipendono dallo snapshot interessato.</span><span class="sxs-lookup"><span data-stu-id="99dd0-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="99dd0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99dd0-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="99dd0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="99dd0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99dd0-109">*AffectedSnapshot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99dd0-109">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99dd0-110">Riferimento [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) allo snapshot del sistema virtuale interessato.</span><span class="sxs-lookup"><span data-stu-id="99dd0-110">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="99dd0-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="99dd0-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99dd0-112">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito facoltativamente un [**\_ ConcreteJob CIM**](cim-concretejob.md) che rappresenta il processo.</span><span class="sxs-lookup"><span data-stu-id="99dd0-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="99dd0-113">Questo parametro è di lettura/scrittura in Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="99dd0-113">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99dd0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99dd0-114">Return value</span></span>

<span data-ttu-id="99dd0-115">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="99dd0-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="99dd0-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="99dd0-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="99dd0-117">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="99dd0-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="99dd0-118">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="99dd0-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="99dd0-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="99dd0-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="99dd0-120">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="99dd0-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="99dd0-121">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="99dd0-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="99dd0-122">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="99dd0-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="99dd0-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="99dd0-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="99dd0-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="99dd0-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="99dd0-125">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="99dd0-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="99dd0-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="99dd0-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="99dd0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99dd0-127">Requirements</span></span>



| <span data-ttu-id="99dd0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="99dd0-128">Requirement</span></span> | <span data-ttu-id="99dd0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="99dd0-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99dd0-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99dd0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="99dd0-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="99dd0-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="99dd0-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99dd0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="99dd0-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="99dd0-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="99dd0-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="99dd0-134">Namespace</span></span><br/>                | <span data-ttu-id="99dd0-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="99dd0-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="99dd0-136">MOF</span><span class="sxs-lookup"><span data-stu-id="99dd0-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99dd0-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99dd0-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="99dd0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="99dd0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99dd0-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="99dd0-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="99dd0-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99dd0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99dd0-141">**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="99dd0-141">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




