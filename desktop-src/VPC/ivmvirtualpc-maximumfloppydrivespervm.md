---
title: Proprietà IVMVirtualPC MaximumFloppyDrivesPerVM (VPCCOMInterfaces. h)
description: Recupera il numero massimo di unità floppy per macchina virtuale.
ms.assetid: f0dc351b-73de-4b6b-a953-5d5b683c4e31
keywords:
- Proprietà MaximumFloppyDrivesPerVM Virtual PC
- Proprietà MaximumFloppyDrivesPerVM Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, proprietà MaximumFloppyDrivesPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumFloppyDrivesPerVM
- IVMVirtualPC.get_MaximumFloppyDrivesPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecc0d672affce5364e1658d5198681268109a1b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121078"
---
# <a name="ivmvirtualpcmaximumfloppydrivespervm-property"></a><span data-ttu-id="2a878-106">Proprietà IVMVirtualPC:: MaximumFloppyDrivesPerVM</span><span class="sxs-lookup"><span data-stu-id="2a878-106">IVMVirtualPC::MaximumFloppyDrivesPerVM property</span></span>

<span data-ttu-id="2a878-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2a878-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2a878-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2a878-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2a878-109">Recupera il numero massimo di unità floppy per macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2a878-109">Retrieves the maximum number of floppy drives per virtual machine.</span></span>

<span data-ttu-id="2a878-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2a878-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a878-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a878-111">Syntax</span></span>


```C++
HRESULT get_MaximumFloppyDrivesPerVM(
  [out, retval] long *maxDrives
);
```



## <a name="property-value"></a><span data-ttu-id="2a878-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2a878-112">Property value</span></span>

<span data-ttu-id="2a878-113">Numero massimo di unità floppy per macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2a878-113">The maximum number of floppy drives per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2a878-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2a878-114">Error codes</span></span>



| <span data-ttu-id="2a878-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="2a878-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="2a878-116">Significato</span><span class="sxs-lookup"><span data-stu-id="2a878-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a878-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2a878-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="2a878-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="2a878-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="2a878-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2a878-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="2a878-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="2a878-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="2a878-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2a878-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="2a878-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="2a878-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="2a878-123"><dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="2a878-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="2a878-124">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="2a878-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2a878-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a878-125">Requirements</span></span>



| <span data-ttu-id="2a878-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a878-126">Requirement</span></span> | <span data-ttu-id="2a878-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2a878-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a878-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a878-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2a878-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2a878-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a878-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a878-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2a878-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2a878-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2a878-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2a878-132">End of client support</span></span><br/>    | <span data-ttu-id="2a878-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2a878-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2a878-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="2a878-134">Product</span></span><br/>                  | <span data-ttu-id="2a878-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2a878-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2a878-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a878-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a878-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a878-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2a878-138">IID</span><span class="sxs-lookup"><span data-stu-id="2a878-138">IID</span></span><br/>                      | <span data-ttu-id="2a878-139">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="2a878-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2a878-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a878-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a878-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="2a878-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

