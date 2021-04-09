---
title: Proprietà IVMVirtualMachine SavedStateFilePath (VPCCOMInterfaces. h)
description: Recupera il percorso completo del file di stato salvato.
ms.assetid: 01bd5491-4d08-4558-ac33-01b096f057a2
keywords:
- Proprietà SavedStateFilePath Virtual PC
- Proprietà SavedStateFilePath Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà SavedStateFilePath
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SavedStateFilePath
- IVMVirtualMachine.get_SavedStateFilePath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9baea53e3fce2455a2bdfa361e56b45b9b65d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120878"
---
# <a name="ivmvirtualmachinesavedstatefilepath-property"></a><span data-ttu-id="048a7-106">Proprietà IVMVirtualMachine:: SavedStateFilePath</span><span class="sxs-lookup"><span data-stu-id="048a7-106">IVMVirtualMachine::SavedStateFilePath property</span></span>

<span data-ttu-id="048a7-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="048a7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="048a7-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="048a7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="048a7-109">Recupera il percorso completo del file di stato salvato.</span><span class="sxs-lookup"><span data-stu-id="048a7-109">Retrieves the full path to the saved state file.</span></span>

<span data-ttu-id="048a7-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="048a7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="048a7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="048a7-111">Syntax</span></span>


```C++
HRESULT get_SavedStateFilePath(
  [out, retval] BSTR *savedStateFilePath
);
```



## <a name="property-value"></a><span data-ttu-id="048a7-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="048a7-112">Property value</span></span>

<span data-ttu-id="048a7-113">Percorso completo del file di stato salvato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="048a7-113">The fully qualified path to the virtual machine's saved state file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="048a7-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="048a7-114">Error codes</span></span>



| <span data-ttu-id="048a7-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="048a7-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="048a7-116">Significato</span><span class="sxs-lookup"><span data-stu-id="048a7-116">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="048a7-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="048a7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="048a7-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="048a7-118">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="048a7-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="048a7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="048a7-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="048a7-120">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="048a7-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="048a7-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="048a7-122">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="048a7-122">The configuration is unknown.</span></span><br/>                           |
| <dl> <span data-ttu-id="048a7-123"><dt>Macchina virtuale \_ E \_ VM \_ senza \_ \_ stato salvato</dt> <dt>0xA00400501</dt></span><span class="sxs-lookup"><span data-stu-id="048a7-123"><dt>VM\_E\_VM\_NO\_SAVED\_STATE</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="048a7-124">Alla macchina virtuale non è associato alcun file di stato salvato.</span><span class="sxs-lookup"><span data-stu-id="048a7-124">The virtual machine has no associated saved state file.</span></span><br/> |
| <dl> <span data-ttu-id="048a7-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="048a7-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="048a7-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="048a7-126">An unexpected error has occurred.</span></span><br/>                       |



## <a name="requirements"></a><span data-ttu-id="048a7-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="048a7-127">Requirements</span></span>



| <span data-ttu-id="048a7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="048a7-128">Requirement</span></span> | <span data-ttu-id="048a7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="048a7-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="048a7-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="048a7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="048a7-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="048a7-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="048a7-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="048a7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="048a7-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="048a7-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="048a7-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="048a7-134">End of client support</span></span><br/>    | <span data-ttu-id="048a7-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="048a7-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="048a7-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="048a7-136">Product</span></span><br/>                  | <span data-ttu-id="048a7-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="048a7-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="048a7-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="048a7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="048a7-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="048a7-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="048a7-140">IID</span><span class="sxs-lookup"><span data-stu-id="048a7-140">IID</span></span><br/>                      | <span data-ttu-id="048a7-141">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="048a7-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="048a7-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="048a7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="048a7-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="048a7-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

