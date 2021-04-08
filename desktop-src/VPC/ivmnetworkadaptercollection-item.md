---
title: Proprietà Item di IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Oggetto IVMNetworkAdapter che corrisponde all'indice specificato.
ms.assetid: 3de76e24-3315-473f-870b-074be8bcfe70
keywords:
- Proprietà elemento Virtual PC
- Proprietà elemento Virtual PC, interfaccia IVMNetworkAdapterCollection
- Interfaccia IVMNetworkAdapterCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Item
- IVMNetworkAdapterCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63d2f7ee389938a44c6608241fb3fb2d48ec1bca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964869"
---
# <a name="ivmnetworkadaptercollectionitem-property"></a><span data-ttu-id="6db13-106">Proprietà IVMNetworkAdapterCollection:: Item</span><span class="sxs-lookup"><span data-stu-id="6db13-106">IVMNetworkAdapterCollection::Item property</span></span>

<span data-ttu-id="6db13-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6db13-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6db13-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6db13-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6db13-109">Recupera l'oggetto [**IVMNetworkAdapter**](ivmnetworkadapter.md) che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="6db13-109">Retrieves the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span>

<span data-ttu-id="6db13-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6db13-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6db13-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6db13-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMNetworkAdapter **networkInterface
);
```



## <a name="property-value"></a><span data-ttu-id="6db13-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6db13-112">Property value</span></span>

<span data-ttu-id="6db13-113">Oggetto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="6db13-113">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6db13-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="6db13-114">Error codes</span></span>



| <span data-ttu-id="6db13-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="6db13-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6db13-116">Significato</span><span class="sxs-lookup"><span data-stu-id="6db13-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6db13-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6db13-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6db13-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="6db13-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="6db13-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6db13-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6db13-120">Il parametro *interfaccia* è **null**.</span><span class="sxs-lookup"><span data-stu-id="6db13-120">The *networkInterface* parameter is **NULL**.</span></span> <br/>                                      |
| <dl> <span data-ttu-id="6db13-121"><dt>Disp \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="6db13-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="6db13-122">L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="6db13-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="6db13-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6db13-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6db13-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="6db13-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="6db13-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6db13-125">Requirements</span></span>



| <span data-ttu-id="6db13-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6db13-126">Requirement</span></span> | <span data-ttu-id="6db13-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6db13-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6db13-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6db13-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6db13-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6db13-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6db13-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6db13-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6db13-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6db13-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6db13-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6db13-132">End of client support</span></span><br/>    | <span data-ttu-id="6db13-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6db13-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="6db13-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="6db13-134">Product</span></span><br/>                  | <span data-ttu-id="6db13-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6db13-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="6db13-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6db13-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6db13-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6db13-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="6db13-138">IID</span><span class="sxs-lookup"><span data-stu-id="6db13-138">IID</span></span><br/>                      | <span data-ttu-id="6db13-139">IID \_ IVMNetworkAdapterCollection è definito come ebaeafe9-EBCD-47CF-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="6db13-139">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6db13-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6db13-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db13-141">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="6db13-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="6db13-142">**IVMNetworkAdapterCollection**</span><span class="sxs-lookup"><span data-stu-id="6db13-142">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

