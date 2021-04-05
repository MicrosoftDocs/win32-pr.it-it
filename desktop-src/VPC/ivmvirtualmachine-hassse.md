---
title: Proprietà IVMVirtualMachine HasSSE (VPCCOMInterfaces. h)
description: Determina se il processore supporta il set di istruzioni SSE. | Proprietà IVMVirtualMachine HasSSE (VPCCOMInterfaces. h)
ms.assetid: 949dd93b-aa4e-4506-91ed-ed625a535d5f
keywords:
- Proprietà HasSSE Virtual PC
- Proprietà HasSSE Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà HasSSE
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasSSE
- IVMVirtualMachine.get_HasSSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a367ddc7b32ff4627976d2c5b63ec3565dbace53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886239"
---
# <a name="ivmvirtualmachinehassse-property"></a><span data-ttu-id="18d86-107">Proprietà IVMVirtualMachine:: HasSSE</span><span class="sxs-lookup"><span data-stu-id="18d86-107">IVMVirtualMachine::HasSSE property</span></span>

<span data-ttu-id="18d86-108">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="18d86-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="18d86-109">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="18d86-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="18d86-110">Determina se il processore supporta il set di istruzioni SSE.</span><span class="sxs-lookup"><span data-stu-id="18d86-110">Determines whether the processor supports the SSE instruction set.</span></span>

<span data-ttu-id="18d86-111">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="18d86-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d86-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18d86-112">Syntax</span></span>


```C++
HRESULT get_HasSSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="18d86-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="18d86-113">Property value</span></span>

<span data-ttu-id="18d86-114">**True** se il processore supporta il set di istruzioni SSE, **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="18d86-114">**TRUE** if the processor supported the SSE instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="18d86-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="18d86-115">Error codes</span></span>



| <span data-ttu-id="18d86-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="18d86-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="18d86-117">Significato</span><span class="sxs-lookup"><span data-stu-id="18d86-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="18d86-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="18d86-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="18d86-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="18d86-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="18d86-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="18d86-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="18d86-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="18d86-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="18d86-122"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="18d86-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="18d86-123">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="18d86-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="18d86-124"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="18d86-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="18d86-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="18d86-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="18d86-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18d86-126">Requirements</span></span>



| <span data-ttu-id="18d86-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="18d86-127">Requirement</span></span> | <span data-ttu-id="18d86-128">Valore</span><span class="sxs-lookup"><span data-stu-id="18d86-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d86-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18d86-129">Minimum supported client</span></span><br/> | <span data-ttu-id="18d86-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="18d86-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18d86-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18d86-131">Minimum supported server</span></span><br/> | <span data-ttu-id="18d86-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="18d86-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="18d86-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="18d86-133">End of client support</span></span><br/>    | <span data-ttu-id="18d86-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="18d86-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="18d86-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="18d86-135">Product</span></span><br/>                  | <span data-ttu-id="18d86-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="18d86-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="18d86-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18d86-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="18d86-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="18d86-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="18d86-139">IID</span><span class="sxs-lookup"><span data-stu-id="18d86-139">IID</span></span><br/>                      | <span data-ttu-id="18d86-140">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="18d86-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="18d86-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18d86-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d86-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="18d86-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

