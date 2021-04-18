---
title: Proprietà annullabile IVMVirtualMachine (VPCCOMInterfaces. h)
description: Determina se le unità di annullamento sono abilitate per i dischi rigidi connessi alla macchina virtuale.
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- Proprietà annullabile Virtual PC
- Proprietà annullabile Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà annullabile
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Undoable
- IVMVirtualMachine.get_Undoable
- IVMVirtualMachine.put_Undoable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2cbc77f4d68fbdbfcc8d3998e3c207b8f4245c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517854"
---
# <a name="ivmvirtualmachineundoable-property"></a><span data-ttu-id="ca058-106">Proprietà IVMVirtualMachine:: undoable</span><span class="sxs-lookup"><span data-stu-id="ca058-106">IVMVirtualMachine::Undoable property</span></span>

<span data-ttu-id="ca058-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ca058-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ca058-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ca058-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ca058-109">Determina se le unità di annullamento sono abilitate per i dischi rigidi connessi alla macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="ca058-109">Determines whether undo drives are enabled for hard disks connected to the virtual machine (VM).</span></span>

<span data-ttu-id="ca058-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ca058-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca058-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca058-111">Syntax</span></span>


```C++
HRESULT put_Undoable(
  [in]          VARIANT_BOOL enableUndo
);

HRESULT get_Undoable(
  [out, retval] VARIANT_BOOL *isUndoable
);
```



## <a name="property-value"></a><span data-ttu-id="ca058-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ca058-112">Property value</span></span>

<span data-ttu-id="ca058-113">Specifica la **variante \_ true** se le unità di annullamento sono abilitate per i dischi rigidi connessi alla macchina virtuale e **Variant \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ca058-113">Specifies **VARIANT\_TRUE** if undo drives are enabled for hard disks connected to the VM and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ca058-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ca058-114">Error codes</span></span>



| <span data-ttu-id="ca058-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="ca058-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="ca058-116">Significato</span><span class="sxs-lookup"><span data-stu-id="ca058-116">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ca058-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ca058-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="ca058-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ca058-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="ca058-119"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ca058-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="ca058-120">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="ca058-120">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="ca058-121"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ca058-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="ca058-122">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="ca058-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="ca058-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ca058-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="ca058-124">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="ca058-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="ca058-125"><dt>Macchina virtuale \_ 0xA0040302 \_ virtuale E pref \_ VM \_ attiva</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ca058-125"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="ca058-126">La macchina virtuale è in esecuzione o è stata salvata.</span><span class="sxs-lookup"><span data-stu-id="ca058-126">The VM is running or saved.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="ca058-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca058-127">Remarks</span></span>

<span data-ttu-id="ca058-128">Se le unità di annullamento sono disabilitate, eventuali file di unità di annullamento esistenti verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="ca058-128">If undo drives are disabled, any existing undo drive files will be deleted.</span></span>

<span data-ttu-id="ca058-129">Non è possibile impostare questa proprietà se la macchina virtuale è in esecuzione o è stata salvata.</span><span class="sxs-lookup"><span data-stu-id="ca058-129">You cannot set this property if the VM is running or saved.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca058-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca058-130">Requirements</span></span>



| <span data-ttu-id="ca058-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca058-131">Requirement</span></span> | <span data-ttu-id="ca058-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ca058-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca058-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca058-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ca058-134">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ca058-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca058-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca058-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ca058-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ca058-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ca058-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ca058-137">End of client support</span></span><br/>    | <span data-ttu-id="ca058-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ca058-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ca058-139">Prodotto</span><span class="sxs-lookup"><span data-stu-id="ca058-139">Product</span></span><br/>                  | <span data-ttu-id="ca058-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ca058-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ca058-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca058-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca058-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca058-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ca058-143">IID</span><span class="sxs-lookup"><span data-stu-id="ca058-143">IID</span></span><br/>                      | <span data-ttu-id="ca058-144">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="ca058-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ca058-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca058-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca058-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="ca058-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

