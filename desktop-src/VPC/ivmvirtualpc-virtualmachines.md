---
title: Proprietà IVMVirtualPC VirtualMachines (VPCCOMInterfaces. h)
description: Recupera una raccolta enumerabile di macchine virtuali.
ms.assetid: 9e8dcd65-7cf8-4cdd-a412-62cbb96eb8ec
keywords:
- Proprietà VirtualMachines Virtual PC
- Proprietà VirtualMachines Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, proprietà VirtualMachines
topic_type:
- apiref
api_name:
- IVMVirtualPC.VirtualMachines
- IVMVirtualPC.get_VirtualMachines
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44e141208994fa3d759074e7cbb294e1e2158917
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302668"
---
# <a name="ivmvirtualpcvirtualmachines-property"></a><span data-ttu-id="219b5-106">Proprietà IVMVirtualPC:: VirtualMachines</span><span class="sxs-lookup"><span data-stu-id="219b5-106">IVMVirtualPC::VirtualMachines property</span></span>

<span data-ttu-id="219b5-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="219b5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="219b5-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="219b5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="219b5-109">Recupera una raccolta enumerabile di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="219b5-109">Retrieves an enumerable collection of virtual machines.</span></span>

<span data-ttu-id="219b5-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="219b5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="219b5-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="219b5-111">Syntax</span></span>


```C++
HRESULT get_VirtualMachines(
  [out, retval] IVMVirtualMachineCollection **virtualMachineCollection
);
```



## <a name="property-value"></a><span data-ttu-id="219b5-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="219b5-112">Property value</span></span>

<span data-ttu-id="219b5-113">Raccolta di oggetti [**IVMVirtualMachine**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="219b5-113">A collection of [**IVMVirtualMachine**](ivmvirtualmachine.md) objects.</span></span> <span data-ttu-id="219b5-114">Vedere [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md).</span><span class="sxs-lookup"><span data-stu-id="219b5-114">See [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="219b5-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="219b5-115">Error codes</span></span>



| <span data-ttu-id="219b5-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="219b5-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="219b5-117">Significato</span><span class="sxs-lookup"><span data-stu-id="219b5-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="219b5-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="219b5-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="219b5-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="219b5-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="219b5-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="219b5-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="219b5-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="219b5-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="219b5-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="219b5-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="219b5-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="219b5-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="219b5-124"><dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="219b5-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="219b5-125">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="219b5-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="219b5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="219b5-126">Requirements</span></span>



| <span data-ttu-id="219b5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="219b5-127">Requirement</span></span> | <span data-ttu-id="219b5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="219b5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="219b5-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="219b5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="219b5-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="219b5-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="219b5-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="219b5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="219b5-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="219b5-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="219b5-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="219b5-133">End of client support</span></span><br/>    | <span data-ttu-id="219b5-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="219b5-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="219b5-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="219b5-135">Product</span></span><br/>                  | <span data-ttu-id="219b5-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="219b5-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="219b5-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="219b5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="219b5-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="219b5-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="219b5-139">IID</span><span class="sxs-lookup"><span data-stu-id="219b5-139">IID</span></span><br/>                      | <span data-ttu-id="219b5-140">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="219b5-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="219b5-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="219b5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="219b5-142">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="219b5-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

