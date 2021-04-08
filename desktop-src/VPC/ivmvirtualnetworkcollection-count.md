---
title: Proprietà Count IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Recupera il numero di reti virtuali in questa raccolta.
ms.assetid: a9a3ab48-74a0-498e-936e-a99c7b027a85
keywords:
- Conteggio proprietà PC virtuale
- Proprietà Count Virtual PC, interfaccia IVMVirtualNetworkCollection
- Interfaccia IVMVirtualNetworkCollection Virtual PC, proprietà Count
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Count
- IVMVirtualNetworkCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82e3244327d5840c8f7cce8ed498f90cd406d573
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742735"
---
# <a name="ivmvirtualnetworkcollectioncount-property"></a><span data-ttu-id="77e70-106">Proprietà IVMVirtualNetworkCollection:: count</span><span class="sxs-lookup"><span data-stu-id="77e70-106">IVMVirtualNetworkCollection::Count property</span></span>

<span data-ttu-id="77e70-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="77e70-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="77e70-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="77e70-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="77e70-109">Recupera il numero di reti virtuali in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="77e70-109">Retrieves the number of virtual networks in this collection.</span></span>

<span data-ttu-id="77e70-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="77e70-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="77e70-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77e70-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="77e70-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="77e70-112">Property value</span></span>

<span data-ttu-id="77e70-113">Numero di reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="77e70-113">The number of virtual networks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="77e70-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="77e70-114">Error codes</span></span>



| <span data-ttu-id="77e70-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="77e70-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="77e70-116">Significato</span><span class="sxs-lookup"><span data-stu-id="77e70-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="77e70-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="77e70-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="77e70-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="77e70-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="77e70-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="77e70-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="77e70-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="77e70-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="77e70-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="77e70-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="77e70-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="77e70-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="77e70-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77e70-123">Requirements</span></span>



| <span data-ttu-id="77e70-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="77e70-124">Requirement</span></span> | <span data-ttu-id="77e70-125">Valore</span><span class="sxs-lookup"><span data-stu-id="77e70-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77e70-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77e70-126">Minimum supported client</span></span><br/> | <span data-ttu-id="77e70-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="77e70-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="77e70-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77e70-128">Minimum supported server</span></span><br/> | <span data-ttu-id="77e70-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="77e70-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="77e70-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="77e70-130">End of client support</span></span><br/>    | <span data-ttu-id="77e70-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="77e70-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="77e70-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="77e70-132">Product</span></span><br/>                  | <span data-ttu-id="77e70-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="77e70-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="77e70-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77e70-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="77e70-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="77e70-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="77e70-136">IID</span><span class="sxs-lookup"><span data-stu-id="77e70-136">IID</span></span><br/>                      | <span data-ttu-id="77e70-137">IID \_ IVMVirtualNetworkCollection è definito come 8ed680be-4242-4B2A-A21C-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="77e70-137">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77e70-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77e70-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e70-139">**IVMVirtualNetworkCollection**</span><span class="sxs-lookup"><span data-stu-id="77e70-139">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

