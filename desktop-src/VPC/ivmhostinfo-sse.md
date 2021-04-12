---
title: Proprietà SSE IVMHostInfo (VPCCOMInterfaces. h)
description: Determina se il processore supporta il set di istruzioni SSE. | Proprietà SSE IVMHostInfo (VPCCOMInterfaces. h)
ms.assetid: 135704db-757a-45b1-884a-5e26ef7d65c7
keywords:
- Proprietà SSE Virtual PC
- Proprietà SSE Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà SSE
topic_type:
- apiref
api_name:
- IVMHostInfo.SSE
- IVMHostInfo.get_SSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02bef292e7dbcae48b9e2a6a94e7f879212a0dfc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353481"
---
# <a name="ivmhostinfosse-property"></a><span data-ttu-id="4d76b-107">Proprietà IVMHostInfo:: SSE</span><span class="sxs-lookup"><span data-stu-id="4d76b-107">IVMHostInfo::SSE property</span></span>

<span data-ttu-id="4d76b-108">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4d76b-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4d76b-109">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4d76b-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4d76b-110">Determina se il processore supporta il set di istruzioni SSE.</span><span class="sxs-lookup"><span data-stu-id="4d76b-110">Determines whether the processor supports the SSE instruction set.</span></span>

<span data-ttu-id="4d76b-111">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4d76b-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d76b-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d76b-112">Syntax</span></span>


```C++
HRESULT get_SSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="4d76b-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4d76b-113">Property value</span></span>

<span data-ttu-id="4d76b-114">**True** se le istruzioni SSE sono supportate dal processore host; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="4d76b-114">**TRUE** if SSE instructions are supported by the host processor, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4d76b-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4d76b-115">Error codes</span></span>



| <span data-ttu-id="4d76b-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="4d76b-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4d76b-117">Significato</span><span class="sxs-lookup"><span data-stu-id="4d76b-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4d76b-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4d76b-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4d76b-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4d76b-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="4d76b-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4d76b-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4d76b-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="4d76b-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="4d76b-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4d76b-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4d76b-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="4d76b-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4d76b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d76b-124">Requirements</span></span>



| <span data-ttu-id="4d76b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d76b-125">Requirement</span></span> | <span data-ttu-id="4d76b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4d76b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d76b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d76b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4d76b-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4d76b-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4d76b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d76b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4d76b-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4d76b-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4d76b-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4d76b-131">End of client support</span></span><br/>    | <span data-ttu-id="4d76b-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d76b-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4d76b-133">Prodotto</span><span class="sxs-lookup"><span data-stu-id="4d76b-133">Product</span></span><br/>                  | <span data-ttu-id="4d76b-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4d76b-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4d76b-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d76b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d76b-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d76b-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4d76b-137">IID</span><span class="sxs-lookup"><span data-stu-id="4d76b-137">IID</span></span><br/>                      | <span data-ttu-id="4d76b-138">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="4d76b-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="4d76b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d76b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d76b-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="4d76b-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

