---
title: Proprietà IVMHostInfo FloppyDrives (VPCCOMInterfaces. h)
description: Recupera le lettere di unità associate alle unità floppy host.
ms.assetid: 9a8ab4b5-6ee8-463f-809b-b88cd28d9373
keywords:
- Proprietà FloppyDrives Virtual PC
- Proprietà FloppyDrives Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà FloppyDrives
topic_type:
- apiref
api_name:
- IVMHostInfo.FloppyDrives
- IVMHostInfo.get_FloppyDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1c31e3ece942f31fc6245c9f23a2995eb7b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400723"
---
# <a name="ivmhostinfofloppydrives-property"></a><span data-ttu-id="40390-106">Proprietà IVMHostInfo:: FloppyDrives</span><span class="sxs-lookup"><span data-stu-id="40390-106">IVMHostInfo::FloppyDrives property</span></span>

<span data-ttu-id="40390-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="40390-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="40390-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="40390-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="40390-109">Recupera le lettere di unità associate alle unità floppy host.</span><span class="sxs-lookup"><span data-stu-id="40390-109">Retrieves the drive letters associated with host floppy drives.</span></span>

<span data-ttu-id="40390-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="40390-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="40390-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40390-111">Syntax</span></span>


```C++
HRESULT get_FloppyDrives(
  [out, retval] VARIANT *floppyDrives
);
```



## <a name="property-value"></a><span data-ttu-id="40390-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="40390-112">Property value</span></span>

<span data-ttu-id="40390-113">Matrice di lettere di unità.</span><span class="sxs-lookup"><span data-stu-id="40390-113">An array of drive letters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="40390-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="40390-114">Error codes</span></span>



| <span data-ttu-id="40390-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="40390-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="40390-116">Significato</span><span class="sxs-lookup"><span data-stu-id="40390-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="40390-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="40390-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="40390-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="40390-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="40390-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="40390-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="40390-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="40390-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="40390-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="40390-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="40390-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="40390-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="40390-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40390-123">Requirements</span></span>



| <span data-ttu-id="40390-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="40390-124">Requirement</span></span> | <span data-ttu-id="40390-125">Valore</span><span class="sxs-lookup"><span data-stu-id="40390-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40390-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40390-126">Minimum supported client</span></span><br/> | <span data-ttu-id="40390-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="40390-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40390-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40390-128">Minimum supported server</span></span><br/> | <span data-ttu-id="40390-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="40390-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="40390-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="40390-130">End of client support</span></span><br/>    | <span data-ttu-id="40390-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="40390-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="40390-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="40390-132">Product</span></span><br/>                  | <span data-ttu-id="40390-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="40390-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="40390-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40390-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="40390-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="40390-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="40390-136">IID</span><span class="sxs-lookup"><span data-stu-id="40390-136">IID</span></span><br/>                      | <span data-ttu-id="40390-137">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="40390-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="40390-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40390-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40390-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="40390-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

