---
title: Proprietà IVMHostInfo ProcessorSpeedString (VPCCOMInterfaces. h)
description: Velocità del processore host, in megahertz (MHz) o gigahertz (GHz), sotto forma di stringa.
ms.assetid: 1a4a42bf-b7aa-4eec-8df5-1820aac82de3
keywords:
- Proprietà ProcessorSpeedString Virtual PC
- Proprietà ProcessorSpeedString Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà ProcessorSpeedString
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorSpeedString
- IVMHostInfo.get_ProcessorSpeedString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91b8cb19baef62275954f0c1d9f6475c5b4817f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478802"
---
# <a name="ivmhostinfoprocessorspeedstring-property"></a><span data-ttu-id="38611-106">IVMHostInfo::P proprietà rocessorSpeedString</span><span class="sxs-lookup"><span data-stu-id="38611-106">IVMHostInfo::ProcessorSpeedString property</span></span>

<span data-ttu-id="38611-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="38611-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="38611-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="38611-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="38611-109">Recupera la velocità del processore host, in megahertz (MHz) o gigahertz (GHz), sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="38611-109">Retrieves the speed of the host processor, in megahertz (MHz) or gigahertz (GHz), as a string.</span></span>

<span data-ttu-id="38611-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="38611-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="38611-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38611-111">Syntax</span></span>


```C++
HRESULT get_ProcessorSpeedString(
  [out, retval] BSTR *processorSpeedString
);
```



## <a name="property-value"></a><span data-ttu-id="38611-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="38611-112">Property value</span></span>

<span data-ttu-id="38611-113">Velocità del processore, in megahertz o gigahertz.</span><span class="sxs-lookup"><span data-stu-id="38611-113">The processor speed, in megahertz or gigahertz.</span></span>

## <a name="error-codes"></a><span data-ttu-id="38611-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="38611-114">Error codes</span></span>



| <span data-ttu-id="38611-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="38611-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="38611-116">Significato</span><span class="sxs-lookup"><span data-stu-id="38611-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="38611-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="38611-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="38611-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="38611-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="38611-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="38611-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="38611-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="38611-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="38611-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="38611-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="38611-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="38611-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="38611-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38611-123">Requirements</span></span>



| <span data-ttu-id="38611-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="38611-124">Requirement</span></span> | <span data-ttu-id="38611-125">Valore</span><span class="sxs-lookup"><span data-stu-id="38611-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="38611-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38611-126">Minimum supported client</span></span><br/> | <span data-ttu-id="38611-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="38611-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38611-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38611-128">Minimum supported server</span></span><br/> | <span data-ttu-id="38611-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="38611-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="38611-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="38611-130">End of client support</span></span><br/>    | <span data-ttu-id="38611-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="38611-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="38611-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="38611-132">Product</span></span><br/>                  | <span data-ttu-id="38611-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="38611-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="38611-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38611-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="38611-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="38611-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="38611-136">IID</span><span class="sxs-lookup"><span data-stu-id="38611-136">IID</span></span><br/>                      | <span data-ttu-id="38611-137">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="38611-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="38611-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38611-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38611-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="38611-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

