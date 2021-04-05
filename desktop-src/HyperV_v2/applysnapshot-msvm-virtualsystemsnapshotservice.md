---
description: Applica uno snapshot della macchina virtuale alla macchina virtuale dalla quale è stato creato.
ms.assetid: 45f1ec8f-aa96-4060-8f8c-0471d0ad4a21
title: Metodo ApplySnapshot della classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 735e827935689a0f0ede7fbac1d582ea40772ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881866"
---
# <a name="applysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="6dae8-103">Metodo ApplySnapshot della classe MSVM \_ VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="6dae8-103">ApplySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="6dae8-104">Applica uno snapshot della macchina virtuale alla macchina virtuale dalla quale è stato creato.</span><span class="sxs-lookup"><span data-stu-id="6dae8-104">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dae8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6dae8-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6dae8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6dae8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dae8-107">*Snapshot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6dae8-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dae8-108">Riferimento a una classe derivata da [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) che rappresenta lo snapshot della macchina virtuale da applicare.</span><span class="sxs-lookup"><span data-stu-id="6dae8-108">A reference to a class derived from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) that represents the virtual machine snapshot to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="6dae8-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="6dae8-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dae8-110">Questa operazione viene sempre eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="6dae8-110">This operation is always performed asynchronously.</span></span> <span data-ttu-id="6dae8-111">Questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6dae8-111">This method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dae8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6dae8-112">Return value</span></span>

<span data-ttu-id="6dae8-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6dae8-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6dae8-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="6dae8-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6dae8-115">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="6dae8-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6dae8-116">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="6dae8-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6dae8-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="6dae8-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6dae8-118">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="6dae8-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6dae8-119">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="6dae8-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6dae8-120">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="6dae8-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6dae8-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6dae8-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6dae8-122">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="6dae8-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6dae8-123">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="6dae8-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6dae8-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="6dae8-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6dae8-125">**Stato non valido** (32775)</span><span class="sxs-lookup"><span data-stu-id="6dae8-125">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6dae8-126">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6dae8-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6dae8-127">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6dae8-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6dae8-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6dae8-128">Requirements</span></span>



| <span data-ttu-id="6dae8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dae8-129">Requirement</span></span> | <span data-ttu-id="6dae8-130">Valore</span><span class="sxs-lookup"><span data-stu-id="6dae8-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dae8-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6dae8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6dae8-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6dae8-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6dae8-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6dae8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6dae8-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6dae8-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6dae8-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6dae8-135">Namespace</span></span><br/>                | <span data-ttu-id="6dae8-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6dae8-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6dae8-137">MOF</span><span class="sxs-lookup"><span data-stu-id="6dae8-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6dae8-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6dae8-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6dae8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6dae8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dae8-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6dae8-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6dae8-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6dae8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dae8-142">**\_VirtualSystemSnapshotService MSVM**</span><span class="sxs-lookup"><span data-stu-id="6dae8-142">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="6dae8-143">**ApplyVirtualSystemSnapshot (V1)**</span><span class="sxs-lookup"><span data-stu-id="6dae8-143">**ApplyVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/applyvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="6dae8-144">**ApplyVirtualSystemSnapshotEx (V1)**</span><span class="sxs-lookup"><span data-stu-id="6dae8-144">**ApplyVirtualSystemSnapshotEx (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-virtualsystemmanagementservice-applyvirtualsystemsnapshotex)
</dt> </dl>

 

