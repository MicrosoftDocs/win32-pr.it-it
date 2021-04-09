---
title: Proprietà SSE2 IVMHostInfo (VPCCOMInterfaces. h)
description: Determina se il processore supporta il set di istruzioni SSE2. | Proprietà SSE2 IVMHostInfo (VPCCOMInterfaces. h)
ms.assetid: 1db5583c-fb8e-400e-87d3-3c4309696307
keywords:
- Proprietà SSE2 del PC virtuale
- Proprietà SSE2 Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà SSE2
topic_type:
- apiref
api_name:
- IVMHostInfo.SSE2
- IVMHostInfo.get_SSE2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28286262d02512f58df8c3a00e4ba07a67c2916f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886203"
---
# <a name="ivmhostinfosse2-property"></a><span data-ttu-id="39c73-107">Proprietà IVMHostInfo:: SSE2</span><span class="sxs-lookup"><span data-stu-id="39c73-107">IVMHostInfo::SSE2 property</span></span>

<span data-ttu-id="39c73-108">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="39c73-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="39c73-109">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="39c73-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="39c73-110">Determina se il processore supporta il set di istruzioni SSE2.</span><span class="sxs-lookup"><span data-stu-id="39c73-110">Determines whether the processor supports the SSE2 instruction set.</span></span>

<span data-ttu-id="39c73-111">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="39c73-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="39c73-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39c73-112">Syntax</span></span>


```C++
HRESULT get_SSE2(
  [out, retval] VARIANT_BOOL *sse2Enabled
);
```



## <a name="property-value"></a><span data-ttu-id="39c73-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="39c73-113">Property value</span></span>

<span data-ttu-id="39c73-114">**True** se le istruzioni SSE2 sono supportate dal processore host; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="39c73-114">**TRUE** if SSE2 instructions are supported by the host processor, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="39c73-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="39c73-115">Error codes</span></span>



| <span data-ttu-id="39c73-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="39c73-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="39c73-117">Significato</span><span class="sxs-lookup"><span data-stu-id="39c73-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="39c73-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="39c73-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="39c73-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="39c73-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="39c73-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="39c73-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="39c73-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="39c73-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="39c73-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="39c73-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="39c73-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="39c73-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="39c73-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39c73-124">Requirements</span></span>



| <span data-ttu-id="39c73-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c73-125">Requirement</span></span> | <span data-ttu-id="39c73-126">Valore</span><span class="sxs-lookup"><span data-stu-id="39c73-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39c73-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39c73-127">Minimum supported client</span></span><br/> | <span data-ttu-id="39c73-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="39c73-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39c73-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39c73-129">Minimum supported server</span></span><br/> | <span data-ttu-id="39c73-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="39c73-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="39c73-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="39c73-131">End of client support</span></span><br/>    | <span data-ttu-id="39c73-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39c73-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="39c73-133">Prodotto</span><span class="sxs-lookup"><span data-stu-id="39c73-133">Product</span></span><br/>                  | <span data-ttu-id="39c73-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="39c73-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="39c73-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39c73-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c73-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="39c73-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="39c73-137">IID</span><span class="sxs-lookup"><span data-stu-id="39c73-137">IID</span></span><br/>                      | <span data-ttu-id="39c73-138">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="39c73-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="39c73-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39c73-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c73-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="39c73-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

