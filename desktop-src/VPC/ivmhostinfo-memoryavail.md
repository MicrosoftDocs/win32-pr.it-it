---
title: Proprietà IVMHostInfo MemoryAvail (VPCCOMInterfaces. h)
description: Recupera la quantità di memoria fisica disponibile nel computer host, in megabyte.
ms.assetid: cb593d02-cdb9-40f6-b57f-72fc3278f1bb
keywords:
- Proprietà MemoryAvail Virtual PC
- Proprietà MemoryAvail Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà MemoryAvail
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryAvail
- IVMHostInfo.get_MemoryAvail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df6be8bf62595720d01372ee891184952a0dd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302340"
---
# <a name="ivmhostinfomemoryavail-property"></a><span data-ttu-id="d6e71-106">Proprietà IVMHostInfo:: MemoryAvail</span><span class="sxs-lookup"><span data-stu-id="d6e71-106">IVMHostInfo::MemoryAvail property</span></span>

<span data-ttu-id="d6e71-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d6e71-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d6e71-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d6e71-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d6e71-109">Recupera la quantità di memoria fisica disponibile nel computer host, in megabyte.</span><span class="sxs-lookup"><span data-stu-id="d6e71-109">Retrieves the amount of available physical memory in the host machine, in megabytes.</span></span>

<span data-ttu-id="d6e71-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d6e71-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6e71-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6e71-111">Syntax</span></span>


```C++
HRESULT get_MemoryAvail(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="d6e71-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d6e71-112">Property value</span></span>

<span data-ttu-id="d6e71-113">Memoria fisica disponibile, in megabyte.</span><span class="sxs-lookup"><span data-stu-id="d6e71-113">The available physical memory, in megabytes.</span></span> <span data-ttu-id="d6e71-114">Questo valore è una **variante** di tipo \_ decimale VT.</span><span class="sxs-lookup"><span data-stu-id="d6e71-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d6e71-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d6e71-115">Error codes</span></span>



| <span data-ttu-id="d6e71-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="d6e71-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d6e71-117">Significato</span><span class="sxs-lookup"><span data-stu-id="d6e71-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d6e71-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d6e71-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d6e71-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d6e71-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d6e71-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d6e71-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d6e71-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="d6e71-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d6e71-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d6e71-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d6e71-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d6e71-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d6e71-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6e71-124">Requirements</span></span>



| <span data-ttu-id="d6e71-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6e71-125">Requirement</span></span> | <span data-ttu-id="d6e71-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d6e71-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e71-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6e71-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d6e71-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d6e71-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d6e71-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6e71-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d6e71-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d6e71-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d6e71-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d6e71-131">End of client support</span></span><br/>    | <span data-ttu-id="d6e71-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d6e71-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d6e71-133">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d6e71-133">Product</span></span><br/>                  | <span data-ttu-id="d6e71-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d6e71-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d6e71-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6e71-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6e71-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6e71-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d6e71-137">IID</span><span class="sxs-lookup"><span data-stu-id="d6e71-137">IID</span></span><br/>                      | <span data-ttu-id="d6e71-138">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="d6e71-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="d6e71-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6e71-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6e71-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="d6e71-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

