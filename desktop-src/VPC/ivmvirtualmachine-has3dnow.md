---
title: Proprietà IVMVirtualMachine Has3DNow (VPCCOMInterfaces. h)
description: Determina se il processore supporta il set di istruzioni 3DNow. | Proprietà IVMVirtualMachine Has3DNow (VPCCOMInterfaces. h)
ms.assetid: 525ee7f0-081c-4f87-b2b7-ffec09f632c4
keywords:
- Proprietà Has3DNow Virtual PC
- Proprietà Has3DNow Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà Has3DNow
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Has3DNow
- IVMVirtualMachine.get_Has3DNow
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b347fa802b999707e43019e9b7808c844c0288f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761860"
---
# <a name="ivmvirtualmachinehas3dnow-property"></a><span data-ttu-id="370f6-107">Proprietà IVMVirtualMachine:: Has3DNow</span><span class="sxs-lookup"><span data-stu-id="370f6-107">IVMVirtualMachine::Has3DNow property</span></span>

<span data-ttu-id="370f6-108">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="370f6-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="370f6-109">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="370f6-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="370f6-110">Determina se il processore supporta il set di istruzioni 3DNow.</span><span class="sxs-lookup"><span data-stu-id="370f6-110">Determines whether the processor supports the 3DNow instruction set.</span></span>

<span data-ttu-id="370f6-111">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="370f6-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="370f6-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="370f6-112">Syntax</span></span>


```C++
HRESULT get_Has3DNow(
  [out, retval] VARIANT_BOOL *threeDNowEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="370f6-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="370f6-113">Property value</span></span>

<span data-ttu-id="370f6-114">**True** se il processore supporta il set di istruzioni 3DNow, **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="370f6-114">**TRUE** if the processor supported the 3DNow instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="370f6-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="370f6-115">Error codes</span></span>



| <span data-ttu-id="370f6-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="370f6-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="370f6-117">Significato</span><span class="sxs-lookup"><span data-stu-id="370f6-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="370f6-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="370f6-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="370f6-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="370f6-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="370f6-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="370f6-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="370f6-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="370f6-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="370f6-122"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="370f6-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="370f6-123">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="370f6-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="370f6-124"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="370f6-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="370f6-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="370f6-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="370f6-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="370f6-126">Requirements</span></span>



| <span data-ttu-id="370f6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="370f6-127">Requirement</span></span> | <span data-ttu-id="370f6-128">Valore</span><span class="sxs-lookup"><span data-stu-id="370f6-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="370f6-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="370f6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="370f6-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="370f6-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="370f6-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="370f6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="370f6-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="370f6-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="370f6-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="370f6-133">End of client support</span></span><br/>    | <span data-ttu-id="370f6-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="370f6-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="370f6-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="370f6-135">Product</span></span><br/>                  | <span data-ttu-id="370f6-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="370f6-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="370f6-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="370f6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="370f6-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="370f6-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="370f6-139">IID</span><span class="sxs-lookup"><span data-stu-id="370f6-139">IID</span></span><br/>                      | <span data-ttu-id="370f6-140">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="370f6-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="370f6-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="370f6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="370f6-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="370f6-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

