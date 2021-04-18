---
title: Proprietà IVMHostInfo ParallelPort (VPCCOMInterfaces. h)
description: Recupera la porta parallela host che può essere collegata al Guest.
ms.assetid: 4c9486b8-ab66-4874-b467-a7a0ab7934f1
keywords:
- Proprietà ParallelPort Virtual PC
- Proprietà ParallelPort Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà ParallelPort
topic_type:
- apiref
api_name:
- IVMHostInfo.ParallelPort
- IVMHostInfo.get_ParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0a2050ff505f5ed7a54cf3857ea28661d4d3d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517349"
---
# <a name="ivmhostinfoparallelport-property"></a><span data-ttu-id="442ea-106">IVMHostInfo::P proprietà arallelPort</span><span class="sxs-lookup"><span data-stu-id="442ea-106">IVMHostInfo::ParallelPort property</span></span>

<span data-ttu-id="442ea-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="442ea-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="442ea-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="442ea-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="442ea-109">Recupera la porta parallela host che può essere collegata al Guest.</span><span class="sxs-lookup"><span data-stu-id="442ea-109">Retrieves the host parallel port that can be attached to the guest.</span></span>

<span data-ttu-id="442ea-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="442ea-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="442ea-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="442ea-111">Syntax</span></span>


```C++
HRESULT get_ParallelPort(
  [out, retval] BSTR *vmParallelPort
);
```



## <a name="property-value"></a><span data-ttu-id="442ea-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="442ea-112">Property value</span></span>

<span data-ttu-id="442ea-113">Nome della porta parallela.</span><span class="sxs-lookup"><span data-stu-id="442ea-113">The name of the parallel port.</span></span>

## <a name="error-codes"></a><span data-ttu-id="442ea-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="442ea-114">Error codes</span></span>



| <span data-ttu-id="442ea-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="442ea-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="442ea-116">Significato</span><span class="sxs-lookup"><span data-stu-id="442ea-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="442ea-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="442ea-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="442ea-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="442ea-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="442ea-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="442ea-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="442ea-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="442ea-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="442ea-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="442ea-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="442ea-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="442ea-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="442ea-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="442ea-123">Requirements</span></span>



| <span data-ttu-id="442ea-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="442ea-124">Requirement</span></span> | <span data-ttu-id="442ea-125">Valore</span><span class="sxs-lookup"><span data-stu-id="442ea-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="442ea-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="442ea-126">Minimum supported client</span></span><br/> | <span data-ttu-id="442ea-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="442ea-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="442ea-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="442ea-128">Minimum supported server</span></span><br/> | <span data-ttu-id="442ea-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="442ea-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="442ea-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="442ea-130">End of client support</span></span><br/>    | <span data-ttu-id="442ea-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="442ea-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="442ea-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="442ea-132">Product</span></span><br/>                  | <span data-ttu-id="442ea-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="442ea-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="442ea-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="442ea-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="442ea-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="442ea-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="442ea-136">IID</span><span class="sxs-lookup"><span data-stu-id="442ea-136">IID</span></span><br/>                      | <span data-ttu-id="442ea-137">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="442ea-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="442ea-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="442ea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="442ea-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="442ea-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

