---
title: Proprietà Memory IVMHostInfo (VPCCOMInterfaces. h)
description: Recupera la quantità totale di memoria fisica nel computer host, in megabyte.
ms.assetid: 178013c0-cf29-4f1e-9a9d-d6a5dbd4fe2d
keywords:
- Proprietà memoria Virtual PC
- Proprietà Memory Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà Memory
topic_type:
- apiref
api_name:
- IVMHostInfo.Memory
- IVMHostInfo.get_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f634bfe3bf81dcb13c9f09d8f19a5a82aa6902
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302416"
---
# <a name="ivmhostinfomemory-property"></a><span data-ttu-id="254aa-106">Proprietà IVMHostInfo:: memory</span><span class="sxs-lookup"><span data-stu-id="254aa-106">IVMHostInfo::Memory property</span></span>

<span data-ttu-id="254aa-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="254aa-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="254aa-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="254aa-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="254aa-109">Recupera la quantità totale di memoria fisica nel computer host, in megabyte.</span><span class="sxs-lookup"><span data-stu-id="254aa-109">Retrieves the total amount of physical memory in the host machine, in megabytes.</span></span>

<span data-ttu-id="254aa-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="254aa-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="254aa-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="254aa-111">Syntax</span></span>


```C++
HRESULT get_Memory(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="254aa-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="254aa-112">Property value</span></span>

<span data-ttu-id="254aa-113">Quantità totale di memoria fisica, in megabyte.</span><span class="sxs-lookup"><span data-stu-id="254aa-113">The total amount of physical memory, in megabytes.</span></span> <span data-ttu-id="254aa-114">Questo valore è una **variante** di tipo \_ decimale VT.</span><span class="sxs-lookup"><span data-stu-id="254aa-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="254aa-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="254aa-115">Error codes</span></span>



| <span data-ttu-id="254aa-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="254aa-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="254aa-117">Significato</span><span class="sxs-lookup"><span data-stu-id="254aa-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="254aa-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="254aa-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="254aa-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="254aa-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="254aa-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="254aa-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="254aa-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="254aa-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="254aa-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="254aa-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="254aa-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="254aa-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="254aa-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="254aa-124">Requirements</span></span>



| <span data-ttu-id="254aa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="254aa-125">Requirement</span></span> | <span data-ttu-id="254aa-126">Valore</span><span class="sxs-lookup"><span data-stu-id="254aa-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="254aa-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="254aa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="254aa-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="254aa-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="254aa-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="254aa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="254aa-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="254aa-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="254aa-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="254aa-131">End of client support</span></span><br/>    | <span data-ttu-id="254aa-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="254aa-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="254aa-133">Prodotto</span><span class="sxs-lookup"><span data-stu-id="254aa-133">Product</span></span><br/>                  | <span data-ttu-id="254aa-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="254aa-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="254aa-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="254aa-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="254aa-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="254aa-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="254aa-137">IID</span><span class="sxs-lookup"><span data-stu-id="254aa-137">IID</span></span><br/>                      | <span data-ttu-id="254aa-138">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="254aa-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="254aa-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="254aa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="254aa-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="254aa-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

