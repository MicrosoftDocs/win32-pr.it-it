---
title: Proprietà IVMHostInfo ThreeDNow (VPCCOMInterfaces. h)
description: Determina se il processore supporta il set di istruzioni 3DNow. | Proprietà IVMHostInfo ThreeDNow (VPCCOMInterfaces. h)
ms.assetid: 4987e326-d8fa-4dfa-b592-9dd90cedb0ef
keywords:
- Proprietà ThreeDNow Virtual PC
- Proprietà ThreeDNow Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà ThreeDNow
topic_type:
- apiref
api_name:
- IVMHostInfo.ThreeDNow
- IVMHostInfo.get_ThreeDNow
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76737b9512e42aef5549985e3ec38953ef02d8b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321787"
---
# <a name="ivmhostinfothreednow-property"></a><span data-ttu-id="3511a-107">Proprietà IVMHostInfo:: ThreeDNow</span><span class="sxs-lookup"><span data-stu-id="3511a-107">IVMHostInfo::ThreeDNow property</span></span>

<span data-ttu-id="3511a-108">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3511a-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3511a-109">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3511a-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3511a-110">Determina se il processore supporta il set di istruzioni 3DNow.</span><span class="sxs-lookup"><span data-stu-id="3511a-110">Determines whether the processor supports the 3DNow instruction set.</span></span>

<span data-ttu-id="3511a-111">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3511a-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3511a-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3511a-112">Syntax</span></span>


```C++
HRESULT get_ThreeDNow(
  [out, retval] VARIANT_BOOL *threeDNowEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="3511a-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3511a-113">Property value</span></span>

<span data-ttu-id="3511a-114">**True** se le istruzioni 3DNow sono supportate dal processore host; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="3511a-114">**TRUE** if 3DNow instructions are supported by the host processor, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3511a-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="3511a-115">Error codes</span></span>



| <span data-ttu-id="3511a-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="3511a-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3511a-117">Significato</span><span class="sxs-lookup"><span data-stu-id="3511a-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3511a-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3511a-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3511a-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3511a-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="3511a-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3511a-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3511a-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="3511a-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="3511a-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3511a-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3511a-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="3511a-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3511a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3511a-124">Requirements</span></span>



| <span data-ttu-id="3511a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3511a-125">Requirement</span></span> | <span data-ttu-id="3511a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="3511a-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3511a-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3511a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3511a-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3511a-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3511a-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3511a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3511a-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3511a-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3511a-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3511a-131">End of client support</span></span><br/>    | <span data-ttu-id="3511a-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3511a-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3511a-133">Prodotto</span><span class="sxs-lookup"><span data-stu-id="3511a-133">Product</span></span><br/>                  | <span data-ttu-id="3511a-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3511a-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3511a-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3511a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3511a-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3511a-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3511a-137">IID</span><span class="sxs-lookup"><span data-stu-id="3511a-137">IID</span></span><br/>                      | <span data-ttu-id="3511a-138">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="3511a-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="3511a-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3511a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3511a-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="3511a-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

