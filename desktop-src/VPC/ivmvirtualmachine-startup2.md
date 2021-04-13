---
title: Metodo IVMVirtualMachine Startup2 (VPCCOMInterfaces. h)
description: Avvia la macchina virtuale dallo stato non inizializzato o salvato con opzioni avanzate.
ms.assetid: c2679ea1-bbd5-42dc-9326-2019ad99554c
keywords:
- Metodo Startup2 Virtual PC
- Metodo Startup2 Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo Startup2
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b40149b0b21abc126261d8b1ddec34b9948371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400665"
---
# <a name="ivmvirtualmachinestartup2-method"></a><span data-ttu-id="d1dee-106">Metodo IVMVirtualMachine:: Startup2</span><span class="sxs-lookup"><span data-stu-id="d1dee-106">IVMVirtualMachine::Startup2 method</span></span>

<span data-ttu-id="d1dee-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d1dee-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d1dee-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d1dee-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d1dee-109">Avvia la macchina virtuale (VM) dallo stato non inizializzato o salvato, con opzioni avanzate.</span><span class="sxs-lookup"><span data-stu-id="d1dee-109">Starts the virtual machine (VM) from either the uninitialized or saved state, with advanced options.</span></span>

<span data-ttu-id="d1dee-110">Questo metodo fornisce un meccanismo per avviare una macchina virtuale con un disco differenze anche se il timestamp del disco padre è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="d1dee-110">This method provides a mechanism to start a VM with a differencing disk even if the parent disk's timestamp has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1dee-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1dee-111">Syntax</span></span>


```C++
HRESULT Startup2(
  [in]          VMStartupOption startupOption,
  [out, retval] IVMTask         **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="d1dee-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1dee-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1dee-113">*startupOption* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1dee-113">*startupOption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1dee-114">Opzione di avvio avanzata.</span><span class="sxs-lookup"><span data-stu-id="d1dee-114">The advanced startup option.</span></span> <span data-ttu-id="d1dee-115">I valori possibili sono dall'enumerazione [**VMStartupOption**](vmstartupoption.md) .</span><span class="sxs-lookup"><span data-stu-id="d1dee-115">The possible values are from the [**VMStartupOption**](vmstartupoption.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="d1dee-116">*startupTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d1dee-116">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d1dee-117">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia dello stato di avanzamento della sequenza di avvio.</span><span class="sxs-lookup"><span data-stu-id="d1dee-117">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the start sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1dee-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1dee-118">Return value</span></span>

<span data-ttu-id="d1dee-119">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="d1dee-119">This method can return one of these values.</span></span>



| <span data-ttu-id="d1dee-120">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1dee-120">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="d1dee-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1dee-121">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1dee-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d1dee-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="d1dee-123">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d1dee-123">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d1dee-124"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d1dee-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="d1dee-125">Il parametro *startupOption* non è valido.</span><span class="sxs-lookup"><span data-stu-id="d1dee-125">The *startupOption* parameter is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="d1dee-126"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d1dee-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="d1dee-127">Il parametro *startupTask* è **null**.</span><span class="sxs-lookup"><span data-stu-id="d1dee-127">The *startupTask* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="d1dee-128"><dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="d1dee-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="d1dee-129">Il chiamante deve avere le autorizzazioni di accesso Execute per avviare questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1dee-129">The caller must have execute access permissions to start this VM.</span></span><br/> |
| <dl> <span data-ttu-id="d1dee-130"><dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="d1dee-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="d1dee-131">L'operazione non è stata completata in modo tempestivo.</span><span class="sxs-lookup"><span data-stu-id="d1dee-131">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="d1dee-132"><dt>**Macchina virtuale \_ E \_ out \_ of \_ Resource**</dt> <dt>0xA0040203</dt></span><span class="sxs-lookup"><span data-stu-id="d1dee-132"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="d1dee-133">Risorse host insufficienti.</span><span class="sxs-lookup"><span data-stu-id="d1dee-133">There are not enough host resources.</span></span><br/>                              |
| <dl> <span data-ttu-id="d1dee-134"><dt>**Macchina virtuale \_ E \_ un \_ numero \_ eccessivo di VM**</dt> <dt>0xA0040204</dt></span><span class="sxs-lookup"><span data-stu-id="d1dee-134"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="d1dee-135">Troppe macchine virtuali attive.</span><span class="sxs-lookup"><span data-stu-id="d1dee-135">There are too many active VMs.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d1dee-136"><dt>**Macchina virtuale \_ E \_ macchina virtuale \_ che esegue**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="d1dee-136"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="d1dee-137">La macchina virtuale è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d1dee-137">The VM is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="d1dee-138"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d1dee-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="d1dee-139">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d1dee-139">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="d1dee-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1dee-140">Remarks</span></span>

<span data-ttu-id="d1dee-141">I valori seguenti possono essere restituiti tramite la proprietà [**Error**](ivmtask-error.md) dell'oggetto [**IVMTask**](ivmtask.md) restituito.</span><span class="sxs-lookup"><span data-stu-id="d1dee-141">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="d1dee-142">Codice [**errore**](ivmtask-error.md) /valore</span><span class="sxs-lookup"><span data-stu-id="d1dee-142">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="d1dee-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1dee-143">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="d1dee-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span><span class="sxs-lookup"><span data-stu-id="d1dee-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="d1dee-145">L'hardware non supporta la virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d1dee-145">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="d1dee-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span><span class="sxs-lookup"><span data-stu-id="d1dee-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="d1dee-147">La virtualizzazione hardware è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="d1dee-147">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="d1dee-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span><span class="sxs-lookup"><span data-stu-id="d1dee-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="d1dee-149">Sono installati sia Virtual PC 2007 che Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="d1dee-149">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="d1dee-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span><span class="sxs-lookup"><span data-stu-id="d1dee-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="d1dee-151">È installato altro software di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d1dee-151">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="d1dee-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span><span class="sxs-lookup"><span data-stu-id="d1dee-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="d1dee-153">Risorse host insufficienti.</span><span class="sxs-lookup"><span data-stu-id="d1dee-153">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="d1dee-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1dee-154">Requirements</span></span>



| <span data-ttu-id="d1dee-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1dee-155">Requirement</span></span> | <span data-ttu-id="d1dee-156">Valore</span><span class="sxs-lookup"><span data-stu-id="d1dee-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1dee-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1dee-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d1dee-158">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d1dee-158">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1dee-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1dee-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d1dee-160">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d1dee-160">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d1dee-161">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d1dee-161">End of client support</span></span><br/>    | <span data-ttu-id="d1dee-162">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d1dee-162">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d1dee-163">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d1dee-163">Product</span></span><br/>                  | <span data-ttu-id="d1dee-164">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1dee-164">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d1dee-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1dee-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1dee-166"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1dee-166"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d1dee-167">IID</span><span class="sxs-lookup"><span data-stu-id="d1dee-167">IID</span></span><br/>                      | <span data-ttu-id="d1dee-168">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d1dee-168">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d1dee-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1dee-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1dee-170">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="d1dee-170">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

