---
description: Elimina uno snapshot della macchina virtuale esistente.
ms.assetid: 84752bb3-cae1-4a93-89bc-e735c058feda
title: Metodo DestroySnapshot della classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 91c2e59baa8bb22f5ea9f128130d7dc440e28ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884874"
---
# <a name="destroysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="838f8-103">Metodo DestroySnapshot della classe MSVM \_ VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="838f8-103">DestroySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="838f8-104">Elimina uno snapshot della macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="838f8-104">Destroys an existing virtual machine snapshot.</span></span> <span data-ttu-id="838f8-105">Questo metodo può, come effetto collaterale, eliminare altri snapshot che dipendono dallo snapshot interessato.</span><span class="sxs-lookup"><span data-stu-id="838f8-105">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="838f8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="838f8-106">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="838f8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="838f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="838f8-108">*AffectedSnapshot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="838f8-108">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="838f8-109">Riferimento [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) che rappresenta lo snapshot della macchina virtuale da eliminare.</span><span class="sxs-lookup"><span data-stu-id="838f8-109">A [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) reference that represents the virtual machine snapshot to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="838f8-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="838f8-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="838f8-111">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="838f8-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="838f8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="838f8-112">Return value</span></span>

<span data-ttu-id="838f8-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="838f8-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="838f8-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="838f8-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="838f8-115">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="838f8-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="838f8-116">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="838f8-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="838f8-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="838f8-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="838f8-118">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="838f8-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="838f8-119">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="838f8-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="838f8-120">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="838f8-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="838f8-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="838f8-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="838f8-122">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="838f8-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="838f8-123">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="838f8-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="838f8-124">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="838f8-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="838f8-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="838f8-125">Requirements</span></span>



| <span data-ttu-id="838f8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="838f8-126">Requirement</span></span> | <span data-ttu-id="838f8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="838f8-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="838f8-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="838f8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="838f8-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="838f8-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="838f8-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="838f8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="838f8-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="838f8-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="838f8-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="838f8-132">Namespace</span></span><br/>                | <span data-ttu-id="838f8-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="838f8-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="838f8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="838f8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="838f8-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="838f8-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="838f8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="838f8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="838f8-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="838f8-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="838f8-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="838f8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="838f8-139">**\_VirtualSystemSnapshotService MSVM**</span><span class="sxs-lookup"><span data-stu-id="838f8-139">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="838f8-140">**RemoveVirtualSystemSnapshot (V1)**</span><span class="sxs-lookup"><span data-stu-id="838f8-140">**RemoveVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

