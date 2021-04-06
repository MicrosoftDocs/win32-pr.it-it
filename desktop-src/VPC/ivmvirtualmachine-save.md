---
title: Metodo Save IVMVirtualMachine (VPCCOMInterfaces. h)
description: Salva lo stato della macchina virtuale (VM).
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Salva il metodo Virtual PC
- Salva metodo Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo Save
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Save
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b4dbe18b89f107657d67fb7e7b90e024b01383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742882"
---
# <a name="ivmvirtualmachinesave-method"></a><span data-ttu-id="ad21e-106">Metodo IVMVirtualMachine:: Save</span><span class="sxs-lookup"><span data-stu-id="ad21e-106">IVMVirtualMachine::Save method</span></span>

<span data-ttu-id="ad21e-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ad21e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ad21e-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ad21e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ad21e-109">Salva lo stato della macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="ad21e-109">Saves the virtual machine (VM) state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad21e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad21e-110">Syntax</span></span>


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a><span data-ttu-id="ad21e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad21e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad21e-112">*saveTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ad21e-112">*saveTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ad21e-113">Oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia dello stato di avanzamento della sequenza di salvataggio dello stato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad21e-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's state saving sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad21e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad21e-114">Return value</span></span>

<span data-ttu-id="ad21e-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="ad21e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="ad21e-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad21e-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="ad21e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad21e-117">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad21e-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ad21e-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="ad21e-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ad21e-119">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="ad21e-120"><dt>**E \_ ERRORE**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="ad21e-120"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="ad21e-121">Non è stato possibile salvare la macchina virtuale perché i file modifiche disco sono stati contrassegnati per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="ad21e-121">The VM could not be saved because the undo disks were marked for deletion.</span></span><br/>    |
| <dl> <span data-ttu-id="ad21e-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ad21e-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="ad21e-123">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="ad21e-123">The parameter is **NULL**.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="ad21e-124"><dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="ad21e-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="ad21e-125">Il chiamante deve disporre delle autorizzazioni di accesso Execute per salvare lo stato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad21e-125">The caller must have execute access permissions to save the state of this VM.</span></span><br/> |
| <dl> <span data-ttu-id="ad21e-126"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="ad21e-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="ad21e-127">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ad21e-127">The VM is not running.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ad21e-128"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ad21e-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="ad21e-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="ad21e-129">An unexpected error has occurred.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="ad21e-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad21e-130">Remarks</span></span>

<span data-ttu-id="ad21e-131">La macchina virtuale viene spenta al completamento dell'attività di **salvataggio** .</span><span class="sxs-lookup"><span data-stu-id="ad21e-131">The VM is turned off when the **Save** task reaches completion.</span></span> <span data-ttu-id="ad21e-132">La proprietà [**IVMVirtualMachine:: state**](ivmvirtualmachine-state.md) conterrà **vmVMState \_ Saving** mentre è in corso il salvataggio, seguito da **vmVMState \_ salvato** al termine del salvataggio e la macchina virtuale è disattivata.</span><span class="sxs-lookup"><span data-stu-id="ad21e-132">The [**IVMVirtualMachine::State**](ivmvirtualmachine-state.md) property will contain **vmVMState\_Saving** while the save is in progress, followed by **vmVMState\_Saved** when the save has completed and the VM is turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad21e-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad21e-133">Requirements</span></span>



| <span data-ttu-id="ad21e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad21e-134">Requirement</span></span> | <span data-ttu-id="ad21e-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ad21e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad21e-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad21e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ad21e-137">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ad21e-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ad21e-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad21e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ad21e-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ad21e-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ad21e-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ad21e-140">End of client support</span></span><br/>    | <span data-ttu-id="ad21e-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ad21e-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ad21e-142">Prodotto</span><span class="sxs-lookup"><span data-stu-id="ad21e-142">Product</span></span><br/>                  | <span data-ttu-id="ad21e-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ad21e-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ad21e-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad21e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad21e-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad21e-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ad21e-146">IID</span><span class="sxs-lookup"><span data-stu-id="ad21e-146">IID</span></span><br/>                      | <span data-ttu-id="ad21e-147">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="ad21e-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ad21e-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad21e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad21e-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="ad21e-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

