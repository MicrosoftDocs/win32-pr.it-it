---
title: Enumerazione VMVMState (VPCCOMInterfaces. h)
description: Specifica lo stato di una macchina virtuale.
ms.assetid: 952dab9d-3d38-4cc5-ab75-4ee5096f7923
keywords:
- VMVMState enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMVMState
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45505e4fb4b444b15697afca4576e889f2da9a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302409"
---
# <a name="vmvmstate-enumeration"></a><span data-ttu-id="a9410-104">Enumerazione VMVMState</span><span class="sxs-lookup"><span data-stu-id="a9410-104">VMVMState enumeration</span></span>

<span data-ttu-id="a9410-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a9410-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a9410-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a9410-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a9410-107">Specifica lo stato di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a9410-107">Specifies the state of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9410-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9410-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVMState_Invalid        = 0,
  vmVMState_TurnedOff      = 1,
  vmVMState_Saved          = 2,
  vmVMState_TurningOn      = 3,
  vmVMState_Restoring      = 4,
  vmVMState_Running        = 5,
  vmVMState_Paused         = 6,
  vmVMState_Saving         = 7,
  vmVMState_TurningOff     = 8,
  vmVMState_MergingDrives  = 9,
  vmVMState_DeleteMachine  = 10
} VMVMState;
```



## <a name="constants"></a><span data-ttu-id="a9410-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="a9410-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a9410-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="a9410-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="a9410-111">Uno stato non valido (non deve verificarsi se la macchina virtuale esiste).</span><span class="sxs-lookup"><span data-stu-id="a9410-111">An invalid state (should not occur if the virtual machine exists).</span></span>

</dd> <dt>

<span data-ttu-id="a9410-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**\_turnedOff vmVMState**</span><span class="sxs-lookup"><span data-stu-id="a9410-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmVMState\_TurnedOff**</span></span>
</dt> <dd>

<span data-ttu-id="a9410-113">Disattivato e non salvato.</span><span class="sxs-lookup"><span data-stu-id="a9410-113">Off and not saved.</span></span>

</dd> <dt>

<span data-ttu-id="a9410-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState \_ salvato**</span><span class="sxs-lookup"><span data-stu-id="a9410-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState\_Saved**</span></span>
</dt> <dd>

<span data-ttu-id="a9410-115">Ma il Guest viene salvato.</span><span class="sxs-lookup"><span data-stu-id="a9410-115">Off but the guest is saved.</span></span>

</dd> <dt>

<span data-ttu-id="a9410-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**\_TurningOn vmVMState**</span><span class="sxs-lookup"><span data-stu-id="a9410-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**vmVMState\_TurningOn**</span></span>
</dt> <dd>

<span data-ttu-id="a9410-117">In fase di attivazione.</span><span class="sxs-lookup"><span data-stu-id="a9410-117">In the process of turning on.</span></span>

</dd> <dt>

<span data-ttu-id="a9410-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**\_ripristino vmVMState**</span><span class="sxs-lookup"><span data-stu-id="a9410-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**vmVMState\_Restoring**</span></span>
</dt> <dd>

<span data-ttu-id="a9410-119">Ripristino dello stato.</span><span class="sxs-lookup"><span data-stu-id="a9410-119">Restoring the state.</span></span>

</dd> <dt>

<span data-ttu-id="a9410-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="a9410-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState\_Running**</span></span>
</dt> <dd>

<span data-ttu-id="a9410-121">In esecuzione e non in pausa.</span><span class="sxs-lookup"><span data-stu-id="a9410-121">Running and not paused.</span></span>

</dd> <dt>

<span data-ttu-id="a9410-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState \_ sospeso**</span><span class="sxs-lookup"><span data-stu-id="a9410-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState\_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="a9410-123">In esecuzione e sospesa.</span><span class="sxs-lookup"><span data-stu-id="a9410-123">Running and paused.</span></span>

</dd> <dt>

<span data-ttu-id="a9410-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**\_salvataggio vmVMState**</span><span class="sxs-lookup"><span data-stu-id="a9410-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**vmVMState\_Saving**</span></span>
</dt> <dd>

<span data-ttu-id="a9410-125">Salvataggio dello stato.</span><span class="sxs-lookup"><span data-stu-id="a9410-125">Saving the state.</span></span>

</dd> <dt>

<span data-ttu-id="a9410-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**\_TurningOff vmVMState**</span><span class="sxs-lookup"><span data-stu-id="a9410-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmVMState\_TurningOff**</span></span>
</dt> <dd>

<span data-ttu-id="a9410-127">In fase di disattivazione.</span><span class="sxs-lookup"><span data-stu-id="a9410-127">In the process of turning off.</span></span>

</dd> <dt>

<span data-ttu-id="a9410-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**\_MergingDrives vmVMState**</span><span class="sxs-lookup"><span data-stu-id="a9410-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmVMState\_MergingDrives**</span></span>
</dt> <dd>

<span data-ttu-id="a9410-129">Durante il processo di Unione delle unità di annullamento.</span><span class="sxs-lookup"><span data-stu-id="a9410-129">In the process of merging undo drives.</span></span>

</dd> <dt>

<span data-ttu-id="a9410-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**\_DeleteMachine vmVMState**</span><span class="sxs-lookup"><span data-stu-id="a9410-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmVMState\_DeleteMachine**</span></span>
</dt> <dd>

<span data-ttu-id="a9410-131">Eliminazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a9410-131">Deleting the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9410-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9410-132">Requirements</span></span>



| <span data-ttu-id="a9410-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9410-133">Requirement</span></span> | <span data-ttu-id="a9410-134">Valore</span><span class="sxs-lookup"><span data-stu-id="a9410-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9410-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9410-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a9410-136">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a9410-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9410-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9410-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a9410-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a9410-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a9410-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a9410-139">End of client support</span></span><br/>    | <span data-ttu-id="a9410-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9410-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a9410-141">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a9410-141">Product</span></span><br/>                  | <span data-ttu-id="a9410-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a9410-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a9410-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9410-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9410-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9410-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9410-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9410-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9410-146">**IVMVirtualMachine:: state**</span><span class="sxs-lookup"><span data-stu-id="a9410-146">**IVMVirtualMachine::State**</span></span>](ivmvirtualmachine-state.md)
</dt> <dt>

[<span data-ttu-id="a9410-147">**IVMVirtualMachineEvents:: OnStateChange**</span><span class="sxs-lookup"><span data-stu-id="a9410-147">**IVMVirtualMachineEvents::OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)
</dt> <dt>

[<span data-ttu-id="a9410-148">**IVMVirtualPCEvents::OnVMStateChange**</span><span class="sxs-lookup"><span data-stu-id="a9410-148">**IVMVirtualPCEvents::OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md)
</dt> </dl>

 

