---
title: Proprietà IVMHostInfo MemoryAvailString (VPCCOMInterfaces. h)
description: Recupera la quantità di memoria fisica disponibile nel computer host, in megabyte, sotto forma di stringa.
ms.assetid: a0f17dda-2042-4aec-9968-6662d32684cf
keywords:
- Proprietà MemoryAvailString Virtual PC
- Proprietà MemoryAvailString Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà MemoryAvailString
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryAvailString
- IVMHostInfo.get_MemoryAvailString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea003b94d0d4604dfba3daf545a51b9d69b6708c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477416"
---
# <a name="ivmhostinfomemoryavailstring-property"></a><span data-ttu-id="cce40-106">Proprietà IVMHostInfo:: MemoryAvailString</span><span class="sxs-lookup"><span data-stu-id="cce40-106">IVMHostInfo::MemoryAvailString property</span></span>

<span data-ttu-id="cce40-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cce40-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cce40-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cce40-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cce40-109">Recupera la quantità di memoria fisica disponibile nel computer host, in megabyte, sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="cce40-109">Retrieves the amount of available physical memory in the host machine, in megabytes, as a string.</span></span>

<span data-ttu-id="cce40-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cce40-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cce40-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cce40-111">Syntax</span></span>


```C++
HRESULT get_MemoryAvailString(
  [out, retval] BSTR *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="cce40-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="cce40-112">Property value</span></span>

<span data-ttu-id="cce40-113">Memoria fisica disponibile, in megabyte.</span><span class="sxs-lookup"><span data-stu-id="cce40-113">The available physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cce40-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="cce40-114">Error codes</span></span>



| <span data-ttu-id="cce40-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="cce40-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="cce40-116">Significato</span><span class="sxs-lookup"><span data-stu-id="cce40-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="cce40-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cce40-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="cce40-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="cce40-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="cce40-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="cce40-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="cce40-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="cce40-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="cce40-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cce40-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="cce40-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="cce40-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cce40-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cce40-123">Requirements</span></span>



| <span data-ttu-id="cce40-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cce40-124">Requirement</span></span> | <span data-ttu-id="cce40-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cce40-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cce40-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cce40-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cce40-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cce40-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cce40-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cce40-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cce40-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cce40-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cce40-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="cce40-130">End of client support</span></span><br/>    | <span data-ttu-id="cce40-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cce40-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cce40-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="cce40-132">Product</span></span><br/>                  | <span data-ttu-id="cce40-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cce40-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cce40-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cce40-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cce40-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cce40-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cce40-136">IID</span><span class="sxs-lookup"><span data-stu-id="cce40-136">IID</span></span><br/>                      | <span data-ttu-id="cce40-137">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="cce40-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="cce40-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cce40-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce40-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="cce40-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

