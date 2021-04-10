---
title: Proprietà stato IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera lo stato corrente della macchina virtuale.
ms.assetid: a4214dfc-09d2-4d6b-a053-e75e99063411
keywords:
- Proprietà stato PC virtuale
- Proprietà state Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, state (proprietà)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.State
- IVMVirtualMachine.get_State
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11616f2a88b9238da11a4edec00c048e69885a07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964706"
---
# <a name="ivmvirtualmachinestate-property"></a><span data-ttu-id="e90c4-106">Proprietà IVMVirtualMachine:: state</span><span class="sxs-lookup"><span data-stu-id="e90c4-106">IVMVirtualMachine::State property</span></span>

<span data-ttu-id="e90c4-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e90c4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e90c4-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e90c4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e90c4-109">Recupera lo stato corrente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e90c4-109">Retrieves the current state of the virtual machine.</span></span>

<span data-ttu-id="e90c4-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e90c4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e90c4-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e90c4-111">Syntax</span></span>


```C++
HRESULT get_State(
  [out, retval] VMVMState *virtualMachineState
);
```



## <a name="property-value"></a><span data-ttu-id="e90c4-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e90c4-112">Property value</span></span>

<span data-ttu-id="e90c4-113">Stato corrente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e90c4-113">The current state of the virtual machine.</span></span> <span data-ttu-id="e90c4-114">Per un elenco di valori, vedere [**VMVMState**](vmvmstate.md).</span><span class="sxs-lookup"><span data-stu-id="e90c4-114">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="e90c4-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e90c4-115">Error codes</span></span>



| <span data-ttu-id="e90c4-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="e90c4-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e90c4-117">Significato</span><span class="sxs-lookup"><span data-stu-id="e90c4-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e90c4-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e90c4-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e90c4-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e90c4-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="e90c4-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e90c4-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e90c4-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="e90c4-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="e90c4-122"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e90c4-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="e90c4-123">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="e90c4-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="e90c4-124"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e90c4-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e90c4-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="e90c4-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e90c4-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e90c4-126">Requirements</span></span>



| <span data-ttu-id="e90c4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e90c4-127">Requirement</span></span> | <span data-ttu-id="e90c4-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e90c4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e90c4-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e90c4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e90c4-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e90c4-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e90c4-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e90c4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e90c4-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e90c4-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e90c4-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e90c4-133">End of client support</span></span><br/>    | <span data-ttu-id="e90c4-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e90c4-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e90c4-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="e90c4-135">Product</span></span><br/>                  | <span data-ttu-id="e90c4-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e90c4-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e90c4-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e90c4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e90c4-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e90c4-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e90c4-139">IID</span><span class="sxs-lookup"><span data-stu-id="e90c4-139">IID</span></span><br/>                      | <span data-ttu-id="e90c4-140">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="e90c4-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e90c4-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e90c4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90c4-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="e90c4-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

