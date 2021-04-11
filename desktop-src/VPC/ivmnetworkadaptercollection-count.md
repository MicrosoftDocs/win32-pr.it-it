---
title: Proprietà Count IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Recupera il numero di interfacce di rete in questa raccolta.
ms.assetid: 0b6391fa-62fe-4db1-b0a2-565ab17157ab
keywords:
- Conteggio proprietà PC virtuale
- Proprietà Count Virtual PC, interfaccia IVMNetworkAdapterCollection
- Interfaccia IVMNetworkAdapterCollection Virtual PC, proprietà Count
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Count
- IVMNetworkAdapterCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a287122d9829cd98f355d44e6bd408f6ca0d67a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118911"
---
# <a name="ivmnetworkadaptercollectioncount-property"></a><span data-ttu-id="e6d54-106">Proprietà IVMNetworkAdapterCollection:: count</span><span class="sxs-lookup"><span data-stu-id="e6d54-106">IVMNetworkAdapterCollection::Count property</span></span>

<span data-ttu-id="e6d54-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e6d54-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e6d54-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e6d54-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e6d54-109">Recupera il numero di interfacce di rete in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="e6d54-109">Retrieves the number of network interfaces in this collection.</span></span>

<span data-ttu-id="e6d54-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e6d54-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d54-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6d54-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="e6d54-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e6d54-112">Property value</span></span>

<span data-ttu-id="e6d54-113">Il numero di interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="e6d54-113">The number of network interfaces.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e6d54-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e6d54-114">Error codes</span></span>



| <span data-ttu-id="e6d54-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="e6d54-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e6d54-116">Significato</span><span class="sxs-lookup"><span data-stu-id="e6d54-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e6d54-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e6d54-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e6d54-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e6d54-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="e6d54-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e6d54-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e6d54-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="e6d54-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="e6d54-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e6d54-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e6d54-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="e6d54-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e6d54-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6d54-123">Requirements</span></span>



| <span data-ttu-id="e6d54-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6d54-124">Requirement</span></span> | <span data-ttu-id="e6d54-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e6d54-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d54-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6d54-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e6d54-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e6d54-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e6d54-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6d54-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e6d54-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e6d54-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e6d54-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e6d54-130">End of client support</span></span><br/>    | <span data-ttu-id="e6d54-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6d54-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="e6d54-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="e6d54-132">Product</span></span><br/>                  | <span data-ttu-id="e6d54-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e6d54-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="e6d54-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6d54-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6d54-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6d54-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="e6d54-136">IID</span><span class="sxs-lookup"><span data-stu-id="e6d54-136">IID</span></span><br/>                      | <span data-ttu-id="e6d54-137">IID \_ IVMNetworkAdapterCollection è definito come ebaeafe9-EBCD-47CF-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="e6d54-137">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6d54-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6d54-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d54-139">**IVMNetworkAdapterCollection**</span><span class="sxs-lookup"><span data-stu-id="e6d54-139">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

