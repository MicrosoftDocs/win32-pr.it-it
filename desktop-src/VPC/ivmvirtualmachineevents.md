---
title: Interfaccia IVMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Definisce l'interfaccia evento in uscita per l'interfaccia IVMVirtualMachine.
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- Interfaccia IVMVirtualMachineEvents Virtual PC
- Interfaccia IVMVirtualMachineEvents Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2ded96f5a39a520d3b5a712e63fbb0a65d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478670"
---
# <a name="ivmvirtualmachineevents-interface"></a><span data-ttu-id="b04d7-105">Interfaccia IVMVirtualMachineEvents</span><span class="sxs-lookup"><span data-stu-id="b04d7-105">IVMVirtualMachineEvents interface</span></span>

<span data-ttu-id="b04d7-106">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b04d7-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b04d7-107">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b04d7-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b04d7-108">Definisce l'interfaccia evento in uscita per l'interfaccia [**IVMVirtualMachine**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="b04d7-108">Defines the outgoing event interface for the [**IVMVirtualMachine**](ivmvirtualmachine.md) interface.</span></span> <span data-ttu-id="b04d7-109">Il client implementa questi metodi per ricevere gli eventi inviati da [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="b04d7-109">The client implements these methods to receive events sent from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="members"></a><span data-ttu-id="b04d7-110">Membri</span><span class="sxs-lookup"><span data-stu-id="b04d7-110">Members</span></span>

<span data-ttu-id="b04d7-111">L'interfaccia **IVMVirtualMachineEvents** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b04d7-111">The **IVMVirtualMachineEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b04d7-112">**IVMVirtualMachineEvents** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b04d7-112">**IVMVirtualMachineEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="b04d7-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="b04d7-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b04d7-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="b04d7-114">Methods</span></span>

<span data-ttu-id="b04d7-115">L'interfaccia **IVMVirtualMachineEvents** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b04d7-115">The **IVMVirtualMachineEvents** interface has these methods.</span></span>



| <span data-ttu-id="b04d7-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="b04d7-116">Method</span></span>                                                                                   | <span data-ttu-id="b04d7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b04d7-117">Description</span></span>                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b04d7-118">**OnAdditionsAvailable**</span><span class="sxs-lookup"><span data-stu-id="b04d7-118">**OnAdditionsAvailable**</span></span>](ivmvirtualmachineevents-onadditionsavailable.md)             | <span data-ttu-id="b04d7-119">Riceve la notifica che i componenti di integrazione sono disponibili in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b04d7-119">Receives notification that integration components are available in a virtual machine.</span></span><br/>                                                |
| [<span data-ttu-id="b04d7-120">**OnAdditionsUninstalled**</span><span class="sxs-lookup"><span data-stu-id="b04d7-120">**OnAdditionsUninstalled**</span></span>](ivmvirtualmachineevents-onadditionsuninstalled.md)         | <span data-ttu-id="b04d7-121">Riceve una notifica di disinstallazione dei componenti di integrazione in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b04d7-121">Receives notification that integration components are uninstalled in a virtual machine.</span></span><br/>                                              |
| [<span data-ttu-id="b04d7-122">**OnConfigurationChanged**</span><span class="sxs-lookup"><span data-stu-id="b04d7-122">**OnConfigurationChanged**</span></span>](ivmvirtualmachineevents-onconfigurationchanged.md)         | <span data-ttu-id="b04d7-123">Riceve la notifica che un valore nella configurazione per questa macchina virtuale è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="b04d7-123">Receives notification that a value in the configuration for this virtual machine has changed.</span></span><br/>                                        |
| [<span data-ttu-id="b04d7-124">**OnDiskOutOfSpace**</span><span class="sxs-lookup"><span data-stu-id="b04d7-124">**OnDiskOutOfSpace**</span></span>](ivmvirtualmachineevents-ondiskoutofspace.md)                     | <span data-ttu-id="b04d7-125">Riceve una notifica che indica che un disco richiesto per una macchina virtuale è insufficiente e non è possibile eseguire la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b04d7-125">Receives notification that a disk required for a virtual machine is out of space and the virtual machine is unable to run.</span></span><br/>           |
| [<span data-ttu-id="b04d7-126">**OnEnhancedVideoModeChanged**</span><span class="sxs-lookup"><span data-stu-id="b04d7-126">**OnEnhancedVideoModeChanged**</span></span>](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | <span data-ttu-id="b04d7-127">Riceve una notifica della modifica del supporto di una macchina virtuale per la modalità video avanzata.</span><span class="sxs-lookup"><span data-stu-id="b04d7-127">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span><br/>                                          |
| [<span data-ttu-id="b04d7-128">**OnGuestLogoff**</span><span class="sxs-lookup"><span data-stu-id="b04d7-128">**OnGuestLogoff**</span></span>](ivmvirtualmachineevents-onguestlogoff.md)                           | <span data-ttu-id="b04d7-129">Riceve la notifica che un utente si è disconnesso dal sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="b04d7-129">Receives notification that a user has logged off from the guest operating system.</span></span><br/>                                                    |
| [<span data-ttu-id="b04d7-130">**OnGuestShutdown**</span><span class="sxs-lookup"><span data-stu-id="b04d7-130">**OnGuestShutdown**</span></span>](ivmvirtualmachineevents-onguestshutdown.md)                       | <span data-ttu-id="b04d7-131">Riceve la notifica che il sistema operativo guest è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="b04d7-131">Receives notification that guest operating system has shut down.</span></span><br/>                                                                     |
| [<span data-ttu-id="b04d7-132">**OnHeartbeatStopped**</span><span class="sxs-lookup"><span data-stu-id="b04d7-132">**OnHeartbeatStopped**</span></span>](ivmvirtualmachineevents-onheartbeatstopped.md)                 | <span data-ttu-id="b04d7-133">Riceve una notifica di arresto dell'heartbeat di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b04d7-133">Receives notification that a virtual machine's heartbeat has stopped.</span></span> <span data-ttu-id="b04d7-134">Ciò indica in genere che si è verificato un arresto anomalo del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="b04d7-134">This usually indicates the guest operating system has crashed.</span></span><br/> |
| [<span data-ttu-id="b04d7-135">**OnRequestShutdown**</span><span class="sxs-lookup"><span data-stu-id="b04d7-135">**OnRequestShutdown**</span></span>](ivmvirtualmachineevents-onrequestshutdown.md)                   | <span data-ttu-id="b04d7-136">Riceve la notifica che è stata effettuata una richiesta di arresto.</span><span class="sxs-lookup"><span data-stu-id="b04d7-136">Receives notification that a shutdown request has been made.</span></span><br/>                                                                         |
| [<span data-ttu-id="b04d7-137">**OnReset**</span><span class="sxs-lookup"><span data-stu-id="b04d7-137">**OnReset**</span></span>](ivmvirtualmachineevents-onreset.md)                                       | <span data-ttu-id="b04d7-138">Riceve la notifica che una macchina virtuale è stata reimpostata.</span><span class="sxs-lookup"><span data-stu-id="b04d7-138">Receives notification that a virtual machine has been reset.</span></span><br/>                                                                         |
| [<span data-ttu-id="b04d7-139">**OnStateChange**</span><span class="sxs-lookup"><span data-stu-id="b04d7-139">**OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)                           | <span data-ttu-id="b04d7-140">Riceve una notifica che lo stato di una macchina virtuale è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="b04d7-140">Receives notification that a virtual machine's state has changed.</span></span><br/>                                                                    |
| [<span data-ttu-id="b04d7-141">**OnTripleFault**</span><span class="sxs-lookup"><span data-stu-id="b04d7-141">**OnTripleFault**</span></span>](ivmvirtualmachineevents-ontriplefault.md)                           | <span data-ttu-id="b04d7-142">Riceve una notifica che una macchina virtuale presenta tre errori.</span><span class="sxs-lookup"><span data-stu-id="b04d7-142">Receives notification that a virtual machine has triple-faulted.</span></span><br/>                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="b04d7-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b04d7-143">Requirements</span></span>



| <span data-ttu-id="b04d7-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="b04d7-144">Requirement</span></span> | <span data-ttu-id="b04d7-145">Valore</span><span class="sxs-lookup"><span data-stu-id="b04d7-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b04d7-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b04d7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b04d7-147">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b04d7-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b04d7-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b04d7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b04d7-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b04d7-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b04d7-150">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b04d7-150">End of client support</span></span><br/>    | <span data-ttu-id="b04d7-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b04d7-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b04d7-152">Prodotto</span><span class="sxs-lookup"><span data-stu-id="b04d7-152">Product</span></span><br/>                  | <span data-ttu-id="b04d7-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b04d7-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b04d7-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b04d7-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="b04d7-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b04d7-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b04d7-156">IID</span><span class="sxs-lookup"><span data-stu-id="b04d7-156">IID</span></span><br/>                      | <span data-ttu-id="b04d7-157">DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="b04d7-157">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



 

