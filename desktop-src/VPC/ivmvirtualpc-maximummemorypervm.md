---
title: Proprietà IVMVirtualPC MaximumMemoryPerVM (VPCCOMInterfaces. h)
description: Recupera la quantità massima consentita di memoria fisica per ogni macchina virtuale, in megabyte.
ms.assetid: eb30dd6c-8f37-4cf9-9ed7-47925b5b1112
keywords:
- Proprietà MaximumMemoryPerVM Virtual PC
- Proprietà MaximumMemoryPerVM Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, proprietà MaximumMemoryPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumMemoryPerVM
- IVMVirtualPC.get_MaximumMemoryPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936d88c29df4be934e03d1c0b7bde60139bde268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873261"
---
# <a name="ivmvirtualpcmaximummemorypervm-property"></a><span data-ttu-id="87cfa-106">Proprietà IVMVirtualPC:: MaximumMemoryPerVM</span><span class="sxs-lookup"><span data-stu-id="87cfa-106">IVMVirtualPC::MaximumMemoryPerVM property</span></span>

<span data-ttu-id="87cfa-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="87cfa-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="87cfa-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="87cfa-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="87cfa-109">Recupera la quantità massima consentita di memoria fisica per ogni macchina virtuale, in megabyte.</span><span class="sxs-lookup"><span data-stu-id="87cfa-109">Retrieves the maximum allowable quantity of physical memory per virtual machine, in megabytes.</span></span>

<span data-ttu-id="87cfa-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="87cfa-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="87cfa-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87cfa-111">Syntax</span></span>


```C++
HRESULT get_MaximumMemoryPerVM(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="87cfa-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="87cfa-112">Property value</span></span>

<span data-ttu-id="87cfa-113">Quantità massima consentita, in megabyte, della memoria fisica per ogni macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="87cfa-113">The maximum allowable quantity, in megabytes, of physical memory per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="87cfa-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="87cfa-114">Error codes</span></span>



| <span data-ttu-id="87cfa-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="87cfa-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="87cfa-116">Significato</span><span class="sxs-lookup"><span data-stu-id="87cfa-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="87cfa-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="87cfa-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="87cfa-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="87cfa-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="87cfa-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="87cfa-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="87cfa-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="87cfa-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="87cfa-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="87cfa-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="87cfa-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="87cfa-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="87cfa-123"><dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="87cfa-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="87cfa-124">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="87cfa-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="87cfa-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87cfa-125">Requirements</span></span>



| <span data-ttu-id="87cfa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="87cfa-126">Requirement</span></span> | <span data-ttu-id="87cfa-127">Valore</span><span class="sxs-lookup"><span data-stu-id="87cfa-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="87cfa-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87cfa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="87cfa-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="87cfa-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87cfa-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87cfa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="87cfa-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="87cfa-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="87cfa-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="87cfa-132">End of client support</span></span><br/>    | <span data-ttu-id="87cfa-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="87cfa-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="87cfa-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="87cfa-134">Product</span></span><br/>                  | <span data-ttu-id="87cfa-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="87cfa-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="87cfa-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87cfa-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="87cfa-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="87cfa-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="87cfa-138">IID</span><span class="sxs-lookup"><span data-stu-id="87cfa-138">IID</span></span><br/>                      | <span data-ttu-id="87cfa-139">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="87cfa-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="87cfa-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87cfa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87cfa-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="87cfa-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

