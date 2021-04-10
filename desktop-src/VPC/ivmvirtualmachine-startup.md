---
title: Metodo di avvio IVMVirtualMachine (VPCCOMInterfaces. h)
description: Avvia la macchina virtuale dallo stato non inizializzato o salvato.
ms.assetid: 82f9b6f1-99b1-4402-93f5-b4aa3520a505
keywords:
- Metodo di avvio Virtual PC
- Metodo di avvio Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo Startup
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a45e0952fc1a17fc6ba2ea639f2ee87f7b9ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964707"
---
# <a name="ivmvirtualmachinestartup-method"></a><span data-ttu-id="6357a-106">Metodo IVMVirtualMachine:: Startup</span><span class="sxs-lookup"><span data-stu-id="6357a-106">IVMVirtualMachine::Startup method</span></span>

<span data-ttu-id="6357a-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6357a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6357a-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6357a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6357a-109">Avvia la macchina virtuale dallo stato non inizializzato o salvato.</span><span class="sxs-lookup"><span data-stu-id="6357a-109">Starts the virtual machine from either the uninitialized or saved state.</span></span>

## <a name="syntax"></a><span data-ttu-id="6357a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6357a-110">Syntax</span></span>


```C++
HRESULT Startup(
  [out, retval] IVMTask **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="6357a-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="6357a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6357a-112">*startupTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6357a-112">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6357a-113">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia dello stato di completamento della sequenza di avvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6357a-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's startup sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6357a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6357a-114">Return value</span></span>

<span data-ttu-id="6357a-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="6357a-115">This method can return one of these values.</span></span>



| <span data-ttu-id="6357a-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="6357a-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="6357a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6357a-117">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6357a-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6357a-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="6357a-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="6357a-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="6357a-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6357a-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="6357a-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="6357a-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="6357a-122"><dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="6357a-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="6357a-123">Il chiamante deve disporre delle autorizzazioni di accesso Execute per avviare questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6357a-123">The caller must have execute access permissions to start this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="6357a-124"><dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="6357a-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="6357a-125">L'operazione non è stata completata in modo tempestivo.</span><span class="sxs-lookup"><span data-stu-id="6357a-125">The operation did not complete in a timely manner.</span></span><br/>                             |
| <dl> <span data-ttu-id="6357a-126"><dt>**Macchina virtuale \_ E \_ out \_ of \_ Resource**</dt> <dt>0xA0040203</dt></span><span class="sxs-lookup"><span data-stu-id="6357a-126"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="6357a-127">Risorse host insufficienti.</span><span class="sxs-lookup"><span data-stu-id="6357a-127">There are not enough host resources.</span></span><br/>                                           |
| <dl> <span data-ttu-id="6357a-128"><dt>**Macchina virtuale \_ E \_ un \_ numero \_ eccessivo di VM**</dt> <dt>0xA0040204</dt></span><span class="sxs-lookup"><span data-stu-id="6357a-128"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="6357a-129">Troppe macchine virtuali attive.</span><span class="sxs-lookup"><span data-stu-id="6357a-129">There are too many active virtual machines.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6357a-130"><dt>**Macchina virtuale \_ E \_ macchina virtuale \_ che esegue**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="6357a-130"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="6357a-131">La macchina virtuale è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6357a-131">The virtual machine is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="6357a-132"><dt>**Macchina virtuale \_ E \_ 0xA00400687 padre \_ modificato**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6357a-132"><dt>**VM\_E\_PARENT\_MODIFIED**</dt> <dt>0xA00400687</dt></span></span> </dl>                    | <span data-ttu-id="6357a-133">Non è possibile avviare la macchina virtuale perché il VHD padre è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="6357a-133">The virtual machine cannot be started as the parent VHD has been modified.</span></span><br/>     |
| <dl> <span data-ttu-id="6357a-134"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6357a-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="6357a-135">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="6357a-135">An unexpected error has occurred.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="6357a-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="6357a-136">Remarks</span></span>

<span data-ttu-id="6357a-137">Se la macchina virtuale viene salvata, verrà ripristinata dallo stato salvato.</span><span class="sxs-lookup"><span data-stu-id="6357a-137">If the virtual machine is saved, it will be restored from the saved state.</span></span>

<span data-ttu-id="6357a-138">I valori seguenti possono essere restituiti tramite la proprietà [**Error**](ivmtask-error.md) dell'oggetto [**IVMTask**](ivmtask.md) restituito.</span><span class="sxs-lookup"><span data-stu-id="6357a-138">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="6357a-139">Codice [**errore**](ivmtask-error.md) /valore</span><span class="sxs-lookup"><span data-stu-id="6357a-139">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="6357a-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6357a-140">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="6357a-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span><span class="sxs-lookup"><span data-stu-id="6357a-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="6357a-142">L'hardware non supporta la virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="6357a-142">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="6357a-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span><span class="sxs-lookup"><span data-stu-id="6357a-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="6357a-144">La virtualizzazione hardware è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="6357a-144">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="6357a-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span><span class="sxs-lookup"><span data-stu-id="6357a-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="6357a-146">Sono installati sia Virtual PC 2007 che Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="6357a-146">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="6357a-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span><span class="sxs-lookup"><span data-stu-id="6357a-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="6357a-148">È installato altro software di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="6357a-148">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="6357a-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span><span class="sxs-lookup"><span data-stu-id="6357a-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="6357a-150">Risorse host insufficienti.</span><span class="sxs-lookup"><span data-stu-id="6357a-150">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="6357a-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6357a-151">Requirements</span></span>



| <span data-ttu-id="6357a-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="6357a-152">Requirement</span></span> | <span data-ttu-id="6357a-153">Valore</span><span class="sxs-lookup"><span data-stu-id="6357a-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6357a-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6357a-154">Minimum supported client</span></span><br/> | <span data-ttu-id="6357a-155">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6357a-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6357a-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6357a-156">Minimum supported server</span></span><br/> | <span data-ttu-id="6357a-157">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6357a-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6357a-158">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6357a-158">End of client support</span></span><br/>    | <span data-ttu-id="6357a-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6357a-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6357a-160">Prodotto</span><span class="sxs-lookup"><span data-stu-id="6357a-160">Product</span></span><br/>                  | <span data-ttu-id="6357a-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6357a-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6357a-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6357a-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="6357a-163"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6357a-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6357a-164">IID</span><span class="sxs-lookup"><span data-stu-id="6357a-164">IID</span></span><br/>                      | <span data-ttu-id="6357a-165">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="6357a-165">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6357a-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6357a-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6357a-167">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="6357a-167">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

