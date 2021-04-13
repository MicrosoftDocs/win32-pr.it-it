---
title: Interfaccia IVMTask (VPCCOMInterfaces. h)
description: Utilizzare l'interfaccia IVMTask per monitorare e controllare le attività asincrone per diversi metodi COM.
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- Interfaccia IVMTask Virtual PC
- Interfaccia IVMTask Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMTask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e1d519471fe5b1fc32cb6365d1139243c85538
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518382"
---
# <a name="ivmtask-interface"></a><span data-ttu-id="59c26-105">Interfaccia IVMTask</span><span class="sxs-lookup"><span data-stu-id="59c26-105">IVMTask interface</span></span>

<span data-ttu-id="59c26-106">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="59c26-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="59c26-107">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="59c26-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="59c26-108">Utilizzare l'interfaccia **IVMTask** per monitorare e controllare le attività asincrone per diversi metodi com.</span><span class="sxs-lookup"><span data-stu-id="59c26-108">Use the **IVMTask** interface to monitor and control asynchronous tasks for various COM methods.</span></span>

## <a name="members"></a><span data-ttu-id="59c26-109">Membri</span><span class="sxs-lookup"><span data-stu-id="59c26-109">Members</span></span>

<span data-ttu-id="59c26-110">L'interfaccia **IVMTask** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="59c26-110">The **IVMTask** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="59c26-111">**IVMTask** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="59c26-111">**IVMTask** also has these types of members:</span></span>

-   [<span data-ttu-id="59c26-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="59c26-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="59c26-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="59c26-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="59c26-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="59c26-114">Methods</span></span>

<span data-ttu-id="59c26-115">L'interfaccia **IVMTask** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="59c26-115">The **IVMTask** interface has these methods.</span></span>



| <span data-ttu-id="59c26-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="59c26-116">Method</span></span>                                                 | <span data-ttu-id="59c26-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59c26-117">Description</span></span>                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59c26-118">**Annulla**</span><span class="sxs-lookup"><span data-stu-id="59c26-118">**Cancel**</span></span>](ivmtask-cancel.md)                       | <span data-ttu-id="59c26-119">Annulla l'attività.</span><span class="sxs-lookup"><span data-stu-id="59c26-119">Cancels the task.</span></span><br/>                                                                |
| [<span data-ttu-id="59c26-120">**WaitForCompletion**</span><span class="sxs-lookup"><span data-stu-id="59c26-120">**WaitForCompletion**</span></span>](ivmtask-waitforcompletion.md) | <span data-ttu-id="59c26-121">Attende il completamento dell'attività o l'intervallo di timeout specificato.</span><span class="sxs-lookup"><span data-stu-id="59c26-121">Waits for the task to complete or for the specified time-out interval to elapse.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="59c26-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="59c26-122">Properties</span></span>

<span data-ttu-id="59c26-123">L'interfaccia **IVMTask** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="59c26-123">The **IVMTask** interface has these properties.</span></span>



| <span data-ttu-id="59c26-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="59c26-124">Property</span></span>                                                        | <span data-ttu-id="59c26-125">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="59c26-125">Access type</span></span>          | <span data-ttu-id="59c26-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59c26-126">Description</span></span>                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="59c26-127">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="59c26-127">**Description**</span></span>](ivmtask-description.md)<br/>           | <span data-ttu-id="59c26-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="59c26-128">Read-only</span></span><br/> | <span data-ttu-id="59c26-129">Descrizione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="59c26-129">A description of the task.</span></span><br/>                              |
| [<span data-ttu-id="59c26-130">**Errore**</span><span class="sxs-lookup"><span data-stu-id="59c26-130">**Error**</span></span>](ivmtask-error.md)<br/>                       | <span data-ttu-id="59c26-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="59c26-131">Read-only</span></span><br/> | <span data-ttu-id="59c26-132">Errore registrato per questa attività.</span><span class="sxs-lookup"><span data-stu-id="59c26-132">The error recorded for this task.</span></span><br/>                       |
| [<span data-ttu-id="59c26-133">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="59c26-133">**ErrorDescription**</span></span>](ivmtask-errordescription.md)<br/> | <span data-ttu-id="59c26-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="59c26-134">Read-only</span></span><br/> | <span data-ttu-id="59c26-135">Descrizione dell'errore localizzata registrata per questa attività.</span><span class="sxs-lookup"><span data-stu-id="59c26-135">The localized error description recorded for this task.</span></span><br/> |
| [<span data-ttu-id="59c26-136">**ID**</span><span class="sxs-lookup"><span data-stu-id="59c26-136">**ID**</span></span>](ivmtask-id.md)<br/>                             | <span data-ttu-id="59c26-137">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="59c26-137">Read-only</span></span><br/> | <span data-ttu-id="59c26-138">Identificatore univoco per questa attività.</span><span class="sxs-lookup"><span data-stu-id="59c26-138">A unique identifier for this task.</span></span><br/>                      |
| [<span data-ttu-id="59c26-139">**IsCancelable**</span><span class="sxs-lookup"><span data-stu-id="59c26-139">**IsCancelable**</span></span>](ivmtask-iscancelable.md)<br/>         | <span data-ttu-id="59c26-140">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="59c26-140">Read-only</span></span><br/> | <span data-ttu-id="59c26-141">Indica se l'attività può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="59c26-141">Indicates whether the task can be canceled.</span></span><br/>             |
| [<span data-ttu-id="59c26-142">**IsComplete**</span><span class="sxs-lookup"><span data-stu-id="59c26-142">**IsComplete**</span></span>](ivmtask-iscomplete.md)<br/>             | <span data-ttu-id="59c26-143">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="59c26-143">Read-only</span></span><br/> | <span data-ttu-id="59c26-144">Indica se l'attività è stata completata.</span><span class="sxs-lookup"><span data-stu-id="59c26-144">Indicates whether the task has completed.</span></span><br/>               |
| [<span data-ttu-id="59c26-145">**PercentCompleted**</span><span class="sxs-lookup"><span data-stu-id="59c26-145">**PercentCompleted**</span></span>](ivmtask-percentcompleted.md)<br/> | <span data-ttu-id="59c26-146">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="59c26-146">Read-only</span></span><br/> | <span data-ttu-id="59c26-147">Percentuale di completamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="59c26-147">The completion percentage of the task.</span></span><br/>                  |
| [<span data-ttu-id="59c26-148">**Risultato**</span><span class="sxs-lookup"><span data-stu-id="59c26-148">**Result**</span></span>](ivmtask-result.md)<br/>                     | <span data-ttu-id="59c26-149">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="59c26-149">Read-only</span></span><br/> | <span data-ttu-id="59c26-150">Risultato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="59c26-150">The result of the task.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="59c26-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="59c26-151">Remarks</span></span>

<span data-ttu-id="59c26-152">Un oggetto **IVMTask** viene restituito da metodi che potrebbero richiedere una quantità di tempo significativa per il completamento.</span><span class="sxs-lookup"><span data-stu-id="59c26-152">An **IVMTask** object is returned by methods that could potentially require a significant amount of time to complete.</span></span> <span data-ttu-id="59c26-153">Ciò consente all'applicazione di monitorare lo stato di avanzamento dell'operazione desiderata senza forzare il blocco dell'ulteriore esecuzione in attesa del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="59c26-153">This allows the application to monitor the progress of the desired operation without forcing it to block further execution while waiting for the completion of the operation.</span></span>

<span data-ttu-id="59c26-154">I metodi seguenti restituiscono un oggetto **IVMTask** che può essere usato per tenere traccia dello stato di avanzamento:</span><span class="sxs-lookup"><span data-stu-id="59c26-154">The following methods return an **IVMTask** object that can be used to track progress:</span></span>

-   [<span data-ttu-id="59c26-155">**IVMGuestOS:: disconnessione**</span><span class="sxs-lookup"><span data-stu-id="59c26-155">**IVMGuestOS::Logoff**</span></span>](ivmguestos-logoff.md)
-   [<span data-ttu-id="59c26-156">**IVMGuestOS:: Restart**</span><span class="sxs-lookup"><span data-stu-id="59c26-156">**IVMGuestOS::Restart**</span></span>](ivmguestos-restart.md)
-   [<span data-ttu-id="59c26-157">**IVMGuestOS:: Shutdown**</span><span class="sxs-lookup"><span data-stu-id="59c26-157">**IVMGuestOS::Shutdown**</span></span>](ivmguestos-shutdown.md)
-   [<span data-ttu-id="59c26-158">**IVMHardDisk:: Compact**</span><span class="sxs-lookup"><span data-stu-id="59c26-158">**IVMHardDisk::Compact**</span></span>](ivmharddisk-compact.md)
-   [<span data-ttu-id="59c26-159">**IVMHardDisk:: Convert**</span><span class="sxs-lookup"><span data-stu-id="59c26-159">**IVMHardDisk::Convert**</span></span>](ivmharddisk-convert.md)
-   [<span data-ttu-id="59c26-160">**IVMHardDisk:: merge**</span><span class="sxs-lookup"><span data-stu-id="59c26-160">**IVMHardDisk::Merge**</span></span>](ivmharddisk-merge.md)
-   [<span data-ttu-id="59c26-161">**IVMHardDisk::MergeTo**</span><span class="sxs-lookup"><span data-stu-id="59c26-161">**IVMHardDisk::MergeTo**</span></span>](ivmharddisk-mergeto.md)
-   [<span data-ttu-id="59c26-162">**IVMVirtualMachine::MergeUndoDisks**</span><span class="sxs-lookup"><span data-stu-id="59c26-162">**IVMVirtualMachine::MergeUndoDisks**</span></span>](ivmvirtualmachine-mergeundodisks.md)
-   [<span data-ttu-id="59c26-163">**IVMVirtualMachine:: Reset**</span><span class="sxs-lookup"><span data-stu-id="59c26-163">**IVMVirtualMachine::Reset**</span></span>](ivmvirtualmachine-reset.md)
-   [<span data-ttu-id="59c26-164">**IVMVirtualMachine:: Save**</span><span class="sxs-lookup"><span data-stu-id="59c26-164">**IVMVirtualMachine::Save**</span></span>](ivmvirtualmachine-save.md)
-   [<span data-ttu-id="59c26-165">**IVMVirtualMachine:: Startup**</span><span class="sxs-lookup"><span data-stu-id="59c26-165">**IVMVirtualMachine::Startup**</span></span>](ivmvirtualmachine-startup.md)
-   [<span data-ttu-id="59c26-166">**IVMVirtualMachine:: Startup2**</span><span class="sxs-lookup"><span data-stu-id="59c26-166">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
-   [<span data-ttu-id="59c26-167">**IVMVirtualMachine:: bivio**</span><span class="sxs-lookup"><span data-stu-id="59c26-167">**IVMVirtualMachine::TurnOff**</span></span>](ivmvirtualmachine-turnoff.md)
-   [<span data-ttu-id="59c26-168">**IVMVirtualPC::CreateDifferencingVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="59c26-168">**IVMVirtualPC::CreateDifferencingVirtualHardDisk**</span></span>](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [<span data-ttu-id="59c26-169">**IVMVirtualPC::CreateDynamicVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="59c26-169">**IVMVirtualPC::CreateDynamicVirtualHardDisk**</span></span>](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [<span data-ttu-id="59c26-170">**IVMVirtualPC::CreateFixedVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="59c26-170">**IVMVirtualPC::CreateFixedVirtualHardDisk**</span></span>](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a><span data-ttu-id="59c26-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59c26-171">Requirements</span></span>



| <span data-ttu-id="59c26-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="59c26-172">Requirement</span></span> | <span data-ttu-id="59c26-173">Valore</span><span class="sxs-lookup"><span data-stu-id="59c26-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="59c26-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59c26-174">Minimum supported client</span></span><br/> | <span data-ttu-id="59c26-175">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="59c26-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59c26-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59c26-176">Minimum supported server</span></span><br/> | <span data-ttu-id="59c26-177">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="59c26-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="59c26-178">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="59c26-178">End of client support</span></span><br/>    | <span data-ttu-id="59c26-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59c26-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="59c26-180">Prodotto</span><span class="sxs-lookup"><span data-stu-id="59c26-180">Product</span></span><br/>                  | <span data-ttu-id="59c26-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="59c26-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="59c26-182">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59c26-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="59c26-183"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="59c26-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="59c26-184">IID</span><span class="sxs-lookup"><span data-stu-id="59c26-184">IID</span></span><br/>                      | <span data-ttu-id="59c26-185">IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="59c26-185">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



 

