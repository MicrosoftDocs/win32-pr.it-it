---
title: Enumerazione VMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Specifica gli eventi della macchina virtuale.
ms.assetid: 158bdada-6fd3-488c-9ff1-e04df9a79127
keywords:
- VMVirtualMachineEvents enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1e1d8f4d89c28f63886444537fb9d894fc42e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048662"
---
# <a name="vmvirtualmachineevents-enumeration"></a><span data-ttu-id="2e0a7-104">Enumerazione VMVirtualMachineEvents</span><span class="sxs-lookup"><span data-stu-id="2e0a7-104">VMVirtualMachineEvents enumeration</span></span>

<span data-ttu-id="2e0a7-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2e0a7-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2e0a7-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2e0a7-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2e0a7-107">Specifica gli eventi della macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="2e0a7-107">Specifies the virtual machine (VM) events.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e0a7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e0a7-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualMachineEvent_StateChanged              = 1,
  vmVirtualMachineEvent_RequestShutdown           = 2,
  vmVirtualMachineEvent_Reset                     = 3,
  vmVirtualMachineEvent_TripleFault               = 4,
  vmVirtualMachineEvent_HeartbeatStopped          = 5,
  vmVirtualMachineEvent_ConfigurationChanged      = 6,
  vmVirtualMachineEvent_EnhancedVideoModeChanged  = 7,
  vmVirtualMachineEvent_AdditionsUninstalled      = 8,
  vmVirtualMachineEvent_AdditionsAvailable        = 9,
  vmVirtualMachineEvent_GuestShutdown             = 10,
  vmVirtualMachineEvent_GuestLogoff               = 11,
  vmVirtualMachineEvent_DiskOutOfSpace            = 12
} VMVirtualMachineEvents;
```



## <a name="constants"></a><span data-ttu-id="2e0a7-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="2e0a7-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2e0a7-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**\_StateChanged vmVirtualMachineEvent**</span><span class="sxs-lookup"><span data-stu-id="2e0a7-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmVirtualMachineEvent\_StateChanged**</span></span>
</dt> <dd>

<span data-ttu-id="2e0a7-111">Lo stato di una macchina virtuale è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="2e0a7-111">A VM's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="2e0a7-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**\_RequestShutdown vmVirtualMachineEvent**</span><span class="sxs-lookup"><span data-stu-id="2e0a7-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_RequestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="2e0a7-113">È stato richiesto un arresto.</span><span class="sxs-lookup"><span data-stu-id="2e0a7-113">A shutdown has been requested.</span></span>

</dd> <dt>

<span data-ttu-id="2e0a7-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**reimpostazione vmVirtualMachineEvent \_**</span><span class="sxs-lookup"><span data-stu-id="2e0a7-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**vmVirtualMachineEvent\_Reset**</span></span>
</dt> <dd>

<span data-ttu-id="2e0a7-115">Una macchina virtuale è stata reimpostata.</span><span class="sxs-lookup"><span data-stu-id="2e0a7-115">A VM has been reset.</span></span>

</dd> <dt>

<span data-ttu-id="2e0a7-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**\_TripleFault vmVirtualMachineEvent**</span><span class="sxs-lookup"><span data-stu-id="2e0a7-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmVirtualMachineEvent\_TripleFault**</span></span>
</dt> <dd>

<span data-ttu-id="2e0a7-117">Una macchina virtuale presenta tre errori.</span><span class="sxs-lookup"><span data-stu-id="2e0a7-117">A VM has triple-faulted.</span></span>

</dd> <dt>

<span data-ttu-id="2e0a7-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**\_HeartbeatStopped vmVirtualMachineEvent**</span><span class="sxs-lookup"><span data-stu-id="2e0a7-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**vmVirtualMachineEvent\_HeartbeatStopped**</span></span>
</dt> <dd>

<span data-ttu-id="2e0a7-119">L'heartbeat di una macchina virtuale è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="2e0a7-119">A VM's heartbeat has stopped.</span></span> <span data-ttu-id="2e0a7-120">Questo in genere indica che il sistema operativo guest si è arrestato in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="2e0a7-120">This usually indicates that the guest operating system has crashed.</span></span>

</dd> <dt>

<span data-ttu-id="2e0a7-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**\_ConfigurationChanged vmVirtualMachineEvent**</span><span class="sxs-lookup"><span data-stu-id="2e0a7-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**vmVirtualMachineEvent\_ConfigurationChanged**</span></span>
</dt> <dd>

<span data-ttu-id="2e0a7-122">Un valore nella configurazione per questa macchina virtuale è stato modificato</span><span class="sxs-lookup"><span data-stu-id="2e0a7-122">A value in the configuration for this VM has changed</span></span>

</dd> <dt>

<span data-ttu-id="2e0a7-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**\_EnhancedVideoModeChanged vmVirtualMachineEvent**</span><span class="sxs-lookup"><span data-stu-id="2e0a7-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmVirtualMachineEvent\_EnhancedVideoModeChanged**</span></span>
</dt> <dd>

<span data-ttu-id="2e0a7-124">È stata modificata la modalità video di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2e0a7-124">A VM's video mode has changed.</span></span>

</dd> <dt>

<span data-ttu-id="2e0a7-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**\_AdditionsUninstalled vmVirtualMachineEvent**</span><span class="sxs-lookup"><span data-stu-id="2e0a7-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmVirtualMachineEvent\_AdditionsUninstalled**</span></span>
</dt> <dd>

<span data-ttu-id="2e0a7-126">I componenti di integrazione sono stati disinstallati dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2e0a7-126">Integration components have been uninstalled from the VM.</span></span>

</dd> <dt>

<span data-ttu-id="2e0a7-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**\_AdditionsAvailable vmVirtualMachineEvent**</span><span class="sxs-lookup"><span data-stu-id="2e0a7-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmVirtualMachineEvent\_AdditionsAvailable**</span></span>
</dt> <dd>

<span data-ttu-id="2e0a7-128">L'integrazione è disponibile nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="2e0a7-128">Integration are available in the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="2e0a7-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**\_GuestShutdown vmVirtualMachineEvent**</span><span class="sxs-lookup"><span data-stu-id="2e0a7-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_GuestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="2e0a7-130">È in corso l'arresto di un sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="2e0a7-130">A guest operating system is shutting down.</span></span>

</dd> <dt>

<span data-ttu-id="2e0a7-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**\_GuestLogoff vmVirtualMachineEvent**</span><span class="sxs-lookup"><span data-stu-id="2e0a7-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmVirtualMachineEvent\_GuestLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="2e0a7-132">Un utente si è disconnesso dal sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="2e0a7-132">A user logged off from the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="2e0a7-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**\_DiskOutOfSpace vmVirtualMachineEvent**</span><span class="sxs-lookup"><span data-stu-id="2e0a7-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmVirtualMachineEvent\_DiskOutOfSpace**</span></span>
</dt> <dd>

<span data-ttu-id="2e0a7-134">Uno spazio su disco richiesto dalla macchina virtuale è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="2e0a7-134">A disk required by the VM is low on space.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e0a7-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e0a7-135">Requirements</span></span>



| <span data-ttu-id="2e0a7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e0a7-136">Requirement</span></span> | <span data-ttu-id="2e0a7-137">Valore</span><span class="sxs-lookup"><span data-stu-id="2e0a7-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e0a7-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e0a7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2e0a7-139">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2e0a7-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e0a7-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e0a7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2e0a7-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2e0a7-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2e0a7-142">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2e0a7-142">End of client support</span></span><br/>    | <span data-ttu-id="2e0a7-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2e0a7-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2e0a7-144">Prodotto</span><span class="sxs-lookup"><span data-stu-id="2e0a7-144">Product</span></span><br/>                  | <span data-ttu-id="2e0a7-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2e0a7-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2e0a7-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e0a7-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e0a7-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e0a7-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e0a7-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e0a7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e0a7-149">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="2e0a7-149">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

