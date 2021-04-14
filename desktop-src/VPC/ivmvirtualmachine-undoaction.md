---
title: Proprietà IVMVirtualMachine UndoAction (VPCCOMInterfaces. h)
description: Azione predefinita da eseguire su tutte le unità di annullamento quando la macchina virtuale viene arrestata.
ms.assetid: fcdd5217-4909-435a-b11d-63578ab46e37
keywords:
- Proprietà UndoAction Virtual PC
- Proprietà UndoAction Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, Proprietà UndoAction
topic_type:
- apiref
api_name:
- IVMVirtualMachine.UndoAction
- IVMVirtualMachine.get_UndoAction
- IVMVirtualMachine.put_UndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039a9e65863e41ba2c7edc1befd2598aa16bb362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478322"
---
# <a name="ivmvirtualmachineundoaction-property"></a><span data-ttu-id="852c9-106">Proprietà IVMVirtualMachine:: UndoAction</span><span class="sxs-lookup"><span data-stu-id="852c9-106">IVMVirtualMachine::UndoAction property</span></span>

<span data-ttu-id="852c9-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="852c9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="852c9-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="852c9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="852c9-109">Recupera e imposta l'azione predefinita da eseguire su tutte le unità di annullamento quando la macchina virtuale (VM) viene spenta usando [**il metodo**](ivmvirtualmachine-turnoff.md) di disattivazione o arrestata usando il metodo [**Shutdown**](ivmguestos-shutdown.md) o spenta dall'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="852c9-109">Retrieves and sets the default action to be performed on all undo drives when the virtual machine (VM) is turned off using the [**TurnOff**](ivmvirtualmachine-turnoff.md) method or shut down using the [**Shutdown**](ivmguestos-shutdown.md) method or turned off from within the guest operating system.</span></span>

<span data-ttu-id="852c9-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="852c9-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="852c9-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="852c9-111">Syntax</span></span>


```C++
HRESULT put_UndoAction(
  [in]          VMUndoAction undoAction
);

HRESULT get_UndoAction(
  [out, retval] VMUndoAction *undoAction
);
```



## <a name="property-value"></a><span data-ttu-id="852c9-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="852c9-112">Property value</span></span>

<span data-ttu-id="852c9-113">Specifica l'azione predefinita da eseguire su tutte le unità di annullamento quando la macchina virtuale viene arrestata dall'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="852c9-113">Specifies the default action to be performed on all undo drives when the VM is shut down from within the guest operating system.</span></span> <span data-ttu-id="852c9-114">Per un elenco di valori, vedere [**VMUndoAction**](vmundoaction.md).</span><span class="sxs-lookup"><span data-stu-id="852c9-114">For a list of values, see [**VMUndoAction**](vmundoaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="852c9-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="852c9-115">Error codes</span></span>



| <span data-ttu-id="852c9-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="852c9-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="852c9-117">Significato</span><span class="sxs-lookup"><span data-stu-id="852c9-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="852c9-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="852c9-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="852c9-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="852c9-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="852c9-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="852c9-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="852c9-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="852c9-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="852c9-122"><dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="852c9-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="852c9-123">Il parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="852c9-123">The parameter is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="852c9-124"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="852c9-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="852c9-125">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="852c9-125">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="852c9-126"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="852c9-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="852c9-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="852c9-127">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="852c9-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="852c9-128">Requirements</span></span>



| <span data-ttu-id="852c9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="852c9-129">Requirement</span></span> | <span data-ttu-id="852c9-130">Valore</span><span class="sxs-lookup"><span data-stu-id="852c9-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="852c9-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="852c9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="852c9-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="852c9-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="852c9-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="852c9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="852c9-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="852c9-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="852c9-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="852c9-135">End of client support</span></span><br/>    | <span data-ttu-id="852c9-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="852c9-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="852c9-137">Prodotto</span><span class="sxs-lookup"><span data-stu-id="852c9-137">Product</span></span><br/>                  | <span data-ttu-id="852c9-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="852c9-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="852c9-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="852c9-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="852c9-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="852c9-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="852c9-141">IID</span><span class="sxs-lookup"><span data-stu-id="852c9-141">IID</span></span><br/>                      | <span data-ttu-id="852c9-142">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="852c9-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="852c9-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="852c9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="852c9-144">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="852c9-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

