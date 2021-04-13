---
title: Metodo IVMVirtualMachine MergeUndoDisks (VPCCOMInterfaces. h)
description: Unisce i file modifiche disco virtuali.
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- Metodo MergeUndoDisks Virtual PC
- Metodo MergeUndoDisks Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo MergeUndoDisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48863bf998ebc02bac93aa9e74d8cdbe07265477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341063"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a><span data-ttu-id="19394-106">Metodo IVMVirtualMachine:: MergeUndoDisks</span><span class="sxs-lookup"><span data-stu-id="19394-106">IVMVirtualMachine::MergeUndoDisks method</span></span>

<span data-ttu-id="19394-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="19394-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="19394-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="19394-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="19394-109">Unisce i file modifiche disco virtuali.</span><span class="sxs-lookup"><span data-stu-id="19394-109">Merges the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="19394-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19394-110">Syntax</span></span>


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="19394-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="19394-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19394-112">*undoMergeTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="19394-112">*undoMergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="19394-113">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia della creazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="19394-113">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19394-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19394-114">Return value</span></span>

<span data-ttu-id="19394-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="19394-115">This method can return one of these values.</span></span>



| <span data-ttu-id="19394-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="19394-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="19394-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19394-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="19394-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="19394-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="19394-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="19394-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="19394-120"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="19394-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="19394-121">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="19394-121">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="19394-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="19394-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="19394-123">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="19394-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="19394-124"><dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="19394-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="19394-125">Il sistema non è in grado di trovare il percorso specificato dal parametro *convertedDiskImagePath* o uno dei dischi padre non è valido.</span><span class="sxs-lookup"><span data-stu-id="19394-125">The system cannot find the path specified by the *convertedDiskImagePath* parameter or one of the parent disks is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="19394-126"><dt>**E \_**</dt> <dt>0x80070005</dt> AccessDenied</span><span class="sxs-lookup"><span data-stu-id="19394-126"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                               | <span data-ttu-id="19394-127">L'utente corrente non dispone di accesso sufficiente al file padre.</span><span class="sxs-lookup"><span data-stu-id="19394-127">The current user has insufficient access to the parent file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="19394-128"><dt>**E \_ GESTISCi**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="19394-128"><dt>**E\_HANDLE**</dt> <dt>0x80070006</dt></span></span> </dl>                                     | <span data-ttu-id="19394-129">Uno dei dischi padre è in uso.</span><span class="sxs-lookup"><span data-stu-id="19394-129">One of the parent disks is in use.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="19394-130"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="19394-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="19394-131">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="19394-131">The configuration is unknown.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="19394-132"><dt>**Macchina virtuale \_ E \_ macchina virtuale \_ che esegue**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="19394-132"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                            | <span data-ttu-id="19394-133">La macchina virtuale è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="19394-133">The virtual machine is running.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="19394-134"><dt>**Macchina virtuale \_ E \_ file \_ \_**</dt> di sola lettura <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="19394-134"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                       | <span data-ttu-id="19394-135">L'elemento padre di file modifiche disco virtuali è contrassegnato come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="19394-135">The parent of virtual undo disks is marked as read only.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="19394-136"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="19394-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="19394-137">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="19394-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="19394-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="19394-138">Remarks</span></span>

<span data-ttu-id="19394-139">Non è possibile chiamare **MergeUndoDisks** mentre la macchina virtuale è ancora in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="19394-139">**MergeUndoDisks** cannot be called while the virtual machine is still running.</span></span> <span data-ttu-id="19394-140">Usare [**IVMVirtualMachine:: Save**](ivmvirtualmachine-save.md) per salvare lo stato della macchina virtuale prima di chiamare **MergeUndoDisks** o [**IVMVirtualMachine:: bivio**](ivmvirtualmachine-turnoff.md) per spegnere la macchina virtuale senza salvare lo stato corrente in anticipo.</span><span class="sxs-lookup"><span data-stu-id="19394-140">Use [**IVMVirtualMachine::Save**](ivmvirtualmachine-save.md) to save the state of the virtual machine before calling **MergeUndoDisks**, or [**IVMVirtualMachine::TurnOff**](ivmvirtualmachine-turnoff.md) to turn off the virtual machine without saving its current state beforehand.</span></span>

## <a name="requirements"></a><span data-ttu-id="19394-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19394-141">Requirements</span></span>



| <span data-ttu-id="19394-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="19394-142">Requirement</span></span> | <span data-ttu-id="19394-143">Valore</span><span class="sxs-lookup"><span data-stu-id="19394-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="19394-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19394-144">Minimum supported client</span></span><br/> | <span data-ttu-id="19394-145">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="19394-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19394-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19394-146">Minimum supported server</span></span><br/> | <span data-ttu-id="19394-147">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="19394-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="19394-148">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="19394-148">End of client support</span></span><br/>    | <span data-ttu-id="19394-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="19394-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="19394-150">Prodotto</span><span class="sxs-lookup"><span data-stu-id="19394-150">Product</span></span><br/>                  | <span data-ttu-id="19394-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="19394-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="19394-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19394-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="19394-153"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="19394-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="19394-154">IID</span><span class="sxs-lookup"><span data-stu-id="19394-154">IID</span></span><br/>                      | <span data-ttu-id="19394-155">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="19394-155">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="19394-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19394-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19394-157">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="19394-157">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

